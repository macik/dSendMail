dSendMail2 (version 2.37 from 20/07/2010)
==========

PHP Class to sending SMTP e-mails.

Original credits:
-----------------

*  Author:  Alexandre Tedeschi (d)
*  E-Mail:  alexandrebr at gmail dot com
*  Company: www.imaginacom.com
*  Londrina - PR / Brazil
*  License: Freeware

Requirements:
-------------

    If you want to use SMTP, sockets must be enabled
    If your SMTP server uses SSL, SSL extension must be enabled
    No other classes are required

Other credits:
--------------

* Thanks to Manuel Lemos  (SMTP and SASL classes)
* Thanks to Richard Heyes (MIME classes)

Public properties
=================

```php
$m->error (Read-only property)
$m->delay (default: 1. Seconds of delay when mass-mailing)

$m->debug (dumping-debug)
$m->logFolder (default: false. fill it if you want to save logs)
$m->logFile   (default: false. fill it if you want to save logs)
```

Public methods
==============

```php
$m->easyMail   ($to, $subject, $message[, $from[, $html[, $attach]]])
$m->setPriority($priority)   (1=High, 3=Normal, 5=Low)
$m->setCharset ($charset)
$m->setFrom    ($from_mail[, $from_name])
$m->setTo      ($visible_targets)
$m->setBcc     ($hidden_targets)
$m->setSubject ($subject)
$m->setMessage ($body[, $isHtml[, $autoNl2br]])
$m->autoAttachFile($filename, $filedata)
$m->send       ([$startInPart])

$m->setHTMLFile($filename[, $importImages])
$m->setEMLFile ($filename)
$m->importHTML ($filebody, $baseDir[, $importImages])
$m->importEML  ($filebody)
$m->exportEML  ([$setUnsent])

$m->sendThroughSMTP($server[, $port[, $user[, $pass[, $ssl]]]])
$m->sendThroughMail()
$m->sendThroughGMail  ("username@gmail.com",   "password");
$m->sendThroughYahoo  ("username@yahoo.com",   "password");
$m->sendThroughHotMail("username@hotmail.com", "password");

$m->allowDupe() (Allow duplicated targets)
$m->blockDupe() (Automatically remove duplicated targets in To/Cc/Bcc list - Default)
```

Note: see example files to get real usage cases.

