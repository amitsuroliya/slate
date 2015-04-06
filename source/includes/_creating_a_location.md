# Creating a Location

<p>Use <code>https://punchh.com/api/v1/locations</code> to create a location</p>
<h2><a aria-hidden="true" href="#authentication" class="anchor" id="user-content-authentication"><span class="octicon octicon-link"></span></a>Authentication</h2>
<p>This API is authenticated. User token must be provided as credentials.</p>
<h2><a aria-hidden="true" href="#form-data" class="anchor" id="user-content-form-data"><span class="octicon octicon-link"></span></a>Form Data</h2>
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
      <td align="left"><code>latitude</code></td>
      <td align="left"><code>23.3343</code></td>
      <td align="left">Latitude of the location</td>
      <td align="left">Mandatory</td>
    </tr>
    <tr>
      <td align="left"><code>longitude</code></td>
      <td align="left"><code>32.0203</code></td>
      <td align="left">Longitude of the location</td>
      <td align="left">Mandatory</td>
    </tr>
    <tr>
      <td align="left"><code>name</code></td>
      <td align="left"><code>My Corner Bakery</code></td>
      <td align="left">Name of the location</td>
      <td align="left">Mandatory</td>
    </tr>
    <tr>
      <td align="left"><code>cuisine_type</code></td>
      <td align="left"><code>Bakery</code></td>
      <td align="left">Cuisine Type of the location</td>
      <td align="left">Mandatory</td>
    </tr>
    <tr>
      <td align="left"><code>location_photo</code></td>
      <td align="left">MULTI-PART FILE</td>
      <td align="left">A photo of the location</td>
      <td align="left">Not Mandatory</td>
    </tr>
  </tbody>
</table>
```shell
Example Request

curl https://punchh.com/api/v1/locations -X POST -d 'latitude=12.23&amp;longitude=22.00&amp;name=My Corner Bakery&amp;cuisine_type=Bakery' -u 'user_token:x' -H 'punchh-app-key:xxx'

```
```shell
Example Response
```
```shell
Error Response
```