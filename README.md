# SOA Software API HOOK
Put a nice company logo image here. 
Link to product documentation and product overview page
## SmartyStreets API 
### About the API
- Verify Addresses with SmartyStreet's USPS Address Verification API
- Home Page: [SmartyStreet] (https://smartystreets.com)
- API Documentation: [SmartyStreet API docs] (https://smartystreets.com/docs)

### Pre-Reqs
- Create an Account with [SmartyStreet] (https://smartystreets.com)
- Login to Obtain the Auth ID and Auth Token
- Using Firefox or any browser go to (https://api.smartystreets.com) and export the complete SSL certificate hierarchy as a .DER
- Import the certificates into policy manager by selecting the Configure tab -> Security -> Certificates and click "Add Trusted CA Certificate" * note this will take a couple of minutes to propagate to network director. 
- Install Authentication Custom Policies Follow instruction [Here] (https://bitbucket.org/akana/apihooks/src/f0a543b41c437a319e2a6573891813a01ff57f68/pso.experimental.extensions/?at=master)

### Getting Started Instructions
#### Download and Import
- Download SmartyStreetAPIHook.zip (https://github.com/lheritage/Demo/tree/master/dist)
- Login to PolicyManager  example: http://localhost:9900
- Select the select the parent organization you want to import the API Hook into.  The import will create a whole new organization.  Click on the "Import Package" from the Actions navigation window on the right side of the screen
  - click on button to browse for the org_SmartyStreetOrg_export.zip archive file and click Okay.

#### Verify Import
- Expand the organization you imported into.  You should now see a new organization called SmartyStreetOrg.
- Expand the services folder of the SmartyStreetOrg.  You should see two physical and on virtual service.
- Expand scripts.  You should see OpenAPI-Common
- Expand  Policies -> Operation Policies.  You should see two defined.  SmartyStreet-HelloWorldConfig and SmartyStreet_SecurityPolicy

#### Configure Security
- Expand Policies -> Operation Policies and click on SmartyStreet-HelloWorldConfig
- From the XML Policy window in the center pane, click on Modify
- Enter your auth-id and your auth-token for smartystreets.  Get it by logging into smartystreets
- Click Apply
- From the Policy Workflow pane on the right select Activate Policy


#### Policy Activation
- We also need to activate the SmartyStreet_SecurityPolicy.  
- Select SmartyStreet_SecurityPolicy
- From the Policy Workflow pane on the right select Activate Policy



#### Offer an Anonymous Contract
-

#### Verify Connectivity
- Using your browser http://{Your HOST example: localhost:9901}/smarty/v1/validateStreet?street=12100 Wilshire Blvd&city=Los Angeles&state=CA&zipcode=90025

### Modify and Build
In the event you need to change the API Hook.   Here are the instructions to do so. 

### License
Put a link to an open source license

