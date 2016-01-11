---
node_id: 1529
title: Rackspace Name Servers
permalink: article/rackspace-name-servers
type: article
created_date: '2012-07-24 00:56:30'
created_by: RackKCAdmin
last_modified_date: '2014-02-11 15:1221'
last_modified_by: ross.diaz
products: Cloud Servers
body_format: tinymce
---

What Is a Name Server?
----------------------

A name server is part of the Domain Name System (DNS) that translates a
human readable domain name (such as rackspace.com) into its
corresponding IP address. This information is reported up a hierarchical
chain of name servers that store the domain-to-IP mappings in a
directory. When you request a website by entering the domain name in
your browser, this high level directory is queried and communicates with
other name servers in the hierarchy to find the IP address that matches
the domain you requested. To host your domain on a Rackspace Cloud
Server, you'll need to update your domain with the names of the
Rackspace name servers so that the DNS system knows where to locate the
new IP address for your domain.

The Rackspace Name Servers
--------------------------

The Rackspace name servers are:

-   **dns1.stabletransit.com**
-   **dns2.stabletransit.com**

Using the Rackspace Name Servers
--------------------------------

If you have an existing domain that is already registered with another
service provider and you want to host it from your Rackspace Cloud
Server, contact the domain registrar to change the name servers to the
Rackspace name servers. This DNS change is typically propagated to the
internet within 48 hours. During this 48 hour period, we highly
recommend that you not make any further DNS changes. If you must make
changes during this time, the changes must be made on both sets of DNS
servers. Failure to update both servers will cause random
inconsistencies.

Finding Your Current Name Servers
---------------------------------

If you don't know your current name servers, a
[WHOIS](http://whois.domaintools.com/ "http://whois.domaintools.com")
search can provide this information.

**Note**: Rackspace is *not* a domain registrar such
as [Namecheap](http://www.namecheap.com/), [Dreamhost](http://dreamhost.com/domains/),
or [GoDaddy](http://www.godaddy.com/). The only time that Rackspace
serves as a domain registrar is if you are using our [Cloud
Sites](http://www.rackspace.com/cloud/cloud_hosting_products/sites/ "http://www.rackspace.com/cloud/cloud_hosting_products/sites/")
service. To host a domain that you have registered on your Rackspace
Cloud Server, go to your domain registrar and [set the nameservers to
Rackspace's
nameservers](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-6-transferring-your-domain-to-be-served-from-rackspace-cloud).
This will allow DNS to route to your domain hosted on your Cloud Server.

### Related Information

[Transferring Your
Domain](http://www.rackspace.com/knowledge_center/node/2345 "Transferring Your Domain")
[Learn More About
DNS](http://www.rackspace.com/knowledge_center/article/dns-creating-a-dns-record-for-cloud-servers "Learn More About DNS")
