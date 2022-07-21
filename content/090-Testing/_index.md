---
title: "Testing"
chapter: true
weight: 90
---

Congrats! At this point, you've configured the external routing of SalesForce chats through the Genesys Cloud CX routing engine. Now what we need to do is find a way to test and make sure everything is working as we expect it to. For the following instructions, I am going to assume that you don't have your own website; however, if you do have your own website and wish to test on the website you can simply copy and paste the chat button code in the area on the page where you want the button to appear.
![Chat Button Code](/images/chatButtonCode.jpg)

If you wish to test without using your own website, follow these steps: 
1. In SalesForce, navigate to the setup portal. 
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box, search and select All Sites under Digital Experiences
![All Sites](/images/allSites.jpg)
3. Click to create a New site.
4. Choose any template. I like the Help Center template personally. 
    - Navigate through the config options
    - Give the site a name & URL
    - These settings don't matter too much. Just click through the wizard to create the site and press finish
5. Once your site is created, click on Builder to edit your website.
![Builder](/images/builder.jpg)
6. On the Experience Builder page, click on Components and then select the Embedded Service Chat. You can drag this component anywhere on the website.
![Embedded Service Chat](/images/embeddedServiceChat.jpg)
7. Some configuration fields will open when you drag the Embedded Service Chat component on the screen. Under Chat Deployment, select the chat button you created from the drop down list. You can edit whatever else you like, but that is the only one that is required.
![Chat Deployment](/images/chatDeployment.jpg)
8. You now should see a widget in bottom right side of screen...

