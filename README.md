# Procurement System



## Running the application on Bluemix or other Cloud Foundry platforms

1. If you do not already have access to a Cloud Foundry PaaS, [sign up for Bluemix](https://console.ng.bluemix.net/registration/).

2. Download and install the [Cloud Foundry CLI](https://github.com/cloudfoundry/cli).

3. Clone the app to your local environment from your terminal using the following command:

   ```
git clone https://github.com/rameshpoomalai/ProcurementSystem.git
   ```

4. Change into the newly created directory:

   ```
cd ProcurementSystem
   ```

5. Open the `manifest.yml` file and change the `host` value to something unique.

   The host you choose will determine the subdomain of your application's URL.

6. Connect to Bluemix in the command line tool and log in.

   ```
cf api <API_URL> # e.g. https://api.ng.bluemix.net
cf login
   ```

7. Create an instance of the IBM Graph service.

   ```
cf create-service "IBM Graph" Standard ProcurementSystemGraph
   ```
cf create-service-key ProcurementSystemGraph ProcurementSystemGraph

8. Create an instance of the Discovery Service.

  ```
cf create-service "Discovery" Free ProcurementSystemDiscovery
  ```
9. Push the app.

   ```
# optionally, log in
cf api <API_URL> # e.g. https://api.ng.bluemix.net
cf login
# deploy the app
cf push
   ```
## Documentation

  * [IBM Graph documentation](https://ibm-graph-docs.ng.bluemix.net/)
  * [IBM Graph interactive guide for Node.js](https://ibm-graph-docs.ng.bluemix.net/interactive-guide-node-js.html)

## Structure of this application

```
├── assets - frontend assets: css, js, images
├── data
│   └── schema.json - Schema for Procurement System
│   └── gremlin.json - Static data like Supplier, Plant, Region..
├── index.js - main program
├── manifest.yml - manifest that describes the application and its deployment to cloud foundry
├── package.json - node package file with metadata about the project, e.g. dependencies
├── setup.js - setup script to set the schema and import static data
└── templates
    └── index.jade - jade template
```

## Running on Bluemix

The fastest way to deploy this application to Bluemix is to click the **Deploy to Bluemix** button below.

[![Deploy to Bluemix](https://deployment-tracker.mybluemix.net/stats/4dfc8a74f582329adf35199126090e45/button.svg)](https://bluemix.net/deploy?repository=https://github.com/rameshpoomalai/ProcurementSystem.git)

**Don't have a Bluemix account?** If you haven't already, you'll be prompted to sign up for a Bluemix account when you click the button.  Sign up, verify your email address, then return here and click the the **Deploy to Bluemix** button again. Your new credentials let you deploy to the platform and also to code online with Bluemix and Git. If you have questions about working in Bluemix, find answers in the [Bluemix Docs](https://www.ng.bluemix.net/docs/).

## Contribute

See [CONTRIBUTING.md](./CONTRIBUTING.md)

## Running on Bluemix

The fastest way to deploy this application to Bluemix is to click the **Deploy to Bluemix** button below.

[![Deploy to Bluemix](https://deployment-tracker.mybluemix.net/stats/4dfc8a74f582329adf35199126090e45/button.svg)](https://bluemix.net/deploy?repository=https://github.com/rameshpoomalai/ProcurementSystem.git)

**Don't have a Bluemix account?** If you haven't already, you'll be prompted to sign up for a Bluemix account when you click the button.  Sign up, verify your email address, then return here and click the the **Deploy to Bluemix** button again. Your new credentials let you deploy to the platform and also to code online with Bluemix and Git. If you have questions about working in Bluemix, find answers in the [Bluemix Docs](https://www.ng.bluemix.net/docs/).

## Contribute

See [CONTRIBUTING.md](./CONTRIBUTING.md)
