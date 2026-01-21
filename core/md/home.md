---
layout: core
index: false
use_footer: demo_sample
title: Home
description: Home template.
---
{%- include ui.html %}

<style>
  #hero_block { padding:1rem 2rem }
  #hero_block h1 { padding-top:0;margin-top:1rem }
  #hero_block h2 { border:0;font-weight:normal;font-size:1.2em;margin-top:1rem }
</style>
<div id="hero_block" class="box no_overflow">
  <div class="relative"><div class="_bimoji">💎</div></div>
  <h1>💎 Site title</h1>
  <h2>Your site's description</h2>
</div>

{{ thin_hr }}

`// home content in markdown`