# Installable Metadata Template

Contains additional Permision Sets and Permission Set Groups for the [Gateway SMS Package](https://github.com/EncludeLtd/Gateway-SMS-Package)

## Deploy
<a href="https://githubsfdeploy.herokuapp.com?owner=Enclude-Components&repo=gateway-sms-post-install&ref=main">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/deploy.png">
</a>

## Permission Sets

| Name | Description |
|------|-------------|
| SMS Gateway External Credentials | Grants access to the Engage Hub external credential principal, enabling callouts to the SMS gateway. |
| SMS Gateway External Client App | Placeholder permission set used to authorize the SMS gateway external client app. |

## Permission Set Groups

| Name | Assign To | Includes |
|------|-----------|----------|
| SMS Gateway User | Standard and admin users | SMS Gateway External Credentials, encsms__SMS_User |
| SMS Gateway API User | Minimum Access API User | SMS Gateway External Client App, encsms__SMS_Gateway |

> **Note:** Do not assign `SMS Gateway API User` to standard or admin users — it is intended only for the dedicated integration/API user profile.

