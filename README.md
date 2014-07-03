# Scatter Gather to email and Logger


This example shows us the use of the scatter-gather flow control to send the same message to a logger and a gmail account in parallel. 

### Assumptions

This document describes the details of the example within the context of Anypoint™ Studio, Mule ESB’s graphical user interface (GUI). This document assumes that you are familiar with Mule ESB and the [Anypoint Studio interface](http://www.mulesoft.org/documentation/display/current/Anypoint+Studio+Essentials). 

### Example Use Case

In this example a sample data in JSON format received through an  using the datamapper and is sent to an email address using the SMTP connector. The Datamapper also computes the total price for each order by multiplying the unit price with the number of units. This example has been configured for gmail.

### Set Up and Run this Example

1. **Open** the project in the studio interface

2. Navigate to src/main/app and **edit common.properties** as follows:

 
        # SMPT Services configuration
        smtp.host=smtp.gmail.com
        smtp.port=587
        smtp.user=senderemailid%40gmail.com
        smtp.password=senderpassword

        # Mail details
        mail.from=senderemailid@gmail.com
        mail.to=receiveremailid@gmail.com
        mail.subject=Processing Finished Report
    
3. **Run** the project as a Mule application

4. Send a sample JSON data to your localhost server running your mule application. 
         
        Sample JSON data: { "a": 3, "b": 4 }

5. Login to receiveremailid@gmail.com to **verify** if the  data was received via email. You could also verify the studio console to check if you received a message from the Logger Component as follows:
        
        INFO  2014-07-03 16:10:00,974 [[scatter-gather-master].ScatterGatherWorkManager.01] org.mule.api.processor.LoggerMessageProcessor: Processing finished: {b=4, a=3}
    

### Go Further

* Read more about the [SMTP Connector](http://www.mulesoft.org/documentation/display/current/SMTP+Transport+Reference)

* Read more about the [Scatter Gather Flow Control](http://www.mulesoft.org/documentation/display/current/Scatter-Gather)

* Check out this [blog](http://blogs.mulesoft.org/parallel-multicasting-simplified/) on Parallel Processing in Mule.



   
