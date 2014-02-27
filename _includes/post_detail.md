				<p>
					{% if post.previous.url %} 
						<a href="{{post.previous.url}}" title="Previous Post: {{post.previous.title}}">
						&laquo; Previous Blog Post</a>  |
					{% endif %}
					  <a href="/archives/">Archives</a>  
					{% if post.next.url %}
						|  <a href="{{post.next.url}}" title="Next Post: {{post.next.title}}">Next Blog Post &raquo; 					</a>
					{% endif %}
				</p>    

<h1>{{ post.title }}</h1>
<h4>{{ post.date | date: "%B %e, %Y" }}</h4>
    
{% if post.video_url %}
 <div class="less-fancy-video-header">
  <iframe
   class="yt-embed"
   src="{{page.video_url }}?&rel=0&showinfo=0&autohide=1&hd=1&wmode=transparent"
   frameborder="0"
   allowfullscreen="true">
  </iframe>
 </div>
{% endif %}

{{ content }}
