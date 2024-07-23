Technical Design Document

**Project Title**: Shopify Store Information 

**Author** : Abinayashri, Gokul Krishnan

**Version**:

---

## Table of Contents

- [Objective](#objective)
- [Problem Description and Proposed Solution](#problem-description-and-proposed-solution)
- [Flow Diagram for Server Restart](#flow-diagram-for-server-restart)
- [Config Migration and DB Migration](#config-migration-and-db-migration)
- [Interface/API Definitions (Schemas)](#interfaceapi-definitions-schemas)
- [Test Cases](#test-cases)
  
---

## **Objective**

  To fetch and show details such as order value, order count, shopify store start date on the settings menu in the dashboard
  
---

## **Frontend Implementation**

- **GENERATE NEW COMPONENT**

- **GENERATE NEW SERVICE**

- **SETTINGS.SERVICE.TS**
  - **Set up the FuseNavigationItem**
  - **Add guard set up to prevent unauthorized access**
 
- **SETTINGS.SERVICE.TS**
  - **Set up the FuseNavigationItem**

- **CONFIG.MODEL.TS AND CONFIG.SERVICE.TS**
  - **Set up the config of client and access companydetails field to check for storeproviders.**
  -**Check if StoreProviders are shopify then Storeinfo -> true else it will be false, therefore it ensures that shopify-storeinfo is visible only to shopify stores**
    
- **SHOPIFY-STOREINFO.COMPONENT.HTML**
  - **To display the received response from the component.ts**

- **SHOPIFY-STOREINFO.COMPONENT.TS**
  - **Communicate with the service to make an api call to the backend**
  - **Once the call has been made and the response has been received, then display it in html file**
- **Uses snackbar service to throw an error message if any error has been occurred in fetching the results.**
  
- **STOREINFO.SERVICE.TS**
  - **Uses http get function to call the backend api and stores the responses and return them to ts file.**

- **SETTINGS.GUARD.TS**
  - **CANACTIVATE: To restrict the unauthorized user from route access**
  - **CANLOAD: Prevents the module from download**

## **Backend Implementation**

- **define a helper function for fetching order count and order value from the db in src/services/helper.ts file**
- **declare an abstract function in src/services/storeProvider.ts file**
- **define the abstract function in src/services/shopify/controller.ts file**
- **define an endpoint /store-info in the src/services/routes.ts file**
- **call the helper and abstract function in the route function in scr/services/routes.ts**

## **Flow Diagram**
<img width="830" alt="RESPONSE" src="https://github.com/user-attachments/assets/5e7609f0-7ae1-4e42-9498-5e05c10372a5">

## **API Endpoints**
- **assistedsales/store-info**

## **API definitions**

- **GET store information**
	- **description : retrieves the starting date of the shopify store, total order value, total order count**
	- **endpoint :  assistedsales/store-info**
	- **http method : GET**
	- **expected response: JSON object**
		{
		    "orderCount": "95",
		    "orderValue": "54231.00",
		    "startDate": "2021-07-07T01:16:07+05:30"
		}



