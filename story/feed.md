---
description: Story feed is collections of stories.
---

# /story/feed

Don't get confuse with RSS feed or data feed. \(We are lack of terms. Lucky we didn't call it Larry as story collections. - [https://www.youtube.com/watch?v=av9OftW](https://www.youtube.com/watch?v=av9OftW)\)

{% api-method method="get" host="https://api.newscraft.io" path="/v1/story/feed" %}
{% api-method-summary %}
Get list of feeds
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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/story/feed" %}
{% api-method-summary %}
Add new feed
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

{% api-method-body-parameters %}
{% api-method-parameter name="slug" type="string" required=false %}
Slug name
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Feed name
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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/story/feed/:id" %}
{% api-method-summary %}
Edit existing feed
{% endapi-method-summary %}

{% api-method-description %}
Edit feed name \(as for now\). Will update the documentation if more meta-info add for the feed.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Feed ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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

{% api-method-body-parameters %}
{% api-method-parameter name="slug" type="string" required=false %}
slug
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Feed name
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/story/feed/:id" %}
{% api-method-summary %}
Delete feed
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Slug ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publish ID
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/story/feed/:id/sort" %}
{% api-method-summary %}
Get stories for feed
{% endapi-method-summary %}

{% api-method-description %}
Will response with list of stories for this feed collection.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Feed ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "items":
        [
            "xxx",
            "yyy",
            "zzz"
        ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.newscraft.io" path="/v1/story/feed/:id/sort" %}
{% api-method-summary %}
Submit stories for feed
{% endapi-method-summary %}

{% api-method-description %}
Send list of stories ID for this feed collection.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Feed ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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

POST with JSON body

```javascript
{
    "items": [
        "1aad71b0e77c036fab8936eec49300b9", // entry ID
        "fb0a3e5bca259b108efeca5362d39642",
        "7701b2b5956aea60e937407223507465",
        "62a3486ea1519ffd66de342bec2859e4",
        "7cb7726f0a8c362118848e5e8981a32a",
        "0b536b0aff8759aa726fc87cb71bf45e",
        "b1d8af089f014c8bf04709e10d7d76d3"
        ]
}
```

{% api-method method="get" host="https://api.newscraft.io" path="/v1/story/feed/:id/rev" %}
{% api-method-summary %}
Get feed revision
{% endapi-method-summary %}

{% api-method-description %}
Display feed revision
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Feed ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/story/feed/:id/rev" %}
{% api-method-summary %}
Restore feed revision
{% endapi-method-summary %}

{% api-method-description %}
Caution: Action will be automatically replace stories list in feed
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Feed ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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

{% api-method-body-parameters %}
{% api-method-parameter name="rev\_id" type="string" required=true %}
Revision ID
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

