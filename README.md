prestashop - 500 error
===================
https://www.prestashop.com/forums/topic/421126-request-exceeded-the-limit-of-10-internal-redirects-due-to-probable-configuration-error/
===================

CloudFlare installation:
==========
http://www.cpanelkb.net/cloudflare-plugin-install/
http://crybit.com/install-cloudflare-plugin-on-cpanel/
http://stackoverflow.com/questions/23860877/how-to-install-cloudflare-on-cpanel-servers
==========www.iwebtool.com/speed_test
www.linkvendor.com › Website Speed Test
http://www.webpagetest.org/

ini_set('memory_limit','512M');-----in the config.php for joomla error

+===============================================+
du -sch * | sort -n----for auditing of account

+===================+
siteground.com
DKMIcore.org
+===========+

php.ini
==========================
safe_mode = Off
disable_functions = 
memory_limit = 128M
upload_max_filesize = 20M 
post_max_size = 20M 
session.gc_maxlifetime = 1440 (Set a higher value for session.gc_maxlifetime in your php.ini file.)
max_execution_time = 300
session.save_path = /home/alveston/public_html/tmp
+===============================+


To block country IP
======================
go to configure firewall >> seach for cc_deny and put country code there and update
http://webstore.lexi.com/s.nl/ctype.KB/it.I/id.378/KB.3234/.f
+===================+


for mod_security error 406 or can' edit any thing in website .htaccess 
======================================================
+===========+
<IfModule mod_security.c>
SecFilterEngine Off
SecFilterScanPOST Off
</IfModule>
+===========+

tail -f error_logs


To check IP blacklisated on Direct admin go to following:
+====================+
cd /usr/local/directadmin/data/admin/
vi ip_blacklist
+=====================+


How to make Wordpress a Multisite CMS-refer following links
=================================
http://www.youtube.com/watch?v=3gu3MPCynfw
http://codex.wordpress.org/Create_A_Network
===================================

corvette tuner wp clone install 
==========================
https://www.youtube.com/watch?v=5c5dUiApETE




QUESTION
———
We own/lease a Linux server from anySiteHosting.com and would like to enable the feature to allow users to visit their site via a temp url like http://cp.OURDOMAIN/~CPANELUSERNAME
=====================================================
ANSWER:
———
Access the following menu path: WHM: Main >> Security Center >> Apache mod_userdir Tweak
Tick the check-box labeled Enable mod_userdir Protection
Untick all check-boxes under the column heading Exclude Protection
Locate the virtual host that you wish to use from the list under column heading Host.
Input the desired cPanel account username, or usernames as a space-separated list, under the column heading Additional Users.
Click Save, at the bottom of the page, to submit and finalize changes.
+===============================================+




How to install RVsitebuilder with cpanel on linux server?
===========================================

=> SSH into the server :

cd /usr/local/cpanel/whostmgr/docroot/cgi/
rm -rf /usr/local/cpanel/whostmgr/docroot/cgi/rvsitebuilderinstaller/
rm -f rvsitebuilderinstaller.tar
wget http://download.rvglobalsoft.com/rvsitebuilderinstaller.tar
tar -xvf rvsitebuilderinstaller.tar
chmod 755 addon_rvsitebuilder.cgi
rm -f rvsitebuilderinstaller.tar
=========

Note : If CGI directory is not present you can create it.

Then access login into WHM >>Plugins>>RVSiteBuilder Installer >>click next>>enter license key and proceed further.




***Put this code in .htaccess to redirect your any page to 404 page
========================================

Options -Indexes
ErrorDocument 404 /404.php
<IfModule mod_rewrite.c>
RewriteEngine On 
RewriteBase / 
#RewriteCond %{REMOTE_ADDR} !^68\.112\.67\.230$
RewriteRule ^wp\-admin\/$ "http\:\/\/www\.freeguardian\.com\/404\.php" [R=301,L]
RewriteRule ^wp\-login\.php$ "http\:\/\/www\.freeguardian\.com\/404\.php" [R=301,L]
RewriteRule ^wp\-admin\/$ - [L,R=404]
RewriteRule ^(.*)wp-(.*)$ - [L,R=404]
RewriteRule ^(.*)feed(.*)$ - [L,R=404]
RewriteRule ^(.*)feed\/(.*)$ - [L,R=404]
RewriteRule ^(.*)[0-9]{4}\/[0-9]{2}(.*)$ - [L,R=404]
RewriteRule ^(.*)\.htaccess(.*)$ - [L,R=404]
RewriteRule ^(.*)xmlrpc\.php(.*)$ - [L,R=404]
RewriteRule ^(.*)style\.css(.*)$ - [L,R=404]
RewriteRule ^(.*)license\.txt(.*)$ - [L,R=404]
RewriteRule ^(.*)readme\.html(.*)$ - [L,R=404]
</IfModule>
RewriteCond %{HTTP_HOST} ^freeguardian\.com$ [OR]
RewriteCond %{HTTP_HOST} ^www\.freeguardian\.com$
+==========================================+
make 404.php in root directory( public_html)


Imagick
==============

http://www.webcs.com/webcsdocs/docs5/imagick.html
Go to WHM -> Software -> Module Installers -> PHP Pecl (manage). On the box below “Install a PHP Pecl” enter “imagick” and click “Install Now” button – that’s all.  Restart Apache.
==============


+==================+
cat > phpinfo.php
<?
phpinfo(); 
?>
chown username:username phpinfo.php

grep username /etc/userdomains --- to check domain name of user

cpmove-username.tar

+==================+



What is a 301 redirect?
==================
A 301 redirect is the preferred method to preserve your current search engine rankings when redirecting web pages or a web site. The code "301" means that the page has "moved permanently".

How to set up the 301 Redirect?

    To create a .htaccess file: open notepad, name and save the file as .htaccess. (be careful not to save the file as txt)
    If you already have a .htaccess file on your server, download it to your desktop for editing.
    Copy this code into your .htaccess file: 

redirect 301 old.htm http://www.domain.tld/new.htm

    If the .htaccess file already has lines of code in it, skip a line first
    Save the .htaccess file
    Upload this file to the root folder of your server.
    To test it, simply try to load the old site or page in your browser. You should be redirected immediately 
	
	

	
	outlook settings
+========================+	
Incoming Mail Server: mail.domainname.com
Outgoing Mail Server: mail.domainname.com
Incoming Port: 110 (pop) 143 (imap)
Outgoing Port: 587
+=========================+



Rvsitebuilder tutorials
=========================

http://support.rvsitebuilder.com/index.php?x=&mod_id=2&root=2
http://support.rvsitebuilder.com/index.php?x=&mod_id=2&root=89
=========================



For this error:
Fatal error: Class 'PDO' not found in /home/alohakea/public_html/includes/database/database.inc on line 184
put following in php.ini file:
+=================+
extension="pdo.so"
extension="pdo_mysql.so"
+===================+


If php files are getting downloaded instead of executing then put following code in .htaccess file
PHP files are downloading instead of executing
+==================+
AddHandler application/x-httpd-php5 .php
Apache handler
+==================+


Default apache handler
============
DirectoryIndex index.php
===============


To get regular html pages to handle php code, you need to add this line to your htaccess file.
====================
AddHandler application/x-httpd-php5 .html .htm
=====================


To check default handler set on the server
=====================
grep DirectoryIndex /etc/httpd/conf/httpd.conf
=====================


Default wordpress code in .htaccess
============================
# BEGIN WordPress
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>
# END WordPress
+=========================+



Mysql & Mysqldump
=================
cd /backup/mysqlbackup/daily1
ls -l Username_database name.sql
mysql Username_database name < Username_database name.sql (less than sign is for importing the database)
mysqldump paragon_wrdp1 > paragon_wrdp1.sql
=================



To install different components on the server
=====================
http://www.crucialp.com/resources/tutorials/server-administration/how-to-install-zend-optimizer-optimiser-cpanel-whm.php
=====================



cloudlinux documentation
==============
Read this 4 times
http://docs.cloudlinux.com
==============



To correct the files/directory permissions inside public_html directory
======================
find . -type d -exec chmod 755 {} \;
find . -type f -exec chmod 644 {} \;
======================



To install Zend Optimizer:
============================
1. Login to your server via SSH
2. Run: /scripts/installzendopt
==============================

http://rbls.org


Set www redirection in htaccess
=========================
RewriteEngine On
RewriteCond %{HTTP_HOST} ^access-alpinespace.eu
RewriteRule (.*) http://www.access-alpinespace.eu/$1 [R=301,L]
=====================================


To change the site URL from wp-admin backend
==============
For wp sites  >> go wp-admin >> setting >> general >> site URL
==============


.htaccess code to give authorisation particular directory, create .htaccess file in that directory with below code.
============
AuthType Basic
AuthName "admin"
AuthUserFile "/home/username/.htpasswds/public_html/admin/passwd"
require valid-user
===========



For Mambo error: Fatal error: Call to undefined method mosMenu::mosDBTable() in /home/username/public_html/includes/core.classes.php
or
Fatal error: Call to undefined method mosSession::mosDBTable() in /home/username/public_html/includes/core.classes.php on line 

Rerfer this post ( https://www.greycell.co.za/support/index.php?_m=knowledgebase&_a=viewarticle&kbarticleid=128)
+============================+

To correct this

in the file /public_html/includes/database.php

Find the class:

class mosDBTable extends mosDBAbstractRow {

After the line
var $_db = null;

Put in the following:

function mosDBTable($table='', $keyname='id', $db='') {
        $this->mosDBAbstractRow ($table, $keyname, $db);
    }

And your problem will be solved.
+===========================+




To apply changes recursively of php.ini fil, put below code in .htaccess file
==========================
<IfModule mod_suphp.c>
  suPHP_ConfigPath /home/cozcomul/public_html
  <Files php.ini>
    order allow,deny
    deny from all
  </Files>
</IfModule>
===========================



SPF record format:
===========================================================
http://www.royhochstenbach.com/projects/spfgenerator/
http://www.openspf.org/SPF_Record_Syntax
=============
Domain name. IN TXT "v=spf1 a mx ptr ~all"
(v=spf1 +a +mx +ip4:209.59.146.231 ?all) 
e.g. v=spf1 a mx include:emailsrvr.com ~all
=============


How to disable magic_quotes_gpc in php.ini
===================
magic_quotes_gpc = Off
magic_quotes_runtime = Off
magic_quotes_sybase = Off
extension=pdo.so
extension=pdo_mysql.so
===================

or in .htaccess
=============
php_flag magic_quotes_gpc Off
============



http://postimage.org


===========
Running `/usr/local/cpanel/scripts/updatenow --upcp --log=/var/cpanel/updatelogs/update.1364314802.log` failed, exited with code 65280
===========



============================================
How to Protect Your WordPress wp-config.php File and Your .htaccess File
============================================
1) To protect wp-config.php file, put below code in .htaccess file providing both this files are placed in the same directory.

<Files wp-config.php>
order allow,deny
deny from all
</Files>

2)To protect .htaccess file, put below code in .htaccess file:

<Files .htaccess>
order allow,deny
deny from all
</Files>
==========================================



Display the PHP errors when developing and hide them when live
=================
php_flag display_errors off---------.htaccess
=================


To hide mysql error warning from the site, add below lines in php.ini
=============
log_errors = On
display_errors = Off
=============


To apply all changes made in php.ini file to all public_html directory, add below code in the .htaccess file.
==================================
<IfModule mod_suphp.c>
  suPHP_ConfigPath  	/home/username/public_html
  <Files php.ini>
    order allow,deny
    deny from all
  </Files>
</IfModule>
==================================



How to reset admincp password in Vbulletin
================
http://blog.webhostingdiscussion.net/scripts/how-to-reset-vbulletin-administrator-password.htm
==============


Some Daily Useful Commands
=================
zip -r newfilename.zip  /home/username/public_html-----------entire public_html will be get zipped at pwd
 zip -r public_html public_html/
tail -f /usr/local/apache/logs/error_log | grep IP
exigrep email id /var/log/exim_mainlogs
tail -f email id /var/log/exim_mainlogs | grep (anyword from the email id)
ps -aufx | grep username --------------to check the processes of the particular user on the server

ssh root@67.23.163.140 -----to connect to another server from one server.

