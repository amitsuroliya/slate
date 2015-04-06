# Redemption Code Status (Live)

<p>Use PUT <code>https://punchh.com/api/v1/redemption_codes/:id</code> to fetch status of redemption or to mark it processed or void.</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. Location Key Token must be provided as credentials.</p>
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
			<td align="left"><code>process</code></td>
			<td align="left"><code>true</code></td>
			<td align="left">Optional parameter to mark the redemption code as processed</td>
		</tr>
		<tr>
			<td align="left"><code>void</code></td>
			<td align="left"><code>true</code></td>
			<td align="left">Optional parameter to void the redemption code</td>
		</tr>
		<tr>
			<td align="left"><code>amount</code></td>
			<td align="left"><code>10</code></td>
			<td align="left">Amount for Staged Redemption without Menu Item</td>
		</tr>
	</tbody>
</table>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/redemption_codes/1 -X PUT -d 'process=true' -H 'Authorization: Token token="xxxxxx"'</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<p>invalid</p>
<pre><code>{:status =&gt; "1234567 not found", :category =&gt; "invalid"}
</code></pre>
<p>processed</p>
<pre><code>{:status =&gt; "Processed at &lt;datetime&gt; for Some Business Location. Do NOT give credit against it.",
 :category =&gt; "processed",
 :redemption_amount =&gt; 0.0}
</code></pre>
<p>expired</p>
<pre><code>{:status =&gt; "Expired at &lt;datetime&gt; on customer 'Joe Blow' at Some Business Location for redemption at &lt;datetime&gt;. Please DO NOT give credit against it.",
 :category =&gt; "expired",
 :redemption_amount =&gt; 0.0}
</code></pre>
<p>redeemed</p>
<pre><code>{:status =&gt; "Redeemed at &lt;datetime&gt; by customer 'Joe Blow' for #{location_name}. Please HONOR it.",
 :category =&gt; "redeemable",
 :redemption_amount =&gt; discount}
</code></pre>
<p>unassigned</p>
<pre><code>{:status =&gt;  "In unassigned pool for Some Business Location. Do NOT give credit against it.",
 :category =&gt; "unassigned",
 :redemption_amount =&gt; 0.0}
</code></pre>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>