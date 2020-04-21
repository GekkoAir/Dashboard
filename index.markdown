---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: index
---
 <aside>
    <h4>Latest Article</h4>

    {% for post in site.posts -%}
      {% unless post.categories contains 'release' -%}
      {%- if page.title == post.title %} class="current" {%- endif %}
      <br>
      <br>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% endunless -%}
    {% endfor -%}
    
  </aside>