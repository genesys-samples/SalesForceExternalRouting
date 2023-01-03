---
title: "Testing"
chapter: true
weight: 90
---

Congrats! At this point, you've configured the external routing of Salesforce chats through the Genesys Cloud CX routing engine. Now what we need to do is find a way to test and make sure everything is working as we expect it to. For the following instructions, I am going to assume that you don't have your own website; however, if you do have your own website and wish to test on the website you can simply copy and paste the chat button code in the area on the page where you want the button to appear.
![Chat Button Code](/images/chatButtonCode.jpg)


Follow the following steps to test without the use of your own website: 
1. In Salesforce, navigate to the setup portal. 
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
6. Navigate back to the Setup page (easiest to do this in a separate tab)
7. Search for "Embedded Service Deployments" and click to create a new one
8. Choose Embedded Chat and click next. Then give a descriptive name and select the site you just created as the endpoint
![Embedded Service Deployment](/images/embeddedServiceDeployment.jpg)
9. Back on the Experience Builder page, click on Components and then select the Embedded Service Chat. You can drag this component anywhere on the website.
![Embedded Service Chat](/images/embeddedServiceChat.jpg)
7. Some configuration fields will open when you drag the Embedded Service Chat component on the screen. Under Chat Deployment, select the embedded service deployment you created from the drop down list. You can edit whatever else you like, but that is the only one that is required.
![Chat Deployment](/images/chatDeployment.jpg)
8. You now should see a widget in bottom right side of screen that either says Agent Offline or Chat with an Expert
![Salesforce Widget](/images/SFWidget.jpg)
9. We now need to get rid of some CSP security settings. On the left side click on the settings icon and then Security and Privacy. 
10. Under Content Security Policy, change it to Relaxed CSP. If there is anything under CSP Errors, click allow.
![CSP Settings](/images/CSPSettings.jpg)
11. In the top right hand side of the screen, click on preview
12. If your widget says Agent Offline, open up a new tab and navigate to the Console where you have the Omni-Channel widget deployed. Turn your Omni-Channel status to Available.
![Omni-Channel Status](/images/Omni-ChannelStatus.jpg)
13. Lastly, navigate back to the Experience Builder website and then you may need to refresh your screen. Once your widget says Chat with an Expert, you can click that and fill out the form
    - hint: if you fill out the form with an email & name that matches a Contact in your Salesforce account, the chat will be automatically associated with that account
    ![Chat Widget](/images/chatWidget.jpg)
14. Back from your Salesforce console, you can accept the chat from the Genesys CTI tool which will then trigger Omni-Channel to create a Chat object through Omni-Channel
![Handle Chat](/images/handleChat.jpg)

