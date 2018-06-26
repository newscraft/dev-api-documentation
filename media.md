# /assets

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets" %}
{% api-method-summary %}
Get assets
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all assets item.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets" %}
{% api-method-summary %}
Post asset item
{% endapi-method-summary %}

{% api-method-description %}
This endpoint to upload asset item \(file\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets/:id" %}
{% api-method-summary %}
Get asset item info
{% endapi-method-summary %}

{% api-method-description %}
Get particular asset meta info, filename and URL.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Asset ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}
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

