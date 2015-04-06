# Update a checkin

<p>Use <code>https://punchh.com/api/v1/checkins/:checkin_id</code> to update a checkin. This maybe required to update additional details of a checkin which maybe captured after the punchh.</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.
If the punchh-app-key header is provided, then punchh app's business will be determined and checkin will be scoped to that business automatically.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
<table>
	<thead>
		<tr>
			<th align="left"><strong>field</strong></th>
			<th align="left"><strong>sample value</strong></th>
			<th align="left"><strong>explanation</strong></th>
			<th align="left"><strong>mandatory</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td align="left"><code>share_message</code></td>
			<td align="left"><code>Great Place..5 Stars</code></td>
			<td align="left">Review Left by the guest</td>
			<td align="left">no</td>
		</tr>
		<tr>
			<td align="left"><code>fb_share_id</code></td>
			<td align="left"><code>1232</code></td>
			<td align="left">Facebook shared comment id</td>
			<td align="left">no</td>
		</tr>
		<tr>
		<td align="left"><code>republishable</code></td>
		<td align="left"><code>1</code></td>
		<td align="left">Boolean value indicating whether the business can share this comment</td>
		<td align="left">no</td>
		</tr>
		<tr>
		<td align="left"><code>friend_to_refer</code></td>
		<td align="left"><code>234</code></td>
		<td align="left">User Id of friend to gift a referral punchh to</td>
		<td align="left">no</td>
		</tr>
	</tbody>
</table>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/checkins/1 -X PUT -d 'republishable=1' -u 'user_token:x'</code></p>
<p><code>curl https://punchh.com/api/v1/checkins/1 -X PUT -d 'friend_to_refer=234' -u 'user_token:x'</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>