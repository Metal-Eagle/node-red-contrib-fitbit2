# node-red-contrib-fitbit2

<a href="http://nodered.org" target="_new">Node-RED</a> node that gets information from the Fitbit API.

This node was updated using <https://github.com/inglevir/node-red-contrib-fitbit> as the base. The node was renamed to **fitbit2** to avoid backward compatibility with the core node and is a fork of <https://github.com/borpin/node-red-contrib-fitbit2>.

## Install

---

Run the following command in the root directory of your Node-RED install to install from the Git repository (not currently in NPM).

```bash
npm install Metal-Eagle/node-red-node-fitbit2 --save
```

## Install from a package file

Clone the repository to your local machine and use the following command to create a package file:

```bash
npm pack
```

Upload the package to your Node-RED instance under Manage palette (Alt + Shift + P), then go to the install tab, and click the "upload module tgz file" (<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/5.x/svgs/solid/upload.svg" width="20">) button. Select the package file you created.

## Configure

---

When creating a configuration for Fitbit, you will need to create an app on <https://dev.fitbit.com> with the following settings:

- Callback Url: `https://<YOUR-NODE-RED-SERVER>/fitbit-credentials/auth/callback`
  - Please note the URL **must be HTTPS** (self-signed SSL works).
- OAuth 2.0 Application Type: Server

Other settings are up to you. The app is not fussy about the other URLs.

## Usage

---

One node that gets reports from <a href="http://www.fitbit.com" target="_new">Fitbit</a> via the Web API <https://dev.fitbit.com/build/reference/web-api/>.

### Query node

Fitbit query node supports several endpoints:

- Get Devices information
- Get Activity Log List
- Get Daily Activity Summary
- Get Activity Timeseries
- Get Body Timeseries
- Get Food Timeseries
- Get Food Log
- Get Sleep Log by date
- Get Sleep Log List
- Log Body Weight
- Log Body Fat
- Log activity
- Log food
- Log Water
- Delete activity
- Delete log food

Depending on the endpoint selected, the node will allow different inputs to filter the Fitbit query.

### Note

Node-RED does not currently have a way to update credential data at runtime. App credentials are stored with other credentials, but OAuth2 tokens are saved to disk.

## Credits

- [Inglevir](https://github.com/inglevir)
- [Borpin](https://github.com/borpin)
- [JustinThorReid](https://github.com/JustinThorReid)
