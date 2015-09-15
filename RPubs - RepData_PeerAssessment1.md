<!DOCTYPE html>
<!-- saved from url=(0052)http://rpubs.com/Janusng2000/RepData_PeerAssessment1 -->
<html class="wf-adelle-n3-active wf-adelle-i3-active wf-adelle-n4-active wf-adelle-n7-active wf-adelle-i7-active wf-pragmaticawebcondensed-n4-active wf-active"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>RPubs - RepData_PeerAssessment1</title>
<link href="./RPubs - RepData_PeerAssessment1_files/application-0f4a38981ee7b1c077577f51e3f33627.css" media="all" rel="stylesheet" type="text/css">
<link href="./RPubs - RepData_PeerAssessment1_files/show-060a5f99c65c577dbbcb45abae19cefc.css" media="all" rel="stylesheet" type="text/css">
<script type="text/javascript" async="" src="./RPubs - RepData_PeerAssessment1_files/ga.js"></script><script src="./RPubs - RepData_PeerAssessment1_files/application-b0fb18b4aea86fb908a4b406708b8b1b.js" type="text/javascript"></script>
<script type="text/javascript" src="./RPubs - RepData_PeerAssessment1_files/uao6mzv.js"></script>
<style type="text/css">.tk-adelle{font-family:"adelle","Helvetica",sans-serif;}.tk-pragmatica-web-condensed{font-family:"pragmatica-web-condensed",sans-serif;}</style><link rel="stylesheet" href="./RPubs - RepData_PeerAssessment1_files/uao6mzv-d.css"><script type="text/javascript">try{Typekit.load();}catch(e){}</script>
<script>
  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'UA-20375833-2']);
  _gaq.push(['_setDomainName', 'rpubs.com']);
  _gaq.push(['_trackPageview']);
  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();
</script>

<script type="text/javascript" async="" src="./RPubs - RepData_PeerAssessment1_files/embed.js"></script><link rel="stylesheet" href="./RPubs - RepData_PeerAssessment1_files/loading.8023a7350e47171f7bb79707886cd7c5.css"><script src="./RPubs - RepData_PeerAssessment1_files/alfie.f51946af45e0b561c60f768335c9eb79.js" async="" charset="UTF-8"></script></head>
<body class="show-pub show-toolbars">
<div class="modal fade" id="login" style="display: none">
<div class="modal-header">
<h1>Sign In</h1>
</div>
<div class="modal-body">
<div class="alert" id="login_message" style="display: none"></div>
<form accept-charset="UTF-8" action="http://rpubs.com/auth/login" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="✓"><input name="authenticity_token" type="hidden" value="AxXJ8xpf2YfdsSFVhHZpuJY1/gO+r4j7+3KiAp4jNyc="></div>
<input name="return_url" type="hidden">
<div class="fieldset">
<div class="control-group">
<label class="control-label" for="login_username">Username or Email</label>
<div class="controls">
<input class="input-xlarge" id="login_username" name="username" type="text">
</div>
</div>
<div class="control-group">
<label class="control-label" for="login_password">Password</label>
<div class="controls">
<input class="input-xlarge" id="login_password" name="password" type="password">
</div>
</div>
</div>
</form>


