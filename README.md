# Projects

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem;">

  {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
  {% for post in sorted_posts %}
  <div style="border: 1px solid #ddd; border-radius: 12px; padding: 1rem; background: #fafafa; box-shadow: 0 2px 5px rgba(0,0,0,0.05);">
    
    {% if post.image %}
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="width:100%; border-radius:8px; margin-bottom:0.5rem;">
    {% endif %}
    
    <h3 style="margin-top:0;"><a href="{{ post.url | relative_url }}" style="text-decoration:none; color:#0366d6;">{{ post.title }}</a></h3>
    <p style="color:gray; font-size:0.9em;">{{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
    <a href="{{ post.url | relative_url }}" style="font-weight:bold; color:#0366d6;">Read more →</a>
  </div>
  {% endfor %}

</div>
