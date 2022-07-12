---
title: "Omni-Channel Flow"
chapter: true
weight: 60
---

# Omni-Channel Flow
Omni-Channel Flows can be launched when a customer initiates a chat, voice, or messaging conversation from SalesForce. This Omni-Channel flow is what will create the external routing request thus triggering the SalesForce interaction to route through the Message flow we set up in Architect over in Genesys Cloud CX. Let's set that up for your instance now. 

## Create the Omni-Channel Flow
1. In SalesForce, navigate to the setup portal. 
![SF Setup](/images/SFSetup.jpg)
2. In the quick find box, search for Flows.
![Flows](/images/flows.jpg)
3. Click to create a new flow. Then click on the "All + Templates" tab and then the Omni-Channel Flow tab. Choose the default Omni-Channel Flow and click Create.
![Create Flow](/images/createFlow.jpg)
4. In the toolbox, click Manager and then New Resource.
    - the new resource type will be of variable
    - for the API name, enter recordId (it must be this name specifically)
    - for Data type, choose Text
    - mark it for availability for use outside of the flow
    ![Record Id](/images/recordId.jpg)
5. Once again, in the tooblox click Manager and then New Resource. 
    - this new resource type will also be of variable
    - for the API name, enter input_record
    - for Data type, choose Record
    - for Object, choose Chat Transcript
    - mark it for availability for use outside of the flow
    ![Input Record](/images/input_Record.jpg)
6. In the graphical interface, press the + sign to add a new element in between the Omni-Channel Flow Start and the End. Choose Route Work as the element.
![Route Work](/images/routeWork.jpg)
7. When configuring the Route Work action, input the following values:
    - The label and API name can be anything descriptive that you want. You could even just make it "Route Work."
    - Under Set Input Values and Record ID, choose the recordId variable that you created
    - Under Set Input Values and Service Channel, choose the Service Channel that you created previously
    - For route to, select Queue 
    - When selecting a queue, choose the Queue that you set up previously
    - Then click done
    ![Route Work Config](/images/routeWorkConfig.jpg)
8. Now we are going to create another element right after the Route Work Element we just created. This element will be a Create Records element
![Create Records](/images/createRecords.jpg)
9. When creating the Create Records action, input the following values: 
    - The label and API name can be anything descriptive that you want. You could even just make it "External Routing Request"
    - For How Many Records to Create, just choose One
    - Under How to Set the Record Fields, choose "Use separate resources, and literal values"
    - From the object list, choose External Routing Request
    - Under Set Field Values for External Routing Request, we are going to set 2 fields. 
        1. Open_Messaging_Integration__c - Set the value to the Open Messaging integration platform that you set up earlier from the picklist
        2. Work_Item_ID__c - set the value to the recordId variable that we created earlier
    - Then click done
        ![Create Record Config](/images/createRecordConfig.jpg)
10. Finally, click Save and then click Activate

If you want to watch a video of these steps, you can view that here. https://youtu.be/Of6BkfCdgJ0 

## Activate the Request Deletion flow

