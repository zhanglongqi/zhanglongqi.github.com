---
layout: post
title: "blog domain name setting"
description: ""
category: 
tags: []
---
{% include JB/setup %}

##1. set your DNS record:
Create  a CNAME record to your `USERNAME.github.io`, notice the `io` instead of `com`

`CNAME	blog.longqi.pro	benhuan.github.io	300	N/A	`

After a while, you can verify your setting by `dig` command:

```sh
# longqi at zlq in ~/jekyll/benhuan.github.com on git:master o [23:34:31]
$ dig blog.longqi.pro +nostats +nocomments +nocmd           

; <<>> DiG 9.9.5-3-Ubuntu <<>> blog.longqi.pro +nostats +nocomments +nocmd
;; global options: +cmd
;blog.longqi.pro.		IN	A
blog.longqi.pro.	29	IN	CNAME	benhuan.github.io.
benhuan.github.io.	2750	IN	CNAME	github.map.fastly.net.
github.map.fastly.net.	18	IN	A	103.245.222.133
```
##2. bind your domain name to your blog

Create a `CNAME` file in your `USERNAME.github.com` repository:
```sh
# longqi at zlq in ~/jekyll/benhuan.github.com on git:master x [23:35:28]
$ vim CNAME 
```
Put your domain name inside:
```sh
# longqi at zlq in ~/jekyll/benhuan.github.com on git:master x [23:35:28]
$ cat CNAME 
blog.longqi.pro
```
then commit and push you can access your github page by domain **after a while**, the DNS synchronization needs time.
