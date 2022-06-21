---
title: API Reference

language_tabs:
- bash
- javascript

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference.
[Get Postman Collection](http://localhost/docs/collection.json)

<!-- END_INFO -->

#admin

管理员管理
Class AdminController
<!-- START_b885ad82d83b00f1a424742dbe08fbc4 -->
## AdminList
管理员列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/admin?title=et&authGroup=nulla&limit=et&sort=alias&page=magni" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/admin"
);

let params = {
    "title": "et",
    "authGroup": "nulla",
    "limit": "et",
    "sort": "alias",
    "page": "magni",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/admin`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 管理员账号
    `authGroup` |  optional  | string 管理组ID
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_b885ad82d83b00f1a424742dbe08fbc4 -->

<!-- START_a25b869923aeb5665b37051b153fab1a -->
## AdminCreate
创建管理员

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/admin?name=et&email=voluptatem&cellphone=possimus&portrait=quam&password=alias" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/admin"
);

let params = {
    "name": "et",
    "email": "voluptatem",
    "cellphone": "possimus",
    "portrait": "quam",
    "password": "alias",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/admin`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 管理员账号
    `email` |  optional  | string 邮箱地址
    `cellphone` |  optional  | int 手机号
    `portrait` |  optional  | string 头像地址
    `password` |  optional  | string 密码

<!-- END_a25b869923aeb5665b37051b153fab1a -->

<!-- START_86324a172b7a75997b89ff6746121dd6 -->
## AdminEdit
保存管理员/密码

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/admin/1?id=ea&name=fuga&email=distinctio&cellphone=quas&portrait=eveniet&password=dolor" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/admin/1"
);

let params = {
    "id": "ea",
    "name": "fuga",
    "email": "distinctio",
    "cellphone": "quas",
    "portrait": "eveniet",
    "password": "dolor",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/admin/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 管理员ID
    `name` |  optional  | string 管理员账号
    `email` |  optional  | string 邮箱地址
    `cellphone` |  optional  | int 手机号
    `portrait` |  optional  | string 头像地址
    `password` |  optional  | string 密码

<!-- END_86324a172b7a75997b89ff6746121dd6 -->

<!-- START_3fa80f70d41f2833f64967d45bb8bd84 -->
## AdminDestroy
删除管理员

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/admin/destroy/1?id=dolor" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/admin/destroy/1"
);

let params = {
    "id": "dolor",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/admin/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 管理员ID

<!-- END_3fa80f70d41f2833f64967d45bb8bd84 -->

<!-- START_ae431a5bc1b7b79a3a6d4fee70175a84 -->
## Display a listing of the auth group.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/authGroup" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/authGroup"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/authGroup`


<!-- END_ae431a5bc1b7b79a3a6d4fee70175a84 -->

<!-- START_b3276e98927c4c2dd3e24c9754d2f2ba -->
## Display a listing of the Syslog.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/admin/log" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/admin/log"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/admin/log`


<!-- END_b3276e98927c4c2dd3e24c9754d2f2ba -->

#brand

品牌管理
Class BrandController
<!-- START_10a60d859370ad32df7647f78acad68a -->
## BrandList
品牌列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/brand?name=commodi&limit=est&sort=sit&page=et" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/brand"
);

let params = {
    "name": "commodi",
    "limit": "est",
    "sort": "sit",
    "page": "et",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/brand`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 品牌名称
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_10a60d859370ad32df7647f78acad68a -->

<!-- START_854299fdcabc489fbc3ef9f234a614d3 -->
## BrandCreate
创建品牌

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/brand?name=harum&sort=amet" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/brand"
);

let params = {
    "name": "harum",
    "sort": "amet",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/brand`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 品牌名称
    `sort` |  optional  | int 排序

<!-- END_854299fdcabc489fbc3ef9f234a614d3 -->

<!-- START_bad63e1158b9c9efb536b70548162811 -->
## BrandEdit
保存品牌

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/brand/1?id=eligendi&name=accusantium&sort=mollitia" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/brand/1"
);

let params = {
    "id": "eligendi",
    "name": "accusantium",
    "sort": "mollitia",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/brand/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 品牌ID
    `name` |  optional  | string 品牌名称
    `sort` |  optional  | int 排序

<!-- END_bad63e1158b9c9efb536b70548162811 -->

<!-- START_8ace57ff018a3cc50a7abe68f0c7b376 -->
## BrandDestroy
删除品牌

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/brand/destroy/1?id=in" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/brand/destroy/1"
);

let params = {
    "id": "in",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/brand/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 品牌ID

<!-- END_8ace57ff018a3cc50a7abe68f0c7b376 -->

#dhl

快递公司管理
Class DhlController
<!-- START_c88fd10be0b187d9aebc3ee4a2a134e9 -->
## DhlList
快递公司列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/dhl?title=voluptatum&limit=ullam&sort=et&page=quam" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/dhl"
);

let params = {
    "title": "voluptatum",
    "limit": "ullam",
    "sort": "et",
    "page": "quam",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/dhl`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 公司名称
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_c88fd10be0b187d9aebc3ee4a2a134e9 -->

<!-- START_fd84a39dba4a0fc7361e61ea42222563 -->
## DhlCreate
创建快递公司

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/dhl?name=vitae&abbreviation=est&state=nostrum&sort=quos" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/dhl"
);

let params = {
    "name": "vitae",
    "abbreviation": "est",
    "state": "nostrum",
    "sort": "quos",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/dhl`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 快递公司名称
    `abbreviation` |  optional  | string 快递公司英文缩写
    `state` |  optional  | string 状态
    `sort` |  optional  | string 排序

<!-- END_fd84a39dba4a0fc7361e61ea42222563 -->

<!-- START_b25589cad5241d71f92ea6a151c4912e -->
## DhlEdit
保存快递公司

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/dhl/1?name=rerum&abbreviation=reprehenderit&state=vero&sort=repellat" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/dhl/1"
);

let params = {
    "name": "rerum",
    "abbreviation": "reprehenderit",
    "state": "vero",
    "sort": "repellat",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/dhl/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 快递公司名称
    `abbreviation` |  optional  | string 快递公司英文缩写
    `state` |  optional  | string 状态
    `sort` |  optional  | string 排序

<!-- END_b25589cad5241d71f92ea6a151c4912e -->

<!-- START_4ab92749113bb353930366bef0fdc477 -->
## DhlDestroy
删除快递公司

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/dhl/destroy/1?id=sunt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/dhl/destroy/1"
);

