---

copyright:

  years:  2018

lastupdated: "2018-06-13"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}
{:pre: .pre}

<!-- This template is for getting started with a Bluemix service. It is a task template intended to document productive use of the service. It is not intended for discovery and conceptual information.  -->

<!-- The name of this file should remain index.md.
Please delete out content examples and coding that you are not using for your service. -->

# Getting started with Rainbow
{: #gettingstarted}
<!-- Provide an appropriate ID above -->

<!-- Short description: REQUIRED
The short description section should include one to two sentences describing why a developer would want to use your service in an app. This should be conversational style. For search engine optimization, include the service long name and "Bluemix". Keep the {: shortdesc} after the first paragraph so that the framework renders it properly.

Examples: -->


With Rainbow, you can connect a Rainbow user to an IBM Watson Assistant, and allow users to interact directly to the service.
{:shortdesc}

<!-- If overview content is required, do not include it here. Put it in a separate "## About" section below the task section. -->

<!-- Task section: REQUIRED
The task section includes steps to integrate the service into the app.  
- With task-based, technical information, reduce the conversational style in favor of succinct and direct instructions.
- DO include the basic, most-common-use scenario steps to use the service or integrate it into the app. 
- DO NOT include steps to add the service from the Bluemix catalog; we assume that the user already took steps in the UI to add the service. 
- DO include code snippets in all languages that can be copied, as well as VCAP service info.  
- For additional tasks like configuring, managing, etc., add a task section (## Gerund_task_title) below the task section or "About" section if used. Use a task title such as "Configuring x", "Administering y", "Managing z". -->

<!-- You can include an optional prerequisites paragraph for any prerequisites to be met before integrating the service. For example: -->

<!-- Include a sentence to briefly introduce the steps. Examples: -->

To integrate your app with the service, complete these steps:

1. Sign into [Rainbow API Hub](http://hub.openrainbow.com/){: new_window} or [Register](https://www.openrainbow.com/subscribe_btm/){: new_window} for a Rainbow account

1. From the developer hub dashboard, you are able to select the **applications** entry in the left panel

   ![Developer Dashboard](https://mp.s81c.com/8034F2C/dal05/v1/AUTH_db1cfc7b-a055-460b-9274-1fd3f11fe689/product_documentation_image_/02-dashboard-developer_9e971b00-5b5e-4294-9ad6-b522838c453d.png)

1. Click on **Create Application** button and enter the new application information

   ![Application button](https://mp.s81c.com/8034F2C/dal05/v1/AUTH_db1cfc7b-a055-460b-9274-1fd3f11fe689/product_documentation_image_/04-create-a-new-application_e55ded49-1787-41f6-85ca-1b9d37e4ade2.png)

1. Once created, your new application appears into your applications dashboard. Click on **Keys** button in order to retrieve your *Application ID* and the associated *Secret Key*, both information are necessary for registering your bot.
   
   ![Key details](https://mp.s81c.com/8034F2C/dal05/v1/AUTH_db1cfc7b-a055-460b-9274-1fd3f11fe689/product_documentation_image_/06-key-details_f552fa56-90e8-41b0-9028-d81bac653b53.png)

1. You need also to deploy your application using the **Deploy** button (for *Production* deployment, in Pay as You go context, if not yet done, add a payment method )

   ![Deploy Application](https://mp.s81c.com/8034F2C/dal05/v1/AUTH_db1cfc7b-a055-460b-9274-1fd3f11fe689/product_documentation_image_/08-deploy-application_0625b266-23e5-4b7f-bab4-b51be32b0dd2.png)

1. Create an additional Rainbow user account in order to converse with the Watson Assistant, this will become your bot endpoint for other users.

1. Under IBM Catalog create or reuse an existing Watson Assistant service.

1. If necessary, download and install the [IBM Cloud Command Line Interface](https://console.bluemix.net/docs/starters/install_cli.html){: new_window}

   - Change the API Endpoint
	```bash
	bluemix api https://api.ng.bluemix.net
	```
	{: pre}

   - And login
	```bash
	bluemix login
	```
	{: pre}

1. Log into IBM Cloud Console and create a Rainbow Application Service

   - Click 'Catalog' at the top of the screen
   - Enter 'Rainbow'

    ![Rainbow app from IBM Cloud catalog](https://mp.s81c.com/8034F2C/dal05/v1/AUTH_db1cfc7b-a055-460b-9274-1fd3f11fe689/product_documentation_image_/07-catalog-search-rainbow_4188d622-af68-4b37-9663-cec989929a04.png)

1. After application creation, give a service name, and enter your **Login Email**, **Password**, **Application ID** and **Secret Key**, if you want to target our Sandbox platform instead of the production platform, simply enter *"sandbox"* into **Target Platform**, please consult the [Development on Sanbox](https://hub.openrainbow.com/#/documentation/doc/hub/developer-sandboxed-platform){: new_window} and [Managing tests accounts](https://hub.openrainbow.com/#/documentation/doc/sdk/cli/tutorials/Managing_tests_accounts){: new_window} guides to use this platform.

1. Locally, clone our sample application:

    ```bash
    git clone -b bluemix-rainbow-quickstart https://github.com/Rainbow-CPaaS/StarterKit-SDKNodeJSWatson.git
	````
    {: pre}

1. Deploy the application using the command line tools:

   ```bash
   bluemix app push <Your App Name>
   ```
   {: pre}

1. In the IBM Cloud Dashboard, you are able to see <Your App Name>, click on your Rainbow Service under 'Cloud Foundry Services', then click the 'Create connection +' button. Connect it to your new <Your App Name> application. Do the same with your Watson Assistant service.

	{: screen}



<!-- Related links section: still REQUIRED but moved to toc file (in your same folder).  Edit there.
-->