---
layout:     post
title:      Putty支持中文显示和输入 
category: blog
description: 可以让putty支持中文显示和中文输入，这样通过term编辑blog就方便多了。
---
<br>
对于经常在windows下远程ssh到linux的用户而言，putty可能是你最好的选择。
<br>
可是缺省情况下，putty对中文的支持却让人不敢恭维，如果远程linux的locale设置为zh_CN.*(bg2312,gbk,utf8等等），显示就是乱码。经研究发现，其实putty的中文支持还是很好的，呵呵
<br>
打开putty主程序，选择window-〉Appearance-〉Font settings-〉Change...,选择Fixedsys字体,字符集选择CHINESE_GB2312。
在window-〉Appearance-〉Translation中，Received data assumed to be in which character set 中,把Use font encoding改为UTF-8.
如果经常使用,把这些设置保存在session里面.<br>
<br>
现在打开putty,登录成功后,在shell中输入:export LC_ALL='zh_CN.utf8',现在已经可以完美的支持中文了 [微笑]
<br>
可以打开vim输入中文测试一下,而且也不会出现删除半个汉字的问题. 
