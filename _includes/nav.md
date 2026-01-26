{%- include ui.html %}
{%- if site.github.repository_nwo == 'techie-joe/dove' %}
{%- include dove/nav.md %}
{%- elsif page.use_nav == false -%}
<style>._nav{display:none !important}</style>
{%- else %}

<!-- your nav goes here -->

<!-- but right now lets just hide it -->
<style>._nav{display:none !important}</style>

{%- endif %}