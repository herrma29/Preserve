<!DOCTYPE html>
<html class="fuelux" lang="en">
  <head>
    <meta http-equiv='Content-Type' content='text/html; charset=utf-8'>
		{% if page.url == "/404.html" %}
			<meta http-equiv="refresh" content="5; url=/">
		{% endif %}
    <title>{{ page.title }}</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="/js/all.js" type="text/javascript"></script>
    <link href="/css/bootstrap.min.css" rel="stylesheet">
    <link href="/css/bootstrap-lightbox.min.css" rel="stylesheet">
	<link href="/css/custom.css" rel="stylesheet">


	
	
    <!-- Le HTML5 shim, for IE6-8 support of HTML5 elements -->
    <!--[if lt IE 9]>
      <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->


<script type="text/javascript">
var _gaq = _gaq || [];
_gaq.push(['_setAccount', 'UA-48434878-1']);
_gaq.push(['_trackPageview']);
(function() {
var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;

ga.src = ('https:' == document.location.protocol ? 'https://' : 'http://') + 'stats.g.doubleclick.net/dc.js';

var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
})();
</script>

  </head>
  <body>
    {% include navigation.md %}

    <div class="container">
        <div class="content">
            <div class="row">
		<div class="col-lg-2 col-md-1 hidden-sm hidden-xs">
		</div>
                <div class="col-lg-5 col-md-7 col-sm-8 col-xs-12">
                    {{ content }}
                </div>
                <div class="col-lg-3 col-md-3 col-sm-4 hidden-xs">
                    {% include aboutme.md %}
                </div>
		<div class="col-lg-2 col-md-1 hidden-sm hidden-xs">
		</div>
            </div>
        </div>
    </div>

<!-- Modal -->
<div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-hidden="true">&times;</button>
        <h4 class="modal-title" id="myModalLabel">Modal title</h4>
      </div>
      <div class="modal-body">
        {{ page.modal }}
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div><!-- /.modal-content -->
  </div><!-- /.modal-dialog -->
</div><!-- /.modal -->

    {% include footer.md %}
  </body>
</html>
