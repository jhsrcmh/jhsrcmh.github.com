---
layout: post
title: "scrapy使用技巧"
description: ""
category: 
tags: [工具,爬虫]
---
{% include JB/setup %}
[scrapy](http://scrapy.org/)是一款网络爬虫利器，集合了多种网络客户端开发工具包，支持的协议拓展了http，是一款非常好用的http客户端和网络爬虫工具。
使用非常简单，如下:
 
    from scrapy import Spider, Item, Field
    class Post(Item):
        title = Field()
    class BlogSpider(Spider):
        name, start_urls = 'blogspider', ['http://blog.scrapinghub.com']
        def parse(self, response):
            return [Post(title=e.extract()) for e in response.css("h2 a::text")]


1. 安装

  简易安装如下:
    
    $sudo pip install --upgrade pip
    $sudo pip install scrapy 
    $sudo pip install scrapy --upgrade

  完成上述两步，您应该能够成功的使用scrapy了。
  BUT～～～～～

    gcc error exit with 1

  那应该是gcc以来的python编译包不够，输入下面命令:

    $sudo apt-get install libxml2-dev libxslt1-dev libffi-dev

  BINGO～～～～～
