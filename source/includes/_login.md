# Login

<p>Use <code>https://punchh.com/api/v1/users/login</code> to authenticate a user</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#example-request" class="anchor" id="user-content-example-request"><span class="octicon octicon-link"></span></a>Example Request</h2>
<p><code>curl https://punchh.com/api/v1/users/login -X GET -u 'user_token:x' -H 'punchh-app-key:xxx'</code></p>
<h2><a aria-hidden="true" href="#example-response" class="anchor" id="user-content-example-response"><span class="octicon octicon-link"></span></a>Example Response</h2>
<div class="highlight highlight-json"><pre>{<span class="pl-s"><span class="pl-pds">"</span>authentication_token<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>j5TMpyyrNsqufHg5nmN8<span class="pl-pds">"</span></span>,
 <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>2011-04-20T19:22:27Z<span class="pl-pds">"</span></span>,
 <span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>asanghi@me.com<span class="pl-pds">"</span></span>,
 <span class="pl-s"><span class="pl-pds">"</span>first_name<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Aditya<span class="pl-pds">"</span></span>,
 <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>:<span class="pl-c1">1189</span>,
 <span class="pl-s"><span class="pl-pds">"</span>last_name<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Sanghi<span class="pl-pds">"</span></span>,
 <span class="pl-s"><span class="pl-pds">"</span>updated_at<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>2012-08-13T11:56:19Z<span class="pl-pds">"</span></span>}</pre>
</div>
<div class="highlight highlight-json"><pre>{<span class="pl-s"><span class="pl-pds">"</span>error<span class="pl-pds">"</span></span>:<span class="pl-s"><span class="pl-pds">"</span>Invalid email or password.<span class="pl-pds">"</span></span>}</pre></div>
<h2><a aria-hidden="true" href="#error-response" class="anchor" id="user-content-error-response"><span class="octicon octicon-link"></span></a>Error Response</h2>