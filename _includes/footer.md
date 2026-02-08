{%- include ui.html %}
{%- if page.use_footer == false -%}
<style>._footer{display:none !important}</style>
{%- elsif site.github.repository_nwo == 'techie-joe/dove' %}
{%- include dove/footer.md %}
{%- else %}
{%- unless page.use_footer contains 'edit_link_only' -%}

<!-- your footer goes here -->
{%- unless page.path == '404.md'
        or page.path == 'index.md'
        or page.path == 'pages.md'
        or page.path == 'posts.md' %}
{%- capture site_nav %}{%- include site_nav.md %}{%- endcapture %}
{{ thin_hr }}
<nav class="_common_nav">{{ site_nav | markdownify }}</nav>
{%- endunless %}

{%- endunless %}

{{ thin_hr }}

This site is open source. {% github_edit_link "Improve this page" %}.
{: .text-right.text-gray.small }

{%- endif %}