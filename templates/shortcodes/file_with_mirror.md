{% if get_env(name="USE_CDN", default="false") == "true" %}
    {% set url = "https://files.skmgeek.com/blog/" ~ path %}
{% else %}
    {% set url = "files/" ~ path %}
{% endif %}

*[{{ text }}]({{ get_url(path=url) | safe }})&nbsp;&nbsp;&nbsp;[(Mirror)]({{ mirror }})*