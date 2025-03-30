## JSON Data Format for Internet
JSON is a human-readable format for transmitting data. It was originally developed for JavaScript but can be used in any language and is very popular in web applications.
JSON is a text based format represented as key value pairs.
```java
  {
  "key": value
  }
``` 
Key is any string, while the values can be String, number, array, object.

The curly braces represent json.
```java
{
  "employees":[{
      "name": "Aditya",
      "age": 38,
      "location": "Chicago",
      "active":  true
       },
       {
        "name": "Minakshi",
        "age": 35,
        "location": "Chicago"
        "active": true
       }]
  "Company": "Aditya Automation Learning",
  "locations": ["chicago", "Bhopal","Sehore"],
  "Address":
        {
          "Street": "XYZ Road",
          "City": "Bhopal"
          "Pincode": 462022
        }      

}
``` 

Data Types -
1. String
2. Object
3. Array
4. Number
5. Boolean

#### JSON.stringify() will convert JavaScript Object to JSON that can be sent to webserver.

```java
let data = {
        requestid = 228540
};

const request = {
        method: "POST",
        headers: {"Content-Type": "application/json"},
        body: jSON.stringify({data})
        };

```
#### JSON.parse method can read a JSON string and convert it into a JavaScript Object. The best way to do this is to use this built-in JavaScript function JSON.parse().

let data = {
           "firstname": "aditya", 
           "lastname": "Choudhary" 
           }

let myObj = JSON.parse(data)


### Some example jsons in trading world

#### Place Order - 
The order API is the backbone of the trading industry as it allows application to place order through client's
demat account. The API requires authentication which can be provided by passing Bearer Token in the request header.

Broker's API communicates with NSE API by using a set of protocols and JSON based REST API's to facilitate seamless communication 
between client systems, Broker servers and ultimately Exhange.

Request URL ->
https://api.5paisa.com/api/V1/PlaceOrderRequest

Content-Type  -> application/json
Authorization -> Bearer Token

Request ->

```Java
{
    "payload": {
        "customerid": 123
        "exchange": "NSE",
        "price": "250",
        "qty": 100,
        "side": "Buy",
        "type": "Limit",
        "instrument": {
            "symbol": "SBIN"
          }
      }
}

```
Response:

```Java
{
    "payload":{
        "customerid": 123,
        "exchange": "NSE",
        "status": 0,
        "message": "Success"
    }
}
```

#### Order Status Request - 
This API helps you to check order status of placed orders using the order ID.

Path Parameter -> https://api.5paisa.com/V1/OrderStatus/{orderId}

Query parameter -> https://api.5paisa.com/V1/OrderStatus/search?orderId=123
Query parameter -> https://api.5paisa.com/V1/OrderStatus/search?customerAccountId=000


#### Update Order -
This API helps you to update existing order.

https://api.5paisa.com/api/V1/ModifyOrderRequest/

```Java
  {
     "payload": {
        "price":"98",
        "qty":"50",
        "customerOrderid": "2001",
        "entities": {
           "customerOrderid": 123  
        },
        "customerid": "123",
        "instrument": {
            "symbol": "XYZ"
        }
        "side": "Buy",
        "type": "Limit"
        }
}
```
