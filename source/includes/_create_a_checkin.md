# Create a Checkin

<p>Use <code>https://punchh.com/api/v1/checkins</code> to a Checkin for a user</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#form-data" class="anchor" id="user-content-form-data"><span class="octicon octicon-link"></span></a>Form Data</h2>
<table>
	<thead>
		<tr>
			<th align="left"><strong>field</strong></th>
			<th align="left"><strong>sample value</strong></th>
			<th align="left"><strong>explanation</strong></th>
			<th align="left"><strong>Mandatory</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td align="left"><code>card_id</code></td>
			<td align="left"><code>12</code></td>
			<td align="left">Id of the card being punchhed</td>
			<td align="left">no</td>
		</tr>
		<tr>
			<td align="left"><code>location_id</code></td>
			<td align="left"><code>5</code></td>
			<td align="left">Id of the location being punchhed at</td>
			<td align="left">yes</td>
		</tr>
		<tr>
			<td align="left"><code>recept_image</code></td>
			<td align="left">MULTIPART IMAGE FILE</td>
			<td align="left">Picture of the Receipt</td>
			<td align="left"></td>
		</tr>
		<tr>
			<td align="left"><code>pass_code</code></td>
			<td align="left"><code>1234</code></td>
			<td align="left">Employee Passcode</td>
			<td align="left">necessary with employee code type validation</td>
		</tr>
		<tr>
			<td align="left"><code>qr_decoded</code></td>
			<td align="left"><code>QR Code's Code</code></td>
			<td align="left">Decoded QR Code</td>
			<td align="left">necessary with qr code type validation</td>
		</tr>
		<tr>
			<td align="left"><code>business_id</code></td>
			<td align="left"><code>5</code></td>
			<td align="left">Id of the business where punchh is taking place</td>
			<td align="left">yes if no location_id is present</td>
		</tr>
		<tr>
			<td align="left"><code>latitude</code></td>
			<td align="left"><code>23.00</code></td>
			<td align="left">Latitude of the location where punchh is happening</td>
			<td align="left">yes is no location_id is present</td>
		</tr>
		<tr>
			<td align="left"><code>longitude</code></td>
			<td align="left"><code>32.00</code></td>
			<td align="left">Longitude of the location where punchh is happening</td>
			<td align="left">yes is no location_id is present</td>
		</tr>
		<tr>
			<td align="left"><code>gps_accuracy</code></td>
			<td align="left"><code>200</code></td>
			<td align="left">Number of yards the current lat/lng is accurate upto</td>
			<td align="left">optional</td>
		</tr>
	</tbody>
</table>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and checkin will be scoped to that business automatically.</p>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/checkins -X POST -d 'card_id=1&amp;location_id=1212&amp;qr_decoded=212' -u 'user_token:x'</code></p>
<p><code>curl https://punchh.com/api/v1/checkins -X POST -d 'business_id=1212&amp;qr_decoded=212&amp;latitude=23.00&amp;longitude=10.0' -u 'user_token:x'</code></p>
<p>Fields returned</p>
<p><code>id</code></p>
<p><code>business_id</code></p>
<p><code>card_id</code></p>
<p><code>location_id</code></p>
<p><code>created_at</code></p>
<p><code>share_message</code></p>
<p><code>status</code></p>
<p><code>verification_count</code></p>
<p><code>for_referring_full_name</code></p>
<p><code>points_earned</code></p>
<p><code>points_spent</code></p>
<p><code>location_name</code></p>
<p><code>receipt_picture_url</code></p>
<p><code>points_available</code></p>
<p><code>first_checkin_message</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>