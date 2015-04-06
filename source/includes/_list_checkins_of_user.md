# List Checkins of a User

<p>Use <code>https://punchh.com/api/v1/checkins</code> to fetch unredeemed approved checkins for a user</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
<table>
  <thead>
    <tr>
    <th align="left"><strong>field</strong></th>
    <th align="left"><strong>sample</strong></th>
    <th align="left"><strong>explanation</strong></th>
    <th align="left"><strong>mandatory</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="left"><code>business_id</code></td>
      <td align="left"><code>1</code></td>
      <td align="left">Business Id</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>card_id</code></td>
      <td align="left"><code>2</code></td>
      <td align="left">Card Id</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>location_id</code></td>
      <td align="left"><code>2323</code></td>
      <td align="left">Location Id</td>
      <td align="left">no</td>
    </tr>
  </tbody>
</table>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and checkins will be scoped to that business automatically.</p>
```shell
Example Request

curl https://punchh.com/api/v1/checkins -X GET -u 'user_token:x'

curl https://punchh.com/api/v1/checkins -X GET -u 'user_token:x' -d 'business_id=1'

curl https://punchh.com/api/v1/checkins -X GET -u 'user_token:x' -d 'card_id=1'
```
```shell
Example Response

[{"business_id":40,
  "card_id":35,
  "created_at":"2012-08-08T07:05:56Z",
  "for_referring_full_name":null,
  "id":48948,
  "location_id":297271,
  "share_message":" sdsdsd",
  "status":"loyalty",
  "location_name":"Boudin SF - Fountains at Roseville",
  "receipt_picture_url":"/system/recept_images/000/048/948/82a193451f17d11ff5b4c247559f089bafe92ca6.png"
}]
```
```shell
Error Response
```