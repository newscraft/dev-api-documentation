# /search/entry

{% api-method method="get" host="https://api.newscraft.io/" path="v1/search/entry" %}
{% api-method-summary %}
Search entry
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=false %}
string - story title \(for now\)
{% endapi-method-parameter %}

{% api-method-parameter name="date\_from" type="integer" required=false %}
timestamp: 1531391894
{% endapi-method-parameter %}

{% api-method-parameter name="date\_to" type="integer" required=false %}
timestamp: 1531448643
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

