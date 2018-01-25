---
layout: post
title:  "Code Syntax Testing"
date:   2016-12-17 23:40:00 +0100
categories: jekyll update
---

Jekyll also offers powerful support for code snippets:

{% highlight php  %}
<?php 
echo "hello";
?>
{% endhighlight %}


{% highlight bash %}
sudo bash
cd /usr/local/src/
wget http://www.no-ip.com/client/linux/noip-duc-linux.tar.gz
tar xf noip-duc-linux.tar.gz
cd noip-2.1.9-1/
make install
{% endhighlight %}