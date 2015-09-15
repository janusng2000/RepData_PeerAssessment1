---
####Title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true

##### Loading and preprocessing the data

```{r Include packages and datasets}

library(knitr)
library(datasets) 
library(ggplot2)

setwd("~/RepData_PeerAssessment1")
data <- read.csv("activity.csv")

```

##### What is mean total number of steps taken per day?

```{r}
library(ggplot2)
total.steps <- tapply(data$steps, data$date, FUN=sum, na.rm=TRUE)
qplot(total.steps, binwidth=1000, xlab="total number of steps taken each day")
mean(total.steps, na.rm=TRUE)
median(total.steps, na.rm=TRUE)

```
![plot of chunk unnamed-chunk-1](https://github.com/janusng2000/RepData_PeerAssessment1/blob/master/png/Rplot1.png)

##### What is mean total number of steps taken per day?

```{r}
mean(total.steps, na.rm = TRUE)
```

```{r}
median(total.steps, na.rm=TRUE)
```

```{r}
mean(total.steps, na.rm = TRUE)
```


##### What is the average daily activity pattern?

```{r}
library(ggplot2)
averages <- aggregate(x=list(steps=data$steps), by=list(interval=data$interval),
                      FUN=mean, na.rm=TRUE)
ggplot(data=averages, aes(x=interval, y=steps)) +
    geom_line() +
    xlab("5-minute interval") +
    ylab("average number of steps taken")

```

##### Which 5-minutte interval, On average across all the days in the dataset,, contains the maximum number of steps?

```{r}
averages[which.max(averages$steps), ]
```

##### Inputing missing values 

```{r}
missing <- is.na(data$steps)
# How many missing
table(missing)
```

##### Devise a strategy for filling in all of the missing values in the dataset. The strategy does not need to be sophisticated. All of the missing values are filled in with mean value for that 5-minute interval.

```{r}
##### Replace each missing value with the mean value of its 5-minute interval
fill.value <- function(steps, interval) {
    filled <- NA
    if (!is.na(steps)) 
        filled <- c(steps) else filled <- (averages[averages$interval == interval, "steps"])
    return(filled)
}
filled.data <- data
filled.data$steps <- mapply(fill.value, filled.data$steps, filled.data$interval)
```

##### Make a histogram of the total number of steps taken each day and Calculate and report the mean and median total number of steps taken per day.

```{r}
total.steps <- tapply(filled.data$steps, filled.data$date, FUN = sum)
qplot(total.steps, binwidth = 1000, xlab = "total number of steps taken each day")
```

```{r}
mean(total.steps)
```

```{r}
median(total.steps)
```

##### Are there differences in activity patterns between weekdays and weekends?

```{r}
weekday.or.weekend <- function(date) {
    day <- weekdays(date)
    if (day %in% c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday")) 
        return("weekday") else if (day %in% c("Saturday", "Sunday")) 
        return("weekend") else stop("invalid date")
}
filled.data$date <- as.Date(filled.data$date)
filled.data$day <- sapply(filled.data$date, FUN = weekday.or.weekend)
```

##### Make a panel plot containing a time series plot (i.e. type = "l") of the 5-minute interval (x-axis) and the average number of steps taken, averaged across all weekday days or weekend days (y-axis).

```{r}
averages <- aggregate(steps ~ interval + day, data = filled.data, mean)
ggplot(averages, aes(interval, steps)) + geom_line() + facet_grid(day ~ .) + 
    xlab("5-minute interval") + ylab("Number of steps")
```


