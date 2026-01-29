{%- include ui.html %}
{%- assign _sub = page.layout | remove: '-page'| remove: '-post' %}
{%- case _sub %}
{%- when 'core' or 'mallet' or 'prime' %}
{%- include dove/sample_nav.md sub=_sub %}
{{ thin_hr }}
{%- else %}
{%- if page.use_nav == false -%}
<style>._nav{display:none !important}</style>
{%- else %}

{%- if page.path == 'index.html' -%}
**Home**{%- else -%}[Home]({{ site.home_url }}/)
{%- endif %}
{{- bull -}}
{%- if page.path == 'about.md' -%}
**About**{%- else -%}[About]({{ site.baseurl }}/about)
{%- endif %}
{{- bull -}}
{%- if page.path == 'pages.md' -%}
**Pages**{%- else -%}[Pages]({{ site.baseurl }}/pages)
{%- endif %}
{{- bull -}}
{%- if page.path == 'posts.md' -%}
**Posts**{%- else -%}[Posts]({{ site.baseurl }}/posts)
{%- endif %}

{%- assign _path_starts_with = page.path | slice: 0, 5 %}
{%- if _path_starts_with == 'test_' %}
{{ thin_hr }}
{%- include dove/test_nav.md %}
{%- endif %}

{{ thin_hr }}

{%- endif %}
{%- endcase %}
{%- comment %}
{%- endcomment %}