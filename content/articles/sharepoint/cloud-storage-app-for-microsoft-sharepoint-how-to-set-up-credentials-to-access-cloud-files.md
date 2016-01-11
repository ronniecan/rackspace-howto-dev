---
node_id: 3505
title: 'Cloud Storage App for Microsoft SharePoint: How to Set Up Credentials to Access Cloud Files'
permalink: article/cloud-storage-app-for-microsoft-sharepoint-how-to-set-up-credentials-to-access-cloud-files
type: article
created_date: '2013-06-04 22:13:48'
created_by: rose.contreras
last_modified_date: '2016-01-04 17:5435'
last_modified_by: kyle.laffoon
products: Sharepoint
body_format: tinymce
---

### Previous section

[Cloud Storage App for Microsoft SharePoint:
Overview](https://www.rackspace.com/knowledge_center/article/cloud-storage-app-for-microsoft-sharepoint-overview)

The first time that you access Rackspace Cloud Storage App for
*Microsoft SharePoint*, and every time that you want to log back in
after logging out, you are prompted to provide credentials for your
Rackspace Cloud Files account. In order for the app to access your Cloud
Files account, you must assign it some credentials and a metadata key
that has access to Cloud Files. The metadata key is required to support
the generation of temporary URLs. You can provide the credentials and
metadata key in one of the following ways:

-   If you have not previously used other applications to access Cloud
    Files, [create a new account](#createnew).
-   If you already use other applications to access Cloud Files, [use an
    existing account](#specify).

Create a new account
--------------------

In the Create New Account form (shown in the following figure), provide
credentials for a new user, and provide a metadata key. The app creates
the user and sets the metadata key for your Cloud Files account. The
user's credentials are saved and used to access Cloud Files.

The values that you specify at the top of the form (user name, password,
and email address) are the attributes associated with the newly created
user, and the metadata key is assigned to your Cloud Files account. The
fields at the bottom of the form (in the dark gray box) are the
credentials that the app uses to create the new user and set the
metadata key. The app does not retain these credentials. They are
typically the credentials that you use to log in to the [Rackspace Cloud
Control Panel](https://mycloud.rackspace.com).

![](/knowledge_center/sites/default/files/field/image/Fig%20--%20Create%20New%20Account_0.jpg)

Specify an existing user
------------------------

If you already use other applications to connect to your Cloud Files
account via the REST APIs, then you do not want to change your metadata
key, and you might already have created an API-specific user for the
other applications. In this scenario, provide credentials directly to
the app.

At the top of the Create New Account form, click the **Already have an
account?** link. In the Account Info form (shown in the following
figure), specify the user name, password, and metadata key for the
existing account. The app saves these credentials and uses them to
access the Cloud Files APIs.

![](/knowledge_center/sites/default/files/field/image/Fig%20--%20Use%20Existing%20Account_0.jpg)

Where to go from here
---------------------

After you set up the credentials, you can start using the app. The
information in the next article, [How to Access Cloud Files
Containers](http://www.rackspace.com/knowledge_center/article/cloud-storage-app-for-microsoft-sharepoint-accessing-cloud-files-containers),
provides details on accessing files in the Cloud Storage app.
