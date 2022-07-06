---
title: "Service Channels, Routing Configurations & Queues"
chapter: true
weight: 50
---

## Service Channels
Service channels will allow us to convert SalesForce objects into a work record. They also will let you manage sources of work and their priority compared to other work items. Once you create the service channels, you can then associate them with queues which will ultimately determine how work items are routed to your agents.

1. Navigate to the SalesForce Setup page
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box search for Service Channels
![Service Channels](/images/serviceChannels.jpg)
3. Click to create a new Service Channel
    - The only setting you should need to change is the SalesForce object. For this drop down, choose "Chat Transcript." 
    - Optional: You can check the box to "Minimize the Omni-Channel widget when work is accepted"
    - In the end, your settings should look something like this. 
    ![Service Channel Settings](/images/serviceChannelSettings.jpg)