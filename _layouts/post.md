---
layout: layout
---
				<p>
					{% if page.previous.url %} 
						<a href="{{page.previous.url}}" title="Previous Post: {{page.previous.title}}">
						&laquo; Previous Blog Post</a>  |
					{% endif %}
					  <a href="/archives/">Archives</a>  
					{% if page.next.url %}
						|  <a href="{{page.next.url}}" title="Next Post: {{page.next.title}}">Next Blog Post &raquo; 					</a>
					{% endif %}
				</p>    

<h1>{{ page.title }}</h1>
<h4>{{ page.date | date: "%B %e, %Y" }}</h4>
    
{% if page.video_url %}
<div class="vid">
                <iframe width="560" height="315" src="//www.youtube.com/embed/ac7KhViaVqc" allowfullscreen=""></iframe>
            </div>
{% endif %}

{{ content }}



