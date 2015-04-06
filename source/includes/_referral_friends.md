# Referral Friends

<p>Use <code>https://punchh.com/api/v1/checkins/:checkin_id/referral_friends</code> to fetch a list of friends that have punched at the same business/location as this checkin. This call maybe used to suggest a list of friends to gift a referral punchh to after the first punchh of that user at a business.</p>
<p>The API returns a list of users that maybe applicable for receiving punchhs. If no friends are found, an empty array is returned.</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
```shell
Example Request

curl https://punchh.com/api/v1/checkins/1/referral_friends -X GET -u 'user_token:x' -H 'punchh-app-key:xxx'
```
```shell
Example Response
```
```shell
Error Response
```