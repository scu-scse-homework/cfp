---
layout: default
---

{% for p in site.pages %}
  {% if p.path contains "cfp/" %}
  {{p.title}}, {% for person in p.organizers %}{{person.name | upcase}} {% endfor %}, {{p.only-for-homework}}, {{p.accept-chinese-submission}}
    {% endif %}
{% endfor %}