let params = {
    "id": "sunt",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/dhl/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 快递公司ID

<!-- END_4ab92749113bb353930366bef0fdc477 -->

#general


<!-- START_e19414bb8ca64ad4ee4c4cc63da349c4 -->
## Authorize a client to access the user&#039;s account.

> Example request:

```bash
curl -X POST \
    "http://localhost/api/token" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/token"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/token`


<!-- END_e19414bb8ca64ad4ee4c4cc63da349c4 -->

<!-- START_e536d0d1d7574a9d90932cc5c16f577a -->
## Get all of the authorized tokens for the authenticated user.

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/tokens" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/tokens"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/tokens`


<!-- END_e536d0d1d7574a9d90932cc5c16f577a -->

<!-- START_bc0e97fb13ef4a0137eec58a6c9d16b3 -->
## Delete the given token.

> Example request:

```bash
curl -X DELETE \
    "http://localhost/api/tokens/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/tokens/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`DELETE api/tokens/{token_id}`


<!-- END_bc0e97fb13ef4a0137eec58a6c9d16b3 -->

<!-- START_356aa57a5886f377e4e6eea0dad27149 -->
## api/v1/admin/login
> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/login`


<!-- END_356aa57a5886f377e4e6eea0dad27149 -->

<!-- START_86c1c8ac7d7860dde610d68027c29993 -->
## token刷新

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/refreshToken" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/refreshToken"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/refreshToken`


<!-- END_86c1c8ac7d7860dde610d68027c29993 -->

<!-- START_c46af459729c4acfcafd0731c9253713 -->
## PlugInDownload
下载插件

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/plugin/download/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/plugin/download/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`GET api/v1/admin/plugin/download/{name}`


<!-- END_c46af459729c4acfcafd0731c9253713 -->

<!-- START_15d5cc951f7aa72831cfe309841317f5 -->
## api/v1/admin/uploadPictures
> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/uploadPictures" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/uploadPictures"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/uploadPictures`


<!-- END_15d5cc951f7aa72831cfe309841317f5 -->

<!-- START_04fa17ce63b6fa28038088773f2be56f -->
## api/v1/admin/userInfo
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/userInfo" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/userInfo"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/userInfo`


<!-- END_04fa17ce63b6fa28038088773f2be56f -->

<!-- START_9f2bb0a0fad1e6db4d7a1fb711370f0b -->
## api/v1/admin/index
> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/index" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/index"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/index`


<!-- END_9f2bb0a0fad1e6db4d7a1fb711370f0b -->

<!-- START_bc85dc4937ed5eefb08bd6fadc7afda2 -->
## CategoryList
分类列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/category?title=et&limit=dolor&sort=exercitationem&page=aut" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/category"
);

let params = {
    "title": "et",
    "limit": "dolor",
    "sort": "exercitationem",
    "page": "aut",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/category`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 品牌名称
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_bc85dc4937ed5eefb08bd6fadc7afda2 -->

<!-- START_1a9ede335190f119345c8c74ec82cb57 -->
## CategoryCreate
创建分类

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/category?name=dolorum&pid=sequi&sort=ipsa&is_recommend=tempora&state=sint&specification=molestias&brand=maiores" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/category"
);

let params = {
    "name": "dolorum",
    "pid": "sequi",
    "sort": "ipsa",
    "is_recommend": "tempora",
    "state": "sint",
    "specification": "molestias",
    "brand": "maiores",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/category`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 分类名称
    `pid` |  optional  | int 分类上级ID
    `sort` |  optional  | int 分类排序
    `is_recommend` |  optional  | int 是否推荐
    `state` |  optional  | int 是否显示
    `specification` |  optional  | array 规格列表
    `brand` |  optional  | array 品牌列表

<!-- END_1a9ede335190f119345c8c74ec82cb57 -->

<!-- START_e49e98a63ae5fce5fc468dd99ffc0f4d -->
## CategoryEdit
保存分类

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/category/1?id=omnis&name=dolor&pid=dolores&sort=accusamus&is_recommend=odio&state=sapiente&specification=et&brand=qui" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/category/1"
);

let params = {
    "id": "omnis",
    "name": "dolor",
    "pid": "dolores",
    "sort": "accusamus",
    "is_recommend": "odio",
    "state": "sapiente",
    "specification": "et",
    "brand": "qui",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/category/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 分类ID
    `name` |  optional  | string 分类名称
    `pid` |  optional  | int 分类上级ID
    `sort` |  optional  | int 分类排序
    `is_recommend` |  optional  | int 是否推荐
    `state` |  optional  | int 是否显示
    `specification` |  optional  | array 规格列表
    `brand` |  optional  | array 品牌列表

<!-- END_e49e98a63ae5fce5fc468dd99ffc0f4d -->

<!-- START_89f2e477f85e08a2890ef97e3a8502cc -->
## CategoryDestroy
删除分类

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/category/destroy/1?id=quisquam" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/category/destroy/1"
);

let params = {
    "id": "quisquam",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/category/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 分类ID

<!-- END_89f2e477f85e08a2890ef97e3a8502cc -->

<!-- START_15f5c00b4f078d2b6e7b5c3d83dd5f55 -->
## IndentList
订单列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/indent?title=laboriosam&limit=porro&sort=et&page=voluptas" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent"
);

let params = {
    "title": "laboriosam",
    "limit": "porro",
    "sort": "et",
    "page": "voluptas",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/indent`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 订单查询
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_15f5c00b4f078d2b6e7b5c3d83dd5f55 -->

<!-- START_896ad9fb1ae874aa5a8d1f96512e0494 -->
## IndentDetail
订单详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/indent/1?id=sed" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent/1"
);

let params = {
    "id": "sed",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/indent/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_896ad9fb1ae874aa5a8d1f96512e0494 -->

<!-- START_d63f61c78e0556082a275a8606298eab -->
## IndentShipment
发货

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/indent/shipment" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent/shipment"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/indent/shipment`


<!-- END_d63f61c78e0556082a275a8606298eab -->

<!-- START_202997b3150d4c4a2c18dab39ac55ba0 -->
## IndentDhl
保存配送信息

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/indent/dhl" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent/dhl"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/indent/dhl`


<!-- END_202997b3150d4c4a2c18dab39ac55ba0 -->

<!-- START_bedec22a681cba41eb3fb16a7f45b4d9 -->
## IndentRefund
退款

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/indent/refund/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent/refund/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/indent/refund/{id}`


<!-- END_bedec22a681cba41eb3fb16a7f45b4d9 -->

<!-- START_d49e28d8aea889b5cfffeb7531912c57 -->
## IndentQuery
查询订单状态

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/indent/query/1?id=quod" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent/query/1"
);

let params = {
    "id": "quod",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/indent/query/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_d49e28d8aea889b5cfffeb7531912c57 -->

<!-- START_9a19d92d8d914d1f1b3be8a87445cc46 -->
## IndentReceiving
延长收货时间

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/indent/receiving" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/indent/receiving"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/indent/receiving`


<!-- END_9a19d92d8d914d1f1b3be8a87445cc46 -->

<!-- START_70ad982961d1d8331e1295ed00248a70 -->
## ResourceList
资源列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/resource?name=impedit&limit=ipsam&sort=tenetur&page=placeat" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/resource"
);

