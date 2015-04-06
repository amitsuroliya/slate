# Finding a Location

<p>Use <code>https://punchh.com/api/v1/locations</code> to find a location</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#query-parameters" class="anchor" id="user-content-query-parameters"><span class="octicon octicon-link"></span></a>Query Parameters</h2>
<table>
	<thead>
		<tr>
		<th align="left"><strong>field</strong></th>
		<th align="left"><strong>sample value</strong></th>
		<th align="left"><strong>explanation</strong></th>
		<th align="left">** Mandatory**</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td align="left"><code>latitude</code></td>
			<td align="left"><code>23.3343</code></td>
			<td align="left">Latitude of the location</td>
			<td align="left"></td>
		</tr>
		<tr>
			<td align="left"><code>longitude</code></td>
			<td align="left"><code>32.0203</code></td>
			<td align="left">Longitude of the location</td>
			<td align="left"></td>
		</tr>
		<tr>
			<td align="left"><code>business_id</code></td>
			<td align="left"><code>40</code></td>
			<td align="left">Business Id to scope the search (cannot be provided with name_like)</td>
			<td align="left">optional</td>
		</tr>
		<tr>
			<td align="left"><code>name_like</code></td>
			<td align="left"><code>Burger</code></td>
			<td align="left">Name of location to search (cannot be provided with business_id)</td>
			<td align="left">optional</td>
		</tr>
		<tr>
			<td align="left"><code>max</code></td>
			<td align="left"><code>20</code></td>
			<td align="left">Maximum number of locations to return</td>
			<td align="left"></td>
		</tr>
		<tr>
			<td align="left"><code>gps_accuracy</code></td>
			<td align="left"><code>200</code></td>
			<td align="left">Number of yards the current lat/lng is accurate upto</td>
			<td align="left">optional</td>
		</tr>
	</tbody>
</table>
<p><code>business_id</code> and <code>name_like</code> cannot be provided together.</p>
<p>If the punchh-app-key header is provided, then punchh app's business will be determined and locations will be scoped to that business automatically.</p>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p>
  <code>curl https://punchh.com/api/v1/locations -X GET -d 'latitude=32.232&amp;longitude=23.323' -u 'user_token:x'</code>
  <code>curl https://punchh.com/api/v1/locations -X GET -d 'latitude=32.232&amp;longitude=23.323&amp;name_like=Burger' -u 'user_token:x'</code>
  <code>curl https://punchh.com/api/v1/locations -X GET -d 'latitude=32.232&amp;longitude=23.323&amp;business_id=40' -u 'user_token:x'</code>
  <code>curl https://punchh.com/api/v1/locations -X GET -H 'punchh-app-key: locationaccesskey</code></p>
<h2>
	<a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
	<pre>
	  <code>[{"address":"1247 N Water St","business_id":396,"city":"Milwaukee","country":"United States",
		  "cuisine_type":"American","id":301564,"latitude":"43.0468771","longitude":"-87.9111821",
		  "name":"Vino Volo","post_code":"53202","state":"Wisconsin",
		  "updated_at":"2013-05-10T09:53:55Z","login_required":true,"base_name":"Vino Volo",
		  "photo_path":"/images/punchh-icon-thumb.png","distance":6119.7861920421465,
		  "effective_validation_type":"barcode",
		  "effective_blurb":"Don't forget to recommend us",
		  "location_extra":{"heading1":"Terminal 1","heading2":"Airlines: Aer Lingus", "is_airport":true,"store_number":"BOS"},
		  "location_photos":[{"image_type":"airport_map",
		                      "photo_url":"/path/original/punchh-icon-thumb.png"},
		                     {"image_type":"business_submitted",
		                      "photo_url":"/path/original/colorpicker_rgb_r.png"}]
	    }]
	  </code>
	</pre>
<h2>
<a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>