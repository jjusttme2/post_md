---
title: welcome
date: 2018-10-01 19:14:00
tags:
 - 测试
 - 样式
---
你好

### bash
``` bash
# this is comments
$ whoami
> root
```

### xml

``` xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE validators PUBLIC
	"-//OpenSymphony Group//XWork Validator 1.0//EN"
	"http://www.opensymphony.com/xwork/xwork-validator-1.0.2.dtd">
<validators>
	<field name="age">
		<field-validator type="int">
			<param name="min">1</param>
			<param name="max">150</param>
		</field-validator>
	</field>
</validators>
```
### html
``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">

<html xmlns="http://www.w3.org/1999/xhtml">
<head profile="http://gmpg.org/xfn/11">
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<meta http-equiv="X-UA-Compatible" content="IE=EmulateIE7" />
	<title>test</title>
	<link rel="alternate" type="application/rss+xml" title="RSS 2.0 - 所有文章" href="http://www.netingcn.com/feed" />
	<link rel="alternate" type="application/rss+xml" title="RSS 2.0 - 所有评论" href="http://www.netingcn.com/comments/feed" />
	<link rel="pingback" href="http://www.netingcn.com/xmlrpc.php" />
	<link rel="stylesheet" href="/wp-content/plugins/wp-page-numbers/default/wp-page-numbers.css" type="text/css" media="screen" />
	<script type="text/javascript" src="/wp-content/themes/inove/js/base.js"></script>
</head>

<body>
<!-- wrap START -->
<div id="wrap">

<!-- container START -->
<div id="container"  >

<script type="text/javascript">
  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'UA-26597002-1']);
  _gaq.push(['_trackPageview']);

  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();
</script>


<!-- header START -->
<div id="header">
	<!-- banner START -->
		<!-- banner END -->
	<div id="newlogo">
		<div id="img"><a href="/"><img src="/netingcn-logo.png" /></a></div>
		<div id="desc">
			<h1>网络进行时</h1>
	</div>
	</div>
	<div class="fixed"></div>
</div>
<!-- header END -->


<p style="margin:0;padding:0;height:1px;overflow:hidden;">
    <script type="text/javascript"><!--
        var wumiiSitePrefix = "http://www.netingcn.com";
        var wumiiEnableCustomPos = true;
        var wumiiParams = "&num=4&mode=3&displayInFeed=1&version=1.0.5.7&pf=WordPress3.6";
        var wumiiCategories = ["Linux"];
    //--></script><script type="text/javascript" src="http://widget.wumii.cn/ext/relatedItemsWidget"></script><a href="http://www.wumii.com/widget/relatedItems" style="border:0;"><img src="http://static.wumii.cn/images/pixel.png" alt="alt" style="border:0;padding:0;margin:0;" /></a>
</p><script type='text/javascript' src='http://www.netingcn.com/wp-content/plugins/akismet/_inc/form.js?ver=3.1.3'></script>

<script type="text/javascript" src="/gotop.js"></script>
</body>
</html>

```

### C
``` c
#include <stdio.h>

int main()
{
    int x;
    /* The loop goes while x < 10, and x increases by one every loop*/
    for ( x = 0; x < 10; x++ ) {
        /* Keep in mind that the loop condition checks 
           the conditional statement before it loops again.
           consequently, when x equals 10 the loop breaks.
           x is updated before the condition is checked. */   
        printf( "%d\n", x );
    }
    getchar();
}
```



### java
``` java
public class UserAction extends ActionSupport {
	private Integer age;
	private String name;
	private String email;
}
```
### python

``` python
import base64

a = base64.b64decode('AAoHAR0jJ1AlVVEkU1BUVCAlIlFTUVUiUFRTVFVeU1FXUCVUJxs=')

print(a)

s = '\x00\n\x07\x01\x1d#\'P%UQ$SPTT %"QSQU"PTSTU^SQWP%T\'\x1b'

print(s)
print ord(30)

for n in range(30,126):
    flag = ''
    for i in s:
        flag += chr(ord(i)^n)
    if 'flag' in flag:
        print(flag)

```
### php
``` php
<?php
$connec=mysql_connect("localhost","root","root") or die("不能连接数据库服务器： ".mysql_error());
mysql_select_db("liuyanben",$connec) or die ("不能选择数据库: ".mysql_error());
mysql_query("set names 'gbk'");
?> 
```


