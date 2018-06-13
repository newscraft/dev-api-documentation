---
description: 'This endpoint to retrieve, post and delete story.'
---

# /story/entry

{% api-method method="get" host="https://api.newscraft.io" path="/v1/story/entry" %}
{% api-method-summary %}
Get stories
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get entry.
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

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
The entry ID provided by system. 32-char
{% endapi-method-parameter %}

{% api-method-parameter name="sid" type="string" required=false %}
Custom ID which stored during POST
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
Default, limit is 50 \(maximum\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" required=false %}
Default, start from 0
{% endapi-method-parameter %}

{% api-method-parameter name="feed\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="cat\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="lang\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="author\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
Default, date\_pub. Possible value: date\_pub, date\_mode, title
{% endapi-method-parameter %}

{% api-method-parameter name="sort\_desc" type="boolean" required=false %}
If true, the sort is descending. If false, sort is ascending.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.newscraft.io" path="/v1/story/entry/:id" %}
{% api-method-summary %}
Get single story
{% endapi-method-summary %}

{% api-method-description %}

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

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
The entry ID provided by system. 32-char
{% endapi-method-parameter %}

{% api-method-parameter name="sid" type="string" required=false %}
Custom ID which stored during POST
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
Default, limit is 50 \(maximum\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" required=false %}
Default, start from 0
{% endapi-method-parameter %}

{% api-method-parameter name="feed\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="cat\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="lang\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="author\_id" type="string" required=false %}
32-char
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
Default, date\_pub. Possible value: date\_pub, date\_mode, title
{% endapi-method-parameter %}

{% api-method-parameter name="sort\_desc" type="boolean" required=false %}
If true, the sort is descending. If false, sort is ascending.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.newscraft.io" path="/v1/story/entry" %}
{% api-method-summary %}
Post new story
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=false %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Submit with JSON body

```javascript
{  
   "sid":"999999",
   "title":"Aizu Test",
   "cat_str":"news",
   "author_str":"Reuters",
   "lang_str":"en",
   "summary":"Despite Rodman tweeting about impending visit, US president says athlete has not been invited to S&#39;pore. ",
   "date_pub":1528552260,
   "date_mod":1528552668,
   "status":"published",
   "content":"<p>Aizu - This is a test content. Lorem ipsum dolor sit amet</p><p>Ad cum graeci nostrum.</p>"
}
```

{% api-method method="post" host="https://api.newscraft.io" path="/v1/entry/:id" %}
{% api-method-summary %}
Edit existing story
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Entry ID provided by system
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```javascript
{  
   "sid":"999999",
   "title":"Aizu Test",
   "cat_str":"news",
   "author_str":"Reuters",
   "lang_str":"en",
   "summary":"Despite Rodman tweeting about impending visit, US president says athlete has not been invited to S&#39;pore. ",
   "date_pub":1528552260,
   "date_mod":1528552668,
   "status":"published",
   "content":"<p>Aizu - This is a test content. Lorem ipsum dolor sit amet</p><p>Ad cum graeci nostrum.</p>"
}
```

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/entry/:id" %}
{% api-method-summary %}
Delete single story
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Submit the entry with JSON body data.

{% api-method method="get" host="https://api.newscraft.io" path="/v1/entry/search" %}
{% api-method-summary %}
Search story
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-api-key" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

