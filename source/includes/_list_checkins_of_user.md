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
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/checkins -X GET -u 'user_token:x'</code></p>
<p><code>curl https://punchh.com/api/v1/checkins -X GET -u 'user_token:x' -d 'business_id=1'</code></p>
<p><code>curl https://punchh.com/api/v1/checkins -X GET -u 'user_token:x' -d 'card_id=1'</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<div class="highlight highlight-json"><pre>[{<span class="pl-s"><span class="pl-pds">"</span>business_id<span class="pl-pds">"</span></span>:<span class="pl-c1">40</span>,
  <span class="pl-s"><span class="pl-pds">"</span>card_id<span class="pl-pds">"</span></span>:<span class="pl-c1">35</span>,
  <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>2012-08-08T07:05:56Z<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>for_referring_full_name<span class="pl-pds">"</span></span>:<span class="pl-c1">null</span>,
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>:<span class="pl-c1">48948</span>,
  <span class="pl-s"><span class="pl-pds">"</span>location_id<span class="pl-pds">"</span></span>:<span class="pl-c1">297271</span>,
  <span class="pl-s"><span class="pl-pds">"</span>share_message<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span> sdsdsd<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>loyalty<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>location_name<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Boudin SF - Fountains at Roseville<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>receipt_picture_url<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>/system/recept_images/000/048/948/82a193451f17d11ff5b4c247559f089bafe92ca6.png<span class="pl-pds">"</span></span>}]</pre>
</div>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>