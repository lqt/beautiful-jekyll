---
layout: page
title: Publications
pubs:
    - title:   "Investigating molecular dynamics-guided lead optimization of EGFR inhibitors"    
      author:  "Lavecchia, Martin J and de la Bellacasa, Raimon Puig and Borrell, Jose I and Cavasotto, Claudio N"
      journal: "Bioorganic & medicinal chemistry"
      year:    "2016"
      media:
        - name: "arXiv"
          url:  "https://arxiv.org/abs/1803.05206"
    
   
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
