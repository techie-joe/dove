---
layout: core
index: false
use_footer: demo_sample
title: Home
description: Home template.
---
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

**[Preview the theme](./preview)** to see how it looks and **[start using it](./#how-to-use)** today!

{{ thin_hr }}

`// home content in markdown`