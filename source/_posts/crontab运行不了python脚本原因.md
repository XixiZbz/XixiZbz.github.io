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
   
   
- sys获取的路径是执行程序的路径，不是模块内的路径，注意
- ``` navigator.userAgent
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/61.0.3163.100 Safari/537.36"```

- centos7 安装双版本Python ，命令行 command not found 出现，需要将Python3的路径加入环境变量。

  ```
  PATH=$PATH:$HOME/bin:

  PATH=$PATH:$HOME/bin:/usr/local/python3/bin

  ```
- 腾讯云主机的端口开发需要配置安全组策略，在控制台处。