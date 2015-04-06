# List Redeemable Items

<p>Use GET <code>https://punchh.com/api/v1/redeemables</code> to fetch all redeemables for a business.</p>
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

curl https://punchh.com/api/v1/redeemables.json -X GET -H punchh-app-key:"xxxxxx"
```
```shell
Example Response

[{"description":"Free Dessert","discount_amount":5.99,"id":1,"name":"Free Dessert",
  "points":50,"image":"/redeemable_images/original/missing.png"},
 {"description":"Free Appetizer","discount_amount":5.99,"id":2,"name":"Free Appetizer",
  "points":50,"image":"/redeemable_images/original/missing.png"},
 {"description":"$5 Off T-shirts","discount_amount":5.0,"id":3,"name":"T-Shirt Discount",
  "points":150,"image":"/redeemable_images/original/missing.png"},
 {"description":"$10 Magic Money Credit","discount_amount":10.0,"id":4,"name":"Magic Money",
  "points":200,"image":"/redeemable_images/original/missing.png"}]
```
```shell
Error Response

Error response is a blank array []
```