let params = {
    "name": "impedit",
    "limit": "ipsam",
    "sort": "tenetur",
    "page": "placeat",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/resource`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 资源名称
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_70ad982961d1d8331e1295ed00248a70 -->

<!-- START_1bd3fe090880feda26608dae03ec04fe -->
## ResourceDestroy
删除资源

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/resource/destroy/1?id=sed" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/resource/destroy/1"
);

let params = {
    "id": "sed",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/resource/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 资源ID

<!-- END_1bd3fe090880feda26608dae03ec04fe -->

<!-- START_6923c646da7e84edaf565caf886d9c37 -->
## BannerList
轮播列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/banner?name=rerum&limit=aut&type=rerum&sort=assumenda&page=qui" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/banner"
);

let params = {
    "name": "rerum",
    "limit": "aut",
    "type": "rerum",
    "sort": "assumenda",
    "page": "qui",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/banner`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 轮播名称
    `limit` |  optional  | int 每页显示条数
    `type` |  optional  | int 轮播类型
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_6923c646da7e84edaf565caf886d9c37 -->

<!-- START_003f9ab2865533774093f2ac049500ea -->
## BannerCreate
创建轮播

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/banner?name=officia&type=fugit&url=blanditiis&sort=quia&state=rerum&img=doloribus" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/banner"
);

let params = {
    "name": "officia",
    "type": "fugit",
    "url": "blanditiis",
    "sort": "quia",
    "state": "rerum",
    "img": "doloribus",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/banner`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 轮播名称
    `type` |  optional  | int 轮播类型
    `url` |  optional  | string 轮播跳转地址
    `sort` |  optional  | int 轮播排序
    `state` |  optional  | int 轮播状态
    `img` |  optional  | string 轮播图片

<!-- END_003f9ab2865533774093f2ac049500ea -->

<!-- START_8615672be3c6ad7a19483259bbee81d3 -->
## BannerEdit
保存轮播

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/banner/1?id=aut&name=sit&type=dolores&url=omnis&sort=nam&state=illum&img=recusandae" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/banner/1"
);

let params = {
    "id": "aut",
    "name": "sit",
    "type": "dolores",
    "url": "omnis",
    "sort": "nam",
    "state": "illum",
    "img": "recusandae",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/banner/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 轮播ID
    `name` |  optional  | string 轮播名称
    `type` |  optional  | int 轮播类型
    `url` |  optional  | string 轮播跳转地址
    `sort` |  optional  | int 轮播排序
    `state` |  optional  | int 轮播状态
    `img` |  optional  | string 轮播图片

<!-- END_8615672be3c6ad7a19483259bbee81d3 -->

<!-- START_2f5252ccf0e21d2913037a87d1d17773 -->
## BannerDestroy
删除轮播

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/banner/destroy/1?id=ea" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/banner/destroy/1"
);

let params = {
    "id": "ea",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/banner/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 轮播ID

<!-- END_2f5252ccf0e21d2913037a87d1d17773 -->

<!-- START_8026a32211837ce5f5b6f282153230dc -->
## serve
处理应用的请求消息

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/serve" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/serve"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "code": 50003,
    "message": "非法操作",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/serve`

`POST api/v1/app/serve`

`PUT api/v1/app/serve`

`PATCH api/v1/app/serve`

`DELETE api/v1/app/serve`

`OPTIONS api/v1/app/serve`


<!-- END_8026a32211837ce5f5b6f282153230dc -->

<!-- START_4b2c17eb05b1c4c913cb7c51e9abf0fb -->
## PaymentNotify
支付回调

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/paymentNotify" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/paymentNotify"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 400,
    "message": "Invalid request XML.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/paymentNotify`

`POST api/v1/app/paymentNotify`

`PUT api/v1/app/paymentNotify`

`PATCH api/v1/app/paymentNotify`

`DELETE api/v1/app/paymentNotify`

`OPTIONS api/v1/app/paymentNotify`


<!-- END_4b2c17eb05b1c4c913cb7c51e9abf0fb -->

<!-- START_0171edd33e449de5a27472d53fc2be4e -->
## RefundNotify
退款回调

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/refundNotify" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/refundNotify"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 400,
    "message": "Invalid request XML.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/refundNotify`

`POST api/v1/app/refundNotify`

`PUT api/v1/app/refundNotify`

`PATCH api/v1/app/refundNotify`

`DELETE api/v1/app/refundNotify`

`OPTIONS api/v1/app/refundNotify`


<!-- END_0171edd33e449de5a27472d53fc2be4e -->

<!-- START_3f68318780e37174669eb4dcb051dddc -->
## token刷新

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/refreshToken" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/refreshToken"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/refreshToken`


<!-- END_3f68318780e37174669eb4dcb051dddc -->

<!-- START_1a5fc2e9288d7af961452076cf19c04e -->
## api/v1/app/uploadPictures
> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/uploadPictures" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/uploadPictures"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/uploadPictures`


<!-- END_1a5fc2e9288d7af961452076cf19c04e -->

<!-- START_9c824a277220411217af26064734b5cb -->
## CellphoneCode
手机验证码

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/cellphoneCode?cellphone=quod&state=est" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/cellphoneCode"
);

let params = {
    "cellphone": "quod",
    "state": "est",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/cellphoneCode`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `cellphone` |  optional  | int 手机号
    `state` |  optional  | int 验证码类型 1找回密码 2更换手机

<!-- END_9c824a277220411217af26064734b5cb -->

<!-- START_2f15cf05e35e7a5d88168171de5b2e7b -->
## EmailCode
邮箱验证码

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/emailCode?email=qui&oldEmail=exercitationem" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/emailCode"
);

let params = {
    "email": "qui",
    "oldEmail": "exercitationem",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/emailCode`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `email` |  optional  | string 邮箱
    `oldEmail` |  optional  | string 旧的邮箱

<!-- END_2f15cf05e35e7a5d88168171de5b2e7b -->

<!-- START_3232248591099d41f27495d317e9806a -->
## Login
登录

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/login?cellphone=consequuntur&password=necessitatibus" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/login"
);

let params = {
    "cellphone": "consequuntur",
    "password": "necessitatibus",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/login`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `cellphone` |  optional  | int 手机号
    `password` |  optional  | string 密码

<!-- END_3232248591099d41f27495d317e9806a -->

<!-- START_4e3c9fdc1f9739a1b79c9e9f24d4b137 -->
## Register
注册

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/register?cellphone=ut&password=deserunt&rPassword=quasi&code=eos" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/register"
);

let params = {
    "cellphone": "ut",
    "password": "deserunt",
    "rPassword": "quasi",
    "code": "eos",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/register`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `cellphone` |  optional  | int 手机号
    `password` |  optional  | string 密码
    `rPassword` |  optional  | string 重复密码
    `code` |  optional  | int 验证码

<!-- END_4e3c9fdc1f9739a1b79c9e9f24d4b137 -->

<!-- START_8bcc1874136798a2018f4b5651d8d47c -->
## FindPassword
找回密码

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/findPassword?cellphone=et&password=quisquam&rPassword=ut&code=iusto" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/findPassword"
);

