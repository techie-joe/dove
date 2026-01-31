{%- include ui.html %}
{%- assign _sub = "" %}
{%- assign _case = include.sub | default: page.layout | remove: '-page'| remove: '-post' %}
{%- case _case %}
{%- when 'core' or 'mallet' or 'prime' %}{%- assign _sub = "/" | append: _case %}
{%- endcase %}
<nav class="_common_nav mv">
<a href="#back" onclick="{{onclick}}(function(w){var h=w.history;w.opener?w.close():h.length>1?h.back():w.location.href='/';})(window)" class="button" title="Back to previous page">👈 Back</a>{{-}}
<a href="{{ site.home_url }}{{ _sub }}" class="button" title="Go to Home Page">Home</a>{{-}}
</nav>