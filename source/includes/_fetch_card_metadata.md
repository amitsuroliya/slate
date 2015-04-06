# Fetch Card Metadata

<p>Use <code>https://punchh.com/api/v1/cards</code> to fetch meta data of one or more cards</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is not authenticated.</p>
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
      <td align="left"><code>business_ids</code></td>
      <td align="left"><code>1,2,3,4,5</code></td>
      <td align="left">Comma separated list of business_ids</td>
    </tr>
  </tbody>
</table>
<p>The above field is not mandatory if punchh-app-key header is provided.</p>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and card will be scoped to that business automatically.</p>
```shell
Example Request

curl https://punchh.com/api/v1/cards -X GET -d 'business_ids=1,2,3,4'
```
```shell
Example Response

[{
    "background_color":"#f8f8ec",
    "business_id":1,
    "description":"Complimentary Dessert",
    "disclaimer_color":"#000000",
    "id":1,
    "marketing_info":"Located in the heart of Palo Alto, Mike\u2019s Ristorante provides both a neighborhood restaurant and bar as well as a fine dining destination. By belnding american italian cuisine with french flair, we craft distinctive dishes. ",
    "marketing_message":" ",
    "marketing_title":"Mike's Ristorante",
    "name":"Sample Mike's Ristorante",
    "punches_on_first_row":5,
    "punches_on_second_row":0,
    "referred_punch_color":"#70B3EA",
    "required_punches":5,
    "updated_at":"2012-06-03T10:38:22Z",
    "validation_type":"code",
    "well_designed_card":false,
    "login_required":false,
    "background_url":"",
    "logo_url":"/system/cards/logos/000/000/001/original/mikelogo_long.png",
    "punch_url":"/images/default_punchh.png",
    "marketing_image_url":"/system/cards/marketing_images/000/000/001/original/mikelogo.png",
    "disclaimer":"",
    "marketing_link":"http://localhost:3000/b/1",
    "membership_levels": [
      {"id": 1, "level": "Gold", "description": "This is some description", max_points: 100, min_points: 50,
    "background_image_url": "https://punchh.com/system/membership_levels/3323.jpg"},{..}

  ]},
  {...}
]
```
```shell
Error Response
```