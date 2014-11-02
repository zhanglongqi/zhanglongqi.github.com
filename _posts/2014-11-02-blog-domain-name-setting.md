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

```
$ dig blog.longqi.pro +nostats +nocomments +nocmd  
```

##2. bind your domain name to your blog

Create a `CNAME` file in your `USERNAME.github.com` repository:

```
$ vim CNAME 
```

Put your domain name inside:


```
$ cat CNAME 
blog.longqi.pro
```

then commit and push you can access your github page by domain **after a while**, the DNS synchronization needs time.
