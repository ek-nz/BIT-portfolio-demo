---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
# I edited it because I wanted to add a tag cloud (Elise)
layout: home
nav: true
---
**Tags**
{% assign tags = site.tags | sort %}
{% for tag in tags %}
 <span class="site-tag">
    <a href="{{ site.baseurl }}/tag/{{ tag | first | slugify }}.html"
        style="font-size: {{ tag | last | size  |  times: 10 | plus: 75  }}%">
            {{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
    </a>
</span>
{%- endfor -%}
<br><br>
**Posts by date**