let params = {
    "cellphone": "et",
    "password": "quisquam",
    "rPassword": "ut",
    "code": "iusto",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/findPassword`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `cellphone` |  optional  | int 手机号
    `password` |  optional  | string 密码
    `rPassword` |  optional  | string 重复密码
    `code` |  optional  | int 验证码

<!-- END_8bcc1874136798a2018f4b5651d8d47c -->

<!-- START_2ce76f467b703dd97a767228c327755e -->
## 小程序换取openid

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/miniLogin?platform=est&code=rerum" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/miniLogin"
);

let params = {
    "platform": "est",
    "code": "rerum",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/miniLogin`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `platform` |  optional  | string 平台标识
    `code` |  optional  | string 平台标识

<!-- END_2ce76f467b703dd97a767228c327755e -->

<!-- START_442b76d061067ad7287b21d8b840216d -->
## 授权登录

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/authorization?iv=blanditiis" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/authorization"
);

let params = {
    "iv": "blanditiis",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/authorization`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `iv` |  optional  | array iv

<!-- END_442b76d061067ad7287b21d8b840216d -->

<!-- START_455a4c0133cdb45a9bf6841a5e542288 -->
## BindEmailAddress
绑定邮箱

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/verifyEmail?email=qui&oldEmail=sed&code=atque" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/verifyEmail"
);

let params = {
    "email": "qui",
    "oldEmail": "sed",
    "code": "atque",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/verifyEmail`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `email` |  optional  | string 邮箱
    `oldEmail` |  optional  | string 旧邮箱
    `code` |  optional  | int 验证码

<!-- END_455a4c0133cdb45a9bf6841a5e542288 -->

<!-- START_258c542219055a7f7696729bea8aadc8 -->
## 更新接收通知状态

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/user/notification" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/user/notification"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/user/notification`


<!-- END_258c542219055a7f7696729bea8aadc8 -->

<!-- START_fd83c2ddeddb904645ed9a4edbb64003 -->
## GoodList
商品列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/good?limit=qui&sort=animi&page=corporis&pid=magni" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/good"
);

let params = {
    "limit": "qui",
    "sort": "animi",
    "page": "corporis",
    "pid": "magni",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "code": 50000,
    "message": "非法apply-secret",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/good`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码
    `pid` |  optional  | int 类目ID

<!-- END_fd83c2ddeddb904645ed9a4edbb64003 -->

<!-- START_f0720d6c4f449e64a646e025f3ea0b64 -->
## GoodDetail
商品详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/good/1?id=quos" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/good/1"
);

let params = {
    "id": "quos",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "code": 50000,
    "message": "非法apply-secret",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/good/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_f0720d6c4f449e64a646e025f3ea0b64 -->

<!-- START_97e16b2cc2eef403decdd39abb263d7d -->
## GoodCategory
商品分类

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/goodCategory?tree=repudiandae&is_recommend=amet&limit=impedit&sort=velit&page=facilis" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodCategory"
);

