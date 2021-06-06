# Public-Service-Template
The Public Service Template repository is a collection of ServiceNow configurations.  Their purpose is to shorten the deployment time for public digital services. The main branch is dependent on two plugins described in the installation instructions.  Download directly into a ServiceNow instance and get started!
# Installation Instructions
1. Prepare your ServiceNow instance or <a href="https://developer.servicenow.com/dev.do#!/guides/quebec/developer-program/pdi-guide/obtaining-a-pdi" title="PDI Readme">Get a Personal Developer Instance</a>
	- In the ServiceNow Navigator go to "System Definition" -> "Plugins"
    - Install the Customer Service(com.sn_customerservice) plugin
   
2. Create GitHub Access - use an existing account or <a href="https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home" title="GitHub Create Account">Create a New GitHub Account</a>
3. Create a ServiceNow Credential - if you have a GitHub credential for ServiceNow skip to step 4
	- In the ServiceNow Navigator go to "Connections & Credentials" -> "Credentials"
		- Click on "New" to create a new credential
		- Chose "Basic Auth Credential"
		- Give it a name and enter your GitHub User Name and Password from step 3
4. In the ServiceNow Navigator go to "System Applications" -> "Studio"
5. A dialog appears click on "Import from Source Control"
    - URL: https://github.com/jspirkosn/Public-Service-Template
    - Branch: master 
    - Credential: chose credential from step 3   
6. Access the Public Service Portal - [your instance]/pub
	- Click on the "Services" category
	- Select "Report Streetlight Out"  
7. Enjoy the configurations below!

# Configurations
<details>
<summary>Make the Portal Public - These are steps to make the portal accessible to unauthenticated users</summary>

- **Status:** Complete
- **Demo:** {coming soon}
- **Setup:**
- **Setup Video:**
- **Contributors:** 
	- john.spirko@servicenow.com 
</details>

<details>
<summary>**Anonymous User** - Make it so a user can continue as Guest</summary>

- **Status:** Complete
- **Demo:** {coming soon}
- **Setup:**
- **Setup Video:**
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
