{%- include ui.html %}
{%- include dove/icon.html %}

<style>
  ._article h1.hero { border:0;padding-bottom:0;margin-bottom:1rem }
  ._article h2.desc { border:0;margin-top:-0.7em }
</style>

<div class="relative"><div class="_bimoji">{{icon}}</div></div>

# Main title
{: .hero}

## {{icon}} Slogan and description
{: .desc }

Immediately after is usually a **[call to action](#CTA){: onclick="{{onclick}}" }**.

<div style="margin-top:2.5rem"></div>
<a href="#CTA1" onclick="{{onclick}}" title="Main call to action." class="button primary" style="padding:.5em 1em;font-size:1rem;">Get started</a>{{-}}
<a href="#CTA2" onclick="{{onclick}}" title="Secondary call to action." class="button secondary" style="padding:.5em 1em;font-size:1rem;font-weight:normal;">Learn more</a>

{{ thin_hr }}

`// home page sample written in markdown`

{{ thin_hr }}

{% include dove/vars_page.md %}