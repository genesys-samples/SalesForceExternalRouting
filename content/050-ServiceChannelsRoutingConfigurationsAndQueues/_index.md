---
title: "Service Channels, Routing Configurations & Queues"
chapter: true
weight: 50
---

## Service Channels
Service channels will allow us to convert Salesforce objects into a work record. They also will let you manage sources of work and their priority compared to other work items. Once you create the service channels, you can then associate them with queues which will ultimately determine how work items are routed to your agents.

1. Navigate to the Salesforce Setup page
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box search for Service Channels
![Service Channels](/images/serviceChannels.jpg)
3. Click to create a new Service Channel
    - The only setting you should need to change is the Salesforce object. For this drop down, choose "Chat Transcript." 
    - Optional: You can check the box to "Minimize the Omni-Channel widget when work is accepted"
    - In the end, your settings should look something like this. 
    ![Service Channel Settings](/images/serviceChannelSettings.jpg)

## Routing Configurations
Routing configurations specify how work items are routed to agents. For example, you can define priority. An item routed through a routing configuration with higher priority than a different work item will be routed faster. You can also define the routing model that is used here, which will be important for us today. We are going to be using an external routing model since we are routing chats using Genesys Cloud CX. Follow along with these steps. 

1. Navigate to the Salesforce Setup page
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box, search for Routing Configurations
![Routing Config Search](/images/routingConfigSearch.jpg)
3. Click to create a new routing configuration
    - Edit the following settings: 
        - Give a descriptive routing configuration name
        - Set the routing priority to 1 (this will give this routing configuration the highest priority)
        - Change Routing Model to External Routing
        - Set the Units of Capacity to 1 
            - this means this work item will only take up one unit of capacity. In contrast, a case might be assigned a weight of 3 units of capacity. In this scenario, let's say an agents max capacity is 5. This means that they could handle 2 chats and 1 case (1+1+3=5).
        - In the end, your routing configuration settings should look like this:
            ![Routing Config Settings](/images/routingConfigSettings.jpg)

## Queues
A queue is a location where records can be routed to await processing by a group member. You can think of a queue like a line at the bank. At the end of the line, there are tellers that are waiting to handle your request. A queue in Salesforce also has members assigned to the queue who are waiting to handle the request once they are ready to be processed. Supervisors can monitor the performance of the queue and see how effeciently the members are handling the requests. Importantly to our scenario, queues get linked to a routing configuration. If you recall, our routing configuration used an External Routing method. This link between the Queue and the Routing Configuration is what will allow members of the queue in the Salesforce to be routed objects by Genesys Cloud CX. Follow along with these steps. 

1. Navigate to the Salesforce Setup page
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box, search for Queues
![Queue Search](/images/queueSearch.jpg)
3. Click to create a new queue
    - Edit the following settings
        - Give a descriptive label and queue name
        - For Routing configuration, search and select the routing configuration we made in the previous step
        - Under Supported Objects, move "Chat Transcript" to the Selected Objects side
        - Under Queue Members, Search based on Users and then add yourself and any other Salesforce users you like into the queue
        - Your settings should look like this
        ![Queue Setting 1](/images/queueSetting1.jpg)
        ![Queue Setting 2](/images/queueSetting2.jpg)



