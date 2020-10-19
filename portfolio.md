---
layout: default
title: Portfolio
---
# Recent work

<ol class="ul-reset portfolio_summary container">
{% for example in site.data.sites %}
    <li class="portfolio_summary__entry">
        <div style="background: {{example.bg_thumb}}" class="portfolio_summary__entry_thumb">
            <img alt="" 
            src="{{site.data.config.thumb_path}}{{example.img_name}}.jpg" 
            sizes="(min-width: 800px) 300px, 200px"
            srcset="{{site.data.config.thumb_path}}{{example.img_name}}-200.jpg 200w,     
                    {{site.data.config.thumb_path}}{{example.img_name}}-300.jpg 300w"
              />
        </div>
        <h2 class="portfolio_summary__entry_title">{{example.name}}</h2>
    
    </li>
{% endfor %}
</ol>


{% for example in site.data.sites %}
<section class="{% cycle 'odd', 'even' %} portfolio__entry container container-wide">
    <div class="portfolio__entry_thumbs" style="background: {{example.bg_work}}">
        <div><img src="{{site.data.config.screen_path}}{{example.img_name}}-1.jpg" /></div>
        <div><img src="{{site.data.config.screen_path}}{{example.img_name}}-2.jpg" /></div>
        <div><img src="{{site.data.config.screen_path}}{{example.img_name}}-3.jpg" /></div>
    </div>
    <div class="portfolio__entry_details">
        <h3>{{example.name}}</h3>
        <h4>{{example.subtitle}}</h4>
        {{example.content}}
    </div>
</section>
{% endfor %}