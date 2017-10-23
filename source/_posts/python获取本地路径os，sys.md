title: python获取本地路径os，sys
author: John Doe
tags: []
categories: []
date: 2017-10-20 15:02:00
---
```

#!/bin/env python
#-*- encoding=utf8 -*-

import os,sys

if __name__=="__main__":

  print "__file__=%s" % __file__

  print "os.path.realpath(__file__)=%s" % os.path.realpath(__file__)

  print "os.path.dirname(os.path.realpath(__file__))=%s" % os.path.dirname(os.path.realpath(__file__))

  print "os.path.split(os.path.realpath(__file__))=%s" % os.path.split(os.path.realpath(__file__))[0]　　

  print "os.path.abspath(__file__)=%s" % os.path.abspath(__file__)

  print "os.getcwd()=%s" % os.getcwd()

  print "sys.path[0]=%s" % sys.path[0]

  print "sys.argv[0]=%s" % sys.argv[0]
    
```
<!--more-->

输出结果:


```
D:\>python ./python_test/test_path.py
__file__=./python_test/test_path.py
os.path.realpath(__file__)=D:\python_test\test_path.py
os.path.dirname(os.path.realpath(__file__))=D:\python_test
os.path.split(os.path.realpath(__file__))=D:\python_test
os.path.abspath(__file__)=D:\python_test\test_path.py
os.getcwd()=D:\
sys.path[0]=D:\python_test
sys.argv[0]=./python_test/test_path.py
```