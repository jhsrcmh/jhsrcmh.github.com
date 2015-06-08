---
layout: post
title: "python开发常见问题"
description: ""
category: 
tags: [工具]
---
{% include JB/setup %}
####1. UnicodeEncodeError: 'ascii' codec can't encode characters in position 12~13

  解决方案: 因为系统编码原因导致.解决办法: 
    
    #encoding=utf-8
    import sys
    reload(sys)
    sys.setdefaultencoding('utf8')
