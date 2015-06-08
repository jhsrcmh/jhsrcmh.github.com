---
layout: post
title: "Jsoup使用概览"
description: ""
category: 
tags: [工具]
---
{% include JB/setup %}
最近小伙伴们用Java做爬虫比较多。[Jsoup](http://www.jsoup.org) 是一个小巧，实用的http客户端，提供简洁明了的DOM析取方法。详细的实用教程见Jsoup的[cookbook](http://jsoup.org/cookbook/)。

与Scrapy不同，Jsoup提供的只是简单http客户端的功能，对于HTTP请求链接详见[这里](http://stackoverflow.com/questions/7744075/how-to-connect-via-https-using-jsoup)。

1. Jsoup Connect Options
    * data
      data客户端请求参数，必须是键值对的形式
    * userAgent 客户端代理，CHROME F12中可以查询相关内容
    * cookie 键值对cookie
    * method
    * header 键值对
    * postDataCharset
2. Jsoup Runtime METHOD()
    * html()析取当前匹配标签下的html子文本，（子html）
    * toString()析取当前匹配标签下的文本，（本html)
    * text()析取当前匹配标签下的文本，(子text)
3. Element Selector Syntax
    * get method. 如getElementById(), getElementByClass(), getElementContainText(),getElementMatchingText()..etc.
    * select. 如select("div.class >div >div >h1")，select("img[src$=.png]"),select("img[src^=.png]"),
  select("img[src*=.png]"),select("div[attr~=regex]")。 
  [点击](http://jsoup.org/cookbook/extracting-data/selector-syntax)查看更具体的。
