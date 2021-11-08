
<div class="{{include.class}} text-center">
{%if include.link%}<a href="{{ include.link | absolute_url }}">{% endif %}
<img class="img-fluid" src="{{ include.img | prepend: '/images/' | absolute_url }}" alt="{{ include.alt | default: 'demo image' }}">
{%if include.link%}</a>{% endif %}
{% if include.caption %}<p class="small">{{ include.caption }}</p>{% endif %}
</div>

