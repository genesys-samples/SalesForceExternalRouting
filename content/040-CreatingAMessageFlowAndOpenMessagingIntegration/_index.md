---
title: "Creating a Message Flow and Open Messaging Integration"
chapter: true
weight: 40
---

A Message Flow and Open Messaging integration is how Genesys can provide routing capabilities, self service options, data lookups through integrations and much more. The Message Flow is controlled from Architect, and if you are familiar with Genesys Cloud CX, you are likely familiar with Architect. Architect is a self service Interactive Response builder for all channels in Genesys Cloud CX; whether that be voice, email, chat, message, bot building, etc. The Open Messaging integration is the endpoint that facilitates messaging with 3rd party systems and external messaging services. In this scenario, that external messaging service with be Salesforce OmniChannel.

## Creating a Message Flow and Open Messaging Integration
1. Before we dive into Architect, ensure that your user in Genesys Cloud CX is a part of a queue. If not, follow these instructions to create a new queue and add your user as a member.
    - https://help.mypurecloud.com/articles/create-queues/
2. In Genesys Cloud CX Admin, find Architect and navigate to it. Inside of Architect, from the list of flows select Inbound Message.
![Inbound Message](/images/inboundMessage.jpg)
3. Click Add to create a new flow, and give it a descriptive name
    - Optionally, if you already have a flow you'd like to use, you can skip ahead to Step 6.
    ![Create Inbound Flow](/images/createInboundFlow.jpg)
4. In the Initial State, drag a Transfer to ACD option under the start point. In the options that populate on the right, choose your queue from the drop down list.
    - Optionally, if you are familiar with Architect and want to add your own logic, you can do so now.
    ![Transfer to ACD](/images/transferToACD.jpg)
5. Press publish.
6. Navigate back to the Genesys Cloud CX Admin page and find Platforms under the Message container.
![Platforms](/images/platforms.jpg)
7. Click to create a new integration and choose Open Messaging as the type.
![Open Messaging](/images/openMessaging.jpg)
8. Give the Open Messaging integration a descriptive name. For the outbound notification webhook URL, it does not matter what you put here. You can actually simply put https://whatever.com and then the Outbound Notification Webhook Signature Secret Token needs you to put a value but the value will not matter. You can simply put "123". Then press save. This is a prepackaged integration we have with Salesforce, so these fields are not really used.
![Open Messaging Config](/images/openMessagingConfig.jpg)
9. Now navigate back to the Genesys Cloud CX Admin console and then search for Message Routing
![Message Routing](/images/messageRouting.jpg)
10. Open up Message Routing and then click in the top right corner to create a new message route
11. For the Flow option, choose the message flow that you created earlier. And for the address, choose the platform that you just created. Once, you've done this, you are ready to sync your changes over to Salesforce!
![Message Route](/images/messageRoute.jpg)


## Syncing your Changes over to Salesforce
1. In Salesforce, click on Setup
![SF Setup](/images/SFSetup.jpg)
2. Search for Installed Packages
3. On this page, locate the Genesys Cloud CX for Salesforce External Routing package and click Configure
![Package Configure](/images/packageConfigure.jpg)
4. Lastly, press Retrieve Options. This will query your Genesys Cloud CX account for queues and messaging integrations to sync over into your Salesforce instance. We will then be able to use the queue and message integration that you created for setting up external routing within Salesforce.
![Retrieve Options](/images/retrieveOptions.jpg)
