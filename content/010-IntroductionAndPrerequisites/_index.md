---
title: "Introduction and Prerequisites"
chapter: true
weight: 10
---

# Todays Learning Agenda
1. The Genesys and SalesForce partnership
2. How to install, configure, and test the routing of a SalesForce Chat through the Genesys Cloud CX routing engine
3. How to set up the OmniChannel presence sync with Genesys Cloud CX

# Prerequisites
1. Genesys Cloud CX account with adminstrator access 
2. SalesForce account with adminstrator access
3. Install the Genesys Cloud for SalesForce Managed Package
    - https://help.mypurecloud.com/articles/install-or-upgrade-the-genesys-cloud-for-salesforce-managed-package/
4. SalesForce Agent role assigned to user in Genesys Cloud CX
5. Familiarity with Service Cloud Voice is recommended

A combination of Genesys and SalesForce is a powerful duo. It combines Genesys, a world class system of engagement, with SalesForce, a world class system of record. Today, we will focus specifically on how to integrate SalesForce OmniChannel with the Genesys Cloud CX routing engine. But what is OmniChannel? 

OmniChannel is a SalesForce Servcice Cloud feature. It allows customers to communicate with agents working in SalesForce via almost any channel (SMS, web chat, Facebook, etc), as implied in the name. If you are familiar with Genesys, you might be thinking "but wait, Genesys can provide the same functionality?" You would be correct, but there are some scenarios where businesses might prefer to route SalesForce OmniChannel items through Genesys Cloud CX for our robust routing capabilities. Let's unpack that, and let's start with the differences in the user interface for an agent working in SalesForce.

#### Genesys Cloud CX Objects User Experience
![Genesys Chat UI](/images/genesysChatUI.jpg)
Here you can see that the agents handle the text based interactions in a pop up widget named "GenesysCloudInteractionUtility." All functionality here is Genesys: a Genesys chat routing through Architect into a Genesys queue.

#### SalesForce OmniChannel Objects User Experience
![OmniChannel Chat UI](/images/omniChannelChatUI.jpg)
With the OmniChannel integration, the user experience for agents is more embedded in the page. You can see that when a chat is matched to a contact, it creates a new Chat object in SalesForce and associates that with a contact. The agent can then respond to the chat without the need for any kind of pop up widget. Here the functionality is split between SalesForce and Genesys: the chat itself is SalesForce, but the routing is done by Genesys.

#### Other Scenarios Where Businesses Might Gravitate towards a Genesys Cloud and OmniChannel Integration Approach
1. The business already uses OmniChannel for digital and is happy with it but is looking for a more enterprise level Contact Center
2. Business wants to take advantage of SalesForce einstein Knowledge management capabilities with OmniChannel
3. Business wants to take advantage of Genesys Outbound campaigns inside SalesForce alongside OmniChannel for digital inbound interactions
4. Every business is unique, so there could and will be other scenarios that are not listed here

