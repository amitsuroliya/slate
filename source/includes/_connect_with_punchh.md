# Connect With Punchh

<p>Use <code>https://punchh.com/api/v1/users/connect_with_punch</code> to connect a guest user with Punchh account</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
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
			<td align="left"><code>password</code></td>
			<td align="left"><code>233343232</code></td>
			<td align="left">User's password</td>
			<td align="left">yes</td>
		</tr>
		<tr>
			<td align="left"><code>email</code></td>
			<td align="left"><code>john@example.com</code></td>
			<td align="left">Email of the user</td>
			<td align="left">yes</td>
		</tr>
		<tr>
			<td align="left"><code>first_name</code></td>
			<td align="left"><code>John</code></td>
			<td align="left">First Name of the user</td>
			<td align="left">no</td>
		</tr>
		<tr>
			<td align="left"><code>last_name</code></td>
			<td align="left"><code>Smith</code></td>
			<td align="left">Last Name of the user</td>
			<td align="left">no</td>
		</tr>
		<tr>
			<td align="left"><code>android_token</code></td>
			<td align="left"><code>232323</code></td>
			<td align="left">Android Push Notification Token for the user</td>
			<td align="left">no</td>
		</tr>
		<tr>
			<td align="left"><code>apn_token</code></td>
			<td align="left"><code>232323</code></td>
			<td align="left">Apple Push Notifications for the user</td>
			<td align="left">no</td>
		</tr>
		<tr>
			<td align="left"><code>gcm_token</code></td>
			<td align="left"><code>232323</code></td>
			<td align="left">Apple Push Notifications for the user (Google Cloud Messaging)</td>
			<td align="left">no</td>
		</tr>
	</tbody>
</table>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/users/connect_with_punchh -X PUT -d 'password=23232&amp;email=sd@example.com&amp;first_name=John&amp;last_name=Smith' -u 'user_token:x' -H 'punchh-app-key:xxx'</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>