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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="date\_start" type="string" required=false %}
\(only for MK publisher\) date when the image published
{% endapi-method-parameter %}

{% api-method-parameter name="date\_end" type="string" required=false %}
\(only for MK publisher\) date-end when the image published - use together with date\_start
{% endapi-method-parameter %}

{% api-method-parameter name="keyword" type="string" required=false %}
\(only for MK publisher\) description search
{% endapi-method-parameter %}

{% api-method-parameter name="cursor\_start" type="string" required=false %}
\(only for MK publisher\) next cursor string. provided by previous "page" call
{% endapi-method-parameter %}

{% api-method-parameter name="folder\_id" type="string" required=false %}
Folder ID \(for MK publisher, folder id for recent images is "recent"\)
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="string" required=false %}
\(MK publisher will show default 200 items\) Default 100
{% endapi-method-parameter %}

{% api-method-parameter name="sort\_desc" type="string" required=false %}
\(not available for MK publisher\) true \(descending\) \| false \(ascending\)
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
\(not available for MK publisher\) date\_pub \(default\),  
date\_mod,  
name
{% endapi-method-parameter %}

{% api-method-parameter name="filetype" type="string" required=false %}
\(not available for MK publisher\) image,  
audio,  
application,  
text,  
etc..
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="number" required=false %}
\(not available for MK publisher\) 1 \| 0
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
	"status": true,
	"message": null,
	"result": [
		{
			"id": "53ccedfa2596cf802cbbec3feba3d6b5",
			"type": "image/png",
			"name": "Screen Shot 2018-08-28 at 1.08.19 PM.png-(edited on 20180925040707)",
			"description": "",
			"keyword": "",
			"user_pub": "eshwaren@malaysiakini.com",
			"folder_id": "ac2938d1999d70e6c12240e2d2111111",
			"date_pub": 1537848428,
			"date_mod": 1537848428,
			"user_mod": "",
			"status": 1,
			"img_o": {
				"id": "53ccedfa2596cf802cbbec3feba3d6b5-original.png",
				"hostname": "https://assets.newscraft.io/host/",
				"contentLength": 29065,
				"width": 441,
				"height": 100
			},
			"file": {
				"id": "53ccedfa2596cf802cbbec3feba3d6b5-original.png",
				"hostname": "https://assets.newscraft.io/host/",
				"contentLength": 29065,
				"width": 441,
				"height": 100
			},
			"img_l": {
				"id": "53ccedfa2596cf802cbbec3feba3d6b5-large.png",
				"hostname": "https://assets.newscraft.io/host/",
				"contentLength": 144340,
				"width": 1024,
				"height": null
			},
			"img_m": {
				"id": "53ccedfa2596cf802cbbec3feba3d6b5-medium.png",
				"hostname": "https://assets.newscraft.io/host/",
				"contentLength": 17187,
				"width": 300,
				"height": null
			},
			"img_s": {
				"id": "53ccedfa2596cf802cbbec3feba3d6b5-small.png",
				"hostname": "https://assets.newscraft.io/host/",
				"contentLength": 2957,
				"width": 50,
				"height": 50
			},
			"img_t": {
				"id": "53ccedfa2596cf802cbbec3feba3d6b5-thumb.png",
				"hostname": "https://assets.newscraft.io/host/",
				"contentLength": 3120,
				"width": 100,
				"height": null
			},
			"original_name": "e93cf98166428063ae4ff226fc9e63ad",
			"contentLength": 29065
		}
	]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
	"status": false,
	"message": "NO RESULT",
	"result": null
}
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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID
{% endapi-method-parameter %}

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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="file" type="string" required=true %}
Asset file.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_pub" type="string" required=false %}
User Publish
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Asset name
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Asset description.
{% endapi-method-parameter %}

{% api-method-parameter name="folder\_id" type="string" required=false %}
Folder ID
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/:id" %}
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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="folder\_id" type="string" required=false %}
Folder ID.
{% endapi-method-parameter %}

{% api-method-parameter name="keyword" type="string" required=false %}
keyword
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Asset description.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Asset name.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_mod" type="string" required=false %}
username \| email
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/assets/:id" %}
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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID.
{% endapi-method-parameter %}

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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/dir" %}
{% api-method-summary %}
Create folder
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will create the folder.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="parent\_id" type="string" required=false %}
Parent ID.
{% endapi-method-parameter %}

{% api-method-parameter name="favourite" type="boolean" required=false %}
true \| false
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Folder name.
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets/dir" %}
{% api-method-summary %}
Get list of Folder
{% endapi-method-summary %}

{% api-method-description %}
Return a list of directory and child.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
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

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets/dir/:id" %}
{% api-method-summary %}
Get specific Folder
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Folder ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID.
{% endapi-method-parameter %}

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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/dir/:id" %}
{% api-method-summary %}
Update folder meta info.
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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-pub-id" type="string" required=true %}
Publisher ID.
{% endapi-method-parameter %}

{% api-method-parameter name="x-api-key" type="string" required=true %}
API Key provided by platform provider.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="parent\_id" type="string" required=false %}
Parent ID.
{% endapi-method-parameter %}

{% api-method-parameter name="favourite" type="boolean" required=false %}
true \| false
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Folder name
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

{% api-method method="delete" host="https://api.newscraft.io" path="/v1/assets/dir/:id" %}
{% api-method-summary %}
Delete folder
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
{% api-method-parameter name="x-property-id" type="string" required=true %}
Property ID.
{% endapi-method-parameter %}

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

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/setting" %}
{% api-method-summary %}
Post setting
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
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

JSON body format

```javascript
{
    "images": {
        "max_size_upload": 5000,
        "keyword": true,
        "folder_path": "host"
    },
    "videos": {
        "allow": true,
        "max_size_upload": 250000,
        "keyword": true,
        "folder_path": "host"
    },
    "others": {
        "allow": true,
        "file_format": ["pdf", "mp3", "mp4", "doc", "csv"],
        "keyword": true,
        "folder_path": "host"
    }
}
```

{% api-method method="post" host="https://api.newscraft.io" path="/v1/assets/setting/:id" %}
{% api-method-summary %}
Update setting
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Setting ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
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

JSON body format

```javascript
{
    "images": {
        "max_size_upload": 5000,
        "keyword": true,
        "folder_path": "host"
    },
    "videos": {
        "allow": true,
        "max_size_upload": 250000,
        "keyword": true,
        "folder_path": "host"
    },
    "others": {
        "allow": true,
        "file_format": ["pdf", "mp3", "mp4", "doc", "csv"],
        "keyword": true,
        "folder_path": "host"
    }
}
```

{% api-method method="get" host="https://api.newscraft.io" path="/v1/assets/setting" %}
{% api-method-summary %}
Get setting
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
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

