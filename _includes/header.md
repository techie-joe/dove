{%- include ui.html %}
{%- if page.use_header == false %}
<style>._header{display:none !important}</style>
{%- elsif site.github.repository_nwo == 'techie-joe/dove' %}
{%- include dove/logo.html %}
{%- else -%}
{%- include logo.html %}
{%- endif %}