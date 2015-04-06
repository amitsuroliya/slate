# List Gaming Levels

<p>Use GET <code>https://punchh.com/api/v1/gaming_levels</code> to fetch all gaming_levels for a business.</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>No authentication is required. However punchh-app-key header maybe necessary to automatically identify a business.</p>
<h2><a aria-hidden="true" href="#query-parameter" class="anchor" id="user-content-query-parameter"><span class="octicon octicon-link"></span></a>Query Parameter</h2>
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
      <td align="left"><code>business_id</code></td>
      <td align="left"><code>372</code></td>
      <td align="left">Optional parameter identify a business. Not required if punchh-app-key header is provided</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/gaming_levels.json -X GET -H punchh-app-key:"xxxxxx"
```
```shell
Example Response

[
  {
    "game":"Apples",
    "extra_punchhs":1,
    "level":"Level 10"
  }
]
```
```shell
Error Response

Error response is a blank array []
```