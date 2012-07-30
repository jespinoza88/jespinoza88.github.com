---
layout: page
title: What I've been up to:
tagline: Now in awesome!
---
{% include JB/setup %}
{% include themes/twitter/page.html %}


<table class="table table-striped">
  <tbody>
	{% for post in site.posts %}	
    <tr>
      <td>
		  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          <i>{{ post.summary }}</i>
		  <p><small>{{ post.date | date: "%B %e, %Y" }} . {{ post.category }} . {% for tag in post.tags %} <a href="/tags/{{ tag }}" title="View posts tagged with &quot;{{ tag }}&quot;">{{ tag }}</a>  {% if forloop.last != true %} {% endif %} {% endfor %} . <a href="http://jespinoza88.github.com{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.url }}"></a></small></p>
	  </td>
    </tr>
    
	{% endfor %}			
  </tbody>
</table>