{%- include ui.html %}
{%- capture _pages %}
- `// links to other page`
- [Example page](#){: onclick="{{onclick}}"}
- [Another link to a page](#){: onclick="{{onclick}}"}
- [You get the point](#){: onclick="{{onclick}}"}
{%- endcapture %}
{{ _pages | markdownify }}