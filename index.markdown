---
layout: default
---
<section id="content" class="bg-dark">
  <div class="cfp-heading">
    <h1 class="section-heading text-center text-white">Call for Papers</h1>
    <h3 class="section-subheading text-center text-white">School of Cyber Science and Engineering, Sichuan University</h3>
  </div>
  <div class="cfp-list">
  {% assign pc = 0 %}
  {% for p in site.pages %}
    {% if p.path contains "cfp/" %}
    {% assign pc = pc | plus: 1 %}
    {{ pc }}
    {% assign cprefix = "collapse-cfp" %}
    <div class="container">
      <div class="cfp-item text-white">
        <h4><a data-bs-toggle="collapse" href="#{{cprefix}}{{pc}}" class="link-light" role="button" aria-expanded="false" aria-controls="{{cprefix}}{{pc}}">{{p.title | upcase}}</a></h4>
        <div class="meta-item text-white">
          <label>ORGANIZERS:</label>
          <ul>
          {% for person in p.organizers %}
            <li>{{person.name | upcase}}</li>
          {% endfor %}
          </ul>
        </div>
        <div id="{{cprefix}}{{pc}}" class="collapse">
          <div class="cfp-content bg-secondary">
          {{p.content | markdownify}}
          </div>
        </div>
      </div>
    </div>
    {% endif %}
  {% endfor %}
  </div>
</section>
