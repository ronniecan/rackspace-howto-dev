---
node_id: 4244
title: Rackspace Private Cloud Spheres of Support
permalink: article/rackspace-private-cloud-spheres-of-support
type: article
created_date: '2014-09-19 15:34:12'
created_by: Karin Levenstein
last_modified_date: '2016-01-04 16:1720'
last_modified_by: kyle.laffoon
products: Rackspace Private Cloud - OpenStack
body_format: tinymce
---

### Previous Section

[Getting Started with Rackspace Private Cloud -
OpenStack](https://www.rackspace.com/knowledge_center/getting-started/rackspace-private-cloud-openstack)

 

Rackspace Private Cloud is Rackspace&rsquo;s architecture for and support of a
production-ready, scalable, OpenStack based private cloud. To ensure
fanatical support, Rackspace provides support for specific server
configurations and OpenStack projects in Rackspace Private Cloud v9 and
v10.

This document describes what is and is not supported in Rackspace
Private Cloud v9 and v10.

Operating systems
-----------------

Rackspace Private Cloud v9 and v10 support Ubuntu 14.04 LTS (Trusty
Tahr) 64-bit server edition, with with Linux kernel version
3.13.0-34-generic or later. Only OpenStack API clients are supported.

Rackspace does not support the contents of user VMs and will not manage
the VMs once they are running. We do not support clients on Windows.

Web and database servers
------------------------

Rackspace Private Cloud uses Apache for its web server, and MariaDB +
Galera for its database server. No other web and database servers are
supported

Intended capabilities of Rackspace Private Cloud
------------------------------------------------

Feature

Description

Rackspace DC

Customer DC

**Monitoring**

Hardware, Compute/Disk/Memory, OpenStack Services

Yes

-   OpenStack services
-   CPU/Disk/Memory Utilization only

**Manual Patching Processes**

Host OS

Yes

Yes

**Multi-Region Support**

Hosting components over multiple data centers

Yes

No

**OpenStack Endpoint SSL (Ingress)**

Encryption of all API calls

Yes - With SSL termination at a physical load balancer.

Yes - With SSL termination at a physical load balancer.

**Encryption of all management traffic**

Encrypting management traffic in addition to the API call encryption

No

No

**Disaster Recovery**

Recovery from Data Center failures or "Acts of God"

No

No

**Deploy from mirror**

Deploy RPC from an off-line local repository

N/A

No

**Customer images**

Reference glance images provided

-   CentOS 6 and 7
-   Ubuntu 12.04 LTS, 14.04 LTS, 14.10
-   Windows 2012R2 Datacenter
-   Red Hat Enterprise Linux: Contact Red Hat for availability of images
    and licensing

-   CentOS 6 and 7
-   Ubuntu 12.04 LTS, 14.04 LTS, 14.10
-   Red Hat Enterprise Linux: Contact Red Hat for availability of images
    and licensing

OpenStack Features
------------------

 

**Installation**

Configuration

Troubleshooting

Monitoring

Patching

**Nova Compute**

Yes

Yes

Yes

Yes

Yes

**Glance Image Service**

Yes

Yes

Yes

Yes

Yes

**Keystone Identity Service**

Yes

Yes

Yes

Yes

Yes

**Swift Object Store**

v10 only

v10 only

v10 only

v10 only

v10 only

**Cinder Block Storage**

Yes

Yes

Yes

Yes

Yes

**Neutron Networking**

Yes

Yes

Yes

Yes

Yes

**nova-network**

No

No

No

No

No

**Horizon Dashboard**

Yes

Yes

Yes

Yes

Yes

**Ceilometer Telemetry**

No

No

No

No

No

**Heat Orchestration**

Yes

Yes

Yes

Yes

Yes

 

### Next section

[Private Cloud Tech
Resources](http://www.rackspace.com/knowledge_center/article/private-cloud-tech-resources)
