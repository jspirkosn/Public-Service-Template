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

- **Status:** Complete, this automates the build of the CSDM as record producers are added to the catalog
- **Setup:**
	1. Go to [your instance] and login as an Admin user
	2. In the ServiceNow Navigator, go to System Definition -> Tables
	3. Search for and open the table called "Not Available for Subscribers"
	4. Open the "Application Access" tab
	5. Make sure the table is accessible from "All application scopes" and all boxes are checked
	6. This will allow our workflow to update this table from the "Public Service Template" scope
- **Explanation:**
	1. In the ServiceNow Navigator, go to "Process Automation" -> "Flow Designer"
	2. Open the flow called "Public Services Data Modeler" by clicking on it
	3. In the Flow Designer click on the home icon
	4. Selec the Actions menu
	5. Open the action called "Public Service Catalog to Service Portfolio" by clicking on it
	6. Watch the Setup video for a detailed explanation
	7. To try it copy the "Report Streelight Out" Public form. Navigation: Public Services Template -> Public Forms
	8. Once copied go to Public Services Template -> Public Service Offerings 
	9. Observe there is a new offering with the same name as your copied public form
	
- **Setup Video:**
	[Taming the Common Service Data Model (CSDM)!](https://www.youtube.com/watch?v=0njrn7CQPW4)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Creating Public Forms Simplfied - How to remove hours of configuration time</summary>

- **Status:** Complete, uses workflow to automate repetitive configutaiton tasks
- **Setup:**
	1. Go to [your instance] and login as an Admin user
	2. In the ServiceNow Navigator, go to Public Services Template -> Accecc Producter Tables
	3. Warning: This opens catalog item configration to all scopes, be sure you understand the implications
	4. Make sure you are in the Global Scope
	5. Set "Can Create", "Can Update" and "Can Read" to true for all 4 tables
	6. Set "Can Delete" to true for sc_cat_item_subscribe_no_mtom and sc_cat_item_user_criteria_no_mtom
- **Try it:**
	1. Make sure you are in the "Public Service Template" scope 
	2. In the ServiceNow Navigator, go to Public Services Template -> Public Forms
	3. Click new
	4. Enter a name for your public form
	5. In the upper right of the form selec the three dots for more options and toggle template bar so its on
	6. You should see a template bar at the bottom of the form
	7. Click on the "Public Service Form" template
	8. Save the record
	9. At the bottom of the saved form click on the related list called Categories
	10. Click edit and select the catagory called "Non Emergency Issues" 
	11. Go to [your instance URL]/pub 
	12. Navigate to Services -> Non Emergency Issues and open your new Public Form
	13. Check out the map and the variables (the map may not work if the key has expired, this is covered in the next video)
	14. Watch the Setup video for a detailed explanation
	
- **Setup Video:**
	[Creating Public Forms Simplfied](https://www.youtube.com/watch?v=coRN-KzL4J4)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Default Variable Sets - What you need to know about these</summary>

- **Status:** Complete, public map and public common variables
- **Setup:**
	1. Nothing to do here these are already setup
- **About these variable sets:**
	1. Go to [your instance] and login as an Admin user
	2. In the ServiceNow Navigator, go to Service Catalog -> Variable Sets
	3. You should see 2 varaible sets that are part of the "Public Service Template" Application
	4. The public map uses a widget to render an ESRI map (license reguired for production)
	5. The public map variable set, sends data back to public common variables so these need to work as a set
	6. There is a workflow that creates locations if they aren't in the ServiceNow table (covered in the next demo)
	7. There are 2 UI policies that are part of the Public Common Variables Variable set
	8. Watch the explainer video for more details
		
- **Explainer Video:**
	[Variable Sets](https://www.youtube.com/watch?v=i-7c1I8wybc)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Process case from Public Portal - The start of model drive automation</summary>

- **Status:** Complete, flow designer flow
- **Setup:**
	1. Nothing to do here these are already setup
- **About this flow:**
	1. Go to [your instance] and login as an Admin user
	2. In the ServiceNow Navigator, go to Process Automation -> Flow Designer
	3. Open the flow called "Process case from Public Portal"
	4. Take Note: Trigger is new case
	5. Warning: Do not delete the "Report Street Light Out" example, this flow depends on it
	6. Note how the flow handles the consumer determiniation
	7. Note how we use the Service Structure from the common service data model to route the case
	8. Note how the location gets created in ServiceNow when it doesn't exist
	9. Watch the explainer video for more details
		
- **Explainer Video:**
	[Process case from Public Portal](https://www.youtube.com/watch?v=rUTfgQnyIu8)
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>	
<summary>Coming Soon - New things on-deck</summary>
- **Service Builder Workflow**
  
- **Mobile API Endpoint for NewRocket Mobile**
  
- **NewRocket Mobile App**

  </details>
# Build Your Service Catalog (Coming Soon)
