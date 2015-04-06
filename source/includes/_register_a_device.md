# Register a device

<p>
  Use <code class="prettyprint">https://punchh.com/api/v1/users</code> to create a device/guest user
</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is not authenticated.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
<table>
  <thead>
    <tr>
      <th align="left"><strong>field</strong></th>
      <th align="left"><strong>sample value</strong></th>
      <th align="left"><strong>explanation</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="left"><code>device_uuid</code></td>
      <td align="left"><code>2322ab23232ef2323</code></td>
      <td align="left">Unique Device Identifier</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/users -X POST -d 'device_uuid=23abcdef232' -H 'punchh-app-key:xxx'
```
```shell
Example Response

{
  "id":200040,
  "authentication_token":"h1arT2zZML7e9pFxpAnf",
  "created_at":"2013-10-31T06:46:03Z",
  "updated_at":"2013-10-31T06:46:03Z",
  "first_name":"Punchh",
  "last_name":"User",
  "email":"23abcdef232@temp.punchh.com",
  "avatar_remote_url":null
}
```
```shell
Error Response

curl https://punchh.com/api/v1/users -X POST

[device_uuid must be provided]
```