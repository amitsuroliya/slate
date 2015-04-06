# Register a device

<p>
  Use <code class="prettyprint">https://punchh.com/api/v1/users</code> to create a device/guest user
</p>
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
			<td align="left"><code>device_uuid</code></td>
			<td align="left"><code>2322ab23232ef2323</code></td>
			<td align="left">Unique Device Identifier</td>
		</tr>
  </tbody>
</table>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/users -X POST -d 'device_uuid=23abcdef232' -H 'punchh-app-key:xxx'</code></p>
<h2>
  <a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
  <div class="highlight highlight-json"><pre>{<span class="pl-s"><span class="pl-pds">"</span>authentication_token<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>ARfx6xZJZKcrHntUSpzN<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>2012-08-11T10:40:22Z<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>23232@temp.punchh.com<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>first_name<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Punchh<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>:<span class="pl-c1">25934</span>,
    <span class="pl-s"><span class="pl-pds">"</span>last_name<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>User<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>updated_at<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>2012-08-11T10:40:22Z<span class="pl-pds">"</span></span>}</pre>
  </div>
<h2>
<a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>
<p><code>curl https://punchh.com/api/v1/users -X POST</code></p>
<div class="highlight highlight-json"><pre>[<span class="pl-s"><span class="pl-pds">"</span>device_uuid must be provided<span class="pl-pds">"</span></span>]</pre></div>