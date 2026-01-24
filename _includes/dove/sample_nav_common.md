{%- include ui.html %}
{%- assign _sub = "" %}
{%- assign _case = include.sub | default: page.layout %}
{%- case _case %}
{%- when 'prime' or 'prime-page' or 'prime-post' %}{%- assign _sub="/prime" %}
{%- when 'nova' or 'nova-page' or 'nova-post' %}{%- assign _sub="/nova" %}
{%- when 'mallet' or 'mallet-page' or 'mallet-post' %}{%- assign _sub="/mallet" %}
{%- when 'core' or 'core-page' or 'core-post' %}{%- assign _sub="/core" %}
{%- endcase %}
<nav class="_nav_common mv">
<a href="#back" onclick="{{onclick}}(function(w){var h=w.history;w.opener?w.close():h.length>1?h.back():w.location.href='/';})(window)" class="button" title="Back to previous page">👈 Back</a>{{-}}
<a href="{{ site.home_url }}{{ _sub }}/home" class="button" title="Go to Home Page">Home</a>{{-}}
</nav>