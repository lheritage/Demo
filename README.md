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
- Import the certificates into policy manager by selecting the Configure tab -> Security -> Certificates and click Add Trusted CA Certificate
- - note this will take a couple of minutes to propegate to network director. 
- Install Authentication Custom Policies Follow instruction [Here] (http://GitHub.com)

### Getting Started Instructions
#### Download and Import
- Download SmartyStreetAPIHook.zip
- Login to PolicyManager  example: http://localhost:9900
- Select the organization you want to import the API Hook into and click on the "Import Package" from the Actions navigation window on the right side of the screen
  - click on button to browse for the SmartyStreetAPIHook.zip archive file and click Okay.

#### Verify Import
- Expand the services folder in the organization you imported the SmartyStreetAPIHook.zip into and find SmartyStreets_API

#### Configure Security
- Open xxxx
- Put in your Auth ID and Auth Token

#### Verify Connectivity
- Using curl bla bla bla

### Modify and Build
In the event you need to change the API Hook.   Here are the instructions to do so. 

### License
Put a link to an open source license

