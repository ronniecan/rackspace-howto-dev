---
node_id: 3133
title: Cloud Block Storage - Attaching vs. Mounting
permalink: article/cloud-block-storage-attaching-vs-mounting
type: article
created_date: '2012-10-22 05:21:42'
created_by: David Hendler
last_modified_date: '2015-01-23 21:1743'
last_modified_by: jered.heeschen
products: Cloud Block Storage
body_format: tinymce
---

In Cloud Block Storage you both attach and mount a Volume to a Server.
These terms might sound similar, so it can get confusing as to their
differences.

**Attach:** When you attach a Cloud Block Storage Volume to a server, a
logical connection is created from a Cloud Block Storage node to the
hypervisor hosting your cloud server. This is done over a network link
via the iSCSI protocol. The new Volume gets exposed as a virtual device
to the host. To your Cloud Server, the Volume appears as a new raw
storage device. Attaching a Cloud Block Storage Volume can be
accomplished via the API or through Control Panel.

 **Mount:** Mounting is generally done once a volume has been attached
and formatted for use by a computer&rsquo;s operating system. Mounting is the
process in which a user instructs the operating system how to logically
map the directory structure to a physical storage device. You can only
mount a volume through the computer's operating system.

 For more information on how to mount your volume, see Knowledge Center
article [Prepare Your
Volume](/knowledge_center/article/prepare-your-volume).

 
