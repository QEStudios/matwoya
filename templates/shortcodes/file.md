{% if get_env(name="USE_CDN", default="false") == "true" %}
    {{ "https://files.skmgeek.com/blog/" ~ path }}
{% else %}
    {% set file_path = "files/" ~ path %}
    {{ get_url(path=file_path) | safe }}
{% endif %}