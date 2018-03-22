---
layout: page
title: Publications
pubs:
    - title: "A retention index-based QSPR model for the quality control of rice"
      author: "Rojas, Cristian and Tripaldi, Piercosimo and Pérez-González, Andrés and Duchowicz, Pablo R and Diez, Reinaldo Pis"
      journal: "Journal of Cereal Science"
      year: "2018"
      media:
        - name: "paper"
          url:  "https://www.sciencedirect.com/science/article/pii/S0733521017304368"

---

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
