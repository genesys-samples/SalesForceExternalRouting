---
title: "About Our Relationship with Salesforce"
chapter: true
weight: 20
---

<<<<<<< HEAD
# About our Relationship with Salesforce
With the introduction of Service Cloud Voice, some may see Genesys and Salesforce as competitors now. And honestly, in some cases, we do compete; but in MANY MANY more cases we are working together with Salesforce as the CRM and Genesys as the contact center. Genesys has 30+ years of experience in this space and it is what we do. Being a system of record is not one of our core capabilities. Instead, we prefer to invest all of our dollars into experience orchestration. With that being said, orhcestrating experiences almost always requires an integration with a system of record. After all, how can we deliver an exceptional experience without having data and insights into who this person is? Just like you don't make friends without showing an effort to get to know them, you don't make happy customers by guessing on how they want to be engaged and who they are. Since Salesforce is such a leader in the CRM space and we are a leader in the Contact Center space, we've always been very closely aligned. 
=======
# About our Relationship with SalesForce
With the introduction of Service Cloud Voice, some may see Genesys and SalesForce as competitors now. And honestly, in some cases, we do compete; but in MANY MANY more cases we are working together with SalesForce as the CRM and Genesys as the contact center. Genesys has 30+ years of experience in this space and it is what we do. Being a system of record is not one of our core capabilities. Instead, we prefer to invest all of our dollars into experience orchestration. With that being said, orchestrating experiences almost always requires an integration with a system of record. After all, how can we deliver an exceptional experience without having data and insights into who this person is? Just like you don't make friends without showing an effort to get to know them, you don't make happy customers by guessing on how they want to be engaged and who they are. Since SalesForce is such a leader in the CRM space and we are a leader in the Contact Center space, we've always been very closely aligned. 
>>>>>>> 6e4eaf433880daa4da65e31fc6c13080f7816b58

Don't believe me? Genesys recently raised $580 Million in Funding with Salesforce Ventures as the leader in funding. Now you tell me: why would Salesforce invest money into a competitor? The answer is... we aren't competitors really. We are most commonly strategically aligned. 

On top of that, Genesys is the only CCaaS provider participating in both the Cloud Information Model and Open Data Initiative. This shows our commitment to the free flow of of data between platforms and provides a mechanism to ensure compatability of all customer data with Salesforce applications yet to be built.

## The 3 Flavors of Genesys & Salesforce
### 1. Genesys Cloud for Salesforce CTI Integration

This integration utilizes the Salesforce Open CTI framework. This framework allows third party computer-telephony integration (CTI) systems to integrate and lay on top of SaleForce. You actually saw a screenshot of this in the previous chapter. Here is another screenshot as a reminder.
![CTI](/images/CTI.jpg)
The CTI is our most common form of integration and we have the most customers using it because it combines the key strengths of each platform. 
![Genesys Salesforce Strengths](/images/genesysSalesforceStrengths.jpg)
You might be wondering at this point, "since the Salesforce Open CTI framework is open, don't all CCaaS vendors use it?" For the most part, yes. We are not unique in the fact that we have a CTI integration with Salesforce. However, no CCaaS vendor provides a better all in one orchestration experience within Salesforce than Genesys. Due to our API first mind set, our integration comes with unparalled free flow of data between Salesforce and Genesys Cloud CX. Combine the fact that we are highly committed to free flow of data with our Salesforce integration and the fact that we are one of the most highly rated CCaaS solutions in the marketplace and you have a strong solution for Salesforce customers.

### 2. Genesys Cloud for Salesforce CTI integration for Voice and OmniChannel integration for Digital
Our second option here is a combination of the Genesys CTI tool that we just covered and Salesforce OmniChannel. We defined OmniChannel earlier in the workshop and this is actually what we are going to set up today. Essentially, this is an integration that allows Salesforce OmniChannel digital objects to route through the Genesys Cloud CX ACD engine. The voice channel is still handled the same way as described for the CTI integration. We'll dive deeper into how to configure and use this integration in todays workshop. 

### 3. Genesys Cloud for Salesforce BYOT (Service Cloud Voice)*
Our last option is our Service Cloud Voice integration, which actually uses a completely different framework from the CTI framework. This means it has a separate set of API's and capabilities. For further clarification, the Service Cloud Voice BYOT (Bring Your Own Telephony) framework is a framework that opens up telephony integrations from market leading telephony providers. Service Cloud Voice initially was rolled out in connection with Amazon Connect, but this framework opens up Service Cloud Voice to be integrated with any other partner telephony providers. One of the main differences that comes with Service Cloud Voice is the voice object. Now when an agent accepts a voice interaction, it will create a voice object and associate it to any contacts, accounts, cases or any other applicable records. All call controls and features are embedded into the page instead of a pop up.
![Voice Object](/images/voiceObject2.jpg)

*in beta as of the date of the author writing this
