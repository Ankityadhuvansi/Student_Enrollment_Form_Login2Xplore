# JsonPowerDB API

## Description
JsonPowerDB (JPDB) is a Real-time, High-performance, REST API-based database designed for developers. It allows you to access, manipulate, and query data in JSON format with minimal configuration. The database aims to provide a fast, flexible, and easy-to-use solution for managing and interacting with data using REST APIs.

## Benefits of Using JsonPowerDB
- **Real-time Data Access:** Direct access to data without additional layers or complex queries.
- **High Performance:** JPDB is optimized for fast data retrieval and processing.
- **No SQL Required:** You can work with JSON data without writing SQL queries, saving time and reducing complexity.
- **Simple and Lightweight:** Easy to set up and integrate into your applications.
- **REST API Support:** Full support for CRUD operations via REST APIs.

## Release History
- **v1.0.0** - Initial release with basic CRUD functionality for JSON data.
- **v1.1.0** - Added support for advanced querying and filtering features.
- **v1.2.0** - Performance improvements and bug fixes.
- **v1.3.0** - Documentation update and new API endpoints.
  
For more details, visit our [GitHub Repository](https://github.com/).

## Table of Contents
- [JsonPowerDB API](#jsonpowerdb-api)
  - [Description](#description)
  - [Benefits of Using JsonPowerDB](#benefits-of-using-jsonpowerdb)
  - [Release History](#release-history)
  - [Table of Contents](#table-of-contents)
  - [Illustrations](#illustrations)
  - [Scope of Functionalities](#scope-of-functionalities)
  - [Examples of Use](#examples-of-use)
  - [Project Status](#project-status)
  - [Sources](#sources)
  - [Other Information](#other-information)

## Illustrations
(Insert any diagrams or screenshots that show how JsonPowerDB works or how to interact with the API.)

## Scope of Functionalities
- **CRUD Operations:** Perform Create, Read, Update, and Delete operations on JSON data.
- **Data Retrieval:** Retrieve data from JsonPowerDB using filters and queries.
- **Data Management:** Insert, update, and delete records in a flexible and simple way.
- **Authentication and Authorization:** Secure your API with token-based authentication.

## Examples of Use
### Example 1: Creating a New Record
```bash
POST /api/record
{
    "token": <"connection-token">,
    "cmd": "PUT",
    <<"dbName": <"database-name">,>>
    <<"rel": <"relation-name">,>>
    <<"colsAutoIndex": <boolean-value>,>>
    <<"templateStr": <json-template-data>,>>
    "jsonStr": <json-data>
}
```
### Example 5: Retrieving Data (GET)
To retrieve data using JsonPowerDB, send a request with the following JSON structure:
```json
{
    "token": "<connection-token>",
    "cmd": "GET",
    "dbName": "<database-name>",
    "rel": "<relation-name>",
    "jsonStr": {
        "<column-name>": "<column-value>"
    }
}
```
### Example 6: Updating Data (UPDATE)
To update existing records in JsonPowerDB, send a request with the following JSON structure:

```json
{
    "token": "<connection-token>",
    "cmd": "UPDATE",
    "dbName": "<database-name>",
    "rel": "<relation-name>",
    "jsonStr": {
        "<record-no>": {
            "<column-name>": "<new-value>"
        },
        "<record-no>": {
            "<column-name>": "<new-value>"
        }
    }
}
```
### Example 7: Removing Data (REMOVE)
To remove records in JsonPowerDB, send a request with the following JSON structure:

```json
{
    "token": "<connection-token>",
    "cmd": "REMOVE",
    "dbName": "<database-name>",
    "rel": "<relation-name>",
    "record": "<record-number | [record-number1, record-number2,...] | {\"range\":[from-rec-no,to-rec-no]}>",
    "jsonStr": {}
}

````

# Student Enrollment Form

It is a student registration form that stores the user's data in JSONPowerDB. It supports REST APIs and serverless technology. Students can be added, updated based on their roll number. In this form, the roll number is automatically checked and by the help of API, the data entered into other input fields sothat the user can update accordingly. The application uses AJAX requests for smooth and fast interaction. All kinds of data can be stored, such as numbers, strings, dates, etc.




## Benefits of using JsonPowerDB

- Can store structured / semi-structured and unstructured data along with other types of files and big-data.
- Dynamic relational constraints while using CRUD operations. i.e. Relational data can be managed without pre-defining PK, FK, UK, databases, tables etc.
- Free from technology constraints - Low-Code and easy to use from any technology via HTTP Rest AP
- Minimum learning curves, builds faster, cuts time to market, reduces the development cost.
- Helps developers in managing their databases using various tools and techniques.


## Release History
### JsonPowerDB
**Version:** 2.0
#### Execute API

```
var baseUrl = "http://api.login2explore.com:5577";
function executeCommand(reqString, apiEndPointUrl) {
    var url = baseUrl + apiEndPointUrl;
    var jsonObj;
    
    $.post(url, reqString, function (result) {
        jsonObj = JSON.parse(result);
    }).fail(function (result) {
        var dataJsonObj = result.responseText;
        jsonObj = JSON.parse(dataJsonObj);
    });
    return jsonObj;
}
```
#### Create a PUT Request String
```
function createPUTRequest(connToken, jsonObj, dbName, relName) {
    var putRequest = "{\n"
            + "\"token\" : \""
            + connToken
            + "\","
            + "\"dbName\": \""
            + dbName
            + "\",\n" + "\"cmd\" : \"PUT\",\n"
            + "\"rel\" : \""
            + relName + "\","
            + "\"jsonStr\": \n"
            + jsonObj
            + "\n"
            + "}";
    return putRequest;
}

```

## Features

- Simple to Use
- Fast Response
- Detailed User Interface
## Tech Stack

**Client:** HTML,CSS,Javascript

**Server:** JsonPowerDB


## Screenshots

![PC View1](https://i.ibb.co/MnTPjzC/1.png)

![PC View2](https://i.ibb.co/XFNXybp/2.png)



