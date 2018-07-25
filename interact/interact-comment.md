# /interact/comment

{% api-method method="get" host="https://api.newscraft.io" path="/v1/interact/comment/:sid" %}
{% api-method-summary %}
Get Comment List for Particular Story
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="sid" type="string" required=true %}
**Story ID**
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="sort\_desc" type="boolean" required=false %}
true \(descending\) \| false \(ascending\)
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
date\_pub, date\_mod
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=false %}
en \| my \| zh
{% endapi-method-parameter %}

{% api-method-parameter name="cid" type="number" required=false %}
Comment ID
{% endapi-method-parameter %}

{% api-method-parameter name="uid" type="number" required=false %}
User ID
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="number" required=false %}
0. Trash  
2. Published
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/interact/comment/" %}
{% api-method-summary %}
Get Comment List
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
{% api-method-parameter name="sort\_desc" type="boolean" required=false %}
true \(descending\) \| false \(ascending\)
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
date\_pub, date\_mod
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=false %}
en \| my \| zh
{% endapi-method-parameter %}

{% api-method-parameter name="cid" type="number" required=false %}
Comment ID
{% endapi-method-parameter %}

{% api-method-parameter name="uid" type="number" required=false %}
User ID
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="number" required=false %}
0. Trash  
2. Published
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/interact/comment/:cid" %}
{% api-method-summary %}
Delete Comment
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="cid" type="number" required=true %}
comment ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="status" type="number" required=false %}
0. Trash \(default\)  
2. Published
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/interact/comment/report/:cid" %}
{% api-method-summary %}
Get Reported Comment by Comment ID
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="cid" type="string" required=true %}
Comment ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/interact/comment/report" %}
{% api-method-summary %}
Get All Reported Comment
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/interact/comment/report/:rid" %}
{% api-method-summary %}
Delete Reported Comment
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="rid" type="string" required=true %}
Report ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

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

