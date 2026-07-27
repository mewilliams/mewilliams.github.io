---
permalink: /publications/
title: "Publications"
---

## Peer-Reviewed Publications

{% assign pubs = site.data.publications | sort: "year" | reverse %}

{% assign current_year = "" %}

{% for pub in pubs %}

  {% if current_year != pub.year %}

### {{ pub.year }}

  {% assign current_year = pub.year %}
  {% endif %}

**{{ pub.authors }}** ({{ pub.year }}).  
{{ pub.title }}.  
*{{ pub.journal }}*
{% if pub.volume %}, {{ pub.volume }}{% endif %}
{% if pub.pages %}, {{ pub.pages }}{% endif %}.  
{% if pub.doi %}
<a ps://doi.org/{{ pub.doi }}
doi:{{ pub.doi }}
</a>
{% endif %}

<br>

{% endfor %}
