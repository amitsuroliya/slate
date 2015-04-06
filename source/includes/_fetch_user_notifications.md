# Fetch user notifications

<p>Use <code>https://punchh.com/api/v1/users/notifications</code> to fetch notifications for a user</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
<table>
  <thead>
    <tr>
      <th align="left"><strong>field</strong></th>
      <th align="left"><strong>sample value</strong></th>
      <th align="left"><strong>explanation</strong></th>
      <th align="left"><strong>default</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="left"><code>network</code></td>
      <td align="left"><code>apple</code></td>
      <td align="left">Apple or Google</td>
      <td align="left">apple</td>
    </tr>
    <tr>
      <td align="left"><code>qty</code></td>
      <td align="left"><code>5</code></td>
      <td align="left">Number of notifications to fetch</td>
      <td align="left">10</td>
    </tr>
  </tbody>
</table>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and notifications will be scoped to that business automatically.</p>
```shell
Example Request

curl https://punchh.com/api/v1/users/notifications -X GET -d 'network=apple&amp;qty=5' -u 'user_token:x'

Example Response

Error Response
```