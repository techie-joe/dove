{%- include ui.html %}
{%- if page.use_footer == false -%}
<style>._footer{display:none !important}</style>
{%- else %}
{%- unless page.use_footer contains 'edit_link_only' -%}
{%- if page.sample -%}

{{ thin_hr }}

`// site footer`

{%- else %}

{%- capture dove_nav %}
{%- include dove/nav.md %}
{%- endcapture %}

{%- capture tj_footer %}
**Techie Joe's**
{{- angle -}}
[Website](https://techie-joe.github.io){: target="_techiejoe_website" }
{{- bull -}}
[Profile](https://github.com/techie-joe){: target="_techiejoe_profile" }
{{- bull -}}
[ThemeJs](/nova/site/themejs){: target="_themejs" }
{%- endcapture %}

{{ thin_hr }}
<nav class="_common_nav">{{ dove_nav | markdownify }}</nav>
<nav class="_common_nav">{{ tj_footer | markdownify }}</nav>

{%- endif %}
{%- endunless %}

{{ thin_hr }}

This site is open source. {% github_edit_link "Improve this page" %}.
{: .text-right.text-gray.small }

{%- endif %}