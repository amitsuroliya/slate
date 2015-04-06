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
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/cards -X GET -d 'business_ids=1,2,3,4'</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<div class="highlight highlight-json">
  <pre>[{
		<span class="pl-s"><span class="pl-pds">"</span>background_color<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>#f8f8ec<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>business_id<span class="pl-pds">"</span></span>:<span class="pl-c1">1</span>,
		<span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Complimentary Dessert<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>disclaimer_color<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>#000000<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>:<span class="pl-c1">1</span>,
		<span class="pl-s"><span class="pl-pds">"</span>marketing_info<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Located in the heart of Palo Alto, Mike<span class="pl-cce">\u2019</span>s Ristorante provides both a neighborhood restaurant and bar as well as a fine dining destination. By belnding american italian cuisine with french flair, we craft distinctive dishes. <span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>marketing_message<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span> <span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>marketing_title<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Mike's Ristorante<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Sample Mike's Ristorante<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>punches_on_first_row<span class="pl-pds">"</span></span>:<span class="pl-c1">5</span>,
		<span class="pl-s"><span class="pl-pds">"</span>punches_on_second_row<span class="pl-pds">"</span></span>:<span class="pl-c1">0</span>,
		<span class="pl-s"><span class="pl-pds">"</span>referred_punch_color<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>#70B3EA<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>required_punches<span class="pl-pds">"</span></span>:<span class="pl-c1">5</span>,
		<span class="pl-s"><span class="pl-pds">"</span>updated_at<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>2012-06-03T10:38:22Z<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>validation_type<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>code<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>well_designed_card<span class="pl-pds">"</span></span>:<span class="pl-c1">false</span>,
		<span class="pl-s"><span class="pl-pds">"</span>login_required<span class="pl-pds">"</span></span>:<span class="pl-c1">false</span>,
		<span class="pl-s"><span class="pl-pds">"</span>background_url<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>logo_url<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>/system/cards/logos/000/000/001/original/mikelogo_long.png<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>punch_url<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>/images/default_punchh.png<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>marketing_image_url<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>/system/cards/marketing_images/000/000/001/original/mikelogo.png<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>disclaimer<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>marketing_link<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>http://localhost:3000/b/1<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>membership_levels<span class="pl-pds">"</span></span>: [
		  {<span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>, <span class="pl-s"><span class="pl-pds">"</span>level<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Gold<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>This is some description<span class="pl-pds">"</span></span>, <span class="pl-ii">max_points</span>: <span class="pl-c1">100</span>, <span class="pl-ii">min_points</span>: <span class="pl-c1">50</span>,
		<span class="pl-s"><span class="pl-pds">"</span>background_image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://punchh.com/system/membership_levels/3323.jpg<span class="pl-pds">"</span></span>},{<span class="pl-ii">..</span>}
		]},{<span class="pl-ii">...</span>}]
  </pre>
</div>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>