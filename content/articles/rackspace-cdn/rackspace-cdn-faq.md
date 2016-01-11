---
node_id: 4705
title: Rackspace CDN FAQ
permalink: article/rackspace-cdn-faq
type: article
created_date: '2015-06-08 21:09:39'
created_by: Rackspace Support
last_modified_date: '2015-12-16 22:2354'
last_modified_by: catherine.richardson
products: Rackspace CDN
body_format: tinymce
---

Get quick answers to common questions about the Rackspace CDN service.
If you have any questions about the terms used in this FAQ, see the
[Rackspace CDN
terminology](https://www.rackspace.com/knowledge_center/article/rackspace-cdn-terminology)
page.

-   [How does Rackspace CDN benefit my website or web
    application?](#benefit)
-   [How many edge servers does Rackspace CDN give me access
    to?](#howmany)
-   [Can I specify certain files for caching or create specific
    inclusions and exclusions?](#specify)
-   [How can I check the performance of my site?](#performance)
-   [Can I push content to the edge nodes before it's needed?](#push)
-   [How does origin pull work?](#originpull)
-   [Can content be pulled from anywhere, including sources external to
    Rackspace?](#pullanywhere)
-   [What are my options for service traffic over HTTPS?](#https)
-   [Is there a service level agreement (SLA) for Rackspace CDN?](#sla)
-   [Can you provide pricing information for Rackspace
    CDN?](#Pricing%20information)
-   [Is there a list of approved Certificate Authorities (CAs) for
    Rackspace CDN?](#certificate%20authorities)
-   [Will I be charged for edge node storage when I use Rackspace
    CDN?](#storagge)
-   [Does Rackspace CDN honor the Expires header value set by the origin
    server (web
    server)?](#Does%20Rackspace%20CDN%20honor%20the%20Expires%20header%20value%20set%20by%20the%20origin%20server%20(web%20server)?)
-   [What is cacheable content?](#What%20is%20cacheable%20content?)
-   [Does Rackspace CDN support
    SNI?](#Does%20Rackspace%20CDN%20support%20SNI?)
-   [Does Rackspace CDN have a free secure delivery
    option?](#Does%20Rackspace%20CDN%20have%20a%20free%20secure%20delivery%20option?)
-   [What is the process for requesting a dedicated
    certificate?](#What%20is%20the%20process%20for%20requesting%20a%20dedicated%20certificate?)
-   [What should customers expect after they provision a
    certificate?](#What%20should%20customers%20expect%20after%20they%20provision%20a%20certificate?)

 

* * * * *

###  

### How does Rackspace CDN benefit my website or web application?

Benefits include fast load times when serving your content, access
control, and origin protection. For detailed information, see [Features
of Rackspace
CDN](http://www.rackspace.com/knowledge_center/article/features-of-rackspace-cdn).

^[back\\ to\\ top](#top)^

### How many edge servers does Rackspace CDN give me access to?

When you use Rackspace CDN, you have access to over 230 edge nodes
(servers) around the world.   

^[back\\ to\\ top](#top)^

### Can I specify certain files for caching or create specific inclusions and exclusions?

Yes, you can set a time to live (TTL) of 0 on any content that you don't
want served from an edge node. You might choose to do this for dynamic
content that changes for every visitor.  

^[back\\ to\\ top](#top)^

### How can I check the performance of my site?

Many web browser plugins and tools are available. For example:

-   In Firefox, click **Tools** \> **Web Developer** \> **Network**.\
     If you don't see the **Tools** menu, press the **F10** key on your
    keyboard.
-   In Chrome, you can use the [Page load time
    plugin](https://chrome.google.com/webstore/detail/page-load-time/fploionmjgeclbkemipmkogoaohcdbig?hl=en)

Additionally, some customers use YSlow or Pingdom.

^[back\\ to\\ top](#top)^

### Can I push content to edge nodes before it's needed?

No. Rackspace CDN does not prepopulate the edge nodes. Content is copied
to the edge nodes only when it is requested.

^[back\\ to\\ top](#top)^

### How does origin pull work?

Rackspace CDN seamlessly and automatically fetches content from an
origin server and caches it at the edge location if the edge location
doesn&rsquo;t already have it.

^[back\\ to\\ top](#top)^

### Can content be pulled from anywhere, including sources external to Rackspace?

Yes. Rackspace CDN can pull content from any origin with a public IP
address or web address, including servers hosted in our public, private,
or dedicated infrastructures, as well as servers hosted offsite.

^[back\\ to\\ top](#top)^

### What are my options for serving traffic over HTTPS?

Rackspace CDN works with shared domain SSL, SSL SAN certificates, and
fully owned certificates. Our custom SSL options satisfy your security,
budget, and marketing requirements. Pricing for each option is
different.

^[back\\ to\\ top](#top)^

### Is there a service level agreement (SLA) for Rackspace CDN?

Yes. It is located at [Rackspace CDN
SLA](http://www.rackspace.com/information/legal/service-level-guarantee-rackspace-cdn).

^[back\\ to\\ top](#top)^

### Can you provide pricing information for Rackspace CDN?

See [Rackspace CDN
pricing](http://www.rackspace.com/cloud/cdn-content-delivery-network).

^[back\\ to\\ top](#top)^

### Is there a list of approved Certificate Authorities (CAs) for Rackspace CDN?

Yes. See [Rackspace CDN secure delivery
options](https://www.rackspace.com/knowledge_center/article/rackspace-cdn-secure-delivery-options#Secure%20origin).

^[back\\ to\\ top](#top)^

### Will I be charged for edge node storage when I use Rackspace CDN?

No. You are charged for storage on your origin server, but Rackspace CDN
does not charge for edge node storage on top of that.

^[back\\ to\\ top](#top)^

### Does Rackspace CDN honor the Expires header value set by the origin server (web server)?

If the content is cacheable and you have *not* set a time to live (TTL)
rule on the service, edge nodes honor the Expires or Cache Control
headers sent by the origin server. When a request is made to the origin
for content, the edge node looks for Expires or Cache Control headers in
the response sent by the origin. If these headers are present, the TTL
for that content matches the time referenced in the Expires or Cache
Control headers. If both Expires and Cache Control headers are present,
Cache Control takes precedence.

If the content is cacheable and you have set a TTL on the service, the
caching TTL is honored. The Cache Control and Expires headers are
ignored, and content is refreshed based on the TTL value that you set.
This rule applies only to content that matches the path specified in the
TTL rule. For example, if you have a TTL rule for the page
**/images/\***, then all Expires and Cache Control headers for content
that is *not* in the **images** directory is honored.

If the content is not cacheable, it is not cached on the edge nodes,
regardless of the origin headers.

**Note**: A default caching rule with a TTL of 1 day and a request\_url
of /\* is set for all content. You need to remove your default caching
in order to hone origin headers.

^[back\\ to\\ top](#top)^

### What is cacheable content?

Content with the following file extensions is cacheable:

aif, aiff, au, avi, bin, bmp, cab, carb, cct, cdf, class, css, doc, dcr,
dtd, exe, flv, gcf, gff, gif, grv, hdml, hqx, ico, ini, jpeg, jpg, js,
mov, mp3, nc, pct, pdf, png, ppc, pws, swa, swf, txt, vbs, w32, wav,
wbmp, wml, wmlc, wmls, wmlsc, xsd, zip, webp, jxr, hdp, wdp

^[back\\ to\\ top](#top)^

### Does Rackspace CDN support Service Name Indication (SNI)?

SNI is not currently supported.

^[back\\ to\\ top](#top)^

### Does Rackspace CDN have a free secure delivery option?

Yes, customers who use the shared Rackspace domain will not be charged
any certificate fees.

^[back\\ to\\ top](#top)^

### What is the process for requesting a dedicated certificate?

Customers need to submit a ticket from the Control Panel with their
domain details and Rackspace Support will reach out to them.

^[back\\ to\\ top](#top)^

### What should customers expect after they provision a certificate?

The administrator for the domain will be contacted by GeoTrust to verify
the domain. It is critical that customers respond to this verification
request. Certificates will not be provisioned until it is complete.

^[back\\ to\\ top](#top)^
