# Netlolo developer challenge

<p align="center">
  <a href="https://www.netlolo.com" target="_blank">
      <img src="./netlolo_logo.png" alt="Netlolo"/>
  </a>
</p>

[![LICENSE](https://img.shields.io/github/license/henriquecarv/netlolo-challenge.svg)](./LICENSE)
[![Dependabot Status](https://api.dependabot.com/badges/status?host=github&repo=henriquecarv/netlolo-challenge)](https://dependabot.com)

## User Story

A customer needs to search in a orderbook. He wants to buy offers below some price, and also sell offers to earn some money.

Returns json data about offers, based on one or more specific amounts. These results can also be sorted in ascending or descending order with an optional parameter.

## System Requirements
* **[NodeJS](https://nodejs.org/en/)** (version >= 8).

## Installing
* ```npm install```

## Running Application
* ```npm start```

## Running UnitTest
* ```npm test```

### Examples

* **URL**
/offer/:amounts/:sort?

*  **URL Params**

   **Required:**
 
   `amounts=[float]`

   **Optional:**

   `sort=[string]`

   * **Sample Calls:**

  ```javascript
    $.ajax({
      url: "/offer/80000/desc",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  http://localhost:3000/offer/80000/desc

  ```javascript
    $.ajax({
      url: "/offer/30000,20000/asc",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  http://localhost:3000/offer/30000,20000/asc
