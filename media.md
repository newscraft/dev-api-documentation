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

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="integer" required=false %}
Default 30, max 300
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
Support parameters are date\_pub, date\_mod, name
{% endapi-method-parameter %}

{% api-method-parameter name="filetype" type="string" required=false %}
image/jpeg, image/png, audio/mp3
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

{% api-method-body-parameters %}
{% api-method-parameter name="dir" type="string" required=false %}
Folder or Directory name. Should use Folder ID instead. \(next plan\)  
  
Default path: 'host/'.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Asset name.
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Asset description.
{% endapi-method-parameter %}

{% api-method-parameter name="keyword" type="string" required=false %}
Asset keyword.
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets/id-get/:id" %}
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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/id-update/:id" %}
{% api-method-summary %}
Update Asset item info
{% endapi-method-summary %}

{% api-method-description %}
Update asset info by ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Asset ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="folder\_id" type="string" required=false %}
Folder ID.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Asset name.
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Asset description.
{% endapi-method-parameter %}

{% api-method-parameter name="keyword" type="string" required=false %}
Asset keyword.
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/assets/id-delete/:id" %}
{% api-method-summary %}
Delete Asset
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will delete asset specify.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Asset ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/dir-create/" %}
{% api-method-summary %}
Create directory
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will create the folder.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Folder name.
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets/dir-list/" %}
{% api-method-summary %}
Get list of directory
{% endapi-method-summary %}

{% api-method-description %}
Return a list of directory and child.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="dir" type="string" required=false %}
Folder or Directory name. Should use Folder ID instead. \(next plan\)
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="integer" required=false %}
Default 30
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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/dir-update/:id" %}
{% api-method-summary %}
Update directory meta info.
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will update directory info.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Folder of Directory ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Folder or  Directory name.
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/assets/dir-delete/:id" %}
{% api-method-summary %}
Delete directory
{% endapi-method-summary %}

{% api-method-description %}
Delete specify directory by folder/directory ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Folder or Directory ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
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

