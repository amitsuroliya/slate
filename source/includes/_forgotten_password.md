# Forgotten Password

<p>Use <code>https://punchh.com/api/v1/users/forgot_password</code> to send password retrieval email to users.</p>
<p>If the email is not found in the database, NO indication is provided to the user as a measure of security.</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is not authenticated.</p>
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
      <td align="left"><code>email</code></td>
      <td align="left"><code>john@example.com</code></td>
      <td align="left">Email of the user</td>
      <td align="left">yes</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/users/forgot_password -X POST -d 'email=sd@example.com'
```

```shell
Example Response
No response But server sends the mail.
```

```shell
Error Response
```