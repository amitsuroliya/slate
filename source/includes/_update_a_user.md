# Update a User

<p>Use <code>https://punchh.com/api/v1/users</code> to update a user</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2>
  <a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters
</h2>
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
      <td align="left"><code>apn_token</code></td>
      <td align="left"><code>23232323</code></td>
      <td align="left">Apple Push Notification Token</td>
    </tr>
    <tr>
      <td align="left"><code>android_token</code></td>
      <td align="left"><code>23232323</code></td>
      <td align="left">Android Push Notification Token</td>
    </tr>
    <tr>
      <td align="left"><code>first_name</code></td>
      <td align="left"><code>Chris</code></td>
      <td align="left">First Name of the User</td>
    </tr>
    <tr>
      <td align="left"><code>last_name</code></td>
      <td align="left"><code>Martin</code></td>
      <td align="left">Last Name of the User</td>
    </tr>
    <tr>
      <td align="left"><code>access_token</code></td>
      <td align="left"><code>d23232</code></td>
      <td align="left">Facebook Access Token</td>
    </tr>
    <tr>
      <td align="left"><code>gcm_token</code></td>
      <td align="left"><code>232323</code></td>
      <td align="left">Apple Push Notifications for the user (Google Cloud Messaging)</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/users -X PUT -d 'first_name=Chris&email=b80e14f68bed3ca404372f0758f6c54bbde40edf@temp.punchh.com' -H 'punchh-app-key:xxx' -u 'user_token:x'
```
```shell
Example Response

{
  "id":527,
  "authentication_token":"QbAX4aKgPjtXd5HtFVKf",
  "created_at":"2011-01-30T21:35:43Z",
  "updated_at":"2013-10-30T08:42:30Z",
  "first_name":"Punchh",
  "last_name":"User",
  "email":"b80e14f68bed3ca404372f0758f6c54bbde40edf@temp.punchh.com",
  "avatar_remote_url":null
}
```
```shell
Error Response
```