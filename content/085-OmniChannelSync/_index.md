---
title: "OmniChannel Sync"
chapter: true
weight: 85
---
In this workshop today, it's important to know that we now have a scenario where agents could be handling either Genesys Cloud CX interactions or SalesForce interactions that are routed through Genesys Cloud CX. Because of that fact, it means that agents have 2 separate applications where their presences are set: Genesys Cloud CX and SalesForce OmniChannel. These presences are necessary for routing and thus we need a smooth sync between the presences. Luckily, the Genesys Cloud for SalesForce package makes that very easy to manage. 

1. In SalesForce, navigate to the setup portal. 
![SF Setup](/images/SFSetup.jpg)
2. Search for Installed Packages
3. Find the Genesys Cloud for SalesForce package and click configure (this is NOT the external routing package we installed earlier, having this package installed was listed in our prerequisites)
![Configure Package](/images/configurePackage.jpg)
4. Under Choose a Call Center, choose the Lightning option
5. Navigate to the section titled "Omni-Channel Sync Settings" and click the box to Enable Omni-Channel Sync
6. Update the settings to match what you see in the picture below
    - optionally, if you have custom statuses in SalesForce you wish to use, you could use those as well.
![Sync Settings](/images/syncSettings.jpg)

Do keep in mind that if you wish to edit the sync statuses to work differently you can. You can always come back here and edit them later. You are now ready to move on to test what we've built! 