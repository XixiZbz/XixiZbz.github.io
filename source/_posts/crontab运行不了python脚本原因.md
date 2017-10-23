title: 疑难杂症集锦
author: John Doe
date: 2017-10-20 14:45:53
tags:
---
- 可能与linux 下python 有两个版本有关系，没时间折腾这个问题，使用程序内部定时功能，再加上supervisor监控程序防止报错关闭，同时输出错误日志。暂时绕开这个问题
<!--more-->

- yaml 报错 
	```
   yaml.scanner.ScannerError: while scanning for the next token
   found character '%' that cannot start any token yaml
   ```
   - 原因：配置里有非法字符%，用''转义一下就好