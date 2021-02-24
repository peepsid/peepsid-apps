# PeepsIDApps

## Check out https://iamfreedom.us to see the link of apps.

### Adding new apps

- Create a pull request adding your application to the correct blockchain in the "apps.json" file. 
- **Fill out all of the fields, they are all required.**
- Add your logo to the `logos/` folder ( **.svg format only!** ). Make sure that the logo file's name matches the `applink` that you specified in the JSON. 

```
{
  "applink":"",      // This is the identifier you use when connecting to PeepsID
                     // For PeepsIDJS it is what you pass into PeepsIDJS.scatter.connect(applink)
                     // It should be only alphanumerical with no special characters or spaces excluding _ - and .
  "name":"",         // This is the name of your application, it should be in Title Case
  "type":"",         // A small tag showing what type of application this is
  "description":"",  // Short description of your application.
  "url":"",          // The URL to your application, or it's landing page.
  "hasimage":"1",    // Adding this specifies that you have added a logo to the /logos/ directory.
  "subdomains":["*"],// Allows capturing subdomains under the same metas. '*' is a wildcard for all subdomains.
  "token":""         // Allows you to pin a token to this app, so that token displays can link to app meta data
}
```

## Type categories

We are now enforcing strict categories. Please make sure that your app is categorized correctly or it will be rejected.

- Gambling
- Game
- Block Explorer
- Exchange
- Tool
- Forum
- Educational
- Social
- Chain
- Payment
- Wallet

#### Requesting types
To request the addition of types into PeepsID you need to PR both this README as well as the `types.json` file in the root path of this repository.

## Token property
The `token` property allows you to pin an app to a specific token. 
The structure for the token is:
```
{blockchain}:{contract}:{symbol}:{chainId}
```
**Token properties must be all lowercase!** 

For example, the dSocial token is:
```
arisen:dsocial:like:aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906
```

## Important note about the applink key: 
If you are a web app, you will need to use your FQDN ( ie.  peepsid.com ) and not what you are passing into the connection.
