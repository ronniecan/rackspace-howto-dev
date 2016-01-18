---
node_id: 3424
title: Installing PHP on Windows Server 2012
type: article
created_date: '2013-04-22'
created_by: Rackspace Support
last_modified_date: '2016-01-14'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
body_format: tinymce
---

<span>Description</span>
------------------------

This article will detail installing, testing, and configuring PHP on the
Windows Server 2012. This article will use the Microsoft Web Platform
Installer (Web PI) method of installation. It will not cover the use
case of installing PHP from source.

Requirements
------------

Successfully installing PHP on a Windows Server 2012 requires a prior
installation of the IIS framework.

Contents
--------

-   <span>[Installing PHP with Web PI](#phpwebpi)</span>
-   [<span>Testing PHP</span>](#testphp)
-   [<span>Configuring PHP</span>](#extendphp)

[]()Installing PHP with Web PI
------------------------------

1\. Open the Web PI application from the following location on your
filesystem.

    C:\Program Files\Microsoft\Web Platform Installer\WebPlatformInstaller.exe

*Note: If the Web PI application is not currently installed it can be
downloaded via the following link: [Web
PI](http://www.microsoft.com/web/downloads/platform.aspx)*

2\. Search for PHP.

3\. Select **Add** next to the version of PHP you wish to install and
click **Install**.

*Note: At the time of writing this is 5.3.19 and 5.4.9*

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/php_webpi.png" width="854" height="584" />

4\. When prompted to Accept the License terms, review and click **I
Accept**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/php_dependecies.png" width="854" height="585" />

5\. Click **Finish** once the installation is finalized. The PHP runtime
environment will be stored on your local file system at the following
location:

    C:\Program Files (x86)\PHP\%version

[]()[]()Testing PHP
-------------------

Once you have successfully installed PHP you can test its functionality
with a few simple steps.

1\. Create a file using a texteditor and insert the following code
snippit.

    <?php phpinfo(); ?>

2. <span>This code, when run, presents detailed information about the
current PHP configuration of the local system.</span><span> Save the
file as 'info.php' in the IIS root directory.</span>

*<span>Note: The default directory is </span>C:\\inetpub\\wwwroot*

3\. Open a Web browser and go to the following URL:

    http://localhost/info.php

With PHP successfully installed a screen will be presented detailing the
PHP configuration.

*Note: This information can harmful in the wrong hands so please delete
or move the info.php file once the installation is successfully tested.*

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/php_info.png" width="861" height="611" />

Customizing PHP
---------------

Configuration parameters for PHP are stored in the php.ini file, which
resides in the root of the local installation.

1\. Open File Explorer and path to the PHP configuration (php.ini) file.

*Note: The currently loaded configuration file can be found by
leveraging the phpinfo(); script in the [Testing PHP](#testphp)section*

2\. Open the file with text editor and perform any necessary
modifications.

Note: E<span>xplaining the php directives that can be modified is beyond
the scope of this article. Those seeking additional assistance should
consult the official [PHP Manual](http://php.net/manual/en).</span>

3\. Save the file once you have completed modifications.

4\. Next, r**estart the IIS service** to load any configuration changes.
To do so, open the **Server Manager** from the task bar.

5. <span>From the **Tools**'menu select **Internet Information Services
(IIS)** Manager. Select the server on the right hand screen and click
**Restart** in the Manage Server section.</span>

<span><img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/restart_iis.png" width="866" height="616" /></span>

Setting the Default Document
-----------------------------

To ensure php content is served as the first option the default document
setting within the IIS Manager needs to be modified. This section will
detail how to modify the Default Document setting within the IIS Manager
to perform just this.

<span>1. Open the **Server Manager** from the task
bar.</span><span> </span>

<span>2. From the **Tools** menu click **Internet Information Services
(IIS) Manager**.</span>

<span><img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/tools_iis.png" width="872" height="619" /></span>

<span>3. In the Internet Information Services (IIS) Manager select the
server homepage. </span>

<span><img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/home_page.png" width="871" height="620" /></span>

<span>4. Double-click the **Default Document **option.</span>

<span><img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/default_doc.png" width="872" height="621" /></span>

<span>5. Select the **index.php** option and move it to the top of the
list.</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/php_top.png" width="876" height="624" />

<span>6. IIS will now serve index.php files from the wwwroot folder
before all other document types.</span>


