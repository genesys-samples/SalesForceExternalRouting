---
title: "Introduction and Prerequisites"
chapter: true
weight: 10
---

# Todays Learning Agenda
1. The Genesys and Salesforce partnership
2. How to install, configure, and test the routing of a Salesforce Chat through the Genesys Cloud CX CX routing engine
3. How to set up the OmniChannel presence sync with Genesys Cloud CX CX

# Prerequisites
1. Genesys Cloud CX CX account with adminstrator access 
2. Salesforce account with adminstrator access
3. Install the Genesys Cloud CX for Salesforce Managed Package
    - https://help.mypurecloud.com/articles/install-or-upgrade-the-genesys-cloud-for-Salesforce-managed-package/
4. Salesforce Agent role assigned to user in Genesys Cloud CX CX

A combination of Genesys and Salesforce is a powerful duo. It combines Genesys, a world class system of engagement, with Salesforce, a world class system of record. Today, we will focus specifically on how to integrate Salesforce OmniChannel with the Genesys Cloud CX CX routing engine. But what is OmniChannel? 

<<<<<<< HEAD
OmniChannel is a Salesforce Servcice Cloud feature. It allows customers to communicate with agents working in Salesforce via almost any channel (SMS, web chat, Facebook, etc), as implied in the name. If you are familiar with Genesys, you might be thinking "but wait, Genesys can provide the same functionality?" You would be correct, but there are some scenarios where businesses might prefer to route Salesforce OmniChannel items through Genesys Cloud CX CX for our robust routing capabilities. Let's unpack that, and let's start with the differences in the user interface for an agent working in Salesforce.
=======
OmniChannel is a SalesForce Service Cloud feature. It allows customers to communicate with agents working in SalesForce via almost any channel (SMS, web chat, Facebook, etc), as implied in the name. If you are familiar with Genesys, you might be thinking "but wait, Genesys can provide the same functionality?" You would be correct, but there are some scenarios where businesses might prefer to route SalesForce OmniChannel items through Genesys Cloud CX CX for our robust routing capabilities. Let's unpack that, and let's start with the differences in the user interface for an agent working in SalesForce.
>>>>>>> 6e4eaf433880daa4da65e31fc6c13080f7816b58

#### Genesys Cloud CX CX Objects User Experience
![Genesys Chat UI](/images/genesysChatUI.jpg)
Here you can see that the agents handle the text based interactions in a pop up widget named "GenesysCloudInteractionUtility." All functionality here is Genesys: a Genesys chat routing through Architect into a Genesys queue.

#### Salesforce OmniChannel Objects User Experience
![OmniChannel Chat UI](/images/omniChannelChatUI.jpg)
With the OmniChannel integration, the user experience for agents is more embedded in the page. You can see that when a chat is matched to a contact, it creates a new Chat object in Salesforce and associates that with a contact. The agent can then respond to the chat without the need for any kind of pop up widget. Here the functionality is split between Salesforce and Genesys: the chat itself is Salesforce, but the routing is done by Genesys.

#### Other Scenarios Where Businesses Might Gravitate towards a Genesys Cloud CX and OmniChannel Integration Approach
1. The business already uses OmniChannel for digital and is happy with it but is looking for a more enterprise level Contact Center
<<<<<<< HEAD
2. Business wants to take advantage of Salesforce einstein Knowledge management capabilities with OmniChannel
3. Business wants to take advantage of Genesys Outbound campaigns inside Salesforce alongside OmniChannel for digital inbound interactions
4. Every business is unique, so there could and will be other scenarios that are not listed here
=======
2. Business wants to take advantage of SalesForce einstein Knowledge management capabilities with OmniChannel
3. Business wants to take advantage of Genesys Outbound campaigns inside SalesForce alongside OmniChannel for digital inbound interactions
4. Every business is unique, so there will be other scenarios that are not listed here
>>>>>>> 6e4eaf433880daa4da65e31fc6c13080f7816b58

