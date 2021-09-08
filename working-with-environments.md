[Back to main page](README.md)

# Working With Environments To Connect To Multiple C360 Instances

While the variables are stored by default in the collection you can use Postman with [environments](#https://learning.postman.com/docs/sending-requests/managing-environments/) to work with multiple C360 instances in parallel.

The pre-request script has been written to determine if an environment has been selected. If it has been, the environment variables will be used for the authorization. By default in Postman the environment variables will supersede the collection level variables. 

> ⚠️  Using environments means that you will store Marketing Cloud credentials in clear in Postman. Do this at your own risk.

- [Import the Template Environment](#import-the-template-environment)
- [Configure the Environment](#configure-the-environment)

## Import the Template Environment

1. Using a browser, [sign in to Postman](https://identity.getpostman.com/login)
2. Open the main collection with [this link](https://www.postman.com/salesforce-developers/workspace/salesforce-developers)
3. Select the **Environments** tab (item A in following screenshot)
4. Click **C360 Template Environment** (B)
5. Click on the “three dots” icon on the right (C) and select **Export** from the menu

    ![Export environment screenshot](images/export-env.png)

    This downloads a `C360 Template Environment.postman_environment.json` file.

6. Close the browser tab. We'll continue the installation on the Postman app
7. In the Postman app, click **Import**
8. Drag and drop the JSON file you just downloaded in the gray zone
9. Click **Import**

## Configure the Environment

1. Click on the Environments icon
2. Click on the “three dots” icon on the right of the environment template and select duplicate

	![Manage environment screenshot](images/manage-env.png)

    This creates a `C360 Template Environment Copy` template.

3. Click **C360 Template Environment Copy**
4. Rename the environment with something meaningful in relation with your Marketing Cloud instance (e.g.: “Playground 1”)
5. Set values in the **CURRENT VALUE** column for the following variables. If you need instructions for getting these variables go to: [Configure the Collection](install-the-collection.md#configure-the-collection)

|Variable|Example Value|Description|Used In Direct APIs|Used In Connect APIs
|-|-|-|-|-|
|loginUrl|login.salesforce.com|Using login.salesforce.com will be fine unless you are using a sandbox.|X|X|
|version|52.0|Salesforce API version number||X|
|clientId|3MVG9l2zHsylwlpR6H5xByqIHvFbLVATgzkY...|Consumer key from the connected app.|X|X|
|clientSecret|775C20434DB475FC326765353AF5210D4...|Consumer secret from the connected app.||X|
|privateKey|-----BEGIN RSA PRIVATE KEY----- MIIEpAIBAAKCAQEA6spOAo1NhTsOhj19M  <br />...<br />  rEOBZ458a3O4EOfHP1luZb4ZGrnTDRcA== <br /> -----END RSA PRIVATE KEY-----| Contents of host.key file.|X||
|userName|aaroncates@aaroncates-20210405.demo|User Name of the authorized user.|X|X|
|password|superSecretPassword1!|Password of the authorized user.||X|
|securityToken|fVhwzeDFMrAh4IC9hS|Salesforce security token for the authorized user. Details for securing a token available [here](https://developer.salesforce.com/docs/atlas.en-us.api.meta/api/sforce_api_concepts_security.htm).||X|

8. Click **Update** and close the environments dialog
9. Select your environment from the environment dropdown

    ![Select environment screenshot](images/select-env.png)
10. All requests will now use the selected environment instead of the collection level variables.

[Back to main page](README.md)