( rsync -avz --rsh='ssh -p22' root@67.23.163.140:/backup/cpbackup/daily/* . ) ---this is wil copy entire backup files from the daily directory to destination folder which we have created on the receiver server.
 
 http://www.michianawireless.com/mail-errors.htm ----to check all the mail issues.
================= 
 
 
cd /etc/hosts.deny --list of all deny hosts


IMP commands to regarding emails
============
(http://www.simplehelp.net/2008/12/01/how-to-send-email-from-the-linux-command-line/)
============



To restore multiple backups
=================
http://forums.cpanel.net/f5/restore-backup-via-ssh-multiple-accounts-135029.html
http://forums.cpanel.net/f5/how-can-i-restore-multiple-accounts-cpanel-backups-195351.html
http://hiox.org/444-backup-and.php
https://forums.hostdime.com/showthread.php?5599-Restoring-Cpanel-Backups-via-SSH
http://www.webhostingtalk.com/showthread.php?t=897649
=================



Dig command
===========
http://library.linode.com/linux-tools/common-commands/dig
===========



Userful commands
==============
http://centoshelp.org/resources/commands/linux-system-commands/
==============


CSS file templates/template_name/themes/theme_name/template.css


==================
Request exceeded the limit of 10 internal redirects Error
==================================
in .htaccess file insert below codeand insert the below wordpress default code :-

—————————-

# BEGIN WordPress

<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>

# END WordPress
================================
Also, refer this URL: http://www.bestdesigns.co.in/blog/request-exceeded-the-limit-of-10-internal-redirects
===============


Different Ports
+===============+
POP3 is encrypted via SSL on port 995 (unencrypted POP3 uses port 110).
IMAP is encrypted via SSL on port 993 (unencrypted IMAP uses port 143)
SMTP is encrypted via SSL on port 465 (unencrypted SMTP uses port 25 or 26) 
+===============+


Tar Command
=========
To create a tar.gz archive from a given folder you can use the following command

tar -zcvf tar-archive-name.tar.gz source-folder-name 
tar -xvf homedir.tar-----------to untar in SSH
tar -tvf file.tar  -------to view the files in tar.gz
( refer: http://www.cyberciti.biz/faq/list-the-contents-of-a-tar-or-targz-file/
 http://www.cyberciti.biz/faq/tar-extract-linux/)
=========


How to change the site URL of wordpress website?
==============
Edit wp_option --to change the site URL for the wordpress from phpmyadmin
==============


Some log paths
==========
/usr/local/cpanel/logs/access_logs ------------to check cPanel logs
/usr/local/cpanel/logs/error_logs
/usr/local/apache/htdocs-------- we can put any file here and give client to download link as: serverIP/filename
/var/log/messages
/usr/local/apache/conf/httpd.conf
/usr/local/apache/logs/error_logs
/usr/local/apache/logs/access_logs
/usr/local/apache/dom_logs/domainname
/etc/my.cnf
/etc/grub.cnf
top -d2c  ----- to check all the current processes in the detail.
==========


htpasswd generator
=================
http://www.htpasswdgenerator.net/ -------- to create new .htpasswd as well as .htaccess
http://www.rapidtables.com/web/tools/redirect-generator.htm------------site redirect code generator.
=================


http://www.servertechs.net/domain-shows-cpanelwhm-default-page.html


DNS Commands
===============
cat /var/named/domainname.com.db -----------to edit dns zone from shell
/scripts/rebuildhttpdconf ------------ after doing the changes to rebuild httpdconf
dig domainname ---- to view current DNS zone of the domain
===============



Issue: "Could not write to counter file: /var/cpanel/Counters/filename.dat" while we set a counter for a domain
==============
=> Login to your server >> cd /var/cpanel/Counters >> chown username.username to filename.dat >> save and quit

     Refresh your browser and clear their caches.......
==============



FireFox issue: Keeps asking for login.
===================
refer this URL: http://wordpress.org/support/topic/firefox-issue-keeps-asking-for-login
===================



How to install SSL on the addon domain?
================
http://forums.cpanel.net/f5/ssl-addon-domain-309312.html
================



To config new IP address on the server
+===============+
 cd /etc/sysconfig/network-scripts/
    5  ll
    6  vi ifcfg-eth0-range1
    7  ll
    8  ifc
    9  ifconfig 
   10  /etc/init.d/network restart
   11  ifconfig 
   12  vi ifcfg-eth0-range2
   13  vi ifcfg-eth0-range3
   14  vi ifcfg-eth0-range3
   15  ll
   16  /etc/init.d/network restart
 +===============+
 
 
 
 Drupal Error:
 ==============
 PDOException: SQLSTATE[42000] [1044] Access denied for user 'vfp'@'67.205.0.0/255.255.192.0' to database 'vfpvmembers' in lock_may_be_available() (line 167 of /home/bryancasler/vfpmembers.org/includes/lock.inc).
===============
=> check for the settings.php file for correct database name, username, password and also give all privileges while adding user to database
==============


wp-admin redirection issue  fixed
=====================
http://stackoverflow.com/questions/8456360/wordpress-wp-admin-redirects-me-to-a-different-domain
=====================


To redirect to suspend page---out below in the .htaccess of the account.
+==============+
RedirectMatch .* /cgi-sys/suspendedpage.cgi
+===============+


To scan server
===============
clamscan -ir /home/* > /root/scanreport.txt 

No need to use this--| cat /root/scanreport.txt echo ""| mailx -s "Scanreport B for 107.6.39.205" ameya@micrahosting.com
===============


Changing main mail server ip
======================
1) If you are using Exim, Main >> Service Configuration >> Exim Configuration Editor >> Domains and IPs , enable option: "Send outgoing mail from the ip that matches the domain name in /etc/mailips" 

2) pico to /etc/mailips >> *: mail server IP >> save. 
(refer this post: http://forums.cpanel.net/f43/changing-main-mail-server-ip-153445.html

3) /etc/init.d/exim restart

4) Refer this URL: http://forums.eukhost.com/f38/changing-email-server-ip-address-cpanel-server-6781/#.UY1FfbVTBSU
     also (http://blog.my-helper.com/cpanel/change-email-server-ip-on-cpanel/)
	 also (http://www.webhostingtalk.com/showthread.php?t=953917)
======================



To change site URL in magento do below:
===========================
Go to respective database in phpmy admin >> find table "core_config_data" >> edit below fields:

======
web/unsecure/base_url ------------- put current domain name infront of this
web/secure/base_url ----------------put current domain name infront of this
======
============================



/var/cpanel/packages ----- to check all the pacakges 
/var/cpanel/users ----- entries of the all the pacakges here (grep -rl crystalv_seotuch *)
/scripts/chpass username new password ---- to change the password of the cPanel from shell



To install Install cloudfare module and plugin on cpanel
========================
http://linuxworldweb.blogspot.in/2012/03/install-cloudfare-on-cpanel.html
========================


How to edit cPanel theme:
==================
http://www.kvchost.com/hosting-tutorial/800/how-to-change-cpanels-branding-using-whm.html
http://my.kualo.com/knowledgebase/946-how-to-change-cpanels-branding-using-whm.html

Go to: /var/cpanel/userhomes/cpanel/cpanelbranding
==================



Backup file formats
=============
a) cpmove-user6.tar.gz [got by using no options]
b) backup-10.8.2011_18-28-46_user6.tar.gz [got by using --userbackup option]
=============


Private Nameservers
=================
http://hostnit.com/billing/knowledgebase.php?action=displayarticle&id=71
=================


changing Joomla footer
================
http://www.templatemonster.com/help/files/Joomla/Joomla2.5_copyright_information_changing.htm
================


Installing MediaWiki manually
================
http://www.inmotionhosting.com/support/edu/mediawiki/getting-started-mediawiki/install-mediawiki-manually
===============


Script to check spamming on the server - fire below command on shell as root
+=========================+
exim -bpr | grep "<*@*>" | awk '{print $4}'|grep -v "<>" |awk -F "@" '{ print $2}' | sort | uniq -c | sort -n

grep "cwd=" /var/log/exim_mainlog|awk '{for(i=1;i<=10;i++){print $i}}'|sort|uniq -c|grep cwd|sort -n | tail

grep "<= " /var/log/exim_mainlog|grep -v "<= <>"|awk '{print $5}'|sort|uniq -c|sort -n|tail

grep "<= " /var/log/exim_mainlog|grep -v "<= <>"|awk '{print $5,$7}'|cut -d":" -f1|sort|uniq -c|sort -n|tail

grep cwd /var/log/exim_mainlog|grep -v /var/spool|awk -F"cwd=" '{print $2}'|awk '{print $1}'|sort|uniq -c|sort -n
+=========================+


$mysqladmin process


PHP MAIL SCRIPT
==============
http://www.apache.com/resources/simple-php-mail-script-that-works/
http://php.net/manual/en/function.mail.php
==============


To increase webiste speed
====================
http://www.socialmediaexaminer.com/improve-the-speed-of-your-wordpress-site/
http://www.sparringmind.com/speed-up-wordpress/
====================


Install VNC on server
================
http://www.supportfacility.com/blog/install/install-vncserver-on-linux-remote-desktop-linux/
================


How add new dedicated IP address on centos
==============================
http://tutorials.vservercenter.com/articles/add-secondary-ip-address-static-to-centos-server/
==============================

Buzix
===========
Connection refused by host
=================
Also check for IP block on both server.
/etc/init.d/xinetd restart  --- on nagios/server on which getting this warning
/etc/init.d/nagios restart  --- on nagios
=================


===============
http://linuxreviews.org/beginner/#toc18
===============


To create daily backup of all the account in cpback/daily. ( 1st rename the daily directory to do this and make new daily directory 
===============
/scripts/cpbackup --force
rsync -avz /backup/cpbackup/daily/ root@198.20.238.2:/backup/ --- to copy backup to another server.
===============


To change SSH port
===============
pico /etc/ssh/sshd_config  
===============



http://www.htaccessredirect.net/


chattr
================
http://tournasdimitrios1.wordpress.com/2011/01/22/protecting-filesdirectories-even-from-the-root-user-with-chattr/
================


+===========+
lsattr ---- to check list of currently locked directoires.
chattr +ir public_html   ----- to chattr public_html directory
chattr -ir public_html   ----- to remove chattr from public_html directory
+===========+


If Webmail.domainname.TLD is showing default page then do following:
====================
Go to WHM >> Main >> Server Configuration >> Tweak Settings >> serach for "proxy subdomains" >> ON this option.
====================


http://www.mkyong.com/blog/mod_security-blocking-my-ip-when-editing-post-in-wordpress/



How to troubleshoot “111 Can’t open SMTP stream” issue in SquirrelMail
========================
/etc/init.d/iptables restart 
/etc/init.d/iptables stop
/etc/init.d/iptables start

or

The other easy step to resolve this issue is editing /etc/exim.conf where it says

#daemon_smtp_ports = 25 : 587
daemon_smtp_ports = 25

Change it to:

daemon_smtp_ports = 25 : 587
#daemon_smtp_ports = 25
========================


How to install uploadprogress extension php (Prefer to do this from WHM)
========================================
http://forums.cpanel.net/f5/installing-acp-uploadprogress-tutorial-107265.html
http://www.cpanelblog.in/install-uploadprogress-php-extension-linux-machine
========================================


Short Guide to Running Python Scripts with cPanel
============
http://forums.cpanel.net/f5/short-guide-running-python-scripts-cpanel-244361.html
============


How to Configure MailScanner in cPanel
=====================
http://www.granitewebdesign.com/whmcs/knowledgebase/99999131/How-to-Configure-MailScanner-in-cPanel.html
=====================


IP blacklist check URL:
===============
http://www.blacklistalert.org/
http://whatismyipaddress.com/blacklist-check
http://www.mxtoolbox.com/blacklists.aspx
===============


Some Userful scripts
===============
http://forums.cpanel.net/f5/useful-script-sys-admin-56995.html
http://www.inmotionhosting.com/support/website/server-usage/create-server-load-monitoring-bash-script
===============


load-tackling-in-cpanel-servers
====================
http://www.linux.com/learn/tutorials/269481:load-tackling-in-cpanel-servers
=====================


How to manually install SMF ( simple machine forums)
================
http://www.inmotionhosting.com/support/edu/smf/getting-started-smf/smf-manual-install
================


Magento Error - "503 Service Temporarily Unavailable"
============================
delete the following file from your /magento/ installation
maintenance.flag
e.g. rm ./magento/maintenance.flag
============================


to scan any particular directory
========================
maldet -a /home/askypcom/public_html/    --------------- To perform maldet scan
clamscan -ri /home/askypcom/public_html/  ------------ To perform clamscan
cat scan.txt |cut -d ":" -f1 |awk '{system ("rm -f " $1)}'  ---To remove all the resulted infected files from scan.txt file.
========================


To search for any string in files/directoires 
====================
grep "string" * -lr
====================



To check no. of accounts present on the server.
============
wc -l /etc/trueuserdomains
============


Help full exim commands
================
exiqgrep -i -r adithimakazu@yahoo.com | xargs exim -Mrm  -------------to remove all the emails of adithimakazu@yahoo.com  from mail queue 
exiqgrep -i -r adithimakazu@yahoo.com   ---------------to search email sent from this email id.
exiqgrep -i  | xargs exim -Mrm    ................To empty entrie mail queue 
exiqgrep -iz | xargs exim -Mrm  -------- To remove all the Frozen email from queue.
================



To change the magento DB
====================
edit this file: pico /home/username/public_html/app/etc/local.xml
Refer this URL: http://sapnandu-magento.blogspot.in/2010/08/change-magento-database-information.html
====================


TO check the error log in magento website
============================
go to /home/username/public_html/var/report]# cat 1028834884612 (Error log record number)
============================


Useful URL
=================
http://aavivi.blogspot.in/
=================


Can't Delete an Addon Domain - Error from park wrapper: Sorry, you do not control the domain religiousink.com
====================
You will have to remove the add-on domain from all the files cPanel creates an entry in and then add it back. The files are

httpd.conf (restart the httpd service once you edit it)
named.conf and .db file from /var/named/ (restart named service)
/etc/localdomains
/etc/remotedomains
/etc/trueuserdomains
/etc/userdomains
/var/cpanel/users/username (username is the main domains username) 
====================



For error - MySQL: ERROR 1010 (HY000): Error dropping database (can't rmdir './foodb', errno: 39) 
====================
Refer this URL: http://micharg.blogspot.in/2011/05/mysql-error-1010-hy000-error-dropping.html
====================


To findout IP address which are trying to login to any particular account.
+=====================+
/usr/local/cpanel/logs/login_log   - That log shows a list of failed login attempts and deferred login attempts.
/usr/local/cpanel/logs/access_log
/var/logs/messages
cat /usr/local/apache/domlogs/domainname
+=====================+


**********************************************
Very useful URL: http://www.inmotionhosting.com/support/website/getting-started-guides/cpanel-logs-for-access-apache-email-error-ftp-mysql-whm
**********************************************



To check ping is enabled on server or not
====================
cat /proc/sys/net/ipv4/icmp_echo_ignore_all
 if get output as 0 then it is enabled on the server and if it shows 1 then it disbled
====================




RVSitebuilder license error fix
+=======================+
 1021  wget wget http://download.rvglobalsoft.com/rvsitebuilderinstaller.tar
 1022  tar -xvf rvsitebuilderinstaller.tar 
 1023  ll
 1024  cd rvsitebuilderinstaller
 1025  ll
 1026  cp autoinstaller.cgi  /usr/local/cpanel/whostmgr/docroot/cgi/rvsitebuilder
 1027  cp autoinstaller.cgi  /usr/local/cpanel/whostmgr/docroot/cgi/rvsitebuilderinstaller/
 1028  perl  /usr/local/cpanel/whostmgr/docroot/cgi/rvsitebuilderinstaller/autoinstaller.cgi 
 1029  perl  /usr/local/cpanel/whostmgr/docroot/cgi/rvsitebuilderinstaller/autoinstaller.cgi --force
 +=======================+
 
 
 Email codes
 ===============
 https://www.mailenable.com/kb/Content/Article.asp?ID=me020032
 http://www.afterlogic.com/products/xmail-server-pro-windows-docs/xmail-server-docs/smtp-reply-codes.htm
 http://www.symantec.com/business/support/index?page=content&id=TECH95239
 ===============
 
 
 
 How to set maximum email attachment size
 =============================
 http://cpanelstuffs.linuxcabin.com/?p=141
 http://forums.host.co.in/showthread.php?2188-How-to-set-maximum-email-attachment-size-in-exim-email-server
 =============================
 
 
 
 Exim Commands
 ===============
 exiqgrep -f purchase@shyamferro.com -i | xargs exim -Mrm   ----- to remove all the emails from respective emails id
 exiqgrep -r cpmcindi@host.orbitwebhost.com -i
 exiqgrep -f cpmcindi@host.orbitwebhost.com -i
 
 Refer this URL: http://www.cyberciti.biz/faq/exim-remove-all-messages-from-the-mail-queue/
 ==============
 
 
 To sent email from root to any email ID
 +================+
 mail -vv mitoda@intnl.doshisha.ac.jp
 +================+
 
 
 
 How to solve Mail bounce back – retry time not reached for any host after a long failure period
======================================================
http://forums.cpanel.net/f43/t-remote_smtp-defer-53-retry-time-not-reached-any-host-72383.html
http://support.createhosting.co.nz/knowledgebase.php?action=displayarticle&id=53
http://blog.hostripples.com/retry-time-not-reached-for-any-host-after-a-long-failure-period/
http://support.kdaws.com/desk/index.php?/Knowledgebase/Article/View/12/0/instant-bounce-back-retry-time-not-reached-for-any-host-after-a-long-failure-period
http://www.ipserverone.info/control-panel/directadmin/mail-bounce-back-retry-time-not-reached-for-any-host-after-a-long-failure-period/
======================================================


How to use scp
================
 scp -P 3389 root@107.6.46.36:/home/cpmove-cpmcindi.tar.gz .
  rsync -avz --rsh='ssh -p1157' root@66.7.193.169:/backup/cpbackup/daily . --progress
================ 


Buzix SPF & DKMI setup for domain
+=================+
generate a DKIM and do it like this:
/usr/local/cpanel/bin/dkim_keys_install USERNAME
/usr/local/cpanel/bin/spf_installer USERNAME

Adding Domain Keys for All Users
for user in `ls /var/cpanel/users`; do /usr/local/cpanel/bin/dkim_keys_install $user; done

Adding SPF Records for a All Users
for user in `ls /var/cpanel/users`; do /usr/local/cpanel/bin/spf_installer $user; done

Refer this URL: http://billing.holodyn.com/knowledgebase/72/Adding-SPF-Records-and-DomainKeys-within-cPanel.html
+=================+


To edit cPanel theme
===================
/usr/local/cpanel/base/frontend/x3/branding/blueroy/images/logo.png
===================


How to create custom php.ini file in Litespeed Webserver.
=================
(Refer this URL: http://hebahabeeb.blogspot.in/2012/08/how-to-create-custom-phpini-file-in.html)
=================
 
 
 
How to set rediretion
=================
https://kb.mediatemple.net/questions/242/How+do+I+redirect+my+site+using+a+.htaccess+file%3F
=================
 
 
 How to install Ioncube loader
 ======================
 Follow this URL: http://docs.whmcs.com/Ioncube_Installation_Tutorial
 ======================
 
 
 
 
 How To Transfer Accounts from one server to another!
===========================================================================================================
 http://forums.cpanel.net/f5/how-transfer-accounts-one-server-another-60637.html
 
Then do below steps after above steps done 
--------------------------
131  cd /
  132  ll
  133  mkdir -p /backup/cpbackup
  134  cd /backup/cpbackup/
  135  ll
  136  mv /home/daily/ .
--------------------------

Go to Home »Backup » Legacy Backup Configuration
---------------------
Backup Status >> Enable 
Backup Interval >> Daily
Days to Run Backup >> select all day
Incremental Backup >> Enable
Backup Accounts >> Enable 
Compress Account Backups >> Disable 
Save
------------------------------

Then go to Home »Backup »Legacy Restore Backups   ----- to restore all the backups which are located at /backup/cpback/daily.
===========================================================================================================
 
 
 How to use chattr
 ==============
 chattr +ia -R directory name
 ==============
 
 
 10 lsof Command Examples
 ===================
 http://www.lifelinux.com/10-lsof-command-examples/
 ==================
 
 How To Kill Process In Linux
 =====================
 http://www.lifelinux.com/how-to-kill-process-in-linux/
 =====================
 
 
To remove all the emails in the queue if not worked by any command
===================
Go to /var/spool/exim/input  >> rm -rf *  -----It will remove all the mails which are currently present in mail queue.
===================


To skip any directory while doing account backup
====================
/scripts/pkgacct --skiphomedir ripeamat /home  ---- it will skip home directory.
======================

http://www.mobilephoneemulator.com/
http://www.allindiadaily.com/2013/08/more-than-100-keyboard-shortcuts.html




History for server load
==============
 991  pidof php
  992  killall -9 httpd
  993  killall -9 httpd
  994  killall -9 httpd
  995  /etc/init.d/httpd status
  996  /etc/init.d/httpd restart
  997  /etc/init.d/httpd restart
  998  /etc/init.d/httpd status
  999  top -d2c
 ==============
 
 
 
Installing Image::Magick
====================
/scripts/installimagemagick
Please refer this URL: http://www.webcs.com/webcsdocs/docs5/imagick.html
====================

Remove IP from Yahoo blacklist
=======================
https://www.intovps.com/client/knowledgebase/15/Yahoo-rejects-your-e-mail-messages--421-.html
=======================


=============
netstat -n | grep 995
=============


To check database connections.
=============
mysqladmin processlist | grep databasename|wc -l
=============


Centova cast installlation error
=======================
Configuration file could not be updated Could not to connect to Centova Cast daemon on 127.0.0.1:2199 (Connection refused)
Do below to resolve this:

=> root@server2 [~]# lsof -i:2199
root@server2 [~]# chmod 0755 /home/centovacast/scripts/castdctl.sh
root@server2 [~]# /home/centovacast/scripts/castdctl.sh start
Starting cast daemon ... ok
=======================


To install Tinyproxy on Centos
===========================
www.blackhatworld.com/blackhat-seo/proxies/222258-create-your-private-secure-high-anonymous-proxyastep-step-guide.html
http://www.vps.web.id/2009/10/12/install-tinyproxy-on-centos-5-3-vps/
===========================



How to create custom php.ini file in Apache Webserver
==========================
https://snipt.net/torkil/adding-a-custom-phpini-to-a-suphp-powered-cpanel-account/
http://barelyuseful.info/adding-custom-php-ini-to-a-cpanel-account-using-suphp/
http://support.pickaweb.co.uk/articles/how-to-use-your-web-hosting/add-custom-php-ini-in-apache-suphp-servers
==========================


How to enable KeepAlive in apache
======================
http://forums.host.co.in/showthread.php?2337-How-to-enable-KeepAlive-in-apache-2
=======================


How to install and configure APC Cache on a CentOS server?
=================
http://linuxhostingsupport.net/blog/tag/path-to-php-config
We can also install this module through WHM >> Home »Software »Install a Perl Module >> search for apc
=================



To generate wp-config
================
http://generatewp.com/wp-config/
================


FixPermission script
==============
http://boomshadow.net/tech/fixes/fixperms-script/
==============


To Edit server cron jobs
=========
crontab -e
crontab -u vowalla1 -l    -------------- To list the cronjob for particular user
crontab -u vowalla1 -e   -------------- To Edit the cronjob for particular user
http://wiki.dreamhost.com/Crontab
=========



How to install cPanel/WHM and csf on server
======================
http://docs.cpanel.net/twiki/bin/view/AllDocumentation/InstallationGuide/InstallingCpanel#InstallingCpanel
http://configserver.com/free/csf/install.txt
======================



Issue - 451 Temporary local problem + Squirrel mail
================================
1. Login into server using SSH
2. cd /usr/local/cpanel/base/3rdparty/squirrelmail/config/
3. vi config.php
in this configuration file search $useSendmail = false; and replace false to true
then restart exim and courier-imap
/etc/init.d/exim restart
/etc/init.d/courier-imap restart
================================


How to install GD and Imagettftext
========================
Go to WHM >> Easy Apache >> In exaustive option list, you can find this 2 option >> tick on them and rebuild apche.
========================


How to install MySql server in Linux
======================
http://www.rackspace.com/knowledge_center/article/installing-mysql-server-on-linux
http://www.cyberciti.biz/tips/linux-configure-mysql-database.html
======================


Squirrel mail Issue (ERROR: Connection dropped by IMAP server. Query: SELECT "INBOX
=========================
http://fastfixlinux.blogspot.in/2012/11/squirrel-mail-issue-error-connection.html
If above not work then check for this http://vishnulinux.wordpress.com/2012/03/29/error-connection-dropped-by-imap-server/  
=========================


How to setup Cron Job to backup MySql database in cPanel
=========================================
http://www.classicwebdesign.com/db_backup/
https://kb.westhost.com/questions/654/Setting+a+Cron+Job+to+do+a+MySQL+Database+Backup
http://www.a2hosting.com/kb/developer-corner/mysql/mysql-database-backups-using-cron-jobs#Method-1.3A-Include-MySQL-login-information-in-the-cron-job-command
http://www.yourhowto.net/how-to-create-a-cronjob-cpanel-backup/
http://aktripathi.wordpress.com/2013/02/27/cron-job-to-backup-mysql-database-in-cpanel/
=========================================



How to install Softaculous
==================
http://blog.supportpro.com/2011/12/how-to-install-softaculous-in-cpanel-server/
http://morelinux.wordpress.com/2012/05/23/installing-softaculous/
==================


To install php components using easyapache go to below path
=================
/home/cpeasyapache/src/php-5.3.16/ext

for Example --- mbstring
=>  135  cd /home/cpeasyapache/src/php-5.3.16/ext/mbstring/
  136  ll
  137  phpize
  138  ll
  139  ./configure 
  140  make 
  141  make install
  142  ll /usr/local/lib/php/extensions/no-debug-non-zts-20090626/
  143  vi /usr/local/lib/php.ini
=================



How to Install the BIND DNS Server on CentOS 6
+===============+
https://www.digitalocean.com/community/articles/how-to-install-the-bind-dns-server-on-centos-6
http://ostechnix.wordpress.com/2013/01/25/setup-dns-server-step-by-step-in-centos-6-3-rhel-6-3-scientific-linux-6-3-3/
http://www.unixmen.com/dns-server-installation-step-by-step-using-centos-6-3/
+===============+



To check permnant IP block logs
========================
/var/log/lfd.log       for ex - cat /var/log/lfd.log | grep 74.247.247.154
========================



How to install R1soft
===================
http://wiki.r1soft.com/display/CDP3/Setting+up+cPanel+Plugin%20
===================


How to disable SSH reverse mapping checking  ---- (Error - reverse mapping checking getaddrinfo failed - POSSIBLE BREAK-IN ATTEMPT!)
+===================+
http://www.linuxspy.info/tag/reverse-mapping-checking-possible-break-in-attempt-error-with-ssh/
+===================+


How to install ffmpeg mplayer and mancoder on CentOS 6
+==================+
http://www.sudosu.in/2013/03/install-ffmpeg-on-centos-5-cpanel-server.html
http://blog.osmicro.org/how-to-install-ffmpeg-mplayer-and-mancoder-on-centos-6/
http://linuxtechme.wordpress.com/2012/11/06/install-ffmpeg-ffmpeg-php-centos-with-cpanel/
http://d.stavrovski.net/blog/post/install-ffmpeg-and-ffmpeg-php-in-centos-6-with-virtualmin
http://www.ndchost.com/wiki/server-administration/install-ffmpeg
http://blog.shineservers.com/installing-and-configuring-ffmpeg-and-ffpeg-php/
http://datlinux.blogspot.in/2013/04/how-to-install-ffmpeg-on-centos-via-yum.html
+==================+


How to Reset admin password for PHPMotion
======================
http://forums.glowhost.com/knowledge-base/how-reset-admin-password-phpmotion-1217.html
http://wiki.phpmotion.com/HelpAdminPassword
======================


du -cksm * |sort -rn |head -11
(top 10 disk space using files and directories within the current directory)



How to install Fileinfo function on server
=================================
Please refer this URL: http://servertechz.com/linux/enableinstall-php-file-info-module-in-linux-servers/
http://linuxbytknalla.blogspot.in/2013/03/enable-php-fileinfo-on-server.html

steps:

pecl install fileinfo  and then add "extension=fileinfo.so" in php.ini file and restart apache. 

or If that above doesn't work then go for source install
# wget http://pecl.php.net/get/Fileinfo-1.0.4.tgz
# tar -zxf Fileinfo-1.0.4.tgz
# cd Fileinfo-1.0.4
# phpize
# ./configure
# make
# make install

After running the above commands you need to edit php.ini and add the following line.
extension=fileinfo.so

Restart apache service.
# /etc/init.d/httpd restart
=================================



How to cleanup space on the server
=========================
Please refer this URL:
http://mxtoolbox.com/SuperTool.aspx?action=blacklist%3a+46.249.211.55+&run=toolpage
=========================


Setting the timezone for php in the php.ini file
+=====================+
http://www.inmotionhosting.com/support/website/php/setting-the-timezone-for-php-in-the-phpini-file
+======================+


wp-cron optimization.
======
http://www.boltwebhosting.com/wordpress-optimization/wp-cron-php-how-to-stop-it-from-running-frequently.html
======



Iptables ---- http://safesrv.net/quick-how-to-denyallow-ip-using-iptables/
=============
iptables -A whitelist -s 148.243.57.230/24 -j ACCEPT
iptables -A INPUT -s 148.243.57.230 -j ACCEPT
iptables -A INPUT -s 201.141.148.16 -j DROP
=============



How to install FTP/SFTP on centos
===========================
http://www.xiaoclouding.com/blog/install-sftp-and-configure-chroot-on-centos/
===========================


How to create a FTP user with specific /dir/ access only on a Centos / linux installation
=====================
http://unix.stackexchange.com/questions/83221/how-to-create-a-ftp-user-with-specific-dir-access-only-on-a-centos-linux-ins
=====================



To install PHP extensions
=================
yum install php-mcrypt
yum install php-gd
=================


how to install and add Apache Module mod_expires to your .htaccess
=======================
http://www.inmotionhosting.com/support/website/htaccess/apache-module-mod-expires
http://forums.cpanel.net/f5/how-install-mod_expires-35908.html
https://studio.tellme.com/vxml2/ovw/perf/cache_apache13.html
http://www.webproworld.com/webmaster-forum/threads/100407-How-To-Set-Up-The-Mod_Expires-On-An-Apache-Server
=======================



IMP links
=========
http://www.youtube.com/results?search_query=how+to+setup+apache+saroha&sm=3
http://www.youtube.com/watch?v=gVfw6aVZoZA&list=PL157AD5937AA33D79
==========


Enable FTP Passive Mode
==========
http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/FTPPassiveMode
==========



Wordpress Error - "An unexpected error occurred. Something may be wrong with WordPress.org or this server’s configuration. If you continue to have problems, please try the support forums.Try again" (While Adding new plug-in, theme etc)
=====================
To fix above error, do below on the server

=> 1. Ping api.wordpress.org, it will be 72.233.56.139, if it is reachable then,
     2. Edit your host file vi /etc/hosts
     3. Add in this line
      72.233.56.139 api.wordpress.org
    4. Save :wq!
	5. Refresh at wp-admin backend and check again, it should work.
=====================




SolusVM Documentation
===============
http://docs.solusvm.com/
===============



For Joomla language switcher
====================
http://docs.joomla.org/Help32:Extensions_Module_Manager_Language_Switcher#Module
http://www.templatemonster.com/help/joomla-3-x-configuration-multilanguage-site.html#prettyPhoto
====================


How to whitelist Mod_security rules on a CPanel server
===============
http://barelyuseful.info/how-to-whitelist-mod_security-rules-on-a-cpanel-server/
http://linuxtechme.wordpress.com/2013/08/20/mod_security/
===============


 how install JAWStats
 =============================
 http://www.jawstats.com/documentation
 
 Sample config file
-------------
  "statspath"   => "/home/salonyab/tmp/awstats/",
    "updatepath"  => "/usr/local/cpanel/base/awstats.pl/",
    "siteurl"     => "http://salonyab.com/jawstats/",
---------------
 =============================
 
 
 
SSH command to check 
=================
netstat -tulpn
netstat -anp |grep 'tcp\|udp' | awk '{print $5}' | cut -d: -f1 | sort | uniq -c | sort -n
netstat -tulnap | awk '{print $7}' | sed -n -e '/[/]/p' | cut -s -d'/' -f2 | sort | uniq -c | sort -nk 1
=================


Htaccess IP block code generator.
+==================+
http://www.htaccesstools.com/block-ips/
+==================+


Replace command ( Dont use it if you are unsure, risky)
===============
root# replace abc xyz  -- filename (It will replace all xyz by abc)
=============== 


How to install PHP Shield loaders
===================
http://itsmeanee.wordpress.com/2010/11/08/installing-phpshield/
http://kmaiti.blogspot.in/2010/07/how-to-install-phpshield-on-32-or-64.html
http://wiki.phpmotion.com/PHPShield53

-----------------
241  arch 
243  wget http://www.phpshield.com/loaders/ixed4.lin.x86-64.zip
244  ll
245  unzip ixed4.lin.x86-64.zip 
246  ll
247  grep ^exte /usr/local/lib/php.ini
248  cp ixed.5.3.lin /usr/local/lib/php/extensions/no-debug-non-zts-20100525/
249  echo "extension="ixed.5.3.lin"" >> /usr/local/lib/php.ini
250  grep ixed.5.3.lin /usr/local/lib/php.ini
251   php -i | grep extension_dir
252  /etc/init.d/httpd restart
253  /scripts/restartsrv httpd
254  php -i | grep phpshield
255  php -m
 --------------------
==================



How To Configure DNS For Office 365 In cPanel
=================
Add below DNS Records:
myURL.com.             300    MX     0 myURL.com..mail.protection.outlook.com.
myURL.com.             3600   TXT    MS=ms000000   --------It will be diff
autodiscover           3600   CNAME  autodiscover.outlook.com.
myURL.com.             3600   TXT    "v=spf1 include:outlook.com ~all"
_sip._tls              3600   SRV    100 1 443 sipdir.online.lync.com.
_sipfederationtls._tcp 3600   SRV    100 1 5061  sipfed.online.lync.com.
sip                    3600   CNAME  sipdir.online.lync.com.
lyncdiscover           3600   CNAME  webdir.online.lync.com.


http://mytecharticle.com/how-to-configure-dns-for-office-365-in-cpanel/
http://community.office365.com/en-us/forums/166/p/46965/162251.aspx
http://community.office365.com/en-us/forums/166/t/46965.aspx
http://community.office365.com/cfs-filesystemfile.ashx/__key/communityserver-components-userfiles/00-00-06-07-98-Attached+Files/2308.srv-dns-settings-1.png
=================


IMP command
=========
cat /usr/local/apache/domlogs/alpineen/alpineenvironmentalinc.com | grep wp-login.php
=========


To check SSL strength
============
https://www.ssllabs.com/ssltest/index.html
============




Making CPanel PCI Compliant
=======================
https://cbill.netsonic.net/index.php?/knowledgebase/article/71//
https://cbill.netsonic.net/index.php?/knowledgebase/article/70/making-cpanel-pci-compliant--part-2/
=======================



How To Secure&Optimize A cPanel Server
=================
http://www.wjunction.com/48-technical-security-tutorials/38599-how-secure-optimize-cpanel-server-%5Bfull-information%5D.html
=================


Moving SecureCRT from one PC to another PC
+=======================+
http://www.vandyke.com/products/securecrt/faq/025.html
+=======================+


Unable to remove add-on domain from cPanel - Error 
==========================
http://linux-bloggers.blogspot.in/2011/11/unable-to-remove-add-on-domain-from.html
==========================


How to upgrade WHMPHP master reseller 
+=======================+
http://www.whmphp.com/installation.php
+=======================+



How to install Nginxcp
======================
http://nginxcp.com/installation-instruction/
======================


To check mysql logs
=============
tail -f /var/lib/mysql/hostname.err 
=============


To redirect all the pages from http to https, put below code in the .htaccess.
======================
RewriteCond %{HTTPS} off
RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI}

RewriteEngine on
RewriteCond %{HTTP_HOST} ^www\.(.*)
RewriteRule ^.*$ https://%1/$1 [R=301,L]
======================




Unable to create an account in WHM
=================================
Error:
root@pwrreseller [~]# useradd falana
useradd: cannot lock /etc/gshadow; try again later.
==============

Solution:
================
Simply fire below command which will remove corresponding .lock files
=============
root@pwrreseller [~]#  rm -f /etc/passwd.lock /etc/group.lock /etc/gshadow.lock
=============
=================================



How to enable GZIP compression in cPanel Sites
======================
Simply refer this URL: http://windhosting.net/portal/knowledgebase/2/How-to-enable-GZIP-compression-in-cPanel-Sites.html
and to test site compression refer: http://www.whatsmyip.org/http-compression-test/
======================




Uptime Script
======================
*/5 * * * * uptime >> /home/uptime.log
*/5 * * * * ps -eo pcpu,pmem,pid,user,args | sort -k 1 -r | head -10 >> /home/uptime.log
*/5 * * * * date >> /home/uptime.log

   cd /home/
  touch uptime.log
   crontab -e
   /etc/init.d/crond restart
   tail -f uptime.log 
=====================
 
 
 
Linux Server Hardning
==========
http://linuxsupportz.wordpress.com/basic-support/
==========



Plesk Paths
===============
DNS zone file:  /var/named/run-root/var/domain.com
Domain File path: /var/www/vhosts/domain.com/httpdocs
===============


Copy Multiple Accounts/Packages From Another Server
Error  ---- basic credential check failed timeout during ssh session
===============
Set  UsePAM no   ---- In sshd config
Increased timeout
Disabled csf 
/etc/init.d/iptable stop
AllowUsers root@sourceIPaddress ----- pico /etc/ssh/sshd_config
===============


Suspend all cpanel user's
================
root@[~]# ll /var/cpanel/users/ | awk {'print $4'} | awk '{system ("/scripts/suspendacct "$1)}'
================


How to SSH to one server from another server
============
# ssh root@source server IP
#password: source server password
============



How to reduce or free space in /usr partition
=====================
http://www.ezlinuxadmin.com/2010/01/reduce-free-space-usr-partition/
http://forums.cpanel.net/f5/how-optimize-size-usr-local-cpanel-149105.html
=====================



How to install Moodle manually?
==========================
http://www.siteground.com/tutorials/moodle/moodle_installation_manual.htm
==========================


Manually Install ImageMagick On A cPanel Server (http://pawapv.wordpress.com/2013/09/08/installing-imagemagick-for-cpanel/)
=============================
1002  mkdir lx24
 1003  cd /lx24/
 1004  ll
 1005  wget ftp://ftp.imagemagick.org/pub/ImageMagick/ImageMagick.tar.gz
 1006  ll
 1007  tar xvfz ImageMagick.tar.gz
 1008  ll
 1009  cd ImageMagick-6.8.6-7
 1010  cd ImageMagick-6.8.8-9/
 1011  ll
 1012  ./configure
 1013  make
 1014  make install
 1015  /usr/local/bin/convert logo: logo.gif
 1016  which convert
 1017  make check

*******************Bind ImageMagick Into PHP using Imagick*******************

For your new ImageMagick installation to work with your web php scripts, you now need to bind it into PHP. To do this using Imagick, just follow the steps below.

Login to WHM and navigate to the “Module Installers” option under “Software” in the left hand menu
On the following page, select the “Manage” link beside the PHP Pecl language option
Enter imagick into the “Install a PHP Pecl” field and then click the install button.
=============================




Helpful Exim Commands:
=====================
/usr/sbin/exim   -M   email-id        => Force delivery of one message
/usr/sbin/exim -qf                  => Force another queue run
/usr/sbin/exim -qff                 => Force another queue run and attempt to flush the frozen message
/usr/sbin/exim  -Mvl   messageID  => View the log for the message
/usr/sbin/exim  -Mvb  messageID  => View the body of the message
/usr/sbin/exim  -Mvh  messageID  => View the header of the message
/usr/sbin/exim -Mrm  messageID  =>  Remove message without sending any error message
/usr/sbin/exim  -Mg  messageID   =>  Giveup and fail message to bounce the message to the Sender

/usr/sbin/exim -bpr | grep “<” | wc -l    =>Number of emails in the que
/usr/sbin/exim -bpr | grep frozen | wc -l   => How many Frozen mails on the queue
/usr/sbin/exim -bpr | grep frozen | awk {‘print $3'} | xargs exim -Mrm   =>  Deleteing Frozen Messages

To flush the exim queue:

1. login to your server via ssh as root.
2. Type: exim -qff
=====================



Wordpress Error  -   Forbidden
You don't have permission to access /blog/wp-login.php on this server.
=============
The solution is to add this to the beginning of your .htaccess

<Files wp-login.php>
Order Deny,Allow
Deny from all
Allow from all
</Files>
=============



How to reset the password litespeed web admin   ------  ( Refer this URL: http://www.litespeedtech.com/support/forum/threads/lsws-change-password-via-ssh.5351/)
===================
cd /usr/local/lsws/admin/misc (instead of /usr/src/lsws/lsws-4.1.4/admin/misc)
./admpass.sh
===================



To update Open SSL
======================
1) Self-managed CloudLinux
=> 
1. yum clean all
2.  yum update openssl
3.  cagefsctl --force-update (only if you have cagefs installed do you need to run this command, if you do not have this installed skip to step 4)
4.  /etc/init.d/httpd stop
5. /etc/init.d/httpd start
 
 
2) Self-managed cPanel servers
=>
1. SSH to your server
2. yum update openssl
3. /scripts/upcp —force
4. /etc/init.d/cpanel restart
5.  stop apache with the command: service httpd stop
6.  kill any remaining apache processes
7.  start apache with command: service httpd start
8.  Please test your server at http://filippo.io/Heartbleed/ to confirm the server is patched.
9.  If your server still shows vulnerable still after step #8 we have found it is necessary to recompile apache.  Recompile apache and run step #8 again. 

or Go to WHM » Software » Update System Software and update all things
======================



Fixing time drift in the servers (syncing with time servers)   ----------------------  Refer this URL: (http://sakafi.wordpress.com/2008/05/22/fixing-time-drift-in-the-servers-syncing-with-time-servers/)
=========================
# rdate -p rdate.cpanel.net ;date   ------------- check current remote time and current system time
# rdate -s rdate.cpanel.net ;date   ------------  sync remote time to system time.
# hwclock –systohc   ----------- To setup hardware clock in the server
Now execute the same command (step1) after one or two minutes and see the drift in time. Check whether it increases or decreases.
Find ticket rate using # tickadj
=========================




How to install ClamAV on CentOS 
+==========================================================+
(Refer this URL: http://www.etctips.com/how-to-install-clamav-on-centos-6-5/ ,
http://linuxhostingsupport.net/blog/how-to-install-clamav-antivirus-on-linux-cpanel)
=======================
CentOS 64bit  - rpm -Uvh http://download.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
CentOS 32bit - rpm -Uvh http://mirror.overthewire.com.au/pub/epel/6/i386/epel-release-6-8.noarch.rpm
yum install clamav clamd
/etc/init.d/clamd start
==========================
+==========================================================+



How to change the primary IP addres of a WHM/cPanel server
==================
Refer this http://www.codero.com/knowledge-base/questions/248/How+to+change+the+primary+IP+addres+of++a+WHM%7B47%7DcPanel+server

Steps in WHM:

Log into WHM and go to Basic cPanel & WHM Setup
Change the Primary IP here with the option that says "The IP address (only one address) that will be used for setting up shared IP virtual hosts"
Note: This might not actually be necessary.
Log in to SSH, and do the following:

Edit /etc/sysconfig/network-scripts/ifcfg-eth0
Change the IPADDR and GATEWAY lines to match the new IP and Gateway for the new ip
Edit /etc/sysconfig/network
Change the GATEWAY line here if it does not exist in the ifcfg-* file.
Edit /etc/ips
Remove the new primary IP from this file if it is present
Add the old primary IP to this file with the format <IP address>:<Net Mask>:<Gateway>
Edit /var/cpanel/mainip
Replace the old primary IP with the new primary IP
Edit /etc/hosts
Replace the old primary IP with the new one if needed. The hostname's dns will need to be updated too
Restart the network service to make the new IP the primary
service network restart
Note: You're probably going to be disconnected at this point, and have to log in to ssh using the new primary ip.
Restart the ipaliases script to bring up the additional IPs
service ipaliases restart
Run ifconfig and make sure all IPs show up correctly
Update the cpanel license to the new primary IP
Verify you can still log in to WHM and there is no license warning
http://verify.cpanel.net/index.cgi
==================



How to use Zcat commnad (Refer this URl: http://www.commandlinefu.com/commands/using/zcat)
===========
zcat Filename.tar.gz | grep -a -i "String"
===========


Server optimization for Magento Site
==============================
http://www.magentocommerce.com/knowledge-base/entry/how-do-i-know-if-my-server-is-compatible-with-magento
http://magento.com/resources/system-requirements
=============================



How to install cassandra on CentOs
Refer this URL: http://lancegatlin.org/tech/centos-6-install-apache-cassandra-using-datastax
http://crawnix.in/cassandra-thrift-centos/
=====================
  565  java -version   ( If  Java is not installed then install Tomcat from easyapache)
  566  yum install jna
  567  service cassandra status
  568  rpm -Uvh http://dl.fedoraproject.org/pub/epel/5/i386/epel-release-5-4.noarch.rpm
  569  yum install jna
  572  cd /etc/yum.repos.d/
  573  ll
  574  vi /etc/yum.repos.d/datastax.repo
  575  ll
  576  yum install dsc1.1
  577  service cassandra status
  578  yum install cassandra12
  581  java
  582  cd /usr/share/cassandra/lib
  585  ll
  586  wget https://maven.java.net/content/repositories/releases/net/java/dev/jna/jna/3.5.1/jna-3.5.1.jar
  587  chown cassandra:cassandra jna-3.5.1.jar
  588  ll | grep jna-3.5.1.jar
  589  chmod 755 jna-3.5.1.jar
  590  ll | grep jna-3.5.1.jar
  591  chown -R cassandra:cassandra /var/lib/cassandra
  592  chown -R cassandra:cassandra /var/log/cassandra
  593  cd /etc/profile.d/
  594  ll
  595  pico cassandra.sh
  596  pico /etc/csf/csf.conf
  597  csf -r
  598  /usr/local/cassandra/bin/cassandra -f &amp;
  601  service cassandra start
  602  service cassandra status
  603  cat /etc/sysconfig/iptables 
  604  pico /etc/sysconfig/iptables 
  605  /etc/init.d/iptables restart
  606  /etc/init.d/iptables restart
  607  service cassandra restart
  608  service cassandra status
=====================



How to configure autoFTP backup on openvz node
=================
http://linuxbytknalla.blogspot.in/2012/12/autoftpbackup-configuration-on-openvz.html
=================



To clean up memory on the dedicated server  (For the VPS, need to reboot the server to cleanup the memory)
===============
echo 3 > /proc/sys/vm/drop_caches
================


Send an email from the server
=============
echo “Test Email” | mail -v -s “This is a Test Email” testmail@yahoo.com
=============



Email Issue (R=lookuphost defer (-1): host lookup did not complete)
Please refer this URL: http://linuxchaser.wordpress.com/2013/08/26/lookuphost-defer-1-host-lookup-did-not-complete/
http://crybit.com/rdkim_lookuphost-defer-1-host-lookup-did-not-complete/
===============
1) check hostname and hostip
# hostname
# hostname -i

2) check for resolvers and set correct resolvers.
vi /etc/resolv.conf
Or
WHM » Networking Setup » Resolver Configuration
////  xx.x.xxx.x indicates Resolvers Ip:
Primary Resolver xx.x.xxx.x
Secondary Resolver xx.x.xxx.x

3) Check and correct dns records for mail records of domain.

4)
/etc/init.d/exim restart
/etc/init.d/courier-authlib restart
/etc/init.d/courier-imap restart
/etc/init.d/dovecot restart
===============


SolousVm Commands
===================
vzlist -a  ---------- To list all the servers present on the node
vzctl enter CTID  -----  To login to particular server
===================


MySQL Server Won’t Start : PID File Errors
================
http://www.plugged.in/databases/mysql-server-wont-start-pid-file-errors.html
===============


Mysql error - [ERROR] Fatal error: Can't open and lock privilege tables: Table './mysql/user' is marked as crashed and should be repaired   

Refer this URL: 1) http://techietent.blogspot.in/2013/03/table-mysqluser-is-marked-as-crashed.html
					 2) http://techietent.blogspot.in/2013/02/how-repair-all-database-tables.html
