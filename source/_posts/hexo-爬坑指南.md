title: 如何用hexo部署自己的博客
tags:
  - hexo
  - mac
  - win 10
categories: []
date: 2017-10-03 22:57:00
---
#### 环境介绍:
- Macbook pro 和 win10 PC各一台,家中自用Macbook pro ，工作使用Win10电脑。

#### 部署要求：
- 在公司和家中都无缝使用hexo更新部署博客



#### 使用软件及服务
- hexo 用于博客的开发和编辑
- github 用于部署博客，使用xxxx.github.io域名，方便易记。同时记录代码，方便异地下载更新


#### 安装步骤

1. **[安装hexo](http://ibruce.info/2013/11/22/hexo-your-blog/)**
2. **安装github**,太简单了

3. **[异地更新办法](https://www.zhihu.com/question/21193762)**

#### 常见问题:

- [常见问题](http://xuanwo.org/2014/08/14/hexo-usual-problem/#%E6%9C%AC%E5%9C%B0%E6%B5%8F%E8%A7%88%E6%B2%A1%E9%97%AE%E9%A2%98%EF%BC%8CDeploy%E6%8A%A5%E9%94%99)

- [hexo -d 报错](https://www.zhihu.com/question/38219432)


- WARN No layout: index.html （本地主题文件没有部署好，将主题文件git clone到目录下theme文件夹下，改_config.yml下theme属性，注意，该属性名字与theme文件夹下主题文件夹名相同）