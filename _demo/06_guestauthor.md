---
title: A guest author
subtitle: And with a new project
categories: [demo, author-guest]
header_type: splash
tags: [header-splash, demo, example ]
date: 2020-02-29
show_date         : true
show_sociallinks  : true
show_tags         : true
show_categories   : true
show_bottomnavs   : true
show_author       : true
show_comments     : true
project_links:
    - url: https://github.com/
      icon: fab fa-github
      label: Check it on Github
author:
  name: Octocat
  avatar: https://github.com/octocat.png
  location: San Francisco, CA 94107, United States
  links:                
    - url: https://github.com/github/
      icon: "fab fa-github"
    - url: https://twitter.com/github
      icon: fab fa-twitter
    - url: https://github.com/facebook
      icon: "fab fa-facebook"
    - url: https://www.linkedin.com
      icon: "fab fa-linkedin"
---
This page shows how a contributor could be added to your blog. In this case **Octocat** is telling us about its plans on the next months...



```yaml
---
title: A guest author
subtitle: And with a new project
categories: [demo, author-guest]
header_type: splash
tags: [layout-default,header-splash, social-links, tags, categories, bottom-navs, date, comments, project-links, author, author-guest]
date: 2020-02-29
show_date         : true
show_sociallinks  : true
show_tags         : true
show_categories   : true
show_bottomnavs   : true
show_comments     : true
show_author       : true
project_links:
    - url: https://github.com/
      icon: fab fa-github
      label: Check it on Github
author:
  name: Octocat
  avatar: https://github.com/octocat.png
  location: San Francisco, CA 94107, United States
  links:                
    - url: https://github.com/github/
      icon: "fab fa-github"
    - url: https://twitter.com/github
      icon: fab fa-twitter
    - url: https://github.com/facebook
      icon: "fab fa-facebook"
    - url: https://www.linkedin.com
      icon: "fab fa-linkedin"
---
```
{%- for tag in page.tags %}
  {%- if forloop.first -%}
    {%- assign alldocs = site.documents | 
                    where_exp: "item", "item.tag contains tag" -%}
  {%- else -%}
    {%- assign docloop = site.documents | 
                    where_exp: "item", "item.collection contains tag" -%}
    {%- assign alldocs = alldocs | concat: docloop %}
  {%- endif -%}
{%- endfor -%}



{% for document in alldocs %}
  <p> {{ document.title }}
  {% for dtag in document.tag %}
    <small>{{ dtag }}</small>
  {%- endfor -%}
{%- endfor -%}

