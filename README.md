# JSONPowerDB
This is a trial mini project on Netbeans that describes what I learned about the JSONPowerDB.

## Title
Basic Web Form

### Description
JSON stands for JavaScript Object Notation. JSONPowerDB is a next generation database management and processing technology that is built on the most fastest indexing system, Power Index. In this project, I use the methods and Rest APIs through the Talend API Tester to create and manipulate in the database(s).
Based on an externally taken bootstrap website structure, the project focuses on taking information from user through a web form and saving it in JSON database.

### Benefits of Using JSONPowerDB
- Schema free, simple to use
- in built support for querying multiple databases
- multiple security layers
- used to create web or mobile applications
- Serverless support for faster development
- reduces ownership costs

### Release History
0.3.2 / 2022-05-10
* Completed Phase-3 of Pluggable API Framework to include global configuration properties that controls the usage of API globally for all users. 
* The implementation of configuration properties for Pluggable Drive API. 
* A new Pluggable Drive API added which returns the detailed information about file(s) / folder(s) - fileinfo 
* Improved: Responses of Pluggable Drive APIs - uploadtext, uploadbinary, copy,  createfolder to return available Drive Space.
* New functions added from 0.0.5 for pluggable column related APIs and also added createUPDATERecordRequest2()
* Added: A new method in jpdb-commons.js (0.0.4 and 0.0.5) for creating the INC request i.e. createINCRequest(token, jsonObj, dbName, relName, recNo).
* Deprecated: foldersize API
* Improved: Documentation
* Fixed: Various Important bugs fixed.

### Examples of Use
- insert record:
insert record:
{
  "token": "90937455|-31949292686629998|90943112",
    "cmd": "PUT",
    "dbName": "Employees",
    "rel": "Employee-Rel",
    "jsonStr": {
        "id": "1001",
        "name": "Kashish",
        "email": "kash3132001@gmail.com",
        "mobileno": "7023333478"
    }
}
- retrieve data:
{
    "token": "90937455|-31949292686629998|90943112",
    "cmd": "GET",
    "dbName": "Employees",
    "rel": "Employee-Rel",
    "jsonStr":{
        "name": "Kashish"
    }
}
- update:
{
    "token": "90937455|-31949292686629998|90943112",
    "cmd": "UPDATE",
    "dbName": "Employees",
    "rel": "Employee-Rel",
    "jsonStr":{
      "1": {
      "name": "Pankhuri",
       "email": "pankh@gmail.com",
        "mobileno": "0009998887"
        "id": "1000",
        "salary": 1000000
      }
    }
}
- remove record:
{
    "token": "90937455|-31949292686629998|90943112",
    "cmd": "REMOVE",
    "dbName": "Employees",
    "rel": "Employee-Rel",
    "record": "1",
}




