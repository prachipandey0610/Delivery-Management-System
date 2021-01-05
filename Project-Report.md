# Delivery Management System

ASE Course Project Made by TY-C Group 46.

##### Roles & Responsibilities

| Name             | Roll no. | Contribution                                |
| ---------------- | -------- | ------------------------------------------- |
| Mihir Rabade     | 17       | Testing & Debugging                         |
| Prachi Pandey    | 34       | Database (Linking office & Manager)         |
| Neel Parekh      | 38       | Front end (Office Details, Manager Details) |
| Chaitanya Pathak | 42       | Database (Linking Shipment details)         |
| Rashi Wase       | 74       | Front end (Adding Shipment details)         |

# Introduction

- The main aim of Delivery Management System is to keep a **track records of deliveries.** 
- The project starts by adding details of branch and staffs working in their respective branches. 
- Then, the delivery is **marked as** scheduled for delivery. 
- Now, when the parcel is received by the receiver branch, they deliver the parcel and **delivery status is updated** by the sender branch.

Such systems help small business owners to keep a track of their deliveries in more efficient way & thus save time & energy.

## Project Scope

The users of this project are as follows - 

1. Clients (Who can **only check** the status of their delivery)
2. Manager (Who **manages** the office)
3. Office workers (Who enters & updates the delivery **details**)

The scope of this project is to keep track records of the deliveries.

The system will be used for day to day activities like out return, company details, hub rates, booking, non delivery and pickup centers.

Actually It is not easy to do this process manually because it would become very hectic.

Hence it is recommended to automate the process by developing the relevant software as the world is moving from manual working to information and technology era where computerization becomes important in all walks of life.

## Functionality 

Our project provides the following functionalities -

1. Add new Staff and Branch.
2. Enter details of Delivery.
3. Schedule the delivery date and staff.
4. Record the date of delivery.
5. Update the Delivery current status.

## Use Case Diagram

![Use case Diagram for Delivery management System](https://i.imgur.com/eTsdWQA.png)

## Visual Preview

##### Intro Page

![Intro Page](https://i.imgur.com/a3zBcHX.png)

##### Login page for the business owner

![Admin login page](https://i.imgur.com/mxm5kXO.png)

##### Adding Delivery details

![Add shipment page](https://i.imgur.com/HBlr7Dj.png)

##### Delivery status page-1

![Entering Consignment number](https://i.imgur.com/0e64v3z.png) 

##### Delivery status page-2

![image-20201219102012845](https://i.imgur.com/GlTZr2D.png)

## Code Snippet

Code for database connection

```php
<?php
// database connection config
$dbHost = 'localhost';
$dbUser = 'admin'; 
$dbPass = '';
$dbName = 'courier_db';

$dbConn = mysqli_connect($dbHost, $dbUser, $dbPass, $dbName) or die('MySQL connect failed. ' . mysqli_error());
function dbQuery($sql)
{
    global $dbConn;
    $result = mysqli_query($dbConn, $sql);
    return $result;
}
function dbAffectedRows()
{
    global $dbConn;
    return mysqli_affected_rows($dbConn);
}
function dbFetchArray($result, $resultType = MYSQL_NUM)
{
    return mysqli_fetch_array($result, $resultType);
}
function dbFetchAssoc($result)
{
    return mysqli_fetch_assoc($result);
}
function dbFetchRow($result)
{
    return mysqli_fetch_row($result);
}
function dbFreeResult($result)
{
    return mysqli_free_result($result);
}
function dbNumRows($result)
{
    return mysqli_num_rows($result);
}
function dbSelect($dbName)
{
    return mysqli_select_db($dbName);
}
function dbInsertId()
{
    return mysqli_insert_id();
}
```