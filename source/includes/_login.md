# Login

<p>Use <code>https://punchh.com/api/v1/users/login</code> to authenticate a user</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
```shell
Example Request

curl https://punchh.com/api/v1/users/login -X GET -u 'user_token:x' -H 'punchh-app-key:xxx'
```
```shell
Example Response

{"authentication_token":"j5TMpyyrNsqufHg5nmN8",
 "created_at":"2011-04-20T19:22:27Z",
 "email":"asanghi@me.com",
 "first_name":"Aditya",
 "id":1189,
 "last_name":"Sanghi",
 "updated_at":"2012-08-13T11:56:19Z"}
```
```shell
Error Response

{"error":"Invalid email or password."}
```