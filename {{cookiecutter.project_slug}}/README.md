{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{% if is_open_source %}
![PyPI version](https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}.svg)
[![Build Status](https://img.shields.io/travis/ACCESS-NRI/{{ cookiecutter.project_slug }}.svg)](https://travis-ci.com/ACCESS-NRI/{{ cookiecutter.project_slug }})
[![Documentation Status](https://readthedocs.org/projects/{{ cookiecutter.project_slug | replace("_", "-") }}/badge/?version=latest)](https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io/en/latest/?version=latest)
{% endif %}

{% if cookiecutter.add_pyup_badge == 'y' %}
[![Updates](https://pyup.io/repos/github/ACCESS-NRI/{{ cookiecutter.project_slug }}/shield.svg)](https://pyup.io/repos/github/ACCESS-NRI/{{ cookiecutter.project_slug }}/)
{% endif %}

{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: [https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io](https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io)
{% endif %}

## Features

* TODO

## Credits

This package was created with [Cookiecutter](https://github.com/audreyr/cookiecutter) and the [`ACCESS-NRI/cookiecutter-pypackage-access`](https://github.com/ACCESS-NRI/cookiecutter-pypackage-access) project template. 