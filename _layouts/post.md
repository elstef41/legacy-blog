---
layout: default
comments: true
---
<div class="row">
	<div class="col-md-1"></div>
	<div class="col-md-10">

	  	
	    <h1>{{ page.title }}</h1>
	    <p class="post-meta">{{ page.date | date: "%b %-d, %Y" }}</p>

	   
	  	<article class="blog-post-small blog-post-content">
	    	{{ content }}
	  	</article>
	  	
	  	
	  	{% include author_block.html %}
	</div>
	<div class="col-md-1"></div>
</div>