# /search/asset

{% api-method method="get" host="https://api.newscraft.io" path="/v1/search/asset" %}
{% api-method-summary %}
Search Asset item
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="status" type="number" required=false %}
0. trash  
1. published \(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="sort\_desc" type="boolean" required=false %}
true \| false
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
date\_mod \(default\)  
date\_pub  
name
{% endapi-method-parameter %}

{% api-method-parameter name="q" type="string" required=false %}
string search - by name for now
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

