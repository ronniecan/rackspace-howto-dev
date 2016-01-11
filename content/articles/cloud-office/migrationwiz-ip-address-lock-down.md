---
node_id: 3800
title: Locking Down IP Addresses in MigrationWiz
permalink: article/migrationwiz-ip-address-lock-down
type: article
created_date: '2013-12-04 18:56:15'
created_by: milton.prado
last_modified_date: '2013-12-11 21:5026'
last_modified_by: kyle.laffoon
products: Cloud Office
body_format: tinymce
---

When performing an email migration, some customers might need to
restrict access to a defined set of IP addresses, typically for security
reasons.  This article provides the range of IP addresses from which our
MigrationWiz tool can connect, and instructions on locking down your
migration to only these specific IP addresses.  

Note: Due to the restricted IP range, migration speeds are not optimal. 
Consider this when planning your migration timeline.  

### IP Address Ranges

-   192.34.111.0 to 192.34.111.63 (aka 192.34.111.0/26) new
-   208.115.102.1 to 208.115.102.63 (aka 208.115.102.1/26)
-   198.104.255.65 to 198.104.255.126 (aka 198.104.255.64/26)
-   4.53.159.1 to 4.53.159.126 (aka 4.53.159.0/25)
-   216.176.189.162 to 216.176.189.188
-   198.104.202.70
-   4.53.158.186

### To Lock Down Your Migration Profile

Now that you have the range of IP addresses, you need to lock down your
migration profile.  If your migration is assisted, your migration
specialist performs these actions.  If you are performing the migration
yourself, complete the following steps.

1. Log in to the [Full Version of
MigrationWiz](http://www.rackspace.com/knowledge_center/article/accessing-the-full-version-of-migrationwiz).

2. If you have already created a migration, click **Manage
Connectors**. If you are creating a new migration, click **Create a
 Connector**.

![](/knowledge_center/sites/default/files/field/image/Step_1.png)

 

3. In the top-right corner of the window that opens, click **Advanced
Options**.

![](/knowledge_center/sites/default/files/field/image/advanced.png)

 

4. Click the **Performance** tab.

![](/knowledge_center/sites/default/files/field/image/Step_3.png)

 

5. Set the **Preferred Data Center** value to **North America**.

![](/knowledge_center/sites/default/files/field/image/Step_4.png)

 

6. Click on the **Support** tab and type the following in the blank
field:  **ProcessingRequirement=Local**

![](/knowledge_center/sites/default/files/field/image/Step_5.png)

 

7. **Save** all changes

All connections through your migration will now only come from the IP
ranges listed in this article. 

 

 

 