</div>
<div class="modal-footer">
<button class="btn btn-primary" id="login-modal-submit">Sign In</button>
<button class="btn" id="login-modal-cancel">Cancel</button>
</div>
</div>
<div class="navbar-inner" id="pageheader">
<div id="branding">
<h1 id="logo">
<a href="http://rpubs.com/"><span id="R">R</span>Pubs
</a>
</h1>
<span id="tagline">brought to you by RStudio</span>
</div>
<div id="identity">
<div class="btn-group">
<a class="btn btn-inverse btn-small pull-right" href="http://rpubs.com/Janusng2000/RepData_PeerAssessment1#" onclick="rpubs_showLogin(); return false">
Sign in
</a>
<a class="btn btn-inverse btn-small pull-right" href="http://rpubs.com/users/new">
Register
</a>
</div>
</div>
</div>
<div id="pagebody">
<div id="payload">
<iframe src="./RPubs - RepData_PeerAssessment1_files/109097_6bb8a26ccc89416491affb613c418d70.html"></iframe>
<button class="btn btn-tiny" id="btn-show-toolbars">
<i class="icon-resize-small"></i>
</button>
</div>
<div class="navbar navbar-fixed-bottom" id="pagefooter">
<div class="navbar-inner">
<div class="container-fluid">
<ul class="nav" id="pubmeta">
<li id="pubtitle">
<label>RepData_PeerAssessment1</label>
</li>
<li id="pubauthor">
<a href="http://rpubs.com/Janusng2000">by Janus Ng</a>
</li>
<li id="pubtime">
<label>
Last updated
<time datetime="2015-09-15T03:35:24+00:00">33 minutes ago</time>
</label>
</li>
</ul>
<ul class="nav pull-right">
<li>
<button class="btn btn-small btn-success" id="btn-comments">
<i class="icon-comment icon-white"></i>
<span id="comment-verb-hide">
Hide
</span>
Comments
<span id="comment-count">
(–)
</span>
</button>
<button class="btn btn-small btn-info" id="btn-share">
<i class="icon-share icon-white"></i>
Share
</button>
<button class="btn btn-small btn-inverse" id="btn-hide-toolbars">
Hide Toolbars
</button>
</li>
</ul>
</div>
</div>
</div>
<div class="modal fade hide" id="modal-share">
<div class="modal-body">
<btn class="close" data-dismiss="modal" type="button">×</btn>
<h2 class="first">Post on:</h2>
<p>
<a class="btn btn-primary btn-large" href="https://twitter.com/intent/tweet?original_referer=http%3A%2F%2Frpubs.com%2FJanusng2000%2FRepData_PeerAssessment1&source=tweetbutton&text=RepData_PeerAssessment1&url=http%3A%2F%2Frpubs.com%2FJanusng2000%2FRepData_PeerAssessment1" onclick="window.open(this.href, &#39;&#39;, &#39;menubar=no,toolbar=no,resizable=yes,scrollbars=yes,height=275,width=660&#39;);return false;">
Twitter
</a>
<a class="btn btn-primary btn-large" href="https://www.facebook.com/sharer.php?u=http%3A%2F%2Frpubs.com%2FJanusng2000%2FRepData_PeerAssessment1&t=RepData_PeerAssessment1" onclick="window.open(this.href, &#39;&#39;, &#39;menubar=no,toolbar=no,resizable=yes,scrollbars=yes,height=350,width=660&#39;);return false;">
Facebook
</a>
<a class="btn btn-primary btn-large" href="https://plus.google.com/share?url=http%3A%2F%2Frpubs.com%2FJanusng2000%2FRepData_PeerAssessment1" onclick="window.open(this.href, &#39;&#39;, &#39;menubar=no,toolbar=no,resizable=yes,scrollbars=yes,height=600,width=600&#39;);return false;">
Google+
</a>
</p>
<hr>
<h3>Or copy &amp; paste this link into an email or IM:</h3>
<input onclick="this.select()" readonly="readonly" value="http://rpubs.com/Janusng2000/RepData_PeerAssessment1">
</div>
</div>
<script>
  $('#btn-edit').click(function() {
    location.href = "/Janusng2000/109097/edit";
  });
  $('#btn-delete').mouseover(function() {
    $('#btn-delete').removeClass('btn-inverse').addClass('btn-danger');
  });
  $('#btn-delete').mouseout(function() {
    $('#btn-delete').addClass('btn-inverse').removeClass('btn-danger');
  });
  $('#btn-hide-toolbars').click(function() {
    $(document.body).addClass('hide-toolbars');
    $(document.body).removeClass('show-toolbars');
  });
  $('#btn-show-toolbars').click(function() {
    $(document.body).addClass('show-toolbars');
    $(document.body).removeClass('hide-toolbars');
  });
  $('#btn-share').click(function() {
    $('#modal-share').modal().css({
      'margin-left': function () {
        return -($(this).width() / 2);
      }
    });
  });
  $('#btn-comments').click(function() {
    $(document.body).toggleClass('show-comments');
  });
  setInterval(function() {
    // Poll for comment count. Barf.
    var text = $('#dsq-num-posts').text();
    if (text && /^\d+$/.test(text))
      $('#comment-count').text('(' + text + ')');
  }, 1000);
</script>
<div id="comment-wrapper">
<div id="disqus_thread"><iframe id="dsq-1" data-disqus-uid="1" allowtransparency="true" frameborder="0" scrolling="no" tabindex="0" title="Disqus" width="100%" src="./RPubs - RepData_PeerAssessment1_files/saved_resource.html" style="width: 100% !important; border: none !important; overflow: hidden !important; height: 1406px !important;" horizontalscrolling="no" verticalscrolling="no"></iframe><iframe id="dsq-indicator-north" data-disqus-uid="indicator-north" allowtransparency="true" frameborder="0" scrolling="no" tabindex="0" title="Disqus" style="width: 0px !important; border: none !important; overflow: hidden !important; top: 0px !important; min-width: 0px !important; max-width: 0px !important; position: fixed !important; z-index: 2147483646 !important; height: 29px !important; min-height: 29px !important; max-height: 29px !important; display: none !important;"></iframe><iframe id="dsq-indicator-south" data-disqus-uid="indicator-south" allowtransparency="true" frameborder="0" scrolling="no" tabindex="0" title="Disqus" style="width: 0px !important; border: none !important; overflow: hidden !important; bottom: 0px !important; min-width: 0px !important; max-width: 0px !important; position: fixed !important; z-index: 2147483646 !important; height: 29px !important; min-height: 29px !important; max-height: 29px !important; display: none !important;"></iframe></div>
</div>

</div>


</body></html>