# Redemption Code Status (Live)

<p>Use PUT <code>https://punchh.com/api/v1/redemption_codes/:id</code> to fetch status of redemption or to mark it processed or void.</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. Location Key Token must be provided as credentials.</p>
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
      <td align="left"><code>process</code></td>
      <td align="left"><code>true</code></td>
      <td align="left">Optional parameter to mark the redemption code as processed</td>
    </tr>
    <tr>
      <td align="left"><code>void</code></td>
      <td align="left"><code>true</code></td>
      <td align="left">Optional parameter to void the redemption code</td>
    </tr>
    <tr>
      <td align="left"><code>amount</code></td>
      <td align="left"><code>10</code></td>
      <td align="left">Amount for Staged Redemption without Menu Item</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/redemption_codes/1 -X PUT -d 'process=true' -H 'Authorization: Token token="xxxxxx"'
```
```shell
Example Response

{:status => "1234567 not found", :category => "invalid"}

{:status => "Processed at <datetime> for Some Business Location. Do NOT give credit against it.",
 :category => "processed", :redemption_amount => 0.0}

{:status => "Expired at <datetime> on customer 'Joe Blow' at Some Business Location for redemption at <datetime>. Please DO NOT give credit against it.", :category => "expired", :redemption_amount => 0.0}

{:status => "Redeemed at <datetime> by customer 'Joe Blow' for #{location_name}. Please HONOR it.",
 :category => "redeemable", :redemption_amount => discount}

{:status =>  "In unassigned pool for Some Business Location. Do NOT give credit against it.",
 :category => "unassigned", :redemption_amount => 0.0}
```
```shell
Error Response
```