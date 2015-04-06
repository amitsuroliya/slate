# Create a Gaming Achievement

<p>Use <code>https://punchh.com/api/v1/gaming_achievements</code> to create a redemption</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
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
      <td align="left"><code>business_id</code></td>
      <td align="left"><code>100</code></td>
      <td align="left">Business Id</td>
    </tr>
    <tr>
      <td align="left"><code>level</code></td>
      <td align="left"><code>Level 10</code></td>
      <td align="left">Game Level of Game reached</td>
    </tr>
    <tr>
      <td align="left"><code>game</code></td>
      <td align="left"><code>Apples</code></td>
      <td align="left">Name of Game</td>
    </tr>
  </tbody>
</table>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and redemption will be scoped to that business automatically.</p>
```shell
Example Request

curl https://punchh.com/api/v1/gaming_achievements -X POST -d 'level=Sandwich' -d 'game=Scratch n Match' -u 'utoken:x' -H punchh-app-key:"xxx"
```
```shell
Example Response

200 OK no response body
```
```shell
Error Response
```