===============
root@ranjith [/var/lib/mysql/mysql]# service mysql start --skip-grant-tables
now with mysql started, you can repair the mysql/user table
root@ranjith [/var/lib/mysql/mysql]# mysqlcheck -r mysql user
root@ranjith [/var/lib/mysql/mysql]# service mysql stop
Shutting down MySQLs [ OK ]
root@ranjith [/var/lib/mysql/mysql]# service mysql start
Starting MySQL [ OK ]
===============




Mysql Commands
============================================================
 Here the command for repair, alalyze or optimze all database talbes in server.

# mysqlcheck -u root -p --auto-repair --check --optimize --all-databases

Below commands are also do the same without mysql root password:

For Repair:

# mysqlcheck --all-databases -r

For Analyze:

# mysqlcheck --all-databases -a

For optimize:

# mysqlcheck --all-databases -o
============================================================



Squirrel mail Issue (ERROR: Connection dropped by IMAP server. Query: SELECT "INBOX
===================
Then delete all files named " dovecot "in the path "/home/user/mail/domainname.com/user"
rm -f dovecot
===================



How to install Malware Detect (Maldet) for CentOS 6 / Linux
=======================
Malware Detect is very easy to install on CentOS, regardless of the control panel you utilize (cPanel/WHM, Directadmin, etc). Maldet also known as Linux Malware Detect virus scanner for Linux.
There is nothing complicated in installation process, but root access to your server is required. 

Installation via SSH

cd /usr/local/src/
wget http://www.rfxn.com/downloads/maldetect-current.tar.gz
tar -xzf maldetect-current.tar.gz
cd maldetect-*
sh ./install.sh 
maldet --update-ver
maldet --update[/i]
=======================



ConfigServer Internal Server Error 500, after cPanel update: fixed
=================
To resolve this error simply SSH into your server as a root user and run the following command from command line:

curl -s http://download.configserver.com/csupdate | perl

This script will update: cmm, cmc, cmq, cse, csf, cxs, msinstall, msfe
=================



How to install Monitis load monitoring agent on linux server
==================
http://www.monitis.com/support/server-device-monitoring/install-monitis-agent/install-linux-agent/
==================



How to install CMQ - (Please refer -http://configserver.com/free/cmq/INSTALL.txt)
===================
wget http://configserver.com/free/cmq.tgz
tar -xzf cmq.tgz
cd cmq/
sh install.sh
=================



http://support.mailpoet.com/knowledgebase-category/spam/   -------------- Spam check URL



Fix SolusVM Time Zone Issue with VMS (Refer this URL: http://easylinuxalways.blogspot.in/2013/03/fix-solusvm-time-zone-issue-with-vms.html)
====================
1- Go to your virtual machine (CTID in solusvm lets say it's 101)
2- rm /etc//localtime
3- ln -s /usr/share/zoneinfo/EST /etc/localtime

Now ssh to you solusvm machine main machine:

rm /etc//localtime
ln -s /usr/share/zoneinfo/EST /etc/localtime

ntpdate us.pool.ntp.org

This will sync the time

now run the cron every night to sync time
crontab -e

0 0 * * * ntpdate us.pool.ntp.org 
===================



To check server outgoing connection
================
ss -tp
================



inode commands
=================
1) For dedicated customers you can check the inodes of an account on your server by using SSH:
=> quota -s <cpanel username>

2) If you have SSH access to your account you can view the inodes for a specific folder using the following command:
=> echo "Detailed Inode usage for: $(pwd)" ; for d in `find -maxdepth 1 -type d |cut -d\/ -f2 |grep -xv . |sort`; do c=$(find $d |wc -l) ; printf "$c\t\t- $d\n" ; done ; printf "Total: \t\t$(find $(pwd) | wc -l)\n"

3) To display inode in the stats of Cpanel account
=> WHM -> Tweak Settings -> "Display File Usage information in the cPanel stats bar (inode count)"
=================



cPremote Plug-in installation
===================
Refer : http://cpremote.net/Installation-of-cPremote
===================


CPremote backup restoration Commands
===================
Restore email folder of cpanel user CPUSER from the daily backups
/scripts/cpremoterestore --user=CPUSER --from=daily --type=mail

Restore Document root from weekly backup for CPUSER
/scripts/cpremoterestore --user=uweschaf --from=weekly --type=www

Restore the complete home folder of CPUSER from monthly backup
/scripts/cpremoterestore --user=CPUSER --from=monthly --type=homefolder

Restore a full account from daily backup
/scripts/cpremoterestore --user=CPUSER --from=daily --type=full
===================



cPremote Documentation
=================
http://cpremote.net/Documentation
=================



Command to check failed email login attempts 
================
grep "535 Incorrect" /var/log/exim_mainlog | awk -F"set_id=" '{print $2}' | sort | uniq -c | sort -n
==============


Ip related commands
==============
ifconfig
ip a
ip r l
iptables-save
brctl show
==============



All SolousVM commands
===========
http://openvz.org/User_Guide/Operations_on_Containers#Suspending_Container
===========


cyberduck FTP client settings for MAC
============
http://www.simplehelp.net/2007/11/05/how-to-use-cyberduck-to-ftp-files-in-os-x/
=============



How to detect old versions of joomla & Wordpress from command line:
===================
locate joomla/version.php | grep -v virtfs | xargs grep "\$RELEASE" | grep -v cpbackup 2>/dev/null
locate wp-includes/version.php | grep -v virtfs | xargs grep "wp_version = " 2>/dev/null===================

root@linux36 [/var/log]# grep 'Joomla v1' cxs.log
===================



how to increase phpmyadmin import file size
==============
 pico /usr/local/cpanel/3rdparty/etc/phpmyadmin/php.ini
 post_max_size = 55M 
 upload_max_filesize = 55M
==============


Mysql Error - InnoDB: Unable to lock ./ibdata1, error: 11
================
To fix this issue, make a copy of the original files (ibdata1, ib_logfile0, ib_logfile1…).

mv /var/lib/mysql/ibdata1 /var/lib/mysql/ibdata1.bak

cp -a /var/lib/mysql/ibdata1.bak /var/lib/mysql/ibdata1

Now start mysql service.

/etc/init.d/mysql start
================



Mysqldump one table - Taking dump of only one table
=============
Dump -  mysqldump db_name table_name > table_name.sql
restore - mysql -u -p mydatabase < table1.sql
=============


Suspend all accounts in cPanel via SSH
=============
ll /var/cpanel/users/ | awk {'print $4'} | awk '{system ("/scripts/suspendacct "$1)}'
=============


How to reduce size of ibdata1 file in MySQL
===========
http://dba.stackexchange.com/questions/16747/mysql-clean-ibdata1
http://stackoverflow.com/questions/3456159/how-to-shrink-purge-ibdata1-file-in-mysql
http://www.arborisoft.com/how-to-reduce-size-of-ibdata-file-in-mysql/
http://erikimh.com/how-to-shrink-an-ibdata1-file-with-minimal-mysql-downtime/
============



grep " \*\* " exim_mainlog 


To install CMM
===============
http://download.configserver.com/cmm/INSTALL.txt
===============


How to install Fantastico
===================
82  cd /usr/local/cpanel/whostmgr/docroot/cgi
   83  wget -N http://files.betaservant.com/files/free/fantastico_whm_admin.tgz
   84  ll
   85  tar -xzpf fantastico_whm_admin.tgz
   86  ll
   87  rm -rf fantastico_whm_admin.tgz
   88  /usr/local/cpanel/bin/register_appconfig
   89  pico  /var/cpanel/cpanel.config
   91  /usr/local/cpanel/etc/init/startcpsrvd
 ===================
 
 
 
 How to install LiteSpeed on a WHM/cPanel Server?
=================
You can install litespeed on a WHM/Cpanel server by simply following the bellow steps.

1. Log into server via SSH as ‘root’ user.
2. Go to /usr/src
cd /usr/src
3. Download the installation file using wget.
wget http://www.litespeedtech.com/packages/cpanel/lsws_whm_plugin_install.sh
4. chmod 700 lsws_whm_plugin_install.sh
5. sh lsws_whm_plugin_install.sh ( ./lsws_whm_plugin_install.sh)
6. rm -rf lsws_whm_plugin_install.sh
7. Log into WHM. Go to manage pluggins section.
8. Start the installation procedure by clicking on ‘Install LiteSpeed’.
9. This will ask you to enter your license information and admin password. Enter these information and click on ‘Build matching PHP Binary’. (Please do not tick the box to start LiteSpeed immediately).
10. Click on Switch to LiteSpeed
11. Click on Admin Web Console and login
12. Final stages of setup
Go to Configuration > General > Index Files > Edit
You need to set the following and save.
===============================================
Index Files: index.html, index.php, index.php5, index.htm
Auto Index: Yes
Auto Index URI => /_autoindex/default.php
In SSH Type:
ln -sf /usr/local/lib/php/autoindex /usr/local/lsws/share/autoindex
================================================
13. Go to Configuration > Log > Server Log > Edit
Set the following:
===============
Log Level: Info
Debug Level: None
===============
14. Finally click on Actions > Graceful Restart to make these changes permanent.

Now, you have successfully installed Litespeed on WHM/cpanel server.
=====================



How to install RVSoftGlobe Manager
============
https://rvglobalsoft.com/installation/
==========




Redirecting non-www to www with .htaccess
=============
RewriteEngine On
RewriteCond %{HTTP_HOST} !^www\.
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}/$1 [R=301,L]
=============


