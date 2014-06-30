scatter-gather
==============

This example demonstrates routing using Scatter-gather component. After hitting an HTTP endpoint, the result of processing is logged and emailed as well.

Step 1: import the project
Step 2: edit common.properties
Step 3: run mule app
Step 4: use postman to send a POST request to http:/localhost:8081 using any json, e.g.:

{
 "a": 3, "b": 4
}

Step 5: Success: verify you recieved an email and look at the console that should contain:

Processing finished: { "a": 3, "b": 4 }
