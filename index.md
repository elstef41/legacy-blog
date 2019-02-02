---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
<div class="row">
	<div class="col-md-1"></div>
	<div class="col-md-10">

			<h1>Últimas entradas</h1>
                        {% for post in site.posts limit:4 %}
						<hr>
    <ul class="post-list">
        <h3>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
            {{ post.title }}
          </a>
		  </h3>
		  
		<p><i class="fa fa-calendar"></i> &nbsp;{{ post.date | date: "%b %-d, %Y" }} | {% if site.disqus_short_name and page.comments != false and site.disqus_show_comment_count == true %}
         <a href="{{ post.url | prepend: site.baseurl }}#disqus_thread">Comentarios</a>
		{% endif %}</p>
		<article class="blog-post-small blog-post-content">
                  {% if post.content contains '<!-- more -->' %}
                    <p>{{ post.content | split:'<!-- more -->' | first }}
                      <br><br>
                      <a href="{{ post.url }}"class="btn btn-primary btn-sm">Leer más</a>
                    </p>
                  {% else %}
                    {{ post.content }}
			{% endif %}
		</article>
		  <h6></h6>
		</ul>
                        {% endfor %}
	<br>
</div>