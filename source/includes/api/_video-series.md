## VideoSeries

### List VideoSeries

```http
GET /v1/video-series?limit=100 HTTP/1.1
Host: api.candidio.com
Content-Type: application/json
Authorization: Bearer n8P1vbHYYsznzb25oO3PiePEnLzaeRhdq7Zk8YUJ
```



```json
{
	"data": [{
    "type": "video-series",
		"id": "vds_hashhere",
		"title": "VideoSeries title",
		"audience": "",
		"synopsis": "",
		"turnaround": 5,
		"internal_notes": "Internal notes about this video-series.",
    "created_at": "2016-04-04 07:28:30",
    "updated_at": "2016-04-04 07:28:30"
	}],
  "meta": {
		"pagination": {
			"total": 4,
			"count": 4,
			"per_page": 100,
			"current_page": 1,
			"total_pages": 1,
			"links": []
		}
	}
}
```

These endpoints return a collection of paginated video-series.

#### HTTP Request

Get video-series.

`GET https://api.candidio.com/v1/video-series`

Get video-series scoped by workspace.

`GET https://api.candidio.com/v1/workspaces/<ID>/video-series`

#### Embeddable Relationships

Relationship | Description
------------ | -----------
created_by | User that created a video-series.
productions | Productions in a video-series.
collaborators | Users a video-series has been shared with.
workspace | Workspace a video-series belongs to.

#### Available Scopes

Scope | Argument | Description
----- | -------- | -----------
user | ID | Scope video-series by creator or sharing users.
workspace | ID | Scope video-series by workspace they belong to.

### Get a Specific VideoSeries

```http
GET /v1/video-series/<ID> HTTP/1.1
Host: api.candidio.com
Content-Type: application/json
Authorization: Bearer n8P1vbHYYsznzb25oO3PiePEnLzaeRhdq7Zk8YUJ
```



```json
{
	"data": {
    "type": "video-series",
		"id": "vds_hashhere",
		"title": "VideoSeries Name",
		"audience": "",
		"synopsis": "",
		"turnaround": 5,
		"internal_notes": "Internal notes about this video-series.",
    "created_at": "2016-04-04 07:28:30",
    "updated_at": "2016-04-04 07:28:30"
	}
}
```

These endpoints return a specific video-series.

#### HTTP Request

Get video-series.

`GET https://api.candidio.com/v1/video-series/<ID>`

Get video-series scoped by workspace.

`GET https://api.candidio.com/v1/workspaces/<ID>/video-series/<ID>`

#### Embeddable Relationships

Relationship | Description
------------ | -----------
created_by | User that created a video-series.
productions | Productions in a video-series.
collaborators | Users a video-series has been shared with.
workspace | Workspace a video-series belongs to.

#### Available Scopes

Scope | Argument | Description
----- | -------- | -----------
user | ID | Scope video-series by creator or sharing users.
workspace | ID | Scope video-series by workspace it belongs to.

### Create VideoSeries

```http
POST /v1/workspaces/<ID>/video-series HTTP/1.1
Host: api.candidio.com
Content-Type: application/json
Authorization: Bearer n8P1vbHYYsznzb25oO3PiePEnLzaeRhdq7Zk8YUJ

{
  "data": {
  		"title": "VideoSeries Name"
  }
}
```



```json
{
	"data": {
    "type": "video-series",
    "id": "vds_hashhere",
    "title": "VideoSeries Name",
		"audience": "",
		"synopsis": "",
		"turnaround": 5,
    "internal_notes": "Internal notes about this video-series.",
    "created_at": "2016-04-04 07:28:30",
    "updated_at": "2016-04-04 07:28:30"
	}
}
```

These endpoints create video-series.

#### HTTP Request

Create video-series.

`POST https://api.candidio.com/v1/video-series`

Create video-series that belongs to a workspace.

`POST https://api.candidio.com/v1/workspaces/<ID>/video-series`

#### JSON Payload Parameters

Parameter | Required | Description
--------- | -------- | -----------
workspace_id | yes* | Defines workspace to assign shot to.
title | yes | VideoSeries title.
internal_notes | no | Internal notes, for administrators only.

### Update VideoSeries

```http
PUT /v1/workspaces/<ID>/video-series/<ID> HTTP/1.1
Host: api.candidio.com
Content-Type: application/json
Authorization: Bearer n8P1vbHYYsznzb25oO3PiePEnLzaeRhdq7Zk8YUJ

{
  "data": {
  		"title": "VideoSeries Name Updated"
  }
}
```



```json
{
	"data": {
    "type": "video-series",
    "id": "vds_hashhere",
    "title": "VideoSeries Name Updated",
		"audience": "",
		"synopsis": "",
		"turnaround": 5,
    "internal_notes": "Internal notes about this video-series.",
    "created_at": "2016-04-04 07:28:30",
    "updated_at": "2016-04-04 07:28:30"
	}
}
```

These endpoints update video-series.

#### HTTP Request

Update video-series.

`PUT https://api.candidio.com/v1/video-series/<ID>`

Update video-series scoped by workspace.

`PUT https://api.candidio.com/v1/workspaces/<ID>/video-series/<ID>`

#### JSON Payload Parameters

Parameter | Required | Description
--------- | -------- | -----------
workspace_id | yes* | Defines workspace to scope shot by.
title | yes | VideoSeries title.
internal_notes | no | Internal notes, for administrators only.

### Delete VideoSeries

```http
DELETE /v1/workspaces/<ID>/video-series/<ID> HTTP/1.1
Host: api.candidio.com
Content-Type: application/json
Authorization: Bearer n8P1vbHYYsznzb25oO3PiePEnLzaeRhdq7Zk8YUJ
```



```json
{
	"success": {
		"http_code": 200,
		"message": "Success"
	}
}
```

These endpoints delete a specific video-series.

#### HTTP Request

Delete a video-series.

`DELETE https://api.candidio.com/v1/video-series/<ID>`

Delete a video-series scoped by workspace.

`DELETE https://api.candidio.com/v1/workspaces/<ID>/video-series/<ID>`