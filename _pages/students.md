## Current Students

{% for s in site.data.students.current %}

### {{ s.name }}

**{{ s.role }}**  
{{ s.program }}, {{ s.institution }}

**Research Topic:** {{ s.thesis }}

Started: {{ s.start }}

{% endfor %}

---

## Former Postdoctoral Scholars

{% for s in site.data.students.former_postdocs %}

### {{ s.name }}

Postdoctoral Scholar  
{{ s.institution }}

Funding: {{ s.funding }}

{{ s.start }}–{{ s.end }}

{% endfor %}

---

## Graduated Students

{% assign grads = site.data.students.graduated | sort: "year" | reverse %}

{% for s in grads %}

### {{ s.name }} ({{ s.year }})

**{{ s.degree }}**  
{{ s.program }}, {{ s.institution }}

**Thesis:** {{ s.thesis }}

{% endfor %}