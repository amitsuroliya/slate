# Connect With Facebook

<p>Use <code>https://punchh.com/api/v1/users/connect_with_facebook</code> to connect a guest user with facebook</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
<table>
  <thead>
    <tr>
      <th align="left"><strong>field</strong></th>
      <th align="left"><strong>sample value</strong></th>
      <th align="left"><strong>explanation</strong></th>
      <th align="left"><strong>mandatory</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="left"><code>access_token</code></td>
      <td align="left"><code>233343232</code></td>
      <td align="left">Facebook Access Token</td>
      <td align="left">yes</td>
    </tr>
    <tr>
      <td align="left"><code>fb_uid</code></td>
      <td align="left"><code>3202032</code></td>
      <td align="left">Facebook UID</td>
      <td align="left">yes</td>
    </tr>
    <tr>
      <td align="left"><code>email</code></td>
      <td align="left"><code>john@example.com</code></td>
      <td align="left">Email of the user</td>
      <td align="left">yes</td>
    </tr>
    <tr>
      <td align="left"><code>first_name</code></td>
      <td align="left"><code>John</code></td>
      <td align="left">First Name of the user</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>last_name</code></td>
      <td align="left"><code>Smith</code></td>
      <td align="left">Last Name of the user</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>android_token</code></td>
      <td align="left"><code>232323</code></td>
      <td align="left">Android Push Notification Token for the user</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>apn_token</code></td>
      <td align="left"><code>232323</code></td>
      <td align="left">Apple Push Notifications for the user</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>gcm_token</code></td>
      <td align="left"><code>232323</code></td>
      <td align="left">Apple Push Notifications for the user (Google Cloud Messaging)</td>
      <td align="left">no</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/users/connect_with_facebook -X PUT -d 'fb_uid=23232&amp;email=sd@example.com&amp;access_token=232323&amp;first_name=John&amp;last_name=Smith' -u 'user_token:x' -H 'punchh-app-key:xxx'
```

```shell
Example Response

{
  "id":120006,
  "authentication_token":"HMzvYLd64UcDXqybwb6a",
  "created_at":"2013-05-07T11:53:07Z",
  "updated_at":"2013-10-30T09:17:11Z",
  "first_name":"Amit",
  "last_name":"MsCat",
  "email":"enticeatlanta@yahoo.com",
  "avatar_remote_url":"https://fbcdn-profile-a.akamaihd.net/hprofile-ak-prn1/161882_541686154_261895383_q.jpg"
}
```
```shell
Error Response
```