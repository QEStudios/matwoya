{% component file(path: string, text: string) -%}
{% set url = "files/" ~ path -%}
*[{{ text }}]({{ get_url(path=url) | safe }})*
{%- endcomponent %}