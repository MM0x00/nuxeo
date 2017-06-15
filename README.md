# nuxeo 在线实验环境

## 软件简介

Nuxeo平台是一个高度可定制和可扩展的内容管理平台，用于构建业务应用程序。

所属类别是建站系统

## 软件官网

https://www.nuxeo.com/

## Dockerfile 使用方法

### 如何使用
启动一个裸的nuxeo实例
```
$ docker run --name mynuxeo -p 8080:8080 -d nuxeo
```
这个图像包括EXPOSE 8080（nuxeo端口）。应用默认的Nuxeo配置，其具有嵌入式数据库（H2）和嵌入式弹性搜索实例。此设置不适合生产。了解如何通过指定环境变量来设置生产就绪容器。

Nuxeo平台可以访问http：// $ {DOCKER_HOST}：8080 /，默认用户和密码为管理员/管理员。

启动一个nuxeo一些额外的包
```
$ docker run --name mynuxeo -p 8080:8080 -e NUXEO_PACKAGES="nuxeo-web-mobile nuxeo-drive nuxeo-diff nuxeo-spreadsheet nuxeo-dam nuxeo-template-rendering nuxeo-template-rendering-samples nuxeo-showcase-content"
nuxeo
```

## 资源链接

- https://en.wikipedia.org/wiki/Nuxeo
