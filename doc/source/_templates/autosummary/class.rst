{{ fullname }}
{{ underline }}

.. currentmodule:: {{ module }}

.. autoclass:: {{ objname }}
  :no-members:

{% block attributes %}
{% if attributes %}
.. rubric:: Attributes

.. autosummary::
  :toctree:
  :nosignatures:
{% for item in attributes %}
  ~{{ name }}.{{ item }}
{%- endfor %}
{% endif %}
{% endblock %}

{% block methods %}
{% if methods %}
.. rubric:: Methods

.. autosummary::
  :toctree:
  :nosignatures:
{% for item in methods %}
  ~{{ name }}.{{ item }}
{%- endfor %}
{% endif %}
{% endblock %}
