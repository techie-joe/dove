{%- include ui.html %}
{%- if page.use_footer == false -%}
<style>._footer{display:none !important}</style>
{%- else %}
{%- unless page.use_footer contains 'edit_link_only' or page.dir == '/vars/' -%}
{%- if page.sample -%}

{{ thin_hr }}

`// site footer`

{%- else %}

{{ thin_hr }}

{%- unless page.path == 'posts.md' or page.path == 'pages.md' %}
{%- capture dove_nav %}{%- include dove/nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ dove_nav | markdownify }}</nav>
{%- endunless %}

{%- capture tj_footer %}
**Techie Joe's**
{{- angle -}}
[Website](https://techie-joe.github.io){: target="_techiejoe_website" }
{{- bull -}}
[Profile](https://github.com/techie-joe){: target="_techiejoe_profile" }
{{- bull -}}
[ThemeJs](https://techie-joe.github.io/nova/site/themejs){: target="_themejs" }
{%- endcapture %}
<nav class="_common_nav">{{ tj_footer | markdownify }}</nav>

{%- endif %}
{%- endunless %}

{{ thin_hr }}

This site is open source. {% github_edit_link "Improve this page" %}.
{: .text-right.text-gray.small }

{%- endif %}