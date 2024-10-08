Technical Design Document

**Project Title**: COD confirmed order notes

**Author** : Gokul Krishnan

**Version**:

---

## Table of Contents

- [Objective](#Objective)
- [Backend Implementation](#Backend-Implementation)
- [Flow Diagram](#Flow-Diagram)
- [Test Cases](#test-cases)
- [Future Scope](#Future-Scope)

  

## **Objective**

  To start passing order notes for each order whenever a customer places a cod order and confirms the cod order via the COD Confirmation Notification on the bot.




## **Backend Implementation**

- **declare an abstract function in src/services/storeProvider.ts file**
- **define the abstract function for both shopify and woocommerce stores in src/services/shopify/controller.ts  and src/services/woocommerce/controller.ts files respectively**
- **call the abstract function in the endofflow function in src/notifications/controllers/Notifications.ts file**


## **Flow Diagram**
![image](https://github.com/user-attachments/assets/bc253307-b9b9-4d5b-a322-fd0bb9bb48e0)


## **Test cases**
- [Test Cases Sheet](https://docs.google.com/spreadsheets/d/1T1WkJ1I1yV2c2wCxsbaRHHz5E03pEd5Qs4dNTLfI31A/edit?usp=sharing)



## **Future Scope**

- **Online stores other than shopify and woocommerce**
