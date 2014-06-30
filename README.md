scatter-gather
==============

This example demonstrates routing using Scatter-gather component. After hitting an HTTP endpoint, the result of processing is logged and emailed as well.

Step 1: import the project
Step 2: edit common.properties
Step 3: run mule app
Step 4: use postman to send a POST request to http:/localhost:8081 using any json, e.g.:

{
 "email": "aaa@abc.sk", 
 "item name": "aa", 
 "item units": 2, 
 "item price per unit": 10,
 "membership": "free"
}
