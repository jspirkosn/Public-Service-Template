# Public-Service-Template
The Public Service Template repository is a collection of ServiceNow configurations.  Their purpose is to shorten deployment time for public digital services. The main branch is dependent on two plugins described in the installation instructions.  Download directly into a ServiceNow instance and get started!
# Installation Instructions
1. Prepare your ServiceNow instance or <a href="https://developer.servicenow.com/dev.do#!/guides/quebec/developer-program/pdi-guide/obtaining-a-pdi" title="PDI Readme">Get a Personal Developer Instance</a>
	- In the ServiceNow Navigator go to "System Definition" -> "Plugins"
		- Install the Customer Service(com.sn_customerservice) plugin
 		- Install the Consumer Service Portal(com.glide.service-portal.consumer-portal) plugin
   
2. Create GitHub Access - use an existing account or <a href="https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home" title="GitHub Create Account">Create a New GitHub Account</a>
3. Create a ServiceNow Credential - if you have a GitHub credential for ServiceNow skip to step 4
	- In the ServiceNow Navigator go to "Connections & Credentials" -> "Credentials"
		- Click on "New" to create a new credential
		- Chose "Basic Auth Credential"
		- Give it a name and enter your GitHub User Name and Password from step 3
4. In the ServiceNow Navigator go to "System Applications" -> "Studio"
5. A dialog appears - click on "Import from Source Control"
    - URL: https://github.com/jspirkosn/Public-Service-Template
    - Branch: master 
    - Credential: chose credential from step 3   
6. Access the Public Service Portal - [your instance]/pub
	- Click on the "Services" category
	- Select "Report Streetlight Out"  
7. Enjoy the configurations below!

# Configurations
<details>
<summary>Update the Public Service Template on Your Instance - Steps to update an the Public Service Template applicaiton </summary>

- **Status:** Complete
- **Setup:**
	1. In the ServiceNow Navigator go to "System Applications" -> "Studio"
	2. Select the "Public Service Template" Application
	3. Open the top menu for "Source Control"
	3. Select "Apply Remote Changes"
	4. In the dialog box select "Apply Remote Changes" again
	5. This brings the most recent code into your instance	
- **Setup Video:**
	<a href="https://www.youtube.com/watch?v=aX22pNK14rY" title="Public Services Template - Update the Public Services Template on Your Instance">Update the Public Services Template on Your Instance</a>
	
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Make the Portal Public - These are steps to make the portal accessible to unauthenticated users</summary>

- **Status:** Complete
- **Setup:**
	1. Go to [your instance]/pub and make sure you aren't authenticated - You should only see the header to login and background image
	2. In the ServiceNow Navigator go to "Public Services Template" -> "Widgets to Make Public"
	3. Make sure you are in the global scope
	4. Change the Public field to "true" for all 4 of the widgets
	5. In the ServiceNow Navigator go to "Public Services Template" -> "Pages to Make Public"
	6. Change the Public field to "true" for 1 page
	5. Refresh the browser in step 1 - you should now see the search box and catalog navigations  
	
- **Setup Video:**
	<a href="https://www.youtube.com/watch?v=wtkbx07DY5k" title="Make the Portal Public - Setup">Make the Portal Public - Setup</a>
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>Anonymous User - Make it so a user can continue as Guest</summary>
	
- **Prerequisites:** "Make the Portal Public" 
- **Status:** Complete
- **Setup:**
	1. Follow the steps in the "Update the Public Service Template on Your Instance" section above
	2. Go to [your instance]/pub and make sure you aren't authenticated - you should see the search box and catalog navigations
	3. Navigate to Services - Non Emergency Issues
	3. Click on the "Report Streetlight Out" catalog item
	4. On the login page select "Continue as Guest"
	5. You should see a User name or password invalid message
	6. Go to [your instance] and login as an Admin user
	7. Make sure you are in the "Global" scope
	8. In the ServiceNow Navigator go to "Public Services Template" -> "Scripts to Run"
	9. Click on "Create Public User for Anonymous Access" to open it
	10. Once opened click on "Run Fix Scipt"
	11. Click on "Proceed"
	12. Go to [your instance]/pub and make sure you aren't authenticated 
	13. Navigate to Services - Non Emergency Issues
	14. Click on the "Report Streetlight Out" catalog item
	15. On the login page select "Continue as Guest"
	16. You should see a form and it should say "Public Guest" in the upper right-hand corner
	
- **Setup Video:**
	<a href="https://www.youtube.com/watch?v=z80QPiMahpY" title="Anonymous User - Setup">Anonymous User - Setup</a>
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>


- **Service Builder Workflow**
   - Status: Complete 
   - Usage demo: {coming soon}  
   - Instructions:
   - Configuration demo:
   - Contributors: john.spirko@servicenow.com
- **Variable Sets (Map and Common)**
   - Status: Complete 
   - Usage demo: {coming soon}  
   - Instructions:
   - Configuration demo:
   - Contributors: john.spirko@servicenow.com
- **Mobile API Endpoint for NewRocket Mobile**
   - Status: Not Started 
   - Usage demo: {coming soon}  
   - Instructions:
   - Configuration demo:
   - Contributors: john.spirko@servicenow.com
- **NewRocket Mobile App**
   - Status: Not Started 
   - Usage demo: {coming soon}  
   - Instructions:
   - Configuration demo:
   - Contributors: john.spirko@servicenow.com
- **Case Workflow**
   - Status: 50% complete 
   - Usage demo: {coming soon}  
   - Instructions:
   - Configuration demo:
   - Contributors: john.spirko@servicenow.com
