# PO-Bill-Receive
To automatically create bills and purchase receives for a purchase order
# Steps

# 1. Create custom function
Navigate to Settings >> Automation >> Custom Functions >> + New Custom Function.

Name the Custom function and choose the module as Purchase Order.

Copy and paste the script.

# 2. Create connection 
Click on the "Connections" button above the Deluge script section on the top right side.

It will open up Connections Section. Click on "+Add connection".

Scroll down Pick Your Service section and click on Zoho Inventory.

Provide the Connection Name as zom and Give Connection Link name as zom as well.

Also Uncheck the box "Use credentials of Login User".

Under Scopes select ZohoInventory.FullAccess.all

Click Create and Connect, it redirects to a pop up window. Click on Proceed.

Click Accept in the next window and Connection created successfully message will be shown.

# 3. Create workflow
Navigate to Settings >> Automation >> Workflow Rules >> + New Workflow Rule.

Name your workflow rule and choose the module as Purchase Order.

Choose workflow type as Event based When a Purchase Order is : Created or Edited and execute the workflow when : When any field is updated.

Filter the triggers - When - Purchase Receive Status - is - Issued

Just once or everytime? - Just Once.

Choose the appropriate custom function under immediate Actions and save the workflow.

Every time a Purchase Order is changed to issued status, a bill and a purchase receive will get recorded automatically against that purchase order.
