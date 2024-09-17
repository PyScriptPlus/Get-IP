## **jQuery API Request Example**

This repository contains examples of how to use jQuery to perform GET requests using the $.get() method. These examples demonstrate how to send requests to external APIs and handle responses.

Features
API Requests: Sends HTTP GET requests to the ipify API to fetch the user's public IP address.
Parameterized API Request: Demonstrates how to send additional parameters along with the GET request.
Dynamic Content Loading: Uses the .load() method to dynamically load content into an HTML element.

## Fetching Public IP Address

This section demonstrates how to fetch the public IP address of the user using jQuery's `$.get()` method.

```javascript
$(document).ready(function() {
    $("button").click(function() {
        $.get("https://api.ipify.org", function(data, status) {
            alert("Data: " + data + "\nStatus: " + status);
        });
    });
});
```
This code snippet makes a GET request to the https://api.ipify.org API to retrieve the user's public IP address. The result is displayed in an alert box.

## **GET Request with Additional Parameters**

```javascript
$(document).ready(function() {
    $("button").click(function() {
        $.get("https://api.ipify.org", {
            name: "Donald Duck",
            city: "Duckburg"
        }, function(data, status) {
            alert("Data: " + data + "\nStatus: " + status);
        });
    });
});
```
This example sends a GET request with custom parameters (name and city). The server will receive the parameters along with the request.

## **Load Dynamic Content**
```javascript
$("#hello").load("Hello my brother #ip");
```
This line of code dynamically loads the string "Hello my brother" along with the content inside the #ip element into the element with the #hello ID.

## **How to Use**

1.Download or clone this repository.<br>
2.Open the index.html file in your favorite web browser.<br>
3.Click the button to see the IP address retrieval in action.<br>


## **Requirements**

jQuery library (version 3.0+)

## **License**
This project is licensed under the MIT License - see the LICENSE file for details.
