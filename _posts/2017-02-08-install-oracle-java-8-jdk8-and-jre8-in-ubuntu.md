---
title: Install Oracle Java 8 (JDK8 and JRE8) in Ubuntu
tags: Ubuntu Oracle Java Aptitude JDK
---
Currently java stable version is 8.

![Oracle Java]({{ "/assets/oracle-java.png" | absolute_url }})

to install it do these steps:

```bash
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

if an 503 error occured, you are so bad luck because of restrictred countries:

<http://www.oracle.com/us/products/export/export-regulations-345813.html>

So you must proxy your aptitude. edit /etc/apt/apt.conf file and add these lines:

```bash
Acquire::http::Proxy "your-proxy-url";
Acquire::https::Proxy "your-proxy-url";
```

fill with your correct proxy url. then do install steps again.

good luck!