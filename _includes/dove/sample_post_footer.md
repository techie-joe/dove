{%- include ui.html %}
{%- capture _posts %}
- `// links to other post`
- [Example post](#){: onclick="{{onclick}}"}
- [Another link to a post](#){: onclick="{{onclick}}"}
- [You get the point](#){: onclick="{{onclick}}"}
{%- endcapture %}
{{ _posts | markdownify }}