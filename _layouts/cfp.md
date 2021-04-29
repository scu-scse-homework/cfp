---
layout: default
---

<div class="cfp-meta">
<h1><strong>{{ page.title | upcase }}</strong></h1>
<ul class="meta-list">
  <li class="meta-item">
    <label>Organizers: </label>
    <ul>
      {% for person in page.organizers %}
      <li>{{person.name}}</li>
      {% endfor %}
    </ul>
  </li>
  <li = "meta-item">
    <label>Institution: </label>
    <span>School of Cyber Science and Engineering</span>
  </li>
  </ul>
</div>

<hr>

<div class="cfp-content">
{{ page.content }}
</div>
