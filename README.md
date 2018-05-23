# Sunrise

### Configuration


#### Create an API client for a SPA
In the [Admin Center](https://admin.commercetools.com/), select your project and go to the `Developers` section and then the `API Clients` tab. Now click on the `Add API client` button to display a form. There, enter a descriptive name for your new API client and simply click on "Select permissions for an API client suited for a mobile or a single page application", found below the `Permissions` checkboxes.  

#### Configure SUNRISE with your API client 

Create the file `ct-configuration.json` in the root folder with the following contents:
```javascript
{
  "auth": {
    "host": "https://auth.commercetools.com",
    "projectKey": "<your-project-key>",
    "credentials": {
      "clientId": "<your-client-id>",
      "clientSecret": "<your-client-secret>"
    },
    "scopes": ["<your-project-scope-1>", "<your-project-scope-2"]
  },
  "api": {
    "host": "https://api.commercetools.com"
  }
}

```
Replace the project key, client ID, client secret and scopes with your project's API client information. Remember to use an API client suited for single page applications (SPA), as your credentials will be publicly accessible through the browser.