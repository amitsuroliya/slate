---
title: API Reference

language_tabs:
  - shell
  - ruby
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - register_a_device
  - update_a_user
  - login
  - connect_with_facebook
  - connect_with_punchh
  - forgotten_password
  - fetch_user_notifications
  - finding_a_location
  - creating_a_location
  - list_checkins_of_user
  - create_a_checkin
  - update_a_checkin
  - referral_friends
  - fetch_card_metadata
  - create_a_redemption
  - redemption_code
  - redemption_code_status
  - list_redeemable_items
  - register_a_punchh_from_pos
  - list_gaming_levels
  - create_a_gaming_achievement
  - errors

search: true
---

# Introduction

Punchh Server is in the process of implementing a new set of APIs which are more streamlined for client access.

Each API is designed to respond with JSON. It may provide other responses but they should be considered deprecated.

Base URI: [`https://punchh.com/api/v1`](https://punchh.com/api/v1) or [`https://staging.punchh.com/api/v1`](https://staging.punchh.com/api/v1)


Each API call can contain a Punchh App Key to enable certain Client specific behaviour. If this header is not provided, then a default is assumed but all Punchh built apps in future will contain this key. Older clients will eventually be deprecated because of their inability to send the Punchh App Key. Generic format given below.

`curl https://punchh.com/api/v1/RESOURCE -X METHOD -d 'key=value&key1=value1'`

This wiki page serves as a document for that API.

<ul>
  <li>
    <p>
      <strong>UsersController</strong> primarily deals with user specific activities such as login, signup and connecting the account with Facebook or Punchh
    </p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">1.</td>
          <td align="left"><a href="#register-a-device" class="internal present">Register a device</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users</code></td>
        </tr>
        <tr>
          <td align="left">2.</td>
          <td align="left"><a href="#update-a-user" class="internal present">Update a user</a></td>
          <td align="left"><code>PUT</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users</code></td>
        </tr>
        <tr>
          <td align="left">3.</td>
          <td align="left"><a href="#login" class="internal present">Login</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users/login</code></td>
        </tr>
        <tr>
          <td align="left">4.</td>
          <td align="left"><a href="#connect-with-facebook" class="internal present">Connect with Facebook</a></td>
          <td align="left"><code>PUT</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users/connect_with_facebook</code></td>
        </tr>
        <tr>
          <td align="left">5.</td>
          <td align="left"><a href="#connect-with-punchh" class="internal present">Connect with Punchh</a></td>
          <td align="left"><code>PUT</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users/connect_with_punchh</code></td>
        </tr>
        <tr>
          <td align="left">6.</td>
          <td align="left"><a href="#forgotten-password" class="internal present">Forgotten Password</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users/forgot_password</code></td>
        </tr>
        <tr>
          <td align="left">7.</td>
          <td align="left"><a href="#fetch-user-notifications" class="internal present">Fetch User notifications</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v1/users/notifications</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p>
      <strong>LocationsController</strong> deals with Locations Search and Adding a new Location by the user
    </p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">8.</td>
          <td align="left"><a href="#finding-a-location" class="internal present">Finding a Location</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v1/locations</code></td>
        </tr>
        <tr>
          <td align="left">9.</td>
          <td align="left"><a href="#creating-a-location" class="internal present">Creating a Location</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v1/locations</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>CheckinsController</strong> deals with listing checkins of a user, create a checkin and updating a checkin</p>
    <table>
      <thead>
      <tr>
      <th align="left"></th>
      <th align="left"><strong>Description</strong></th>
      <th align="left"><strong>VERB</strong></th>
      <th align="left"><strong>URL</strong></th>
      </tr>
      </thead>
      <tbody>
        <tr>
        <td align="left">10.</td>
        <td align="left"><a href="#list-checkins-of-a-user" class="internal present">List checkins of a user</a></td>
        <td align="left"><code>GET</code></td>
        <td align="left"><code>https://punchh.com/api/v1/checkins</code></td>
        </tr>
        <tr>
        <td align="left">11.</td>
        <td align="left"><a href="#create-a-checkin" class="internal present">Create a Checkin</a></td>
        <td align="left"><code>POST</code></td>
        <td align="left"><code>https://punchh.com/api/v1/checkins</code></td>
        </tr>
        <tr>
        <td align="left">12.</td>
        <td align="left"><a href="#update-a-checkin" class="internal present">Update a Checkin</a></td>
        <td align="left"><code>PUT</code></td>
        <td align="left"><code>https://punchh.com/api/v1/checkins/:checkin_id</code></td>
        </tr>
        <tr>
        <td align="left">13.</td>
        <td align="left"><a href="#referral-friends" class="internal present">Referral Friends</a></td>
        <td align="left"><code>GET</code></td>
        <td align="left"><code>https://punchh.com/api/v1/checkins/:checkin_id/referral_friends</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>CardsController</strong> deals with fetching card meta data</p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">14.</td>
          <td align="left"><a href="#fetch-card-metadata" class="internal present">Fetch card Metadata</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v1/cards</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>RedemptionsController</strong> deals with creating a redemption for a user</p>

    <table>
      <thead>
        <tr>
        <th align="left"></th>
        <th align="left"><strong>Description</strong></th>
        <th align="left"><strong>VERB</strong></th>
        <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
        <td align="left">15.</td>
        <td align="left"><a href="#create-a-redemption" class="internal present">Create a Redemption</a></td>
        <td align="left"><code>POST</code></td>
        <td align="left"><code>https://punchh.com/api/v1/redemptions</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>RedemptionCodesController</strong> deals with fetching redemption codes by the POS and updating their status by the POS</p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">16.</td>
          <td align="left"><a href="#redemption-code-fetch-(bulk)" class="internal present">Redemption Code Fetch (Bulk)</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v1/redemptions_codes</code></td>
        </tr>
        <tr>
          <td align="left">17.</td>
          <td align="left"><a href="#redemption-code-status-(live)" class="internal present">Redemption Code Status (Live)</a></td>
          <td align="left"><code>PUT</code></td>
          <td align="left"><code>https://punchh.com/api/v1/redemptions_codes/:id</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>RedeemablesController</strong> deals with listing redeemable items for a business</p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">18.</td>
          <td align="left"><a href="#list-redeemable-items" class="internal present">List Redeemable Items</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v1/redeemables</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>ReceiptDetailsController</strong> deals with registering information about a receipt from the POS</p>

    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">19.</td>
          <td align="left"><a href="#create-a-receipt-detail-record" class="internal absent">Create a receipt detail record</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v1/receipt_details</code></td>
        </tr>
        <tr>
          <td align="left">20.</td>
          <td align="left"><a href="#register-a-punchh-from-pos" class="internal present">Register a Punchh from POS</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v2/checkins</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>GamingLevelsController</strong> deals with listing gaming levels for a business</p>

    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">21.</td>
          <td align="left"><a href="#list-gaming-levels" class="internal present">List Gaming Levels</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v1/gaming_levels</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p><strong>GamingAchievementsController</strong> informs server of a gaming achievement of a user</p>
    <table>
      <thead>
        <tr>
        <th align="left"></th>
        <th align="left"><strong>Description</strong></th>
        <th align="left"><strong>VERB</strong></th>
        <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
        <td align="left">22.</td>
        <td align="left"><a href="#create-a-gaming-achievement" class="internal present">Create a Gaming Achievement</a></td>
        <td align="left"><code>POST</code></td>
        <td align="left"><code>https://punchh.com/api/v1/gaming_achievements</code></td>
        </tr>
      </tbody>
    </table>
  </li>
</ul>