Redirecting www to non-www
============
RewriteEngine On
RewriteCond %{HTTP_HOST} !^my-domain\.com$ [NC]
RewriteRule ^(.*)$ http://my-domain.com/$1 [R=301,L]
============


how to run fsck 
===============
http://blog.zwiegnet.com/linux-server/lv_root-unexpected-inconsistency-run-fsck-manually/
http://forums.cpanel.net/f5/how-run-fsck-74206.html
http://thesystemadministrator.net/cpanel/how-to-force-a-fsck-on-server-reboot
===============


To block entire country IP address in the .htaccess file
==========
http://incredibill.me/htaccess-block-country-ips
==========



How to Increase /tmp partition size in cPanel and secure it
Refer URL:   http://wiki.vps.net/controlpanels/cpanel/increase-tmp-partition-in-cpanel-and-secure-it/

https://hoststud.com/resources/how-to-increasing-the-size-of-tmpdsk-tmp-in-cpanel.78/
https://www.linuxtweaks.in/increase-tmp-partition-size-in-whm-cpanel/
https://grepitout.com/increase-tmp-directory-size-cpanel/
==============
1. Stop cpanel, apache (litespeed), mysql services:

/etc/init.d/cpanel stop
/etc/init.d/httpd stop
/etc/init.d/lsws stop
/etc/init.d/mysql stop

2. Umount /tmp and /var/tmp:

umount -l /tmp
umount -l /var/tmp

3. Move /usr/tmpDSK file to another location (just in case you’ll need to mount it somewhere else to preserve data):

mv /usr/tmpDSK /usr/tmpDSK_back

4. Modify /scripts/securetmp to set tmpdsksize to desired size:

vi /scripts/securetmp

    $tmpdsksize = 2048000

5. Run:

/scripts/securetmp

6. Start cpanel, apache (litespeed), mysql services:

/etc/init.d/cpanel start
/etc/init.d/httpd start
/etc/init.d/lsws start
/etc/init.d/mysql start

That’s it!
================




Suspend account page issue
=====================
In order to properly handle account suspensions you would need to update /var/cpanel/templates/apache2*/main.local to add:

[% IF file_test('f', '/usr/local/apache/conf/includes/account_suspensions.conf') -%]
Include "/usr/local/apache/conf/includes/account_suspensions.conf"
[% END -%]

Above the following entry:

[% IF file_test('f', '/usr/local/apache/conf/includes/pre_virtualhost_global.conf') -%]
Include "/usr/local/apache/conf/includes/pre_virtualhost_global.conf" 
[% END -%]

Afterwards, run `/scripts/rebuildhttpdconf` and restart the Apache webserver.
=====================




bash flaw attack
===============
Refer link - http://www.pcworld.com/article/2687857/bigger-than-heartbleed-shellshock-flaw-leaves-os-x-linux-more-open-to-attack.html
http://apple.stackexchange.com/questions/146849/how-do-i-recompile-bash-to-avoid-the-remote-exploit-cve-2014-6271-and-cve-2014-7/146851#146851
http://securitywatch.pcmag.com/internet/327769-serious-bash-flaw-lets-attackers-hijack-linux-and-mac-computers


To check, run command from root - env x='() { :;}; echo vulnerable' bash -c "echo this is a test"

o/p - vulnerable
this is a test    

