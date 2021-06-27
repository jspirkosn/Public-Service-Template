# Public-Service-Template
The Public Service Template repository is a collection of ServiceNow configurations.  Their purpose is to shorten deployment time for public digital services. The main branch is dependent on two plugins described in the installation instructions.  Download directly into a ServiceNow instance and get started!
# Installation Instructions
1. Prepare your ServiceNow instance or <a href=https://developer.servicenow.com/dev.do#!/guides/quebec/developer-program/pdi-guide/obtaining-a-pdi title="PDI Readme">Get a Personal Developer Instance</a>
	- In the ServiceNow Navigator, go to "System Definition" -> "Plugins"
		- Install the Customer Service(com.sn_customerservice) plugin
 		- Install the Consumer Service Portal(com.glide.service-portal.consumer-portal) plugin
   
2. Create GitHub Access - use an existing account or [GitHub Create Account](https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
4. Log into your GitHub Account
5. In the browser where you logged in to GitHub, paste this URL: https://github.com/jspirkosn/Public-Service-Template
6. In the upper right hand corner of the page you should see a button to fork the repo, click to create your own fork
7. Once the fork is complete copy the URL, it should be https://github.com/[your github user]/Public-Service-Template
8. Create a ServiceNow Credential - if you have a GitHub credential for ServiceNow, skip to step 8
	- In the ServiceNow Navigator go to "Connections & Credentials" -> "Credentials"
		- Click on "New" to create a new credential
		- Chose "Basic Auth Credential"
		- Give it a name and enter your **GitHub** User Name and Password
9. In the ServiceNow Navigator, go to "System Applications" -> "Studio"
10. A dialog appears - click on "Import from Source Control"
    - URL: https://github.com/[your github user]/Public-Service-Template (the one you copied in step 6)
    - Branch: master 
    - Credential: chose credential from step 7   
11. Access the Public Service Portal - [your instance]/pub
	- Click on the "Services" category
	- Select "Report Streetlight Out"  
12. Enjoy the configurations below!

# Configurations
<details>
<summary>Update the Public Service Template on Your Instance - Steps to update an the Public Service Template applicaiton </summary>

- **Status:** Complete
- **Setup:**
	1. In the ServiceNow Navigator, go to "System Applications" -> "Studio"
	2. Select the "Public Service Template" Application
	3. Open the top menu for "Source Control"
	3. Select "Apply Remote Changes"
	4. In the dialog box, select "Apply Remote Changes" again
	5. This brings the most recent code into your instance	
- **Setup Video:**
	[Update the Public Services Template on Your Instance](https://www.youtube.com/watch?v=aX22pNK14rY)
	
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Make the Portal Public - These are steps to make the portal accessible to unauthenticated users</summary>

- **Status:** Complete
- **Setup:**
	1. Go to [your instance]/pub and make sure you don't authenticate - You should only see the header to login and background image
	2. In the ServiceNow Navigator, go to "Public Services Template" -> "Widgets to Make Public."
	3. Make sure you are in the global scope
	4. Change the Public field to "true" for all 4 of the widgets
	5. In the ServiceNow Navigator, go to "Public Services Template" -> "Pages to Make Public."
	6. Change the Public field to "true" for 1 page
	5. Refresh the browser in step 1 - you should now see the search box and catalog navigations  
	
- **Setup Video:**
	[Make the Portal Public - Setup](https://www.youtube.com/watch?v=wtkbx07DY5k)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Anonymous User - Make it so a user can continue as Guest</summary>
	
- **Prerequisites:** "Make the Portal Public." 
- **Status:** Complete
- **Setup:**
	1. Follow the steps in the "Update the Public Service Template on Your Instance" section above
	2. Go to [your instance]/pub and make sure you don't authenticate - you should see the search box and catalog navigations
	3. Navigate to Services - Non Emergency Issues
	3. Click on the "Report Streetlight Out" catalog item
	4. On the login page, select "Continue as Guest."
	5. You should see a User name or password invalid message
	6. Go to [your instance] and login as an Admin user
	7. Make sure you are in the "Global" scope
	8. In the ServiceNow Navigator, go to "Public Services Template" -> "Scripts to Run."
	9. Click on "Create Public User for Anonymous Access" to open it
	10. Once opened, click on "Run Fix Script."
	11. Click on "Proceed."
	12. Go to [your instance]/pub and make sure you don't authenticate 
	13. Navigate to Services - Non Emergency Issues
	14. Click on the "Report Streetlight Out" catalog item
	15. On the login page, select "Continue as Guest."
	16. You should see a form and it should say "Public Guest" in the upper right-hand corner
	
- **Setup Video:**
	[Anonymous User - Setup](https://www.youtube.com/watch?v=z80QPiMahpY)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Unleash the Common Service Data Model (CSDM)! - CSDM foundations and structure</summary>

- **Status:** Complete
- **Setup:**
	1. Go to [your instance] and login as an Admin user
	2. In the ServiceNow Navigator, go to "Public Services Template" -> "Scripts to Run"
	3. Open the script called "Unleash the Common Service Data Model!" by clicking on it
	4. Run the script by clicking on "Run Fix Script" in the upper right
	4. Watch the Setup video for a detailed explanation
	
- **Setup Video:**
	[Unleash the Common Service Data Model (CSDM)!](https://www.youtube.com/watch?v=FSbpdsAn0Fw)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Taming the Common Service Data Model (CSDM)! - Stop designing and start getting value!</summary>

- **Status:** In progress, this automates the build of the CSDM as record producers are added to the catalog
- **Setup:**
	1. There is nothing to configure, this is an explaination of automation only
	2. Go to [your instance] and login as an Admin user
	3. In the ServiceNow Navigator, go to "Process Automation" -> "Flow Designer"
	4. Open the flow called "Public Services Data Modeler" by clicking on it
	5. In the Flow Designer click on the home icon
	6. Selec the Actions menu
	7. Open the action called "Public Service Catalog to Service Portfolio" by clicking on it
	8. Watch the Setup video for a detailed explanation
	
- **Setup Video:**
	[Taming the Common Service Data Model (CSDM)!](https://www.youtube.com/watch?v=FSbpdsAn0Fw)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Coming Soon - New things on-deck</summary>
- **Service Builder Workflow**

- **Variable Sets (Map and Common)**
  
- **Mobile API Endpoint for NewRocket Mobile**
  
- **NewRocket Mobile App**
  
- **Case Workflow**

  </details>
# Build Your Service Catalog (Coming Soon)
