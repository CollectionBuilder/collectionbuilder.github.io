---
layout: post
title: 'Customizing Footer Date Display'
subtitle:
author: Evan Williamson; Mark McFate
publish-date: March 07, 2025
tags: [customization, tip]
short_description: 'How to tweak the date displayed in the footer'
---

At the bottom of the default footer of the CB templates you will see something like "Last updated 2025". 
The year is generated at the time the site is built giving users a general idea of how actively the site is updated. 
Often maintainers / developers want a more specific date when checking up on content, so if you view the page source, you will find an HTML comment at the bottom of the head section with the full build date.

Like most things in CB, you can customize this by digging into the template if it doesn't meet the needs of your project.

For example, [Mark McFate](https://github.com/SummittDweller) recently wanted to add a more complete date including the month and day to his project footer. 
In the file "_includes/footer.html" he edited the line: 

`{% raw %}<p class="text-white">Last updated {{ site.time | date: '%Y' }}</p>{% endraw %}` 

updating the options on the [Liquid date filter](https://shopify.github.io/liquid/filters/date/) to look like:

`{% raw %}<p class="text-white">Last updated {{ site.time | date: '%Y-%b-%d' }}</p>{% endraw %}`

These options will add a date with year - month abbreviation - day. 

The using the [strftime syntax](https://strftime.net/) you can modify the date filter options to output a date in any format you would like to display.
The value `site.time` will be the current time when Jekyll is building the site. 

Mark also decided to add logic so that on the About page *only* a more specific date would be displayed. 
The line above was edited to look like this:

```{% raw %}
{% assign stamp = site.time | date: '%Y-%b-%d' %}
{% if page.url == "/about.html" %}
    {% assign stamp = site.time | date: '%B %-d, %Y @ %l:%M%P %Z' %}
{% endif %}
<p class="text-white">Last updated: {{ stamp }}</p>
{% endraw %}
```
