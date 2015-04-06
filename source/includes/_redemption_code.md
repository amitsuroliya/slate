# Redemption Code Fetch (Bulk)

<p>Use <code>https://punchh.com/api/v1/redemption_codes</code> to redemption codes for a location (or create if necessary)</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. Location Key Token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#form-data" class="anchor" id="user-content-form-data"><span class="octicon octicon-link"></span></a>Form Data</h2>
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
      <td align="left"><code>processed[]</code></td>
      <td align="left"><code>233343</code></td>
      <td align="left">Redemption Code to be marked as processed. This field can be passed multiple times</td>
    </tr>
    <tr>
      <td align="left"><code>quantity</code></td>
      <td align="left"><code>10</code></td>
      <td align="left">Number of Redemption Codes to be returned; Creating as many as necessary</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/redemption_codes -X POST -d 'quantity=50' -H 'Authorization: Token token="xxxxxx"'

curl https://punchh.com/api/v1/redemption_codes -X POST -d 'processed[]=12121&amp;processed[]=2222&amp;quantity=23' -H 'Authorization: Token token="xxxxxx"'
```
```shell
Example Response
```
```shell
Error Response
```