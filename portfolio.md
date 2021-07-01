---
layout: default
title: Portfolio
---
<h1 class="section_title"><span>Recent work</span></h1>

{% for example in site.data.sites %}
<div class="section-wrap">
<section class="{% cycle 'odd', 'even' %} portfolio__entry container container-wide">
    <div class="portfolio__entry_thumbs" style="background: {{example.bg_work}}">
        <div><img src="{{site.data.config.screen_path}}{{example.img_name}}-1.png" /></div>
        <div><img src="{{site.data.config.screen_path}}{{example.img_name}}-2.png" /></div>
        <div><img src="{{site.data.config.screen_path}}{{example.img_name}}-3.png" /></div>
    </div>
    <div class="portfolio__entry_details container">
        <h3 class="portfolio__entry_details_title">{{example.name}}</h3>
        <h4 class="portfolio__entry_details_subtitle">{{example.subtitle}}</h4>
        {{example.content | markdownify}}
    </div>
</section>
</div>
{% endfor %}