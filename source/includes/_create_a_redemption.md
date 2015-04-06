# Create a Redemption

<p>Use <code>https://punchh.com/api/v1/redemptions</code> to create a redemption</p>
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
      <td align="left"><code>location_id</code></td>
      <td align="left"><code>1212</code></td>
      <td align="left">Location Id where guest wants to redeem</td>
    </tr>
    <tr>
      <td align="left"><code>business_id</code></td>
      <td align="left"><code>100</code></td>
      <td align="left">Business Id where guest wants to redeem</td>
    </tr>
    <tr>
      <td align="left"><code>latitude</code></td>
      <td align="left"><code>12.00</code></td>
      <td align="left">Latitude of the Location where guests want to redeem</td>
    </tr>
    <tr>
      <td align="left"><code>longitude</code></td>
      <td align="left"><code>23.00</code></td>
      <td align="left">Longitude of the Location where guests want to redeem</td>
    </tr>
    <tr>
      <td align="left"><code>redeemed_points</code></td>
      <td align="left"><code>100</code></td>
      <td align="left">Number of requested points to redeem in case of points based redemption</td>
    </tr>
    <tr>
      <td align="left"><code>gps_accuracy</code></td>
      <td align="left"><code>200</code></td>
      <td align="left">Number of yards the current lat/lng is accurate upto</td>
    </tr>
    <tr>
      <td align="left"><code>redeemable_id</code></td>
      <td align="left"><code>2</code></td>
      <td align="left">Redeemable Item being redeemed. Preferred to be provided over redeemable_points</td>
    </tr>
  </tbody>
</table>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and redemption will be scoped to that business automatically.</p>
```shell
Example Request

curl https://punchh.com/api/v1/redemptions -X POST -d 'location_id=1212' -u 'user_token:x'

curl https://punchh.com/api/v1/redemptions -X POST -d 'business_id=100&amp;latitude=12.00&amp;longitude=23.00' -u 'user_token:x'
```
```shell
Example Response
```
```shell
Error Response
```