let params = {
    "tree": "repudiandae",
    "is_recommend": "amet",
    "limit": "impedit",
    "sort": "velit",
    "page": "facilis",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "code": 50000,
    "message": "非法apply-secret",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/goodCategory`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `tree` |  optional  | boolean 返回格式是否为树状结构
    `is_recommend` |  optional  | int 是否首页展示
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_97e16b2cc2eef403decdd39abb263d7d -->

<!-- START_82e7ef3c6c2bc023329bede418155465 -->
## BannerList
轮播列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/banner?type=quam&limit=eum&sort=saepe&page=eos" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/banner"
);

let params = {
    "type": "quam",
    "limit": "eum",
    "sort": "saepe",
    "page": "eos",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (401):

```json
{
    "code": 50000,
    "message": "非法apply-secret",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/banner`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `type` |  optional  | int 轮播类型
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_82e7ef3c6c2bc023329bede418155465 -->

<!-- START_e0ad0f320321d508aa88d7338954db15 -->
## Logout
登出

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/logout" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/logout"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/logout`


<!-- END_e0ad0f320321d508aa88d7338954db15 -->

<!-- START_f5b4963eaa8a9406e374aea4fe1975dd -->
## UserDetail
用户信息

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/user" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/user"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/user`


<!-- END_f5b4963eaa8a9406e374aea4fe1975dd -->

<!-- START_83f2c95b057efdc2575c33574f452869 -->
## UserEdit
保存用户信息

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/user?portrait=numquam&nickname=est" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/user"
);

let params = {
    "portrait": "numquam",
    "nickname": "est",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/user`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `portrait` |  optional  | string 头像
    `nickname` |  optional  | string 昵称

<!-- END_83f2c95b057efdc2575c33574f452869 -->

<!-- START_ecba7b17a66f6292b1941a189a803c13 -->
## UserCancel
注销账号

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/cancel" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/cancel"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/cancel`


<!-- END_ecba7b17a66f6292b1941a189a803c13 -->

<!-- START_60e73a0a57af2a6e5a03291f8ca04256 -->
## MoneyLogList
收支列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/moneyLog?month=quae&limit=eaque&sort=tempore&page=dolorum" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/moneyLog"
);

let params = {
    "month": "quae",
    "limit": "eaque",
    "sort": "tempore",
    "page": "dolorum",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/moneyLog`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `month` |  optional  | string 日期筛选
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_60e73a0a57af2a6e5a03291f8ca04256 -->

<!-- START_8bef58a94086563c278ab19130d2c44e -->
## MoneyLogDetail
收支明细

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/moneyLog/1?id=dolor" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/moneyLog/1"
);

let params = {
    "id": "dolor",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/moneyLog/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 记录ID

<!-- END_8bef58a94086563c278ab19130d2c44e -->

<!-- START_055ed02aa734a4c5c1686ebaca47dca9 -->
## UnifiedPayment
统一在线支付

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/unifiedPayment?type=sequi" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/unifiedPayment"
);

let params = {
    "type": "sequi",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/unifiedPayment`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `type` |  optional  | int 支付类型

<!-- END_055ed02aa734a4c5c1686ebaca47dca9 -->

<!-- START_fffae8c4cef20d34b68d5acef1d13654 -->
## BalancePay
余额支付

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/balancePay?id=illum" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/balancePay"
);

let params = {
    "id": "illum",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/balancePay`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_fffae8c4cef20d34b68d5acef1d13654 -->

<!-- START_2bf64c6bafb0030b2cdd1c633db20f92 -->
## GoodIndentList
商品订单列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/goodIndent?limit=dignissimos&sort=quia&page=quibusdam" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent"
);

let params = {
    "limit": "dignissimos",
    "sort": "quia",
    "page": "quibusdam",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/goodIndent`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_2bf64c6bafb0030b2cdd1c633db20f92 -->

<!-- START_eea7b501fa56b7ca37107c195ed0078b -->
## GoodIndentList
创建商品订单

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent?carriage=est&indentCommodity=est&remark=quaerat&address=aut" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent"
);

let params = {
    "carriage": "est",
    "indentCommodity": "est",
    "remark": "quaerat",
    "address": "aut",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `carriage` |  optional  | int 运费
    `indentCommodity` |  optional  | array 订单商品
    `remark` |  optional  | string 备注
    `address` |  optional  | array 收货地址

<!-- END_eea7b501fa56b7ca37107c195ed0078b -->

<!-- START_d36daeb16b355a6e084ffcee11a90fcf -->
## 添加商品到购物车

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent/addShoppingCart" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/addShoppingCart"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent/addShoppingCart`


<!-- END_d36daeb16b355a6e084ffcee11a90fcf -->

<!-- START_e1f5a26390af9a019c0c1fee1d1fcf69 -->
## 清空购物车

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent/clearShoppingCart" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/clearShoppingCart"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent/clearShoppingCart`


<!-- END_e1f5a26390af9a019c0c1fee1d1fcf69 -->

<!-- START_71c970b89cbe087c66cfb12f804a5e14 -->
## GoodIndentDetail
商品订单详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/goodIndent/detail/1?id=earum" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/detail/1"
);

let params = {
    "id": "earum",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/goodIndent/detail/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_71c970b89cbe087c66cfb12f804a5e14 -->

<!-- START_8fbadc360f47fd3384373630e2475e45 -->
## SynchronizationInventory
同步线上商品库存

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent/synchronizationInventory" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/synchronizationInventory"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent/synchronizationInventory`


<!-- END_8fbadc360f47fd3384373630e2475e45 -->

<!-- START_577ca43196337bf9cd136250f8a05abb -->
## GoodIndentPay
订单支付详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/goodIndent/pay/1?id=at" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/pay/1"
);

let params = {
    "id": "at",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/goodIndent/pay/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_577ca43196337bf9cd136250f8a05abb -->

<!-- START_bb06aa27171182f7748cdfff318647d8 -->
## GoodIndentReceipt
确认收货

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent/receipt/1?id=sint" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/receipt/1"
);

let params = {
    "id": "sint",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent/receipt/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_bb06aa27171182f7748cdfff318647d8 -->

<!-- START_a4a61de81eb0ebba9640cdf0a641ac8a -->
## GoodIndentCancel
取消订单

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent/cancel/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/cancel/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent/cancel/{id}`


<!-- END_a4a61de81eb0ebba9640cdf0a641ac8a -->

<!-- START_7adfed2cb95891b577ceacb08c19e3b0 -->
## GoodIndentDestroy
删除订单

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/goodIndent/destroy/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/destroy/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/goodIndent/destroy/{id}`


<!-- END_7adfed2cb95891b577ceacb08c19e3b0 -->

<!-- START_460d71a590628eb4ca73609c44ee32dd -->
## GoodIndentQuantity
订单数量统计

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/goodIndent/quantity" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/goodIndent/quantity"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/goodIndent/quantity`


<!-- END_460d71a590628eb4ca73609c44ee32dd -->

<!-- START_1d9f927ba58e497304b55c12b3bd358b -->
## ShippingList
收货地址列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/shipping?limit=aut&sort=aut&page=consequatur" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/shipping"
);

let params = {
    "limit": "aut",
    "sort": "aut",
    "page": "consequatur",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/shipping`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_1d9f927ba58e497304b55c12b3bd358b -->

<!-- START_1bb88e4670a65563ee88a3edfaa31486 -->
## ShippingCreate
创建收货地址

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/shipping?cellphone=culpa&defaults=nostrum&name=dicta&location=provident&address=quisquam&latitude=aliquam&longitude=assumenda&house=sapiente" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/shipping"
);

let params = {
    "cellphone": "culpa",
    "defaults": "nostrum",
    "name": "dicta",
    "location": "provident",
    "address": "quisquam",
    "latitude": "aliquam",
    "longitude": "assumenda",
    "house": "sapiente",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/shipping`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `cellphone` |  optional  | int 手机号
    `defaults` |  optional  | int 是否默认
    `name` |  optional  | string 姓名
    `location` |  optional  | string 地址
    `address` |  optional  | string 详情地址
    `latitude` |  optional  | string 纬度
    `longitude` |  optional  | string 经度
    `house` |  optional  | string 门牌号

<!-- END_1bb88e4670a65563ee88a3edfaa31486 -->

<!-- START_c57ab154449aac8195a5181235e6c15a -->
## ShippingEdit
保存收货地址

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/shipping/1?id=nesciunt&cellphone=facilis&defaults=libero&name=consequuntur&location=facilis&address=aut&latitude=autem&longitude=maxime&house=distinctio" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/shipping/1"
);

let params = {
    "id": "nesciunt",
    "cellphone": "facilis",
    "defaults": "libero",
    "name": "consequuntur",
    "location": "facilis",
    "address": "aut",
    "latitude": "autem",
    "longitude": "maxime",
    "house": "distinctio",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/shipping/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 收货地址ID
    `cellphone` |  optional  | int 手机号
    `defaults` |  optional  | int 是否默认
    `name` |  optional  | string 姓名
    `location` |  optional  | string 地址
    `address` |  optional  | string 详情地址
    `latitude` |  optional  | string 纬度
    `longitude` |  optional  | string 经度
    `house` |  optional  | string 门牌号

<!-- END_c57ab154449aac8195a5181235e6c15a -->

<!-- START_411197dd62a790dad41f4df0a3fa57a8 -->
## ShippingFreight
获取运费

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/shipping/freight/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/shipping/freight/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/shipping/freight/{id}`


<!-- END_411197dd62a790dad41f4df0a3fa57a8 -->

<!-- START_b6034096b7d9f25e4cbbd9cb46a5f4ab -->
## ShippingDestroy
删除收货地址

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/shipping/destroy/1?id=fugit" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/shipping/destroy/1"
);

let params = {
    "id": "fugit",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/shipping/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 收货地址ID

<!-- END_b6034096b7d9f25e4cbbd9cb46a5f4ab -->

<!-- START_c307eb5ae39a7c886a20b82b736b1ce4 -->
## ShippingDefaultSet
设为默认

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/shipping/default/set" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/shipping/default/set"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/shipping/default/set`


<!-- END_c307eb5ae39a7c886a20b82b736b1ce4 -->

<!-- START_f663143f5f7c8d22e4f0e095cc1c3b75 -->
## BrowseList
浏览记录列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/browse?limit=aut&sort=qui&page=qui" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/browse"
);

let params = {
    "limit": "aut",
    "sort": "qui",
    "page": "qui",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/browse`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_f663143f5f7c8d22e4f0e095cc1c3b75 -->

<!-- START_caf7c371897c0f62284c3a94805bdb75 -->
## BrowseCreate
创建浏览记录

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/browse?id=perspiciatis" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/browse"
);

let params = {
    "id": "perspiciatis",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/browse`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_caf7c371897c0f62284c3a94805bdb75 -->

<!-- START_6530e2e756505bd1b6afb5faf580e93d -->
## CollectList
收藏列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/collect?limit=quam&sort=omnis&page=suscipit" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/collect"
);

let params = {
    "limit": "quam",
    "sort": "omnis",
    "page": "suscipit",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/collect`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_6530e2e756505bd1b6afb5faf580e93d -->

<!-- START_370ecd4888fb34e32862f4a561e74b82 -->
## CollectDetail
收藏详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/collect/1?id=voluptatem" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/collect/1"
);

let params = {
    "id": "voluptatem",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/collect/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_370ecd4888fb34e32862f4a561e74b82 -->

<!-- START_6e3bce33f2e12b596f70660c2d28ab6c -->
## CollectCreate
创建收藏

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/collect?good_id=et" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/collect"
);

let params = {
    "good_id": "et",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/collect`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `good_id` |  optional  | int 商品ID

<!-- END_6e3bce33f2e12b596f70660c2d28ab6c -->

<!-- START_a4dc624d6d59dcb442a6e704e8d85b3d -->
## CollectDestroy
删除收藏

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/collect/destroy/1?id=autem" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/collect/destroy/1"
);

let params = {
    "id": "autem",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/collect/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_a4dc624d6d59dcb442a6e704e8d85b3d -->

<!-- START_a79f0bc88e9b99043487610ab4f851ca -->
## NotificationList
通知列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/notification?limit=eius&sort=quisquam&page=sunt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/notification"
);

let params = {
    "limit": "eius",
    "sort": "quisquam",
    "page": "sunt",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/notification`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_a79f0bc88e9b99043487610ab4f851ca -->

<!-- START_89b8d6913de6cfc7e88c61d6b4529a87 -->
## NotificationUnread
获取未读通知

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/notification/unread" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/notification/unread"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/notification/unread`


<!-- END_89b8d6913de6cfc7e88c61d6b4529a87 -->

<!-- START_cfee7e1a3d34ad1d65b028ff2a2eb2b7 -->
## NotificationDestroy
删除通知

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/notification/destroy/1?id=voluptas" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/notification/destroy/1"
);

let params = {
    "id": "voluptas",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/notification/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 通知ID

<!-- END_cfee7e1a3d34ad1d65b028ff2a2eb2b7 -->

<!-- START_75209e547772ed45b18ab88813329a1a -->
## NotificationRead
标记为已读

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/notification/read/1?id=blanditiis" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/notification/read/1"
);

let params = {
    "id": "blanditiis",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/notification/read/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 通知ID

<!-- END_75209e547772ed45b18ab88813329a1a -->

<!-- START_67b8dc4c368d1327f50f4745adf50041 -->
## GoodIndentDetail
通知详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/app/notification/detail/1?id=enim" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/notification/detail/1"
);

let params = {
    "id": "enim",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/app/notification/detail/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 订单ID

<!-- END_67b8dc4c368d1327f50f4745adf50041 -->

<!-- START_25d23906c906b4373597ae8258979713 -->
## ChangeCellphone
更换手机

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/changeCellphone?cellphone=eius&oldCellphone=suscipit&code=ipsam" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/changeCellphone"
);

let params = {
    "cellphone": "eius",
    "oldCellphone": "suscipit",
    "code": "ipsam",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/changeCellphone`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `cellphone` |  optional  | string 手机
    `oldCellphone` |  optional  | string 旧手机
    `code` |  optional  | int 验证码

<!-- END_25d23906c906b4373597ae8258979713 -->

<!-- START_2d96d12bf3b3ac0540be9b48443a1533 -->
## AmendPassword
修改密码

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app/amendPassword?nowPassword=dolorem&password=quia&rPassword=repellendus&code=est" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/app/amendPassword"
);

let params = {
    "nowPassword": "dolorem",
    "password": "quia",
    "rPassword": "repellendus",
    "code": "est",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/app/amendPassword`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `nowPassword` |  optional  | string 当前密码
    `password` |  optional  | string 新密码
    `rPassword` |  optional  | string 重复密码
    `code` |  optional  | int 验证码

<!-- END_2d96d12bf3b3ac0540be9b48443a1533 -->

#good

商品管理
Class GoodController
<!-- START_17761ba72fd436382619c21951b207e8 -->
## GoodList
商品列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/good?title=architecto&limit=perspiciatis&sort=excepturi&page=ut" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good"
);

let params = {
    "title": "architecto",
    "limit": "perspiciatis",
    "sort": "excepturi",
    "page": "ut",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/good`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 关键字
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_17761ba72fd436382619c21951b207e8 -->

<!-- START_ef35fb55829326aca574cda9fd98c46d -->
## GoodCreate
创建商品

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/good?name=ab&number=repudiandae&freight_id=vel&category_id=neque&brand_id=consequatur&is_inventory=aut&keywords=est&short_description=exercitationem&details=deleniti&is_show=voluptatum&is_recommend=velit&is_new=maxime&is_hot=officia&sort=distinctio&time=debitis&timing=quae&good_specification=enim&good_sku=et" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good"
);

let params = {
    "name": "ab",
    "number": "repudiandae",
    "freight_id": "vel",
    "category_id": "neque",
    "brand_id": "consequatur",
    "is_inventory": "aut",
    "keywords": "est",
    "short_description": "exercitationem",
    "details": "deleniti",
    "is_show": "voluptatum",
    "is_recommend": "velit",
    "is_new": "maxime",
    "is_hot": "officia",
    "sort": "distinctio",
    "time": "debitis",
    "timing": "quae",
    "good_specification": "enim",
    "good_sku": "et",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/good`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 商品名称
    `number` |  optional  | string 货号
    `freight_id` |  optional  | int    运费模板ID
    `category_id` |  optional  | int 分类ID
    `brand_id` |  optional  | int 品牌ID
    `is_inventory` |  optional  | int 减库存方式
    `keywords` |  optional  | string 关键字
    `short_description` |  optional  | string 短描述
    `details` |  optional  | string 详情
    `is_show` |  optional  | int 是否上架
    `is_recommend` |  optional  | int 是否推荐
    `is_new` |  optional  | int 是否新品
    `is_hot` |  optional  | int 是否热销
    `sort` |  optional  | int 排序
    `time` |  optional  | string 上架时间
    `timing` |  optional  | string 定时上架时间
    `good_specification` |  optional  | array 商品规格
    `good_sku` |  optional  | array 商品SKU

<!-- END_ef35fb55829326aca574cda9fd98c46d -->

<!-- START_9d46f78e29b16116bcff5f671e484392 -->
## GoodEdit
保存商品

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/good/1?id=laboriosam&name=natus&number=repellendus&freight_id=temporibus&category_id=culpa&brand_id=at&is_inventory=et&keywords=ut&short_description=non&details=temporibus&is_show=aut&is_recommend=temporibus&is_new=quo&is_hot=animi&sort=labore&time=voluptas&timing=incidunt&good_specification=quia&good_sku=at" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good/1"
);

let params = {
    "id": "laboriosam",
    "name": "natus",
    "number": "repellendus",
    "freight_id": "temporibus",
    "category_id": "culpa",
    "brand_id": "at",
    "is_inventory": "et",
    "keywords": "ut",
    "short_description": "non",
    "details": "temporibus",
    "is_show": "aut",
    "is_recommend": "temporibus",
    "is_new": "quo",
    "is_hot": "animi",
    "sort": "labore",
    "time": "voluptas",
    "timing": "incidunt",
    "good_specification": "quia",
    "good_sku": "at",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/good/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID
    `name` |  optional  | string 商品名称
    `number` |  optional  | string 货号
    `freight_id` |  optional  | int    运费模板ID
    `category_id` |  optional  | int 分类ID
    `brand_id` |  optional  | int 品牌ID
    `is_inventory` |  optional  | int 减库存方式
    `keywords` |  optional  | string 关键字
    `short_description` |  optional  | string 短描述
    `details` |  optional  | string 详情
    `is_show` |  optional  | int 是否上架
    `is_recommend` |  optional  | int 是否推荐
    `is_new` |  optional  | int 是否新品
    `is_hot` |  optional  | int 是否热销
    `sort` |  optional  | int 排序
    `time` |  optional  | string 上架时间
    `timing` |  optional  | string 定时上架时间
    `good_specification` |  optional  | array 商品规格
    `good_sku` |  optional  | array 商品SKU

<!-- END_9d46f78e29b16116bcff5f671e484392 -->

<!-- START_005e9289263762c8db42bd0ce68c80dc -->
## GoodDestroy
删除商品

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/good/destroy/1?id=ullam" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good/destroy/1"
);

let params = {
    "id": "ullam",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/good/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_005e9289263762c8db42bd0ce68c80dc -->

<!-- START_5093d932ea5f99d9c8065d874fda71da -->
## GoodDetail
商品详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/good/1?id=iste" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good/1"
);

let params = {
    "id": "iste",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/good/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_5093d932ea5f99d9c8065d874fda71da -->

<!-- START_ab6e0b46db052bcfc161854b5bbcbd44 -->
## GoodSpecification
商品规格

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/good/specification/1?id=molestias" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good/specification/1"
);

let params = {
    "id": "molestias",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/good/specification/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_ab6e0b46db052bcfc161854b5bbcbd44 -->

<!-- START_fc898bfab945cc22324cbf3077f3dc3e -->
## GoodState
变更商品状态

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/good/state/1?id=nemo" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/good/state/1"
);

let params = {
    "id": "nemo",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/good/state/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 商品ID

<!-- END_fc898bfab945cc22324cbf3077f3dc3e -->

#manage

管理组管理
Class ManageController
<!-- START_2f90ea0c8532e0547d38762db3fff361 -->
## ManageList
管理组列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/manage" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/manage"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/manage`


<!-- END_2f90ea0c8532e0547d38762db3fff361 -->

<!-- START_8e17c1dceafebf5c9668447e9ceaaaec -->
## ManageCreate
创建管理组

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/manage?roles=eum&introduction=velit&group=sunt" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/manage"
);

let params = {
    "roles": "eum",
    "introduction": "velit",
    "group": "sunt",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/manage`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `roles` |  optional  | array 权限
    `introduction` |  optional  | string 角色名称
    `group` |  optional  | array 管理员

<!-- END_8e17c1dceafebf5c9668447e9ceaaaec -->

<!-- START_c7cf9df74e69b08cd107cc03982f6e28 -->
## ManageEdit
保存管理组

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/manage/1?id=nam&roles=esse&introduction=architecto&group=necessitatibus" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/manage/1"
);

let params = {
    "id": "nam",
    "roles": "esse",
    "introduction": "architecto",
    "group": "necessitatibus",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/manage/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 管理组ID
    `roles` |  optional  | array 权限
    `introduction` |  optional  | string 角色名称
    `group` |  optional  | array 管理员

<!-- END_c7cf9df74e69b08cd107cc03982f6e28 -->

<!-- START_9bb64c776dd652a7ffbff79e674e4225 -->
## ManageDestroy
删除管理组

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/manage/destroy/1?id=vero" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/manage/destroy/1"
);

let params = {
    "id": "vero",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/manage/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 管理组ID

<!-- END_9bb64c776dd652a7ffbff79e674e4225 -->

#member

会员管理
Class MemberController
<!-- START_9e2d21d8e9800032e4202e1812187999 -->
## MemberList
会员列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/member?title=provident&limit=debitis&sort=id&page=ut&timeInterval=et" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/member"
);

let params = {
    "title": "provident",
    "limit": "debitis",
    "sort": "id",
    "page": "ut",
    "timeInterval": "et",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/member`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 用户ID、用户名、手机号
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码
    `timeInterval` |  optional  | string 注册时间区间

<!-- END_9e2d21d8e9800032e4202e1812187999 -->

<!-- START_79887c181a6a84681a631cb57e1af818 -->
## MemberCreate
创建会员

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/member?name=dicta&cellphone=quasi&nickname=et&state=tempora&gender=eos&password=unde" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/member"
);

let params = {
    "name": "dicta",
    "cellphone": "quasi",
    "nickname": "et",
    "state": "tempora",
    "gender": "eos",
    "password": "unde",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/member`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 用户名
    `cellphone` |  optional  | string 手机号
    `nickname` |  optional  | string 昵称
    `state` |  optional  | string 状态
    `gender` |  optional  | string 性别
    `password` |  optional  | string 密码

<!-- END_79887c181a6a84681a631cb57e1af818 -->

<!-- START_8de32b509b38de15d2cdd80670ea9b7d -->
## MemberEdit
保存会员

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/member/1?name=sunt&cellphone=quia&nickname=harum&state=et&gender=incidunt&password=deleniti" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/member/1"
);

let params = {
    "name": "sunt",
    "cellphone": "quia",
    "nickname": "harum",
    "state": "et",
    "gender": "incidunt",
    "password": "deleniti",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/member/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 用户名
    `cellphone` |  optional  | string 手机号
    `nickname` |  optional  | string 昵称
    `state` |  optional  | string 状态
    `gender` |  optional  | string 性别
    `password` |  optional  | string 密码

<!-- END_8de32b509b38de15d2cdd80670ea9b7d -->

#power

权限管理
Class PowerController
<!-- START_ee64d25d504f159b1ee5ed434d1fc299 -->
## PowerList
权限管理

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/power?limit=dolorem&page=tempore&pid=nam&title=animi" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/power"
);

let params = {
    "limit": "dolorem",
    "page": "tempore",
    "pid": "nam",
    "title": "animi",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/power`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `limit` |  optional  | int 每页显示条数
    `page` |  optional  | string 页码
    `pid` |  optional  | int 分组ID
    `title` |  optional  | string ID、权限名称、API名称

<!-- END_ee64d25d504f159b1ee5ed434d1fc299 -->

<!-- START_c6745b8d798b95ad7bd781795f5ed526 -->
## PowerCreate
创建权限

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/power?title=autem&url=velit&icon=nihil&sort=quo&api=ut&pid=harum&state=harum" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/power"
);

let params = {
    "title": "autem",
    "url": "velit",
    "icon": "nihil",
    "sort": "quo",
    "api": "ut",
    "pid": "harum",
    "state": "harum",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/power`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 权限名称
    `url` |  optional  | string 外链
    `icon` |  optional  | string 图标
    `sort` |  optional  | string 排序
    `api` |  optional  | string API
    `pid` |  optional  | int 权限组ID
    `state` |  optional  | int 显示在菜单栏：1是0否

<!-- END_c6745b8d798b95ad7bd781795f5ed526 -->

<!-- START_d43db500be5b63215f5c9e96da980d68 -->
## PowerEdit
保存权限

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/power/1?id=velit&title=ut&url=sequi&icon=deleniti&sort=sint&api=dignissimos&pid=nam&state=atque" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/power/1"
);

let params = {
    "id": "velit",
    "title": "ut",
    "url": "sequi",
    "icon": "deleniti",
    "sort": "sint",
    "api": "dignissimos",
    "pid": "nam",
    "state": "atque",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/power/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 权限ID
    `title` |  optional  | string 权限名称
    `url` |  optional  | string 外链
    `icon` |  optional  | string 图标
    `sort` |  optional  | string 排序
    `api` |  optional  | string API
    `pid` |  optional  | int 权限组ID
    `state` |  optional  | int 显示在菜单栏：1是0否

<!-- END_d43db500be5b63215f5c9e96da980d68 -->

<!-- START_fd4cb0085a5cbf1eaf3c8aedddb0a6df -->
## PowerDestroy
删除权限

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/power/destroy/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/power/destroy/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/power/destroy/{id}`


<!-- END_fd4cb0085a5cbf1eaf3c8aedddb0a6df -->

#redis

Redis管理
Class RedisServiceController
<!-- START_c239b4f1733feb2a23bc1187294642cf -->
## RedisServiceList
Redis列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/redis" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/redis"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/redis`


<!-- END_c239b4f1733feb2a23bc1187294642cf -->

<!-- START_6f1b4cf759118a686f70365e04c8d714 -->
## RedisServiceDetail
获取Redis详情

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/redis/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/redis/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/redis/{name}`


<!-- END_6f1b4cf759118a686f70365e04c8d714 -->

<!-- START_9c6c39e53ac4b80fb700f49be95f87b4 -->
## RedisServiceDestroy
删除Redis

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/redis/destroy/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/redis/destroy/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/redis/destroy/{id}`


<!-- END_9c6c39e53ac4b80fb700f49be95f87b4 -->

<!-- START_c95391e6cfbf539b381549628540b1b0 -->
## RedisPanel
redis面板

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/redisPanel" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/redisPanel"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/redisPanel`


<!-- END_c95391e6cfbf539b381549628540b1b0 -->

#specification

规格管理
Class SpecificationController
<!-- START_fd6c7cd10899abc39d850a10384c8aed -->
## SpecificationList
规格列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/specification?title=placeat&limit=velit&sort=dolores&page=et" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specification"
);

let params = {
    "title": "placeat",
    "limit": "velit",
    "sort": "dolores",
    "page": "et",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/specification`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `title` |  optional  | string 规格名称
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_fd6c7cd10899abc39d850a10384c8aed -->

<!-- START_d9565a0de68678e309e99c2e8fd69539 -->
## SpecificationCreate
创建规格

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/specification?name=id&label=est&type=neque&is_search=quisquam&location=ea&specification_group_id=non&value=doloribus&sort=quos" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specification"
);

let params = {
    "name": "id",
    "label": "est",
    "type": "neque",
    "is_search": "quisquam",
    "location": "ea",
    "specification_group_id": "non",
    "value": "doloribus",
    "sort": "quos",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/specification`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 规格名称
    `label` |  optional  | string 规格标注名称
    `type` |  optional  | int 规格类型
    `is_search` |  optional  | string 是否可搜索
    `location` |  optional  | string 显示位置
    `specification_group_id` |  optional  | int 规格组ID
    `value` |  optional  | string 规格值
    `sort` |  optional  | string 排序

<!-- END_d9565a0de68678e309e99c2e8fd69539 -->

<!-- START_0a0da6d68d17c1fd128129c0f8d97cb7 -->
## SpecificationEdit
保存规格

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/specification/1?id=at&name=ducimus&label=distinctio&type=quod&is_search=minus&location=aut&specification_group_id=repellat&value=voluptate&sort=nostrum" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specification/1"
);

let params = {
    "id": "at",
    "name": "ducimus",
    "label": "distinctio",
    "type": "quod",
    "is_search": "minus",
    "location": "aut",
    "specification_group_id": "repellat",
    "value": "voluptate",
    "sort": "nostrum",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/specification/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 规格ID
    `name` |  optional  | string 规格名称
    `label` |  optional  | string 规格标注名称
    `type` |  optional  | int 规格类型
    `is_search` |  optional  | string 是否可搜索
    `location` |  optional  | string 显示位置
    `specification_group_id` |  optional  | int 规格组ID
    `value` |  optional  | string 规格值
    `sort` |  optional  | string 排序

<!-- END_0a0da6d68d17c1fd128129c0f8d97cb7 -->

<!-- START_5b5753c6de4c54dba30d1b070cee8587 -->
## SpecificationDestroy
删除规格

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/specification/destroy/1?id=praesentium" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specification/destroy/1"
);

let params = {
    "id": "praesentium",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/specification/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 规格ID

<!-- END_5b5753c6de4c54dba30d1b070cee8587 -->

#specificationGroup

规格组管理
Class SpecificationGroupController
<!-- START_e82c6fa789582ec1917e0edf5c618cd0 -->
## SpecificationGroupList
规格组列表

> Example request:

```bash
curl -X GET \
    -G "http://localhost/api/v1/admin/specificationGroup?name=maiores&limit=voluptatem&sort=porro&page=omnis" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specificationGroup"
);

let params = {
    "name": "maiores",
    "limit": "voluptatem",
    "sort": "porro",
    "page": "omnis",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (500):

```json
{
    "status_code": 500,
    "code": 0,
    "message": "Unauthenticated.",
    "result": "error"
}
```

### HTTP Request
`GET api/v1/admin/specificationGroup`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 规格组名称
    `limit` |  optional  | int 每页显示条数
    `sort` |  optional  | string 排序
    `page` |  optional  | string 页码

<!-- END_e82c6fa789582ec1917e0edf5c618cd0 -->

<!-- START_b7fcf9b2bb7020c76f4e4883f5a6da72 -->
## SpecificationGroupCreate
创建规格组

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/specificationGroup?name=est" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specificationGroup"
);

let params = {
    "name": "est",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/specificationGroup`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `name` |  optional  | string 规格组名称

<!-- END_b7fcf9b2bb7020c76f4e4883f5a6da72 -->

<!-- START_45f683a827b60f21eb0047995f6aecbc -->
## SpecificationGroupEdit
保存规格组

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/specificationGroup/1?id=alias&name=temporibus" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specificationGroup/1"
);

let params = {
    "id": "alias",
    "name": "temporibus",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/specificationGroup/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 规格组ID
    `name` |  optional  | string 规格组名称

<!-- END_45f683a827b60f21eb0047995f6aecbc -->

<!-- START_b6f030579e439b18802ec2d0fdb7af14 -->
## SpecificationGroupDestroy
删除规格组

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/admin/specificationGroup/destroy/1?id=non" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/admin/specificationGroup/destroy/1"
);

let params = {
    "id": "non",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```



### HTTP Request
`POST api/v1/admin/specificationGroup/destroy/{id}`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `id` |  optional  | int 规格组ID

<!-- END_b6f030579e439b18802ec2d0fdb7af14 -->


