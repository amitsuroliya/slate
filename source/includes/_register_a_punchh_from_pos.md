# Register a Punchh from POS

<p>Use <code>https://punchh.com/api/v2/checkins</code> to create a punchh from the POS</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. Location Key Token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#form-data" class="anchor" id="user-content-form-data"><span class="octicon octicon-link"></span></a>Form Data</h2>
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
      <td align="left"><code>transaction_no</code></td>
      <td align="left"><code>233343</code></td>
      <td align="left">Transaction Number of the Receipt</td>
    </tr>
    <tr>
      <td align="left"><code>menu_items[]</code></td>
      <td align="left"><code>xxx,xxx,yyy</code></td>
      <td align="left">List of Menu Items</td>
    </tr>
    <tr>
      <td align="left"><code>amount</code></td>
      <td align="left"><code>23.00</code></td>
      <td align="left">Amount of the receipt</td>
    </tr>
    <tr>
      <td align="left"><code>subtotal_amount</code></td>
      <td align="left"><code>23.00</code></td>
      <td align="left">Subtotal Amount of the receipt without taxes and tips</td>
    </tr>
    <tr>
      <td align="left"><code>receipt_datetime</code></td>
      <td align="left"><code>12-23-2012 23:33:33</code></td>
      <td align="left">Time of the receipt</td>
    </tr>
    <tr>
      <td align="left"><code>cc_last4</code></td>
      <td align="left"><code>2323</code></td>
      <td align="left">Last 4 digit of the credit card</td>
    </tr>
    <tr>
      <td align="left"><code>employee_id</code></td>
      <td align="left"><code>12</code></td>
      <td align="left">Employee Id in store</td>
    </tr>
    <tr>
      <td align="left"><code>employee_name</code></td>
      <td align="left"><code>Tom Smith</code></td>
      <td align="left">Employee Name</td>
    </tr>
    <tr>
      <td align="left"><code>user_token</code></td>
      <td align="left"><code>1234</code></td>
      <td align="left">Token string scanned from User's Phone to identify the user</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v2/checkins -X POST
  -d 'user_token=1234&amp;transaction_no=23232&amp;amount=23.0&amp;cc_last4=3434'
  -d 'menu_items[]="cake,2,22.0"'
  -d 'menu_items[]="shake,2,32.0"'
  -H 'Authorization: Token token="xxxxxx"'
```
```shell
Example Response
{
  "first_name":"Aditya",
  "last_name":"Sanghi",
  "avatar_url":"https://punchh.com/someavatarurl.png",
  "checkins":3
}
```
```shell
Error Response
```