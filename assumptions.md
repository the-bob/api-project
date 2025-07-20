## Assumptions.


* The following infrastructure has been provisioned
  * `RDS` MySQL (Aurora or Regular RDS)
  * `Route53`
* All the needed Static Code Analysis, Security Scanning tool etc. is already Available.
* There's already a Docker Registry available (be it `ECR`, `nexus`, `jfrog` etc.) and this assumes that we have a `dev` and a `prod` Registry.
* The database already have a structure of (**NOTE:** there maybe more columns on the tables, but we'll just show what we need for this exercise, also this assumes we have a `users` table.):
  * The id is using `UUIDv7` and it's shortened via `base64` encode. 
  * The date is using `ISO 8601` Format (This includes the timezone)

<table style="width:100%;">
  <tr>
    <td style="vertical-align:top; width:33%;">
      <table border="1" cellpadding="4" cellspacing="0" style="width:100%;">
        <thead>
          <tr>
            <th>venues</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>id</td></tr>
          <tr><td>name</td></tr>
          <tr><td>address</td></tr>
          <tr><td>email</td></tr>
          <tr><td>....</td></tr>
          <tr><td>&nbsp;</td></tr>
        </tbody>
      </table>
    </td>
    <td style="padding-left:10px; vertical-align:top; width:33%;">
      <table border="1" cellpadding="4" cellspacing="0" style="width:100%;">
        <thead>
          <tr>
            <th>classes</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>id</td></tr>
          <tr><td>name</td></tr>
          <tr><td>venueid</td></tr>
          <tr><td>date</td></tr>
          <tr><td>class_size_limit</td></tr>
          <tr><td>....</td></tr>
        </tbody>
      </table>
    </td>
    <td style="padding-left:10px; vertical-align:top; width:33%;">
      <table border="1" cellpadding="4" cellspacing="0" style="width:100%;">
        <thead>
          <tr>
            <th>class_reservation</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>id</td></tr>
          <tr><td>venueid</td></tr>
          <tr><td>classid</td></tr>
          <tr><td>userid</td></tr>
          <tr><td>status</td></tr>
          <tr><td>....</td></tr>
        </tbody>
      </table>
    </td>
  </tr>
</table>


* The `SCM` we're using is `GIT`  then we'll use `GitHub` Cloud.

<hr/>

[back](./README.md)