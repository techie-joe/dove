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

Often appearing immediately after is a **[call to action](#CTA){: onclick="event.preventDefault();" }**.

<div style="margin-top:3rem"></div>
<a href="#CTA1" onclick="event.preventDefault();" title="Main call to action." class="button primary" style="width:10rem;height:3rem;font-size:1.2rem;">Get started</a>{{-}}
<a href="#CTA2" onclick="event.preventDefault();" title="Secondary call to action." class="button secondary" style="width:10rem;height:3rem;font-size:1.2rem;font-weight:normal;">Learn more</a>

{{ thin_hr }}

`// home page sample written in html`