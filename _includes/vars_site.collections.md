{%- assign nl="
" %}
{%- assign pad = "             " %}
{%- assign word_key = "[0] key,[1] key,[n] keys" %}
{%- assign post_keys = "id,url,slug,title,description,author,draft,comments,date,layout,ext,name,path,relative_path,collection,categories,tags,content,excerpt,output,previous,next" %}

###### site.collections

```yml
# {% include plural.md word="[0] collection,[1] collection,[n] collections" val=site.collections %}
{%- for collection in site.collections %}
  {{-nl-}} # collection.{{ forloop.index | append: ' - ' }}
  {%- include plural.md val=collection.keys word=word_key %}
  {{-nl-}}
  {%-
    include inspect.md
    val = collection
    include = "label,docs,files,output,relative_directory,permalink"
    exclude = "directory"
    bloi = "docs"
    pad = pad
    tab = "  "
  %}
  {%- else -%} {{-nl-}} # its empty
{%- endfor %}
```
{: .no_max_height }


###### site.categories

```yml
# {% include plural.md word="[0] category,[1] category,[n] categories" val=site.categories %}
{%- if site.categories %}
  {%- assign sorted_categories = site.categories | sort %}
  {%- for category in sorted_categories %}
    {%- assign key = category[0] %}
    {%- assign _posts = category[1] %}
    {{-nl-}} # category.{{ forloop.index | append: ' - ' }}
    {{- key | append: ' - ' }}
    {%- include plural.md val=_posts word="[0] post,[1] post,[n] posts" %}
    {%- assign sorted_posts = _posts | sort: "id" %}
    {%- for post in sorted_posts %}
      {{-nl-}} {{-"  "-}} # post.{{ forloop.index | append: ' - ' }}
      {%- include plural.md val=post.keys word=word_key %}
      {{-nl-}}
      {%-
        include inspect.md
        val = post
        include = post_keys
        pad = pad
        tab = "    "
      %}
      {%- else -%} {{-nl-}} # its empty
    {%- endfor %}
  {%- endfor %}
  {%- else -%} {{-nl-}} # its empty
{%- endif %}
```

###### site.tags

```yml
# {% include plural.md word="[0] tag,[1] tag,[n] tags" val=site.tags %}
{%- if site.tags %}
  {%- assign sorted_tags = site.tags | sort %}
  {%- for tag in sorted_tags %}
    {%- assign key = tag[0] %}
    {%- assign _posts = tag[1] %}
    {{-nl-}} # tag.{{ forloop.index | append: ' - ' }}
    {{- key | append: ' - ' }}
    {%- include plural.md val=_posts word="[0] post,[1] post,[n] posts" %}
    {%- assign sorted_posts = _posts | sort: "id" %}
    {%- for post in sorted_posts %}
      {{-nl-}} # post.{{ forloop.index | append: ' - ' }}
      {%- include plural.md val=post.keys word=word_key %}
      {{-nl-}}
      {%-
        include inspect.md
        val = post
        include = post_keys
        pad = pad
        tab = "    "
      %}
      {%- else -%} {{-nl-}} # its empty
    {%- endfor %}
  {%- endfor %}
  {%- else -%} {{-nl-}} # its empty
{%- endif %}
```