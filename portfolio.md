---
layout: default
title: Portfolio
---
# Portfolio

<ol class="ul-reset portfolio_summary">
{% for example in site.data.sites %}
    <li class="{% cycle 'odd', 'even' %}" class="portfolio_summary__entry">
        <div style="background: {{example.bg}}" class="portfolio_summary__entry_thumb">
            <img src="{{example.img_thumb}}" />
        </div>
        <h2 class="portfolio_summary__entry_title">{{example.name}}</h2>
    
    </li>
{% endfor %}
</ol>