{%- assign nl="
" %}
{%- assign pad = "                 " %}

###### site.github.public_repositories | where: this-repo

```yml
{%- if site.github.public_repositories %}
  {%- assign sorted_repositories = site.github.public_repositories | where: "full_name",site.github.repository_nwo %}
  {{-nl-}} # {% include plural.md val=sorted_repositories word="[0] repository,[1] repository,[n] repositories" %}
  {%- for repo in sorted_repositories %}
    {{-nl-}} # repo.{{ forloop.index | append: ' ' }}
    {{-nl-}}
    {%-
      include inspect.md
      val = repo
      include = "name,full_name,description,html_url,homepage,created_at,updated_at,pushed_at,topics,language,visibility,size,private,is_template,archived,disabled,allow_forking,fork,forks,watchers,stargazers_count,forks_count,watchers_count,open_issues,open_issues_count,default_branch,releases,contributors,license,owner"
      blok = "license"
      bloi = "releases,contributors"
      pad = pad
      truncate = 100
    %}
  {%- endfor %}
  {%- else -%} {{-nl-}} # no repository found
{%- endif %}
```
{: .no_max_height }