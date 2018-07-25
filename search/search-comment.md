# /search/comment

{% api-method method="get" host="https://api.newscraft.io" path="/v1/search/comment" %}
{% api-method-summary %}
Search Comment
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
{% api-method-parameter name="q" type="string" required=false %}
Comment string
{% endapi-method-parameter %}

{% api-method-parameter name="date\_to" type="number" required=false %}
1532496649
{% endapi-method-parameter %}

{% api-method-parameter name="date\_from" type="number" required=false %}
1532478649
{% endapi-method-parameter %}

{% api-method-parameter name="sort\_desc" type="boolean" required=false %}
true \(descending\) \| false \(ascending\)
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
date\_mod, date\_pub \(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
default 100
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="number" required=false %}
0. Trash  
2. Published \(default\)
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/search/comment/report" %}
{% api-method-summary %}
Search Reported Comment
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
{% api-method-parameter name="q" type="string" required=false %}
Comment string
{% endapi-method-parameter %}

{% api-method-parameter name="date\_to" type="string" required=false %}
1532478540
{% endapi-method-parameter %}

{% api-method-parameter name="date\_from" type="string" required=false %}
1532478649
{% endapi-method-parameter %}

{% api-method-parameter name="sort\_desc" type="string" required=false %}
true \(descending\) \| false \(ascending\)
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
date\_mod \(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="string" required=false %}
Default 100
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
0. Hide  
1. Show \(default\)
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

