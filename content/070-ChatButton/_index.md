---
title: "Chat Button"
chapter: true
weight: 70
---

Chat buttons in Salesforce let you specify how incoming chat requests are directed to agents. These are similar to Genesys chat widgets if you are familiar with those. These are literally the buttons that visitors click to initiate a chat when visiting your website. A button consists of several lines of JavaScript that you can copy and paste into web pages on your website.

## Create a Chat Button
1. In Salesforce, navigate to the setup portal. 
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box, search and select Chat Buttons & Invitations
3. Click to create a new chat button and follow along with the following configuration components
    - For the type, choose Chat Button
    - Give a descriptive Name
    - Under Routing Information, set the Routing Type as Omni-Channel
    - Check the box to "Use a flow for routing"
    - In the Omni-Channel Flow box, search and find the flow that we created at the beginning of the workshop
    - Search and select your queue that we created in the workshop
    - Check the box to "Enable queue"
    - Set Queue Size Per Agent to 5 (You could change this number later if you want)
    - Press save. Your configuration should look something like this: 
    ![Chat Button Config](/images/chatButtonConfig.jpg)