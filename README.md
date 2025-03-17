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

JSON.stringify() will convert JavaScript Object to JSON that can be sent to webserver.

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
When we want to read a JSON (essentially our string of data) and convert it into a JavaScript Object. The best way to do this is to use this built-in JavaScript function JSON.parse().

let data = {
           "firstname": "aditya", 
           "lastname": "Choudhary" 
           }

let myObj = JSON.parse(data)

