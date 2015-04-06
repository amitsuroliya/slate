# List Gaming Levels

<p>Use GET <code>https://punchh.com/api/v1/gaming_levels</code> to fetch all gaming_levels for a business.</p>
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
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/gaming_levels.json -X GET -H punchh-app-key:"xxxxxx"</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<p>[{"game":"Apples","extra_punchhs":1, "level":"Level 10"}]</p>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>
<p>Error response is a blank array []</p>