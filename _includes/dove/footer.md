{%- include ui.html %}
{%- if page.use_footer == false -%}
<style>._footer{display:none !important}</style>
{%- else %}
{%- unless page.use_footer contains 'edit_link_only' or page.dir == '/vars/' -%}
{%- if page.sample -%}

{{ thin_hr }}

`// site footer`

{%- assign _sub = page.layout | remove: '-page'| remove: '-post' %}
{%- case _sub %}
{%- when 'core' or 'mallet' or 'prime' %}
{{ thin_hr }}
{%- capture sample_nav %}{%- include dove/sample_nav.md sub=_sub %}{%- endcapture %}
<nav class="_common_nav">{{ sample_nav | markdownify }}</nav>
{%- endcase %}

{%- else %}

{{ thin_hr }}

{%- unless page.path == 'posts.md' or page.path == 'pages.md' %}
{%- capture dove_nav %}{%- include dove/nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ dove_nav | markdownify }}</nav>
{%- endunless %}

{%- capture tj_nav %}{%- include dove/tj_nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ tj_nav | markdownify }}</nav>

{%- endif %}
{%- endunless %}

{{ thin_hr }}

This site is open source. {% github_edit_link "Improve this page" %}.
{: .text-right.text-gray.small }

{%- endif %}