---
layout: default
permalink: /
---

<div class="title">
    <img src="/assets/images/profile-sm.png" alt="{{ site.author }}" />
    <h1>{{ site.author }}</h1>
    <h3>Ténor TEST</h3>
</div>
<div class="main">
    {% if site.data.general %}
        <ul class="socials websites">
            {% for item in site.data.general %} 
                {% assign key = item[0] %}
                {% assign value = item[1] %}
                <li style="--bg-image: url('/assets/images/{{ key | slugify }}.png')">
                    <a href="{{ key }}{{ value}}" target="_blank">
                        {{ value }}
                    </a>
                </li>
            {% endfor %}
        </ul>
    {% endif %}
    {% if site.data.music %}
        <ul class="socials music">
            {% for item in site.data.music %} 
                {% assign key = item[0] %}
                {% assign value = item[1] %}
                <li style="--bg-image: url('/assets/images/{{ key | slugify }}.png')">
                    <a href="{{ value }}" target="_blank">
                        {{ key }}
                    </a>
                </li>
            {% endfor %}
        </ul>
    {% endif %}
    {% if site.data.social %}
        <ul class="socials">
            {% for item in site.data.social %} 
                {% assign key = item[0] %}
                {% assign value = item[1] %}
                <li class="{{ key }}" style="--bg-image: url('/assets/images/{{ key }}.png')">
                    <a href="https://{{ key }}.com/{{ value }}" target="_blank">
                        <span>{{ key | capitalize }}</span>
                    </a>
                </li>
            {% endfor %}
        </ul>
    {% endif %}
</div>
