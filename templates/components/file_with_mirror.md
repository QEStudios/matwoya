{% component file_with_mirror(path: string, text: string, mirror: string) -%}
{% set url = "files/" ~ path -%}

*[{{ text }}]({{ get_url(path=url) | safe }})&nbsp;&nbsp;&nbsp;[(Mirror)]({{ mirror }})*
{%- endcomponent %}