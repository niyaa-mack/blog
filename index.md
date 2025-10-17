<b> Hola, My name is Shaniya Mack and you get to know me on a deeper level here im about to show you something.</b>



<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>