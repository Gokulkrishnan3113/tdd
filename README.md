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
