## Before running
- Add a cert.pem and key.pem to the private directory
- Change the `id` in mobile-config.js to match the bundle identifier of your
provisioning profile with push permissions

## Issue
When multiple Cordova plugins are in the same project as `raix:push` the app
freezes on the launch screen. The app runs perfectly fine without the Cordova
contact plugin. Test my running `meteor remove cordova:org.apache.cordova.contacts@0.2.14`

## Workaround
It is possible to get the app running with both Cordova plugins installed however
in order to do so you need to add an `alert` on the client. For example: in `client/init.js`
add `alert('hello');`. This alert will pop up and after pressing okay the app will run as normal.