=> Need to update bash version (# yum update bash -y)


o/p - 1) this is a test
2) bash: warning: x: ignoring function definition attempt
bash: error importing function definition for `x'
this is a test
=> Nothing need to do be done, its safe.
=================



how to block bots using .htaccess
=============
http://incredibill.me/htaccess-block-user-agent
==============



How to install ntPHPselector (Refer this URL: http://www.nixtree.com/ntphp.php)
=========================
cd /usr/local/src
wget -N http://nixtree.com/download/free/ntphpselector_manage.sh 
sh ntphpselector_manage.sh install


To recompile php in ntPHPselector, run the following command:
sh ntphpselector_manage.sh recompile <option> 

-- option

2 for 5.2
3 for 5.3
4 for 5.4
5 for 5.5

eg: recompile php5.2 
sh ntphpselector_manage.sh recompile 2

For uninstalling the plugin:
sh ntphpselector_manage.sh uninstall
=========================



madserve installation
============
http://www.madserve.org/download.php
============


revive-adserver installation
==========
http://www.revive-adserver.com/download/
==========


If all DNS records are correct and still php site not working, run below command and whitelist timed out ips on the same server.
===========
Go to specific path and then run #strace php index.php
===========


To install php zip extension on the server
=============
Refer - http://rivenlinux.info/adding-php-zip-module/
pecl install zip
 php -i | grep extension_dir
  243  ls -la /usr/local/lib/php/extensions/no-debug-non-zts-20100525/zip.so
  244  ls -la /usr/local/lib/php/extensions/no-debug-non-zts-20100525/
  245  cd /usr/local/lib/php/extensions/no-debug-non-zts-20100525/
  246  chmod 755 zip.so
  247  ll
  248  php -i | grep php.ini
  249  echo "extension=zip.so" >> /usr/local/lib/php.ini
  250  service httpd restart
=============



The following command may be used to list MySQL modules installed in PHP:
 /usr/local/bin/php -m | grep -i mysql
 yum install php-mysqli
 
 
Buzix
=========
grep " \=\= " /var/log/exim_mainlog
========= 


If easy apache fails
================ 
 I simply hid the offending coreutils-libs package from the RPM database:

[10:56:37 825367 root@5658443 ~]cPs# rpm -e --nodeps --justdb coreutils-libs
error: &quot;coreutils-libs&quot; specifies multiple packages:
  coreutils-libs-8.4-37.el6.x86_64
  coreutils-libs-8.4-31.el6_5.2.x86_64
[10:56:55 825367 root@5658443 ~]cPs# rpm -e --nodeps --justdb coreutils-libs --allmatches
[10:57:15 825367 root@5658443 ~]cPs# 
================


how to setup backup on windows server 2008 r2 standard
============
http://technet.microsoft.com/en-in/library/ee849849(v=ws.10).aspx
============


Spoofing
=========
http://support.hostgator.com/articles/specialized-help/email/problems-with-spoof-spf
=========


To check this load of each container on Node
==============
vzlist -o hostname,laverage,veid  --------- To check the load on all the containers present on node
==============


Check process running under Swap Memory
------
for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r | less
------



echo "delete from brutes; delete from logins;" | mysql cphulkd    ------------------ To remove failed logins from cpHulk

exim -qff -v   ---------------- To run and view mail queue forcefully from SSH


OpenVZ help
============
https://openvz.org/User_Guide/Operations_on_Containers
===========


Named failed
==========
http://forums.cpanel.net/f5/named-failed-start-70031.html
=========



Chkservd service
=======
http://kb.veeble.org/Chkservd_service
=======



Swap (Refer https://www.digitalocean.com/community/tutorials/how-to-add-swap-on-centos-6)
========
swapon -s    ----- To check if swap partiotion is present or not.
swapon  -a -e    ------------ To enable swap for all the partiotions 
swapoff
========



Mysqldump Script
+=================+
 #!/bin/bash
baksrc=/var/lib/mysql
bakdst=/backup/mysqlbackup/daily
backupdst=/backup/mysqlbackup/
dumpdb=/usr/bin/mysqldump



ls -lhd  $baksrc/*_* | awk '{print $9}' | cut -d/ -f5  > /root/mysqldd-list

for db in `cat /root/mysqldd-list` ;
do
$dumpdb $db > $bakdst/$db.sql  2> $bakdst/error.log
done
$dumpdb  mysql > $bakdst/mysql.sql 2> $bakdst/error.log

echo " All Databases backup up successfully to folder $bakdst/ "
echo " Check for any errors at : $bakdst/error.log "

echo "|-----------------------------------------------------------------------------------------------------------------|"  
echo "|.................................. Successfully updated daily  ..................................................|"          
echo "|-----------------------------------------------------------------------------------------------------------------|"  
ls -lah $bakdst/ > $bakdst/list.txt
cat $bakdst/error.log >> $bakdst/list.txt

du -sh $bakdst/*

exit 0
+=================+



To update the roundcube email client (inooDB must be enabled on the server to do this)
==============
/usr/local/cpanel/bin/update-roundcube --force
==============



If pure ftp not working, run this command or you can simply disable uploadscript in /etc/pureftpd.conf
=============== 
/usr/sbin/pure-uploadscript -B -r /etc/pure-ftpd.conf
=============== 



Mysql commands
==================
http://www.cyberciti.biz/faq/howto-linux-unix-creating-database-and-table/
https://www.linode.com/docs/databases/mysql/use-mysql-relational-databases-on-centos-5
http://www.rackspace.com/knowledge_center/article/installing-mysql-server-on-centos
===================



MySQL - Resetting a lost MySQL root password
==============
http://www.rackspace.com/knowledge_center/article/mysql-resetting-a-lost-mysql-root-password
==============


Setup FTP Server On CentOS, RHEL, Scientific Linux 6.5/6.4/6.3
============
http://www.unixmen.com/install-vsftpd-server-on-centos-rhel-scientific-linux-6-4/
============


Very useful URL for the different installations
============
http://www.servermom.org/complete-newbie-guide-to-build-centos-server-to-host-websites/
============



Mysql Commands
=================================
mysql -u root -p
Enter server root password ( #cat /root/.my.cnf)
CREATE DATABASE databasename;
CREATE USER username@localhost;
SET PASSWORD FOR username@localhost= PASSWORD("password");
grant all privileges on databasename.* to Databaseuser@localhost identified by 'password';
FLUSH PRIVILEGES;
mysql> show databases;    --------------- To view all the databases present on the server.
mysql> use databasename  ------------- To make the changes under particular DB
mysql> show tables;   ------ To view all the tables from specifc DB
mysql> describe tablename;   ------ To view the content of specific table under the particular DB   ( for e.g. mysql> describe wp_users;)


To reset the wp-admin password of wordpress site from SSH
==============
mysql> SELECT ID, user_login, user_pass FROM wp_users;
+----+------------+------------------------------------+
| ID | user_login | user_pass                          |
+----+------------+------------------------------------+
|  1 | fargo      | $P$BEIZhgIHXUYoUK3o6.TgJ8yWkqmnr7/ |
+----+------------+------------------------------------+
===============


UPDATE (wp_users) SET user_pass="specify the new pasword in MD5 format" WHERE ID = (specify the id of the user which we need to change the password);   ------  To update/Edit particular table entry
For e.g   UPDATE (wp_users) SET user_pass = MD5(‘”change12@”‘) WHERE ID = (1);
===================================



Google Authenticator
===============
http://www.cyberciti.biz/open-source/howto-protect-linux-ssh-login-with-google-authenticator/
===============


============
/scripts/addpop  email ID  password  --------- Create an email ID from SSH
/scripts/delpop  email ID  ----------- Delete an email ID from SSH
============



roundcube connection to imap server failed dovecot
==============
http://linuxonlinetutorial.blogspot.mx/2013/06/login-isues-in-hordesquirrel-mail-and.html
==============


404 not found: (password protected direcotry in .htaccess)
==============
AuthType Basic
AuthName "staging"
AuthUserFile /home/rachelwa/.htpasswds/public_html/staging/passwd
Require valid-user

ErrorDocument 401 default
==============



To enable Tun-tap module in OpenVZ  (http://crybit.com/how-to-enablecheck-tuntap-module-in-vpsopenvz/)
===============================
[root@Node]# modprobe tun
[root@Node]# lsmod | grep tun
tun    82432  6

vzctl set 116 --devnodes net/tun:rw --save
vzctl set 116 --devices c:10:200:rw --save 
vzctl stop 116 
vzctl set 116 --capability net_admin:on --save
vzctl start 116 
vzctl exec 116 mkdir -p /dev/net
vzctl exec 116 chmod 600 /dev/net/tun
===============================


Find Out What Process Are Using Swap Space : 
=====
for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r | less
=====


How to install r1Soft/idera Agent on CentOS, RHE and Fedora
==================
http://wiki.r1soft.com/display/CDP3/Installing+Agent+on+CentOS,+RHE+and+Fedora
==================


HowTo: Upgrade CentOS Linux 6.4/6.3/6.2/6.1/6.0 to v6.5
===============
http://www.cyberciti.biz/faq/upgrade-to-centos-6-5-from-centos-linux-6-4-6-3-6-2-6-1-6-0/
================


Cloud Linux installation on centOS/cPanel server
=====================
wget http://repo.cloudlinux.com/cloudlinux/sources/cln/cpanel2cl
sh cpanel2cl -k <activation_key>   ------------ Get the trail license for this from http://docs.cloudlinux.com/  >>> Trail license.
reboot
=====================



Disable/enable cPHulk from the command line
=============
/usr/local/cpanel/bin/cphulk_pam_ctl --disable
/usr/local/cpanel/bin/cphulk_pam_ctl --enable
/scripts/cphulkdwhitelist  IP
/scripts/cphulkdblacklist  IP
https://www.example.com:2087/scripts2/doautofixer?autofix=disable_cphulkd     -------------  cPanel autofix script from WHM
============


Cloud Linux Modules installations
=================
yum install cagefs lvemanager   ---- CageFS, LVE installation
yum groupinstall alt-php    ---------- PHP selector installation
yum update cagefs lvemanager
=================



KernelCare Installation  ( Need to purchase license for full version)
===============
To install KernelCare on RPM based system, run: 
$ rpm -i http://patches.kernelcare.com/kernelcare-latest.x86_64.rpm

To check if patches applied: 
$ /usr/bin/kcarectl --info

If you would like to run update manually: 
$ /usr/bin/kcarectl --update
===============


gtmetrix.com
===========
To check for the website spped and its optimization things
===========


Installating Slave on SolusVM
============
https://documentation.solusvm.com/display/DOCS/Installing+a+Slave
============



Error: Domain has exceeded the max defers and failures per hour allowed
Refer http://www.lilio.com/helpdesk/knowledgebase.php?action=displayarticle&id=29)
https://forums.cpanel.net/threads/domain-example-com-has-exceeded-the-max-defers-and-failures-per-hour-5-5.296962/
/var/cpanel/email_send_limits/max_deferfail_example.com
Deleting this file fixed the problem immediately.
==============
If your email is returned with error messages similar to the following, you may have sent too many bounced or deferred messages within one hour.
Domain has exceeded the max defers and failures per hour (5/5 (100%)) allowed. Message discarded.

To avoid misuse by spammers and subsequent blacklisting of the server in spam databases, all email errors are tracked. If more than 50% of email sent from a particular domain within one hour is bounced or deferred by the recipient server, a temporary block on sending additional email will be activated for that domain. After the hour has passed, this block will be automatically lifted.
Important terms
Bounced: Any email messages that are returned with an error status.
Deferred: This usually indicates that the message could not be delivered to the recipient's server, but that additional attempts will be made. In most cases, email servers will attempt to deliver deferred messages several times over a 24 hour period. If the receiving email server becomes available again within this time period, the message will be delivered.
=================



Wordpress issue - Unable to create directory uploads/2015/01
=====================
To Fix this issue >> Login to wp-admin >> Setting >> Media >> Upload Folder >> put this path as the default path (wp-content/uploads)
=====================



How to update awstats for the single account  (Please refer http://forums.cpanel.net/f5/awstats-not-updating-31256.html)
============
1 ) vi /home/username/tmp/awstats/awstats.yourdomain.com.conf

AllowToUpdateStatsFromBrowser=1

2) whm==> tweak settings===> allow users to update from cpanel

3) The Awstats can be updated by using the script /scripts/runweblogs accountname

If the issue is still exists please run the following command from the shell 

/usr/local/cpanel/3rdparty/bin/english/webalizer -N 10 -D /home/username/tmp/webalizer/dns_cache.db -R 250 -p -n domain.com -o /home/username/tmp/webalizer /usr/local/apache/domlogs/domain.com
===========



To whiltelist mod_security rule for the particular domain
==================
/usr/local/apache/conf/userdata/ssl/2/cPanel username/domainname/modsec.conf
==================



How to install WHOIS
===============
yum install jwhois

To use it - whois domainname
===============



How to Remove IP from cpHulk Bruteforce Blacklist
=========================
mysql> use cphulkd;
mysql> select IP, BRUTETIME from brutes order by BRUTETIME;
mysql> select IP, LOGINTIME FROM logins order by LOGINTIME;
mysql> DELETE FROM brutes/logins WHERE IP='115.239.228.35';

To delete all the brute force entries of blocked IPs,

mysql> delete from brutes;
mysql> delete from logins;
=========================



Linux - what process is using swap and how much of it:  swap partition full then run the following commands:
=========================
#for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r
#swapoff -a
#swapon -a -e
=========================



Recover eximstats Database tables
====================
/usr/local/cpanel/bin/updateeximstats    ----------------- It  generate a new instance of the table.
To clear it use following steps

Go to mysql

mysql

use eximstats;

Then from with the query browser run

delete from sends;
delete from smtp;
delete from failures;
delete from defers;
====================



Disabling/Uninstalling FrontPage Extensions in cPanel
===================
In WHM:
Navigate to Home >> FrontPage >> Uninstall FrontPage Extensions.
Select the account for which you would like to uninstall the extensions.
Click UnInstall.

Or

From the command line:
Run /scripts/unsetupfp4 –all as the root user.
We strongly recommend that you rebuild EasyApache without FrontPage® before you attempt to upgrade.
===================



Atomic ModSecurity Rules
======================
https://www.atomicorp.com/wiki/index.php/Atomic_ModSecurity_Rules#Step_5:_Create_the_whitelist_file
https://www.atomicorp.com/wiki/index.php/Mod_security
======================


Disabling Mod_security per domain
===============
 mkdir -p /usr/local/apache/conf/userdata/std/2/Username/domain.com
 cd /usr/local/apache/conf/userdata/std/2/Username/domain.com
 touch vhost.conf
 
 pico vhost.conf
  <IfModule mod_security2.c>
  SecRuleEngine Off
  </IfModule>

  /scripts/ensure_vhost_includes --user=Username
===============



yum error “Cannot retrieve metalink for repository: epel. Please verify its path and try again” updating ContextBroker
===========
yum --disablerepo=epel -y update  ca-certificates
============



Change default MySql Storage engine
==============
The easiest way to change the default engine is to log on phpMyAdmin and then go to Variables >> storage engine
click edit and type InnoDB.
==============



cPanel Different plugins
==================
http://thecpaneladmin.com/plugin-database/
=================



To copy the data from one drive to another drive 
============
e.g. dd if=/dev/sdd of=/dev/sdb  (It will copy all the data from sdd drive to sdb drive)
============


To format drive/partition
=================
mkfs.filesystemextension  Drive/Partition name
e.g. mkfs.ext3 /dev/sdb  (It will format sdb partition with ext3 filesystem)
=================


Mount command
=========
mount drivename directoryname
e.g. mount /dev/sdb /newbackup (It will mount sdb drive on newbackup directory
and add below in /etc/fstab for mounted partition
/dev/sdb       /newbackup                       ext3     defaults       0 0
=========




Call upload script 
----------
/usr/sbin/pure-uploadscript -B -r /etc/pure-ftpd.conf
----------


sohoadmin your session has expired site
=================
Make sure that this parameter is "On" in phpinfo "session.auto_start"
=================



=============
openssl s_client -connect www.sandbox.paypal.com:443
=============




For spamming issue
======================
1. cat /var/spool/exim/input/*/* | grep "auth_id" | awk '{print $2}' | sort | uniq -c | sort -n

2. cd /usr/local/src;
rm -fv emailpasswordreset.sh;
wget vpsmi084.hostpapavps.com/emailpasswordreset.sh;
chmod +x emailpasswordreset.sh;
sh /usr/local/src/emailpasswordreset.sh
wget vpsmi084.hostpapavps.com/mailscam.sh
sh /usr/local/src/emailpasswordreset.sh

3. grep -lr 'accounts@flybluewater.com.au' /var/spool/exim/input | \sed -e 's/^.*\/\([a-zA-Z0-9-]*\)-[DH]$/\1/g' | xargs exim -Mrm

4. exim -bpr | grep frozen | awk {'print $3'} | xargs exim -Mrm;

5. exim -bpru | grep 'woolnerholdings.ca' | awk {'print $3'}| xargs exim -Mrm;

exiqgrep -o 8 -i |  xargs exim -Mrm

service exim restart

exim -bpc

sh  /root/sysutils/tools/mailscam.sh
======================



ClamAV Error:
ERROR: Can't open /var/log/clamav/freshclam.log in append mode (check permissions!).
ERROR: Problem with internal logger (UpdateLogFile = /var/log/clamav/freshclam.log).
===============
Solution: 

touch /var/log/clamav/freshclam.log
chown clamav /var/log/clamav/freshclam.log
chmod 666 /var/log/clamav/freshclam.log
freshclam
===============


Mailman Email Archving not working
==============
Run manually:
/usr/local/cpanel/3rdparty/mailman/bin/arch 
/usr/local/cpanel/3rdparty/bin/python -S /usr/local/cpanel/3rdparty/mailman/cron/nightly_gzip
fs.protected_symlinks_allow_gid with mailman gid to sysctly on all affected servers
==============



Install particular PHP module without running Easyapache on cpanel server
Refer:- http://www.ayyolinux.com/install-php-module-in-cpanel-server-without-running-easyapache/
http://crybit.com/20-common-php-compilation-errors-and-fix-unix/
=============
/home/cpeasyapache/src/php-5.5.29/ext/
- phpize (this will create ./configure command )
- ./configure
- make
- make test
- make install
then add this to server php.ini file --- extension="extensionname.so"
service httpd restart
=============


tcpdump -A -s 0 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)' > /root/tcpdump15102015-http


Installing Twig C extension
============
http://blog.starcklin.com/2014/04/installing-php5-twig-extension/
============


How to install pdflib php extension
==============
http://forum.ahosting.net/f19/pdflib-installation-cpanel-577.html
http://www.mickgenie.com/howto-install-pdflib-lite-and-pdflib-on-centos-server/
==============

To rebuild SNI
===========
/scripts/build_mail_sni --rebuild_map_file --rebuild_dovecot_sni_conf
===========


Installing mailparse
=============
pecl install mailparse
extension=mailparse.so   -- Add it to php.ini & restart httpd service.
=============

tcpdump command to monitor network traffic
==========
Refer http://www.slashroot.in/packet-capturing-tcpdump-command-linux
==========

How to enable FTP account for a suspended user on cpanel?
===========
vi /etc/vftp/CPUsername
What you will have to do is just remove the double exclamation mark “!!” after the colon which is followed by username
CPUsername:!!$1$OwLDOXwc$eA9lg8.:1852:1846::/home/CPUsername:/bin/ftpsh
CPUsername_logs:!!$1$OwL$eoa9lg8.:1852:1846:highw703:/usr/local/apache/domlogs/CPUsername
wq!
===========


Moving /var/cagefs directory
==================
http://docs.cloudlinux.com/index.html?moving__var_cagefs_directory.html
https://helpdesk.cloudlinux.com/index.php?/Knowledgebase/Article/View/85/0/how-do-i-move-varcagefs-to-other-place-cause-of-low-disk-space-on-var
==================


To kill mysqladmin sleep processes
============
mysqladmin proc | grep Sleep | awk '{print $2}' | while read LINE; do mysqladmin kill $LINE; done
============
 
 
symlinks
=============
find . -type l -printf '%p -> %l\n'     ---- To find out list symlinks recursively
ls -la | grep ^l   --- To find out list symlinks in current directory.
=============


Partition Auditing for /home
=============
find / -size +1G -exec ls -hl {} \; | awk {'print $5, $9'} > /root/dc.txt &
find . -type f -name "*log*" -size +1G -exec du -sh {} \;
ll /home/*/backup*tar.gz | awk {'print $9'} | xargs du -sh | grep G
find /home/* -maxdepth 5 -mtime +5 -name "backup*tar.gz" -exec du -sh {} \;
find /home/* -maxdepth 5 -mtime +5 -name "cpmove*tar.gz" -exec du -sh {} \;
find /home/* -maxdepth 5 -mtime +5 -name "*.tar.gz" -exec du -sh {} \; | grep G
find /home/* -maxdepth 5 -mtime +5 -name "*.zip" -exec du -sh {} \;
find . -name "*.sql" -size +1G -exec du -sh {} \;
find /home/*/softaculous_backups/* -mtime +15 -exec du -sh {} \;
find home/*/fantastico_backups -name '.*' -mtime +15 -exec rm {} \;
find /home/*/tmp/Cpanel_Form_file.upload.* -mtime +0 -exec rm {} \;
find /home/. -name "error_log" -size +1G -exec du -sh {} \;
find /home/. -name "debug.log" -size +1G -exec du -sh {} \;
find /home/* -name core.[0-9]* -exec rm -vf {} \;
find . -name "error_log" -size +1G -exec ls -lh {} \;
find /home -type f -name debug.log -print -delete
	
find . -type f -name "download_*tar.gz" -delete -print
find . -type f -name "wp*tar.gz" -delete -print


find -type d -not -perm 775 -o -type f -not -perm 664
find \! -perm 755 -type d
=============

grep domainname /usr/local/apache/logs/error_log | grep ModSecurity | grep id | awk {'print $28'} | sort | uniq -c | sort -n

How to install PHP opcache extension
==================
Login to the server >> first check if its alread installed or not by using below command
php -v. Also, please make sure that do not install opcache if xcache is enabled.


cd /home/cpeasyapache/src/php-5.5.29/ext/opcache/
phpize
./configure
make
make install
php --ini
pico /usr/local/lib/php.ini

Add below line in php.ini
=========
zend_extension=/usr/local/lib/php/extensions/no-debug-non-zts-20121212/opcache.so
opcache.enable=1
opcache.enable_cli=1
opcache.memory_consumption=128
opcache.interned_strings_buffer=8
opcache.max_accelerated_files=4000
opcache.revalidate_freq=60
opcache.fast_shutdown=1
=========

/scripts/restartsrv htpd

To check if it's installed or not, run php -v
==================


screen -S sessionname -p 0 -X quit  ---To terminate screen session.


InnoDB Crash Recovery
=================
http://www.cpanelkb.net/recover-innodb-table-corruption/
https://forums.cpanel.net/threads/innodb-corruption-repair-guide.418722/
http://www.electrictoolbox.com/find-innodb-tables-mysql/
http://www.cpanelkb.net/recover-innodb-table-corruption/
=================


===========
find . -name 'filename' -type f -mtime +1 | xargs rm -f; ----It will remove mentioned files which are older than 1 day or so
===========


Saltstack 
=============
https://wiki.archlinux.org/index.php/Saltstack
https://docs.saltstack.com/en/getstarted/fundamentals/remotex.html
https://docs.saltstack.com/en/latest/topics/installation/arch.html
https://docs.saltstack.com/en/latest/topics/tutorials/modules.html
=============


How to change a wordpress theme via the database
========
http://www.inmotionhosting.com/support/edu/wordpress/change-theme-in-db
========

ERROR: CANNOT REDECLARE IMAGEPALETTETOTRUECOLOR() ON SPIP
=========
Refer http://www.llew.me/tips/error-cannot-redeclare-imagepalettetotruecolor-on-spip/=========
=========

How to Manipulate Filenames Having Spaces and Special Characters in Linux
==========
http://www.tecmint.com/manage-linux-filenames-with-special-characters/
==========


Moving a WordPress Site with Cherry Framework: A Little Tip for LESSPHP Errors
---------
Refer http://smallmouthmediagroup.com/moving-wordpress-site-cherry-framework-tip-lessphp-errors/
---------


How to Add an Admin User to the WordPress Database via MySQL
=============
http://www.wpbeginner.com/wp-tutorials/how-to-add-an-admin-user-to-the-wordpress-database-via-mysql/
=============

How to Block Unwanted Bots from Your Website with .htaccess
==============
http://www.thesitewizard.com/apache/block-bots-with-htaccess.shtml
http://www.inmotionhosting.com/support/website/server-usage/identify-and-block-bad-robots-from-website
==============

How to install PHP APC extension
===============
http://www.networkredux.com/answers/hosting/control-panels/whm-cpanel/how-do-i-install-apc-cpanel
===============


SMTP Error (-1): Connection to server failed
==============
1- This error is typically seen due to a setting in the CSF firewall or another firewall. It might be caused by having the following set:

SMTP_BLOCK = 1
SMTP_ALLOWLOCAL = 0
You would need to change SMTP_ALLOWLOCAL to 1 to enable webmail to function.

2- Check for root@hp160 [~]# cat /var/log/maillog | grep children
Dec 13 03:40:53 hp160 spamd[13640]: prefork: adjust: 0 idle children less than 1 minimum idle children. Increasing spamd children: 631146 started.
Dec 13 03:40:54 hp160 spamd[13640]: prefork: adjust: 2 idle children more than 1 maximum idle children. Decreasing spamd children: 631146 killed.
Dec 13 03:40:56 hp160 spamd[13640]: prefork: adjust: 0 idle children less than 1 minimum idle children. Increasing spamd children: 631216 started.

# cat /etc/cpspamd.conf | grep child
maxchildren=6

Further increase the value of maxchildren in order to resolve this issue.
==============


How to block/prevent xmlrpc.php/wp-login.php attack
================
http://www.akamaras.com/cpanel/how-to-block-brute-force-attacks-against-wp-login-php-on-a-cpanel-server-using-csf/
https://www.mnxsolutions.com/apache/blocking-wordpress-brute-force-attacks-against-wp-login-php.html
http://blog.hostpair.com/how-to-blockprevent-xmlrpc-php-attack/
https://hostingfixes.wordpress.com/2014/08/30/check-and-block-wordpress-and-xmlrc-attack-on-a-cpanel-server/
================


List xmlrpc/wp-login attack ips
===========
egrep 'wp-login.php' /usr/local/apache/domlogs/* | grep -v ftp_log | awk -F : '{print $2}' | awk '{print $1}' | sort | uniq -c | sort -n
egrep 'xmlrpc.php' /usr/local/apache/domlogs/* | grep -v ftp_log | awk -F : '{print $2}' | awk '{print $1}' | sort | uniq -c | sort -n
===========

httpd attack
============
Set the limit in csf as below
root@hp155 [~]# cat /etc/csf/csf.conf | grep -i CONNLIMIT
# PORTFLOOD, CONNLIMIT
# xt_connlimit loaded. Typically, this will be with MONOLITHIC kernels. VPS
CONNLIMIT = "143;5,993;5"
============


To list number of connections to domains in the server
# /usr/bin/lynx -dump -width 500 http://127.0.0.1/whm-server-status | awk 'BEGIN { FS = " " } ; { print $12 }' | sed '/^$/d' | sort | uniq -c | sort -n
---------------------------------------------------------------------------------------------------------
To list the Busiest Site in the server
# /usr/bin/lynx -dump -width 500 http://127.0.0.1/whm-server-status | grep GET | awk '{print $12}' | sort | uniq -c | sort -rn | head
---------------------------------------------------------------------------------------------------------
To list the Busiest Script running on the server
# /usr/bin/lynx -dump -width 500 http://127.0.0.1/whm-server-status | grep GET | awk '{print $14}' | sort | uniq -c | sort -rn | head

#/usr/bin/lynx -dump -width 500 http://127.0.0.1/whm-server-status
---------------------------------------------------------------------------------------------------------


DDOS Attack Useful URL
===========
http://crybit.com/prevent-dos-attack/
https://forums.cpanel.net/threads/how-to-check-which-domain-in-my-server-is-being-ddosed.149397/
http://www.cpanelblog.in/how-to-trace-the-ddos-attack-on-the-server/
https://www.eukhost.com/forums/f42/steps-verify-ddos-attacks-your-cpanel-linux-server-13578/
===========


TCPDump Commands
==================
Refer:
http://www.rationallyparanoid.com/articles/tcpdump.html
http://www.slashroot.in/packet-capturing-tcpdump-command-linux

tcpdump -A dst $(hostname -i) -s 500 | egrep -o -i "Referer: http://[a-z,.]*|((\b[1]?[0-9]{1,2}\b|\b[2]?[0-4][0-9]\b|\b[2]?[5]?[0-5]\b)\.){3}(\b[1]?[0-9]{1,2}\b|\b[2]?[0-4][0-9]\b|\b[2]?[5]?[0-5]\b)" > /root/tcpdump01012016

tcpdump -A -s 0 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)' > /root/tcpdump01012016
tcpdump -A -s 0 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)'
tcpdump -X -s 0 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)'
==================


Wordpress permalink issue
==============
https://wordpress.org/support/topic/permalinks-stuck-on-default-settings
==============


Wordpress Cookies issue
=============
replace wp-includes/class-wp-http-cookie.php by new wp-includes/class-wp-http-cookie.php of that wordpress version
=============


how to rebuild RPM database
==============
https://forums.cpanel.net/threads/corrupted-rpm.263001/
http://www.cyberciti.biz/tips/rebuilding-corrupted-rpm-database.html
http://grepitout.com/how-to-rebuild-rpm-database/
https://cpaneltips.com/rebuilding-a-corrupted-rpm-database/
==============


To remove the Drupal maintenance page
==========
$conf['maintenance_mode'] = false; in setting.php
==========


Error: Fatal:master: service(imap): child 991983 returned error 83 (Out of memory (service imap { vsz_limit=256 MB }
==============
Go to >> Home »Service Configuration »Mailserver Configuration and increase this value "Maximum Size of a Mail Process (MB)"
==============


Mailing list basic info:
===========
Mailman lists can be found at :cd /usr/local/cpanel/3rdparty/mailman/lists/
Scripts Present: /usr/local/cpanel/3rdparty/mailman/bin  
Archives Location:: /usr/local/cpanel/3rdparty/mailman/archives/private
Mailing list error log file: /usr/local/cpanel/3rdparty/mailman/logs/error   
Repair Mailman permissions:	/usr/local/cpanel/3rdparty/mailman/bin/check_perms -f
View all lists:	/usr/local/cpanel/3rdparty/mailman/bin/list_lists
View all list members:	/usr/local/cpanel/3rdparty/mailman/bin/list_members listname_domain.com
Mailman config file: /usr/local/cpanel/3rdparty/mailman/Mailman/mm_cfg.py
===========


500 error on all the sites
==============
chmod 4755 /opt/suphp/sbin/suphp
==============


How to disable STRICT_TRANS_TABLES in mysql
===================
Add below line in /usr/my.cnf and restart mysql
sql_mode=NO_ENGINE_SUBSTITUTION  
===================


reset joomla admin password
=============
https://docs.joomla.org/How_do_you_recover_or_reset_your_admin_password%3F
=============


wordpress compression
=========
http://codex.wordpress.org/Output_Compression
=========


CloudFlare installation:
==========
http://www.cpanelkb.net/cloudflare-plugin-install/
http://crybit.com/install-cloudflare-plugin-on-cpanel/
http://stackoverflow.com/questions/23860877/how-to-install-cloudflare-on-cpanel-servers

/usr/local/cpanel/bin/cloudflare_update.sh
/usr/local/cpanel/bin/cloudflare_update.sh force
cat /usr/local/cpanel/etc/cloudflare.json | grep version
find / -name ModCloudflare.pm
==========


Fixing the 550 No Such User Here email error
=============
http://www.inmotionhosting.com/support/email/bounceback-errors/fixing-no-such-user-here
=============


IMAP, POP3 service was down and wont startup due to the below errors :
dovecot: imap-login: Fatal: master: service(imap-login): child 706162 killed with signal 11 (core dumps disabled)
dovecot: master: Error: service(pop3-login): command startup failed, throttling for 4 secs
dovecot: pop3-login: Fatal: master: service(pop3-login): child 706181 killed with signal 11 (core dumps disabled)
dovecot: master: Error: service(imap-login): command startup failed, throttling for 8 secs”
====================
Updated the vsz_limit limits from 64M to 128M in /etc/dovecot/dovecot.conf and restarted dovecot service.
====================


Email logs symbols meanings
https://forums.cpanel.net/threads/reading-and-understanding-the-exim-main_log.445812/
================
symbols:
<= (When the email arrives to the server from outside email server Or )
=> (When the email goes to the outside email server)
-> (additional address in same delivery)
*> (delivery suppressed by -N)
** (delivery failed; address bounced)
== (delivery deferred; temporary problem)
================


Joomla PHP version warnings
=============
Put this right after "define( '_JEXEC', 1 );" on index.php:
Code:
error_reporting( E_ERROR | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING );

You may need to do that on your administrator folder too.
=============


How to install PHP xdebug
==============
https://www.webmaster.net/tutorials/centos/how-install-xdebug-centos-6x-whm-server-configure-phpstorm-and-forward-firewall-ports.html
==============


How to install centrora WHM plug-in
=========
wget http://www.centrora.com/downloads/install.zip
unzip install.zip
sh install.sh

Go to WHM >> Plug-ins >> centrora
=========


How to install magickwand in linux (ImageMagick version 6.8.2 or greater version required)
See more at: http://datlinux.blogspot.in/2013/06/how-to-install-magickwand-in-linux.html
============
wget http://www.magickwand.org/download/php/MagickWandForPHP-1.0.9-2.tar.bz2
tar -xvjf MagickWandForPHP-1.0.9-2.tar.bz2 
cd MagickWandForPHP-1.0.9-2
phpize
./configure
make
make install
============


Prestashop Issues
==============
http://www.inmotionhosting.com/support/edu/prestashop-15/change-site-url-in-database
http://www.inmotionhosting.com/support/edu/prestashop-15/341-find-database-name
http://www.inmotionhosting.com/support/edu/prestashop-15/337-change-shop-url
==============


webalizer stats
=============
https://forums.cpanel.net/threads/webalizer-stats-not-updating.55190/
=============


Setup Varnish 4 on CentOS 6 as a Caching Server and Load Balancer
===========
http://thornelabs.net/2015/03/29/setup-varnish-4-on-centos-6-as-a-caching-server-and-load-balancer.html
===========


Softaclous and the new theme from Cpanel Paper Lantern Theme issue
Refer http://www.softaculous.com/board/index.php?tid=5128&title=Softaclous_and_the_new_theme_from_Cpanel_Paper_Lantern_Theme
================
ln -s /usr/local/cpanel/whostmgr/docroot/cgi/softaculous/enduser /usr/local/cpanel/base/frontend/paper_lantern/softaculous
/usr/local/cpanel/bin/unregister_cpanelplugin  /usr/local/cpanel/whostmgr/docroot/cgi/softaculous/softaculous.cpanelplugin
/usr/local/cpanel/bin/register_cpanelplugin  /usr/local/cpanel/whostmgr/docroot/cgi/softaculous/softaculous.cpanelplugin
================


Switching to Paper Lantern Theme issue
================
http://boomshadow.net/tech/new-cpanel-and-changing-to-paper-lantern-theme/
================


Disable suhosin
==============
https://myeasylinux.wordpress.com/2010/10/25/disable-suhosin/
http://cpanelplesk.com/disable-suhosin/
==============


prestashop - 500 error
===================
https://www.prestashop.com/forums/topic/421126-request-exceeded-the-limit-of-10-internal-redirects-due-to-probable-configuration-error/
===================

MySQL General logs
====================
root@r107 [~]# mysqladmin variables | grep general_log
| general_log                                       | OFF                                                                                                                    |
| general_log_file                                  | /var/lib/mysql/r107.log
# mysql
mysql> set global general_log = 1;
mysql> show variables where variable_name = 'general_log';
+---------------+-------+
| Variable_name | Value |
+---------------+-------+
| general_log | ON |
+---------------+-------+
1 row in set (0.00 sec)
====================


How To Update or Change MySQL database timezone
=================
http://geeksterminal.com/update-change-mysql-timezone/437/
http://www.inmotionhosting.com/support/website/databases/how-to-change-mysql-server-time-zone
http://crybit.com/time-zone-in-mysql/
http://stackoverflow.com/questions/4562456/mysql-setting-time-zone-in-my-cnf-options-file
=================

Wordpress - Missing a temporary folder
=================
Put below code in php.ini file
upload_tmp_dir = On
upload_tmp_dir = /home/username/public_html/tmp

and create "tmp" directory under public_html/ with 777 permission.
=================


Mysql super privileges
=================
You can add super privileges using phpmyadmin:
Go to PHPMYADMIN > privileges > Edit User > Under Administrator tab Click SUPER. > Go
If you want to do it through Console, do like this:
mysql> GRANT SUPER ON *.* TO user@'localhost' IDENTIFIED BY 'password';
or grant all privileges on DATABASE_NAME.* to USERNAME@localhost identified by 'PASSWORD';
mysql> FLUSH PRIVILEGES;
=================


Apache Configtest for centos7
===========
/usr/local/apache/bin/apachectl configtest
===========


Manage emails of all the email IDs from the default Email ID.
=====================
ln -s tagcouriers.com/toronto/ .toronto\@tagcouriers_com
chown -h user:user .toronto\@tagcouriers_com
=====================

Wordpress media upload http error
=============
1) Install Default to GD plugin
https://github.com/getsource/default-to-gd/blob/master/default-to-gd.php
   OR
2) put below code in .htaccess 

# Exclude the file upload and WP CRON scripts from authentication
<FilesMatch "(async-upload\.php|wp-cron\.php|xmlrpc\.php)$">
    Satisfy Any
    Order allow,deny
    Allow from all
    Deny from none
</FilesMatch>

3) Disable mod_security.
=============


How to disable directory browsing globally on whole WHM/cPanel server
===============
http://geektnt.com/how-to-disable-directory-browsing-globally-on-whole-whmcpanel-server.html
===============

To check RAID
=============
lspci -vv | grep -i raid
cat /proc/mdstat
=============


Route commands
===============
To check existing routes:
route -n
To add new route:
route add -net 192.168.175.0 netmask 255.255.255.0 dev eth0
route add -net 192.168.0.0 netmask 255.255.0.0 gw 192.168.168.1 eth0
To remove existing route:
route del -net 85.13.248.0 netmask 255.255.255.0 dev eth0
===============


Enable the port for the specific IP address in csf 
=============
tcp:out:d=26:d=194.140.187.11 #Ticket- 2411804
=============


How to Build Multiple Versions of PHP With cPanel
==================
http://thewonderfulworldoflinux.com/blog/2014/03/21/how-to-build-multiple-versions-of-php-with-cpanel/
==================


How to increase the number of filelistings in pureftpd
===============
https://sachinpradeeplinux.wordpress.com/2012/03/26/increasing-the-number-of-filelistings-in-pureftpd/
http://cpanelfacts.kevinviews.in/?p=19
http://cpanelplesk.com/increasing-the-number-of-filelistings-in-pureftpd/
===============


How to enable password less authentication between 2 linux servers
================
http://www.tecmint.com/ssh-passwordless-login-using-ssh-keygen-in-5-easy-steps/
================


KVM error message
=================
http://sebcio.blogspot.in/2014/09/comserverenginesrdrendofstream.html
=================

AuthType configured with no corresponding authorization directives error
===================
To resolve this, need to add authuser file details in each page section in .htaccess file
https://blog.ss88.uk/http-ah01627-authtype-configured-with-no-corresponding-authorization-directives
For e.g.

RewriteEngine on
<Files "workshop-participants.php">
  AuthUserFile /home/vsniozee/.htpasswd
  AuthType Basic
  AuthName "Page Protected"
  Require user workshop
</Files>
===================

Resolving “nf_conntrack: table full, dropping packet.”
===============
http://www.pc-freak.net/blog/resolving-nf_conntrack-table-full-dropping-packet-flood-message-in-dmesg-linux-kernel-log/
https://ioflood.com/blog/2015/02/19/nf_conntrack-table-full-dropping-packet-a-solution-for-centos-dedicated-servers/
https://major.io/2014/01/07/nf-conntrack-table-full-dropping-packet/
===============


Prestashop Office 365 contact form issue
==============
https://www.prestashop.com/forums/topic/267708-working-with-office365-smtp-email/
==============


How to show up absolute path at bash prompt
http://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html
http://www.thegeekstuff.com/2008/09/bash-shell-take-control-of-ps1-ps2-ps3-ps4-and-prompt_command
================
[root@hp201 anantp]# echo $PS1  --- To display current PS1 value
[\u@\h \W]\$
[root@hp201 anantp]# PS1="\u@\h [\w]#"   ---- To update new value
root@hp201 [/home/anantp]#

Make this setting permanent by adding export PS1=”\u@\h \w> ” to either .bash_profile (or) .bashrc as shown below.
vi ~/.bash_profile (or)
vi ~/.bashrc
Add to one of the above files: export PS1="\u@\h [\w]#"
================


Error: Token mismatch in phpmyadmin
https://hostingfixes.wordpress.com/2014/09/22/error-token-mismatch-in-phpmyadmin/
=================
>>Check whether disk quota for the account is exceeded
>>Check whether server /tmp directory have the correct permissions and got filled
>>Check users /tmp directory permissions. ie /home/username/tmp.Correct permission is 755.
chmod 755 /home/username/tmp
>>Check “session.save_path” in php.ini file. It should be like below
session.save_path = /tmp
=================

Command to replace all the php files with the 777 permission to 644
================
find . -name "*.php" -perm 777 -print -exec chmod 644 {} \;
================


451 Temporary local problem
================
http://letushare.com/issue-with-exim-require_files-permission-denied-in-logs/
http://blog.triantech.com/issue-with-exim-permission-denied-seen-in-logs/
================

RPM database corrupted 
============
https://forums.cpanel.net/threads/cpanel-email-broken-after-todays-update.542591/
/usr/local/cpanel/scripts/check_cpanel_rpms --fix
============

Wordpress Attack
=============
http://www.inmotionhosting.com/support/website/wordpress/disabling-the-wp-cronphp-in-wordpress
https://codex.wordpress.org/Brute_Force_Attacks
=============


421 Too many concurrent SMTP connections
=============
http://raafat.tawasol.net/421-too-many-concurrent-smtp-connections-please-try-again-later/
https://linuxtechme.wordpress.com/2013/08/29/421-too-many-concurrent-smtp-connections/
=============


How to Resolve the Libgomp: Thread Creation Failed Error
==============
http://www.inmotionhosting.com/support/edu/wordpress/resolving-libgomp-error-thread-creation-failed

Add below code in .htaccess file:
SetEnv MAGICK_THREAD_LIMIT 1
==============


Installing APXS on EasyApache4
================
The APXS module is not installed by default on EasyApach4. You can install it as below:-
yum install ea-apache24-httpd-devel
The path to it is /usr/bin/apxs
================


Connecting to a database with MySQL Workbench 5.2
=============
http://www.inmotionhosting.com/support/website/database-connections/connect-database-remotely-mysql-workbench
=============


csf paths
============
/etc/csf/
/var/lib/csf
============

Apache error: No space left on device: mod_rewrite: Parent could not create RewriteLock
Refer: https://crybit.com/parent-could-not-create-rewritelock/
================
ipcs -s | grep nobody  ---To get semaphore list
ipcs -s | grep nobody | awk '{print $2}' | xargs -n 1 ipcrm sem  --- To delete semaphore list
service httpd restart
To fix this permanently, you can increase the limit of Semaphore in the server.
Add the following lines in the file /etc/sysctl.conf
kernel.msgmni = 1024
kernel.sem = 250 256000 32 1024
Then run sysctl -p to pick up the new changes.
================


Pear error: authentication failure [SMTP: STARTTLS failed (code: 220, response: TLS go ahead)]
=================
pear list - To check the installed pears
pear list-files PearName (for e.g. pear list-files Net_SMTP) -- To check the installed pear file paths
nano /usr/local/lib/php/Net/SMTP.php and replace the below code:

Old code:
if ($tls && version_compare(PHP_VERSION, '5.1.0', '>=') &&
           extension_loaded('openssl') && isset($this->_esmtp['STARTTLS']) &&
           strncasecmp($this->host, 'ssl://', 6) !== 0) {
New code:
if (version_compare(PHP_VERSION, '5.1.0', '>=') && ($this->_esmtp['STARTTLS'] == true)) {
=================


Wordpress SMTP email issue (Warning:  stream_socket_enable_crypto(): Peer certificate CN=)
OpenSSL changes in PHP 5.6.x 
=================
https://wordpress.org/support/topic/openssl-changes-in-php-56x/
http://stackoverflow.com/questions/30371910/phpmailer-generates-php-warning-stream-socket-enable-crypto-peer-certificate

nano ./wp-content/plugins/wp-mail-smtp/wp_mail_smtp.php
and add below code in it

    add_filter('wp_mail_smtp_custom_options','my_wp_mail_smtp_custom_options');

    function my_wp_mail_smtp_custom_options($phpmailer) {
    	$phpmailer->SMTPOptions = [
    		'ssl' => [
    			'verify_peer' => false,
    			'verify_peer_name' => false
    		]
    	];
    	return $phpmailer;
    }
=================


------------
To check the encoding of file: 
file filename
---------------


How to install browscap
=================
Download browscap.ini files to required path from https://browscap.org/
files are (browscap.ini, php_browscap.ini)

root@hp180 [/home/pushm856/etc]# cat php.ini | grep browscap
browscap = On
browscap = /home/pushm856/etc/php5/apache2/browscap.ini (Respective path)
=================


To check the TLS & SSL version in linux
=============
openssl ciphers -v | awk '{print $2}' | sort | uniq
=============


Socket already exists: /var/run/dovecot/auth-master on cPanel
http://linuxpitstop.com/dovecot-error-socket-already-exists/
=============
for i in `ps aux | grep dovecot | awk '{print $2}'` ; do kill -9 $i ; done  (it will remove stuck dovecot process)
/usr/local/cpanel/scripts/restartsrv_dovecot
=============


To update the quota of specific user
=================
edquota <Username>
=================

Softaclous 404 issue with paper_lantern:
http://www.softaculous.com/board/index.php?tid=7750&title=Softaculous_does_not_show_up_after_cpanel_update_11.50
================
Code
ln -s /usr/local/cpanel/whostmgr/docroot/cgi/softaculous/enduser /usr/local/cpanel/base/frontend/paper_lantern/softaculous
For getting the Softaculous icon execute the following command : 
Code
For x3 : 
/usr/local/cpanel/bin/register_cpanelplugin /usr/local/cpanel/whostmgr/docroot/cgi/softaculous/softaculous.cpanelplugin 

For paper_lantern : 
/usr/local/cpanel/scripts/install_plugin /usr/local/cpanel/whostmgr/docroot/cgi/softaculous/softaculous_plugin.tar.bz2
================


See all failed SSH login attempts	
=============
for Debian:
View all failed login attempts: cat /var/log/auth.log | grep 'sshd.*Invalid'
View all successful logins: cat /var/log/auth.log | grep 'sshd.*opened'

for RedHat/CentOS:
View all failed login attempts: cat /var/log/secure | grep 'sshd.*Invalid'
View all successful logins: cat /var/log/secure | grep 'sshd.*opened'
=============


class-smtp.php on line 344
https://github.com/PHPMailer/PHPMailer/issues/368
================
change the file class.smtp.php by adding below code:

public function connect($host, $port = null, $timeout = 30, $options = array())
{
    if(count($options)==0){
        $options["ssl"]=array("verify_peer"=>false,"verify_peer_name"=>false,"allow_self_signed"=>true);
    }
================


AutoInstall SSL Plugin Installation for cPanel
http://support.limestonenetworks.com/knowledge-base/autoinstall-ssl-plugin-installation-for-cpanel/
https://www.autoinstallssl.com/
=====================
1.Download the plugin from here: http://mirror.lstn.net/limestone-sslstore/cPanel_AutoInstallSSL_latest.zip
2.Copy the autoinstallssl folder from the zip file to your WHM/cPanel server, it requires no specific location.
3.As the root user, run the install command at the prompt:
cd autoinstallssl
chmod 777 install
./install

4.Activate ionCube loaders from WHM panel.
Go to “Tweak Setttings “ menu under “Server Configuration “
Click on PHP tab.
Check the ionCube option and click on save.
5.Complete the AUTO-UPDATE setup to ensure functionality in future versions
=====================



Perhaps the DBD::mysql perl module hasn't been fully installed
==========================
Error:
install_driver(mysql) failed: Can't locate DBD/mysql.pm in @INC (@INC contains: /usr/local/lib64/perl5 /usr/local/share/perl5 /usr/lib64/perl5/vendor_perl /usr/share/perl5/vendor_perl /usr/lib64/perl5 /usr/share/perl5 .) at (eval 5) line 3.
Perhaps the DBD::mysql perl module hasn't been fully installed,
or perhaps the capitalisation of 'mysql' isn't right.
Available drivers: DBM, ExampleP, File, Gofer, Proxy, SQLite, Sponge.

Solution: 
yum install perl-DBD-mysql

Ref: 
http://www.microhowto.info/howto/connect_to_a_mysql_database_using_perl_dbi.html
http://stackoverflow.com/questions/17144583/dbd-mysql-installed-but-still-error-install-drivermysql-failed-cant-locate
==========================


CL7 Kernel Commands
==================
grub2-mkconfig   --- To create new grub conf file

awk -F\' '$1=="menuentry " {print i++ " : " $2}' /etc/grub2.cfg    --- Check kernel menu entry in  cloudlinux 7

0 : CloudLinux (3.10.0-427.18.2.lve1.4.23.el7.x86_64) 7.2 (Valeri Kubasov) with debugging
1 : CloudLinux (3.10.0-427.18.2.lve1.4.23.el7.x86_64) 7.2 (Valeri Kubasov)
2 : CloudLinux (3.10.0-427.10.1.lve1.4.22.el7.x86_64) 7.2 (Valeri Kubasov) with debugging
3 : CloudLinux (3.10.0-427.10.1.lve1.4.22.el7.x86_64) 7.2 (Valeri Kubasov)
4 : CloudLinux (3.10.0-427.18.2.lve1.4.18.el7.x86_64) 7.2 (Valeri Kubasov) with debugging
5 : CloudLinux (3.10.0-427.18.2.lve1.4.18.el7.x86_64) 7.2 (Valeri Kubasov)
6 : CloudLinux (3.10.0-427.18.2.lve1.4.15.el7.x86_64) 7.2 (Valeri Kubasov) with debugging
7 : CloudLinux (3.10.0-427.18.2.lve1.4.15.el7.x86_64) 7.2 (Valeri Kubasov)
8 : CloudLinux (3.10.0-427.18.2.lve1.4.14.el7.x86_64) 7.2 (Valeri Kubasov) with debugging
9 : CloudLinux (3.10.0-427.18.2.lve1.4.14.el7.x86_64) 7.2 (Valeri Kubasov)
10 : CloudLinux 7.1 (Vladimir Komarov), with Linux 0-rescue-9fdba1ba51d949608d7bedf7bed26e5c

grub2-set-default 2  --- Set kernel using below command

To install different kernels
yum clean all; yum install kernel-3.10.0-427.10.1.lve1.4.22.el7 kmod-lve-1.4-22.el7 --enablerepo=cloudlinux-updates-testing
==================


htaccess redirect to another domain without changing url
================
RewriteEngine on 
RewriteRule ^(.*)$ http://www.newdomain.org/$1 [R=301,L] 19:26 

Or

RewriteEngine on 
RewriteCond %{HTTP_HOST} ^benangel\.com\.au$ [OR]
RewriteCond %{HTTP_HOST} ^www\.benangel\.com\.au$
RewriteRule ^(.*)$ http://benangel.co/$1 [R=301,L] 
================


Receiving email error message: Please turn on SMTP Authentication in your mail client. mail-pf0-f177.google.com [209.85.192.177]:35381 is not permitted to relay through this server without authentication.
=================
Check the text file /etc/localdomains and check to make sure the domains having problems are present in the list. If not, then add them to the list save the file and then Restart Exim for the changes to take effect.
=================



cPanel other usage
==============
find / -user CPANELUSERNAME
e.g. find / -user albinabo -exec du -sh {} \;
==============


To enable detail mail logs, do below in /etc/exim.conf
=================
log_selector = +all
=================

Wordpress error - the uploaded file could not be moved to wp-content/uploads.
============
Go to wp-contents direcotry and run below
chmod -R g+w uploads/
chown -R nobody uploads/
============


Enabling LOAD DATA LOCAL INFILE in mysql
=============
SHOW GLOBAL VARIABLES LIKE 'local_infile';
SET GLOBAL local_infile = 'ON';
SHOW GLOBAL VARIABLES LIKE 'local_infile';
It should echo the following:

mysql> SHOW GLOBAL VARIABLES LIKE 'local_infile';
+---------------+-------+
| Variable_name | Value |
+---------------+-------+
| local_infile  | OFF   |
+---------------+-------+
1 row in set (0.00 sec)

mysql> SET GLOBAL local_infile = 'ON';
Query OK, 0 rows affected (0.06 sec)

mysql> SHOW GLOBAL VARIABLES LIKE 'local_infile';
+---------------+-------+
| Variable_name | Value |
+---------------+-------+
| local_infile  | ON    |
+---------------+-------+
1 row in set (0.00 sec)
=============



file_get_contents(): SSL operation failed with code 1
Ref: http://stackoverflow.com/questions/26148701/file-get-contents-ssl-operation-failed-with-code-1-and-more
================
<?php
$arrContextOptions=array(
    "ssl"=>array(
        "verify_peer"=>false,
        "verify_peer_name"=>false,
    ),
);  

$response = file_get_contents("https://midi-pro.net/a.txt", false, stream_context_create($arrContextOptions));

echo $response; ?>
================



fix for Eaccelerator filling up /tmp folder – WHM & CPanel
http://kb.eurovps.com:8090/pages/viewpage.action?pageId=5472289
==============
If you simply want to clean out the /tmp/eaccerlator folder, the following command does the trick on CentOS and RedHat systems.
tmpwatch --mtime --all 336 /tmp/eaccelerator

Other thing is to move the eaccerlator cache directory from /tmp to other large pattion space.

vi /usr/lib/php.ini
Find :
eaccelerator.cache_dir=”/tmp/eaccelerator
and change it from /tmp/eaccelerator to /var/cache/eaccelerator and save the file.
# mkdir /var/cache/eaccelerator
#service httpd stop
#rm -rf /tmp/eaccelerator
#service httpd start
==============


How to Install ImageMagick on CentOS & RHEL
Ref: http://tecadmin.net/install-imagemagick-on-centos-rhel/#
=============================
yum install gcc php-devel php-pear
yum install ImageMagick ImageMagick-devel
pecl install imagick
echo "extension=imagick.so" > /usr/local/lib/php.ini
service httpd restart
=============================


Omeka_File_Derivative_Exception
ImageMagick is not properly configured: invalid directory given for the ImageMagick command!
=================
ImageMagick Directory Path should be set to: /usr/bin/ in Omeka admin panel >> Settings >> General
Remove proc_open from disable_functions in php.ini
=================


Install ImageMagick on cPanel with EasyApache 4
=================
yum install ImageMagick-devel ImageMagick-c++-devel ImageMagick-perl
/usr/bin/convert --version
/opt/cpanel/ea-php56/root/usr/bin/pecl install imagick
nano /opt/cpanel/ea-php56/root/etc/php.ini
extension=imagick.so
service httpd restart
/opt/cpanel/ea-php56/root/usr/bin/php -m | grep imagick
=================



Handler for PHP in html
===========
AddHandler application/x-httpd-ea-php56 .html
===========


cPanel bandwidth error message: 
(XID rdxp8q) Database /var/cpanel/bandwidth/horse759.sqlite Connect Error:unable to open database file at cpanel.pl line 2312.
Ref: https://forums.cpanel.net/threads/cpbackup-error.519261/
===============
mv /var/cpanel/bandwidth/username.sqlite /root/username.sqlite-copy
/scripts/build_bandwidthdb_root_cache_in_background
/scripts/rebuild_bandwidthdb_root_cache
===============


DateTime module installation
==============================
You can install the DateTime module using two methods.

1. As suggested above by "cPanelDon" : /scripts/perlinstaller --force DateTime

2. By downloading the module and installing it manually. Use the following steps:
cd /usr/local/src
wget http://search.cpan.org/CPAN/authors/id/D/DR/DROLSKY/DateTime-0.53.tar.gz
tar -zxf DateTime-0.53.tar.gz
cd DateTime*
perl Makefile.pl
make
make install
==============================


GlobalSign Plug-in installation
=================================
Ref:

https://forums.cpanel.net/threads/how-to-install-globalsign-oneclickssl-plugin-successfully.235211/

First, login to your cPanel/WHM server as the root user. Then, copy and paste the following:

/scripts/perlinstaller Config::Crontab
/scripts/perlinstaller Date::Simple
/scripts/perlinstaller Digest::MD5
/scripts/perlinstaller HTTP::Request::Common
/scripts/perlinstaller IO::Handle
/scripts/perlinstaller IPC::Open3
/scripts/perlinstaller JSON::Syck
/scripts/perlinstaller LWP::UserAgent
/scripts/perlinstaller Mozilla::CA
/scripts/perlinstaller Template
/scripts/perlinstaller XML::Simple
/scripts/perlinstaller YAML::Syck
cd /home
wget https://www.globalsign.com/downloads/oneclickssl/cpanel/GlobalSign-OneClickSSL-cPanel-Plugin-3.00.sea
chmod +x GlobalSign-OneClickSSL-cPanel-Plugin-3.00.sea
./GlobalSign-OneClickSSL-cPanel-Plugin-3.00.sea
rm GlobalSign-OneClickSSL-cPanel-Plugin-3.00.sea
You will be prompted for confirmation at the end that it is safe to remove the .sea file. Simply press "y" if the output looks correct.

Then, go to the following page within WHM to configure OneClickSSL.

Main >> Plugins >> GlobalSign OneClickSSL
=================================


Plesk disk space issue
======================
find /var/www/vhosts/*/statistics/logs -type f -size +100000k -exec ls -lh {} \; | awk '{ print $9 ": " $5 }'
find /var/www/vhosts/*/httpdocs -type f -size +100000k -exec ls -lh {} \; | awk '{ print $9 ": " $5 }'
du -sh /usr/local/psa/tmp/
du -sh /usr/local/psa/PMM/
du -sh /var/lib/psa/dumps/
du -sh /var/www/vhosts/default/

cd /var/qmail/mailnames/
find . -type d -name .Trash -exec du -sh {} \;
find . -type d -name .Deleted* -exec du -sh {} \;

/var/log
======================


Apache crashes on reload and websites show 502 Bad Gateway
====================
https://support.plesk.com/hc/en-us/articles/213946305-Apache-crashes-on-reload-and-websites-show-502-Bad-Gateway-seg-fault-or-similar-nasty-error-detected-in-the-parent-process
====================


Reset The Root Password For A Linux VM Hosted On XenServer
https://www.unixmen.com/reset-root-password-linux-vm-hosted-xenserver/
=========================
1- Shut down your server using the Xencenter controls
2- Right click on machine and select Properties
3- Go under Boot options 
You already have something in the OS Boot Parameters you will need to take note of this as You will need to save it and put it back once the password reset is complete.
Change the OS Boot Parameters to rw init=/bin/bash 
Some times for some OS especial CentOS  you will need to write in the field the word single instead of rw init=/bin/bash  so try both if first trick didn’t work.
4- Save and Start your virtual machine
Your system will  boot up in single user mode. So to change your password, you need to type this command:
 bash# passwd root
5- Type in your new password you will then be asked to confirm it
Your password has now been reset.
6- Shutdown your virtual machine.
bash# shutdown -h now
=========================


Frame Forwarding code
=============== 
<FRAMESET ROWS="*,0" FRAMEBORDER=0 BORDER=0 FRAMESPACING=0>https://
https://www.conetix.com.au/support/article/how-enable-fail2bandocs.plesk.com/en-US/12.5/administrator-guide/server-administration/protection-against-brute-force-attacks-fail2ban.73381/
https://www.conetix.com.au/support/article/how-enable-fail2ban
<FRAME SRC="thelaughinn.com.au" NORESIZE>
</FRAMESET>
===============


How to install ModSecurity or Fail2Ban management tool in Plesk
===============
To check whether the license key supports it, go to:

Server Management > Tools & Settings > License Management
and see if there is the line "Security core (ModSecurity and Fail2Ban)".

You can install Fail2Ban component under

Tools & Settings > Updates and Upgrades > Add or Remove Components > Fail2Ban authentication failure monitor
You can install ModSecurity component in:

Tools & Settings > Updates and Upgrades > Add or Remove Components > Web hosting features > ModSecurity Web Application Firewall for Apache

Ref:
https://kb.plesk.com/en/121988
https://docs.plesk.com/en-US/12.5/adminhttps://www.conetix.com.au/support/article/how-enable-fail2banistrator-guide/server-administration/protection-against-brute-force-attacks-fail2ban.73381/
https://www.conetix.com.au/support/article/how-enable-fail2ban
===============


Allow access from specific IP address .htaccess
==============
Order deny,allow
Deny from all
Allow from 203.25.45.2
==============


How to Retrieve and Change the Plesk Admin Password on a Linux Server
------------------
https://support.managed.com/kb/a2039/how-to-retrieve-and-change-the-plesk-admin-password-on-a-linux-server.aspx
------------------


Plesk - How to reinstall ModSecurity package
------------------
https://support.plesk.com/hc/en-us/articles/213941365-How-to-reinstall-ModSecurity-package (use this if ModSecurity is already installed and enabling the rules throws out error).


1. Removed mod_security package installed from atomic repository using command:
# yum remove mod_security

2. Add two strings exclude=*mod_security* in appropriate fields of file /etc/yum.repos.d/atomic.repo in order to omit installation of mod_security package from atomic repository. (You will get more info on what to edit from actual LP010 server)

3. Install mod_security package provided by Plesk using autoinstaller.
------------------


Postfix commands
----------------------
https://jvulinux.wordpress.com/2014/12/26/commands-to-check-spamming-in-postfix-mail-server/
https://www.cyberciti.biz/tips/howto-postfix-flush-mail-queue.html
----------------------


qmail commands
----------------------
http://geeksterminal.com/qmail-commands-logs-plesk-server/580/
https://www.24x7servermanagement.com/blog/how-to-manage-qmail-queue-in-linux-plesk/
----------------------

qmail-remove installation
----------------------
http://www.datanethosting.com/kb/plesk-linux/how-to-install-qmail-remove-on-linux-plesk
----------------------


Unable to activate the subscription in Plesk (Windows server)
================
https://admin-ahead.com/forum/plesk/unable-to-activate-the-subscription-in-plesk-(windows-server)/
https://support.plesk.com/hc/en-us/articles/213941105-Unable-to-activate-subscription-The-subscription-is-suspended-because-its-subscriber-was-suspended
https://support.plesk.com/hc/en-us/articles/213362189-Unable-to-activate-subscription-in-Plesk-10-0-The-subscription-is-still-suspended-due-to-the-following-reason-The-subscription-is-suspended

From command prompt, run below commands

"%plesk_bin%\dbclient.exe" --direct-sql --sql="select status ,id ,name from domains where name='barrabacaravanpark.com.au'"
"%plesk_bin%\dbclient.exe" --direct-sql --sql="update domains set status = 0 where name='barrabacaravanpark.com.au'"
"%plesk_cli%\domain.exe" --webspace-off barrabacaravanpark.com.au
"%plesk_cli%\domain.exe" --webspace-on barrabacaravanpark.com.au
================

How to install and use Memcache
==========
https://kyup.com/tutorials/install-use-memcache/
https://www.liquidweb.com/kb/how-to-install-memcached-on-centos-7/
==========

Passphrase
------------------
openssl rsa -text -in test_rsa_key -passin 'pass:super secret passphrase'
------------------


HyperVisor is already running
https://blogs.technet.microsoft.com/gbanin/2013/06/25/how-to-install-hyper-v-on-a-virtual-machine-in-hyper-v/
----------------------
Go to PowerShell and execute below commands:
Enable-WindowsOptionalFeature –Online -FeatureName Microsoft-Hyper-V –All -NoRestart
Install-WindowsFeature RSAT-Hyper-V-Tools -IncludeAllSubFeature
Install-WindowsFeature RSAT-Clustering -IncludeAllSubFeature
Install-WindowsFeature Multipath-IO
Restart-Computer
----------------------


HyperV - Disk expand/shrink
----------------
https://devinknightsql.com/2014/06/19/reducing-the-disk-size-of-a-hyper-v-virtual-machine/
https://activedirectory.ncsu.edu/2011/10/extending-a-partition-on-window-server-core/
http://www.altaro.com/hyper-v/shrink-hyper-v-virtual-disk-vhd-vhdx/
----------------

CentOS 7 - Single user / Rescue Mode
-------------------------------
http://thegeekdiary.com/centos-rhel-7-how-to-boot-into-rescue-mode-or-emergency-mode/
https://ma.ttias.be/boot-in-single-user-mode-on-centos-7-rhel-7/
-------------------------------


lvreduce on / partiotion
--------------------------
https://rbgeek.wordpress.com/2013/02/11/how-to-reduce-the-root-partition-in-lvm/
http://thegeekdiary.com/centos-rhel-how-to-shrink-lvm-root-file-system/
https://gerardnico.com/wiki/linux/lvreduce
--------------------------


Error - “Device eth0 does not seem to be present, delaying initialization”
---------------------------
https://www.unixmen.com/fix-device-eth0-seem-present-delaying-initialization-error/
https://www.ostechnix.com/solve-device-eth0-not-seem-present-delaying-initialization-error/
---------------------------

How to check cPanel CPU and Memory usage for a specific user
--------------------------
Ref:

https://smyl.es/how-to-check-cpanel-cpu-and-memory-usage-for-a-specific-user/
https://crybit.com/howcommand-to-find-the-resourcecpu-memory-usages-of-users-unixlinux/

#/usr/local/cpanel/bin/dcpumonview

If you want to get the stats for a user for say the past 5 days or so, run this command in SSH:

#domain="thedomain.com"; for i in `seq 1 7 `; do let i=$i+1 ; let  k=$i-1 ; let s="$(date +%s) - (k-1)*86400"; let t="$(date +%s) - (k-2)*86400"; echo `date -Idate -d @$s`; /usr/local/cpanel/bin/dcpumonview `date -d @$s +%s` `date -d @$t +%s` | sed -r -e 's@^<tr bgcolor=#[[:xdigit:]]+><td>(.*)</td><td>(.*)</td><td>(.*)</td><td>(.*)</td><td>(.*)</td></tr>$@Account: \1\tDomain: \2\tCPU: \3\tMem: \4\tMySQL: \5@' -e 's@^<tr><td>Top Process</td><td>(.*)</td><td colspan=3>(.*)</td></tr>$@\1 - \2@' | grep $domain -A3 ; done

#top -c d2 -u username
--------------------------


Redis and Redis PHP extension
https://help.bigscoots.com/cpanel/cpanel-easyapache-4-installing-redis-and-redis-php-extension
------------------------------
Installing the Redis daemon:

for CentOS 6/RHEL 6

rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-6.noarch.rpm
rpm -ivh http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
yum -y install redis --enablerepo=remi --disableplugin=priorities
chkconfig redis on
service redis start
for CentOS 7/RHEL 7

rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
rpm -ivh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm
yum -y install redis --enablerepo=remi --disableplugin=priorities
systemctl enable redis
systemctl start redis


Installing the Redis PHP extension for PHP5.5, PHP5.6 and PHP7.0
wget https://pecl.php.net/get/redis-3.1.0.tgz
tar -xvf redis-*.tgz
cd redis*
phpize
make
./configure
make
make install
echo 'extension=redis.so' >> /usr/local/lib/php.ini
/scripts/restartsrv_httpd
/scripts/restartsrv_apache_php_fpm
------------------------------

How To Change The LVM Volume Group Name That Includes The Root Partition
http://wiki.networksecuritytoolkit.org/index.php/HowTo_Change_The_LVM_Volume_Group_Name_That_Includes_The_Root_Partition
-------------------------
vgrename -v oldvg newvg
ll /dev/mapper/newvg
cat /etc/fstab  --- replace all the old vg instances by new
cat /etc/grub.conf --- replace all the old vg instances by new
mkinitrd -f -v /boot/initramfs-$(uname -r).img $(uname -r)   --- Rebuild The Kernel initramfs File
reboot
-------------------------


sed command instead of replace
-----------------------
sed -i -e 's/vg_vmh/vol/g' /etc/grub.conf
-----------------------


Kernel does not support the prevention of symlink ownership attacks.
https://documentation.cpanel.net/display/CKB/How+to+Harden+Your+cPanel+System%27s+Kernel
------------------------
cd /etc/yum.repos.d/ 
wget https://securedownloads.cpanel.net/cPkernel/cPkernel.repo
yum -y update kernel
Restart the server
------------------------



Repair GRUB: error: unknown filesystem. grub rescue> in Linux Mint/PinguyOS
-------------------------
https://mintguide.org/system/186-repair-grub-error-unknown-filesystem-grub-rescue-in-linux-mint-pinguyos.html
https://www.quora.com/How-do-I-fix-a-grub-rescue-unknown-file-system-error
https://www.easytechguides.com/error-unknown-filesystem-grub-rescue.html
-------------------------


Reset MySQL Root Password on Debian/Ubuntu
--------------------
https://www.vultr.com/docs/reset-mysql-root-password-on-debian-ubuntu
https://support.rackspace.com/how-to/mysql-resetting-a-lost-mysql-root-password/
https://ubuntu.flowconsult.at/en/mysql-set-change-reset-root-password/
--------------------


Upgrade XenServer version
--------------------
http://www.vikash.nl/how-to-upgrade-xenserver-6-5-to-xenserver-7-0/
--------------------


3cx installation
------------------
https://www.3cx.com/docs/manual/configuration-tool/
------------------


AutoSSL issues
-------------------
https://nixcp.com/autossl-not-working/
-------------------


Generate single csr for multiple domains
-------------------------------
https://certificatetools.com/
https://kernelmanic.com/certificate-request-generator-with-multiple-common-names-and-subject-alternative-names/
-------------------------------


Plesk Policy error
------------------
https://support.plesk.com/hc/en-us/articles/213906225-Unable-to-log-into-Plesk-Access-for-administrator-from-address-xx-xx-xx-xx-is-restricted-in-accordance-with-IP-Access-restriction-policy-currently-applied
------------------


Plesk - Install custom PHP extensions 
https://www.plesk.com/blog/product-technology/adding-custom-php-modules-in-plesk/
https://talk.plesk.com/threads/oauth-extension-for-php-7-couldnt-find-pcre-h.343354/
------------------------
yum search plesk-php devel
yum install make plesk-php56-devel gcc glibc-devel libmemcached-devel zlib-devel
/opt/plesk/php/5.6/bin/pecl install memcached
# echo "extension=memcached.so" > /opt/plesk/php/5.6/etc/php.d/memcached.ini
# plesk bin php_handler --reread
------------------------


Windows - Add a new IP address forcefully 
---------------
http://windowsitpro.com/windows-server/solve-iis-listener-problems
---------------


XenServer – Creating a local ISO Library
Ref - http://www.riverlite.co.uk/blog/xenserver-creating-a-local-iso-library/
---------------------
mkdir -p /var/opt/xen/ISO_Store
xe sr-create name-label=LocalISO type=iso device-config:location=/var/opt/xen/ISO_Store device-config:legacy_mode=true content-type=iso
---------------------


How to change boot device on vm installed on Citrix Xen Server to DVD
Ref - http://www.xenlens.com/boot-a-guest-vm-from-cd-or-dvd-in-xenserver/
---------------------
In order to boot from cd or dvd you need to change the guest virtualization type from HVM (fully virtualized) to PV (paravirtualized).
# xe vm-param-set HVM-boot-policy="BIOS order" uuid=[uuid of your vm]

After you have booted from dvd, change back to fully virtualized mode:
# xe vm-param-set HVM-boot-policy="" uuid=[uuid of your vm]
---------------------




Ref URL: https://blogs.msdn.microsoft.com/virtual_pc_guy/2015/02/11/copying-the-vhd-of-a-generation-2-linux-vmand-not-booting-afterwards/
-------------------------------------------------
/boot/efi/EFI/ubuntu

-------------------------------------------------
Log in to the virtual machine.
Change directory to the boot EFI directory : cd /boot/efi/EFI
Copy the ubuntu directory in to a new directory named boot : sudo cp –r ubuntu/ boot
Change directory to the newly created boot directory : cd boot
Rename the shimx64.efi file : sudo mv shimx64.efi bootx64.efi
-------------------------------------------------
What this does is move the boot information out of the UEFI firmware and onto the disk.  With this done you can copy and boot the virtual hard drive with ease.


# grub-install --target=x86_64-efi --efi-directory=/boot/efi --no-nvram --removable
-------------------------
What command above that does is it properly re-installs grub to /boot/efi/EFI in removal mode. (i.e. using the well known /EFI/BOOT/BOOTX64.EFI bootfile).
-------------------------------------------------


R1soft Backup Error - Failed To Backup LVM/MD Configuration
-------------------------------
https://help.serversaustralia.com.au/hc/en-us/articles/115004586426-R1soft-Backup-Error-Failed-to-backup-LVM-MD-Configuration
http://archive.li/Uh8FV

# mv /usr/sbin/r1soft/lib/lvm.static{,.bak}
# ln -s /sbin/lvm /usr/sbin/r1soft/lib/lvm.static
-------------------------------


CDP error - An exception occurred during the request. Win32 call ::GetVolumePathNameW( pathFinal.c_str(), &volumeRootPath[0], (DWORD)volumeRootPath.size() ) failed (123): The filename, directory name, or volume label syntax is incorrect.
--------------------------------
Need to restart following services 

COM + Event System
COM + System Application
VSS
--------------------------------


Plesk Dovecot issue
-------------------
http://support.moonpoint.com/network/email/dovecot/connections-dropped.php
-------------------


Set TLSv1.2 on plesk
--------------------------
[root@vmx20192 ~]# plesk bin server_pref -s | grep proto
ssl-protocols:  TLSv1 TLSv1.1 TLSv1.2
[root@vmx20192 ~]# plesk bin server_pref -u -ssl-protocols TLSv1.2
SUCCESS: Server preferences are successfully updated
[root@vmx20192 ~]# plesk bin server_pref -s | grep proto
ssl-protocols:  TLSv1.2
[root@vmx20192 ~]#
--------------------------

Enable Gzip Plesk
--------------------------------------
https://www.conetix.com.au/support/article/enable-gzip-compression-nginx-site23:10
https://support.plesk.com/hc/en-us/articles/115000716649-How-to-enable-GZIP-compression-in-Apache-
--------------------------------------


Install Memcache on cPanel server
--------------------------------------
https://grepitout.com/install-memcache-cpanel-server/
--------------------------------------


Direct Admin dataskq high load
---------------------------------
http://www.lifelinux.com/how-do-i-fix-dataskq-causing-high-load-on-directadmin/
---------------------------------


How to setup HTTP2 in cPanel/WHM Linux VPS using EasyApache3
--------------------------------
Ref Link: https://vpsineu.com/blog/how-to-setup-http2-in-cpanelwhm-linux-vps-using-easyapache3/
--------------------------------

How to setup HTTP2 in cPanel/WHM Linux VPS using EasyApache4
----------------------------------
https://www.rosehosting.com/blog/how-to-enable-http2-on-whmcpanel-with-easyapache-4/
----------------------------------


Kernel update
---------------------
savedefault --default=0 --once
---------------------


Disk cleanup Windows Plesk
--------------------
C:\Program Files (x86)\Parallels\Plesk\PrivateTemp
C:\Program Files (x86)\Parallels\Plesk\Backup
--------------------


Xen partiotion error
----------------------
http://sysadminosaurus.blogspot.in/2014/06/xenserver-62-unable-to-find-partition.html
----------------------


How to check Internet speed from the command line on Linux
----------------------
Ref Link: http://xmodulo.com/check-internet-speed-command-line-linux.html

wget -O speedtest-cli https://raw.githubusercontent.com/sivel/speedtest-cli/master/speedtest.py
chmod +x speedtest-cli
mv speedtest-cli /usr/local/bin/
chown root:root /usr/local/bin/speedtest-cli
/usr/local/bin/speedtest-cli
----------------------


To pause Xen VM to change kernel
------------------------------
xl create /home/xen/vm1066/vm1066.cfg -c
------------------------------


**** If the agent is installed on CentOS 7, or if you have installed kernel-devel / kernel-headers and ‘r1soft-setup –get-module’ is still failing, check http://repo.r1soft.com/modules/ for the associated kernel and driver.
Ref: http://geekdecoder.com/installing-r1soft-linux-agent-centos/
------------------------------
# cd  /lib/modules/r1soft/
# wget http://repo.r1soft.com/modules/Centos_7_x64/hcpdriver-cki-3.10.0-693.11.6.el7.x86_64.ko
# insmod  hcpdriver-cki-3.10.0-693.11.6.el7.x86_64.ko
# /etc/init.d/cdp-agent restart
# lsmod | grep hcp
# hcpdriver              81014  4
------------------------------


How to use multiple PHP versions on directadmin
=================================
#cd /usr/local/directadmin/custombuild # cat options.conf | grep -i php
#cd /usr/local/directadmin/custombuild # ./build versions | grep -i php
#cd /usr/local/directadmin/custombuild # ./build version

cd /usr/local/directadmin/custombuild
./build set php1_release 7.0
./build set php2_release 5.6
./build set mod_ruid2=no
./build update
./build php n
./build rewrite_confs
=================================



Ref: https://forums.cpanel.net/threads/e-pre-maintenance-ended-however-it-did-not-exit-cleanly.614507/
=================================
cPanel - E Pre Maintenance ended, however it did not exit cleanly

awk '$4=="E"' /var/cpanel/updatelogs/update.XXXXXX.log
=================================


curl -L http://mysqltuner.pl/ | perl
 
 
Downgrade WowzaStreamingEngine
----------------------
 https://vanmarion.nl/blog/blog/rollback-update-4-0-3-4-0-0/
----------------------


Lets encrypt CLI
-----------------
https://letsencrypt-for-cpanel.com/docs/for-admins/cli-reference/
-----------------




htaccess redirect to https://www
------------------
<IfModule mod_rewrite.c>

RewriteEngine On
RewriteCond !{HTTPS} off
RewriteRule ^(.*)$ https://www.%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
RewriteCond %{HTTP_HOST} !^www\.
RewriteRule ^(.*)$ https://www.%{HTTP_HOST}%{REQUEST_URI} [L,R=301]

</IfModule>
------------------


Install cPanel with Google Compute Engine
-------------------
https://blog.cpanel.com/can-i-install-cpanel-with-google-compute-engine/
-------------------


How to Configure Google Drive for WHM Backup
------------------
https://www.buycpanel.com/configure-google-drive-whm-backup/
------------------



How to setup Mailjet on exim for cPanel dnsonly on Google Cloud .
----------------
https://desantolo.com/2016/12/how-to-setup-mailjet-on-exim-for-cpanel-dnsonly-on-google-cloud/2/
What EXIM needs to have in it’s configuration explained:
First we need to add the authentication credentials for the login. In /etc/exim.conf search for “begin authenticators” immediately below copy and paste my code and make sure to add your API key and password.

mailjet_login:
  driver = plaintext
  public_name = LOGIN
  client_send = : {YOUR_API_KEY_GOES_HERE} : {YOUR_PASSWORD}
Now we need to tell exim how to route mail and the rules to bound emails to (basically anything that is not local mail to use the new transport we will be creating on step 3). Search for “begin routers” paste my code and make sure to edit “in-v3.mailjet.com” with the server where your mailjet account got provisioned. You can obtain this from mailjet’s “configure my SMTP”

send_via_mailjet:
 driver = manualroute
 domains = ! +local_domains
 transport = mailjet_smtp
 route_list = "* in-v3.mailjet.com::2525 byname"
 host_find_failed = defer
 no_more
Now we need to create a new email “transport” to rely on mailjet for sending (aka be our middle man), search for “begin transports” and add the following…paste my code and make sure to edit “in-v3.mailjet.com” with the server where your mailjet account got provisioned

mailjet_smtp:
  driver = smtp
  hosts = in-v3.mailjet.com
  hosts_require_auth = <; $host_address
  hosts_require_tls = <; $host_address
Now its time to restart exim to load the changes. Restart the service, on CentOS 7.3 the command would be

# systemctl restart exim.service
If you correctly followed the directions, adding the 3 needed sections to exim.conf and restarted the service now you should be able to try sending yourself a test email. You can do so from the command line like so:

# echo "Subject: desantolo rocks!" | sendmail -v your@email.com
The “-v” will make this transaction be verbose so you can troubleshoot it. You should see a successful email send to the mail relay mailjet server. Important: the email will not be in your inbox yet! You have to approve the sender (the email most likely was sent from root@yourGCE.hostname). I won’t get into the details of how to whitelist because on your mailjet.com dashboard you will see an error message that will say the same thing and point you to their documentation that is simple enough to follow to get your sender whitelisted (in this case root@yourGCE.hostname)
----------------



Install / configure spam experts
-----------------
https://kb.spamexperts.com/29941-integration/227827-cpanel-addon
-----------------

cPanel DNS plugin
---------------------
https://applications.cpanel.net/listings/view/Domains-Statistics/showAsListingCategory:Domains-DNS
---------------------


How to block emails by domain in WHM / Exim
-------------------
https://deano.me/2016/05/how-to-block-emails-by-domain-in-whm-exim/
-------------------



https://applications.cpanel.net/listings/view/SpamExperts-cPanel-add-on




http://thecpaneladmin.com/installing-imagemagick-oncpanel-server/
---------------------------
perl -MCPAN -e 'CPAN::Shell->r'
yum -y install ImageMagick-perl
[root@georgia ~]# /scripts/perlinstaller Image::Magick

# /scripts/perlinstaller DBI
# /scripts/perlinstaller DBD::mysql
---------------------------



https://hostingfixes.wordpress.com/2014/09/05/warning-lastline-parameter-in-history-file-is-so-in-future-may-be-you-need-to-correct-manually-the-line-lastline-in-some-awstats/
--------------------
This warning is erroneously generated because of the difference between GMT and your server local time. Just comment out the line generating the warning in awstats.pl.

Go to

/usr/local/cpanel/3rdparty/bin/awstats.pl
and search for this particular line in it and comment it with a # like below

# Warning if lastline in future
if ( $LastLine > ( $nowtime + 20000 ) ) {
warning(
#”WARNING: LastLine parameter in history file is ‘$LastLine’ so in future. May be you need to correct manually the line LastLine in some awstats*.$SiteConfig.conf files.”
);
}
--------------------



Downgrade MySQL on cPanel server
-------------------
https://iserversupport.com/downgrade-mysql-on-cpanel-server/
-------------------


Using .htaccess to make all .html pages to run as .php files?
-----------------------
https://stackoverflow.com/questions/4687208/using-htaccess-to-make-all-html-pages-to-run-as-php-files
https://stackoverflow.com/questions/4687208/using-htaccess-to-make-all-html-pages-to-run-as-php-files/4687217
-----------------------


install clamav
------------------------
https://www.adminbirds.com/cpanel/install-clamav-on-cpanel-server/
https://www.crybit.com/install-clamav-on-a-cpanel-server/
------------------------



https://nixmash.com/post/fix-for-mysql-rootlocalhost-access-denied-on-new-installs
Access denied for user 'root'@'localhost' (using password: YES)
------------------------
service mysql status
service mysql stop
mysqld_safe --skip-grant-tables
UPDATE mysql.user SET authentication_string = PASSWORD('mypassword'), plugin = 'mysql_native_password' WHERE User = 'root' AND Host = 'localhost';
FLUSH PRIVILEGES;
You may have to kill the mysqld PID ($ sudo kill -9 [PID]) before restarting the DB Server with
service mysql start
------------------------



Install, Configure and Activate RD Licensing
------------------------
https://www.youtube.com/watch?v=r_fMZ9qFAA8
------------------------


How to install Gdrive in CentOS
-------------------
https://www.gocit.vn/bai-viet/how-to-install-gdrive-in-centos/
-------------------


https://gist.github.com/lifeofguenter/45d71d622a4aeea06346


Turn Off Windows firewall in rescue mode using VNC viewer
-----------------------
Ref Link: https://mysuperweb.co.uk/server/windows-firewall/

The first step is to load up CMD-Line, from here we will load up the server registry.

reg load HKLM\Win_SYSTEM C:\windows\system32\config\system

Afterwards we can edit the registry by running the command of regedit.

The firewall setting is located at:

\HKEY_LOCAL_MACHINE\Win_SYSTEM\ControlSet001\Services\SharedAccess\Parameters\FirewallPolicy\PublicProfile
In our example our path is set on ControlSet001. Its possible that you may have multiple ControlSet and it might be different values. This is dependent on your environment.

Here we can see a file called EnableFirewall The current value is 1, we will be looking to change the value into 0.

reg unload HKLM\Win_SYSTEM
-----------------------



change Joomla charset
------------------
https://stackoverflow.com/questions/32565996/how-joomla-selects-charset
------------------


Run jetbackup manually
----------------
https://docs.jetapps.com/jetbackup/jbmcli-manually-running-a-backup-job-from-the-command-line

jetcli backup -P backupmanager::jobs
jetcli backup -vfR jobs -I IDofJob
/etc/jetapps/apps/jetbackup/cli backup -P backupmanager::jobs
/etc/jetapps/apps/jetbackup/cli backup -P backup -vfR jobs -I 1
/etc/jetapps/apps/jetbackup/cli backup -R clearcache
----------------


Set up external IP address for SPF
-----------------
https://techninan.wordpress.com/2012/09/01/change-ip-for-spf-configration-of-all-accounts-in-cpanel/
http://coderstent.com/external-mail-server-spf-setup-cpanel-server/
-----------------


SSL error in Google Chrome
-------------------------------
https://www.codebyamir.com/blog/the-ssl-certificate-used-to-load-resources-from-httpsxxxcom-will-be-distrusted-in-m70-once-distrusted-users-will-be-prevented-from-loading-these-resources
-------------------------------

How to enable browser caching server wide
----------------------
https://www.liquidweb.com/kb/how-to-configure-apache-2-to-control-browser-caching/
----------------------


How to enable personalize in Non-digest Mailman
------------------
Ref Link: http://www.gnu.org/software/mailman/mailman-admin/node18.html
https://wiki.list.org/DOC/How%20do%20I%20enable%20personalization%20%28messages%20tailored%20to%20the%20recipient%29%3F

nano /usr/local/cpanel/3rdparty/mailman/Mailman/mm_cfg.py
OWNERS_CAN_ENABLE_PERSONALIZATION = 1
------------------


Install rsyslog on cPanel 
------------------------
WHM >> Service Manager to see if it's present
[root@oscar ~]# yum install rsyslog
[root@oscar ~]# /usr/local/cpanel/scripts/restartsrv rsyslogd
[root@oscar ~]# /scripts/restartsrv_rsyslogd --status
rsyslog (/usr/sbin/rsyslogd -n) is running as root with PID 28908 (systemd+/proc check method).
------------------------



Run different sub-folders under WordPress
----------------------
https://tanyanam.com/2012/12/09/wordpress-exclude-directory-from-url-rewrite-with-htaccess/
https://stackoverflow.com/questions/2322559/htaccess-wordpress-exclude-folder-from-rewriterule
https://sumtips.com/snippets/htaccess/exclude-folder-from-htaccess-rewrite-rules/
----------------------


Set up Git
----------------
https://documentation.cpanel.net/display/CKB/Guide+to+Git+-+Host+Git+Repositories+on+a+cPanel+Account#903128a78d9f42bcae40860259cf86e4
https://documentation.cpanel.net/display/CKB/Guide+to+Git+-+How+to+Set+Up+Deployment+Cron+Jobs
https://documentation.cpanel.net/display/CKB/Guide+to+Git
http://monkeylogic.com/using-cpanel-to-host-your-git-repository-and-deploy-automatically/
----------------



Install office application on Linux
-----------------
https://tecadmin.net/install-apache-openoffice-on-centos-rhel-and-fedora/
https://www.if-not-true-then-false.com/2010/install-openoffice-org-on-fedora-centos-red-hat-rhel/
https://www.tecmint.com/microsoft-office-alternatives-for-linux/
https://www.tecmint.com/install-libreoffice-on-rhel-centos-fedora-debian-ubuntu-linux-mint/
-----------------



Setup quota on OpenVZ VPS containers
-----------------
https://serversitters.com/setup-quota-on-openvz-vps-containers.html
https://www.crybit.com/whm-showing-disk-usage-0-for-all-users-in-openvz-vps/
-----------------



SFTP through cpanel
===============
https://www.peopleshost.com/2018/02/guide-use-sftp-to-connect-to-a-cpanel-account/
==================


/usr/local/lsws/admin/misc/enable_ruby_python_selector.sh




https://docs.jetbackup.com/manual/whm/CommandLineTools/importExportSettings.html
https://docs.jetbackup.com/manual/whm/CommandLineTools/showHelpScreen.html



https://www.rosehosting.com/blog/install-redis-and-redis-php-on-cpanel/


How to block emails by domain in WHM / Exim
--------------
https://deano.me/2016/05/how-to-block-emails-by-domain-in-whm-exim/
--------------


LVE unable to start
----------------
yum reinstall alt-python27-cllib
lve-create-db --create-missing-tables
systemctl start lvestats
------------------


SMTP mail server on Windows 2016
===================
http://www.vsysad.com/2017/05/install-and-configure-smtp-server-on-windows-server-2016/
http://www.vsysad.com/2014/01/iis-smtp-folders-and-domains-explained/
https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2003/cc738146(v=ws.10)
https://dailysysadmin.com/KB/Article/990/setup-smtp-open-relay-onsite-windows-server-office-365/
===================


https://www.linuxhelp.com/how-to-install-sox-on-centos-6



Remove duplicate packages CL
-----------------------
https://cloudlinux.zendesk.com/hc/en-us/articles/115005427605-How-do-I-fix-duplicated-packages-issue
-----------------------





https://forums.cpanel.net/threads/imagick-pecl-refuses-to-install-for-php-7-1.654383/
# /opt/cpanel/ea-php71/root/usr/bin/pecl config-set php_bin /opt/cpanel/ea-php71/root/usr/bin/php
config-set succeeded

# /opt/cpanel/ea-php71/root/usr/bin/pecl config-set php_ini /opt/cpanel/ea-php71/root/etc/php.ini
config-set succeeded

# /opt/cpanel/ea-php71/root/usr/bin/pecl config-set bin_dir /opt/cpanel/ea-php71/root/usr/bin/
config-set succeeded




Stop lfd notifications
------------------

nano /etc/cpanel_exim_system_filter

Add following code at the end of file

if
$header_subject: matches "lfd*"
then
seen finish
endif

Restart exim service
---------------------
