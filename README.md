## 简介

这是一个基于Springboot2.x，vue2.x的前后端分离的开源智能旅游推荐系统，针对用户输入的旅游偏好描述给出相应的旅游景点推荐。提供前端界面后台服务 的整套系统源码。

- 基于最新的Vue2.x和Elmentui，前端界面清新简洁
- 后台使用Springboot框架
- 基于jieba分词处理技术对输入的语句分解为向量

## 使用技术

- SpringBoot 2.x 后台基本框架
- Vue 2.x 前端基本框架
- ElementUI：后台管理页面UI库
- 后羿数据采集器 数据爬取
- jieba分词技术 语句拆解
- axios 前后端数据请求
- Mybatis 数据库连接

## 模块分层

### 后端模块

```shell
├── HELP.md
├── mvnw
├── mvnw.cmd
├── pom.xml
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── zju
│   │   │           └── scenic
│   │   │               ├── Hello.java
│   │   │               ├── ScenicApplication.java
│   │   │               ├── config #配置参数
│   │   │               │   ├── dao
│   │   │               │   │   ├── DataSourceConfiguration.java
│   │   │               │   │   └── SessionFactoryConfiguration.java
│   │   │               │   ├── service
│   │   │               │   │   └── TransactionManagementConfiguration.java
│   │   │               │   └── web
│   │   │               │       └── MvcCongituration.java
│   │   │               ├── dao #数据库查询
│   │   │               │   ├── ScenicDao.java
│   │   │               │   ├── ScenicVectorDao.java
│   │   │               │   └── WordVectorDao.java
│   │   │               ├── entity #创建实体类
│   │   │               │   ├── Cos.java
│   │   │               │   ├── Scenic.java
│   │   │               │   ├── ScenicVector.java
│   │   │               │   └── WordVector.java
│   │   │               ├── service #服务层 逻辑实现
│   │   │               │   ├── ScenicService.java
│   │   │               │   └── impl
│   │   │               │       └── ScenicServiceImpl.java
│   │   │               └── web #controller层 方法实现
│   │   │                   └── ScenicController.java
│   │   └── resources
│   │       ├── application.properties #数据库，mybatis配置文件
│   │       ├── mapper 
│   │       │   ├── ScenicDao.xml
│   │       │   ├── ScenicVector.xml
│   │       │   └── WordVectorDao.xml
│   │       ├── mybatis-config.xml
│   │       ├── static
│   │       └── templates
│   └── test #测试文件
│       └── java
│           └── com
│               └── zju
│                   └── scenic
│                       ├── ScenicApplicationTests.java
│                       ├── dao
│                       │   ├── ScenicDaoTest.java
│                       │   ├── ScenicVectorDaoTest.java
│                       │   └── WordVectorDaoTest.java
│                       ├── service
│                       │   └── ScenicServiceTest.java
│                       └── util
│                           └── AnsjTest.java
└── tree.text
```

### 后台依赖关系

dbblog-core -> dbblog-auth -> dbblog-manage -> dbblog-portal -> dbblog-search

- 采用多模块的形式，便于后续SpringCloud微服务的改造升级

### 前端模块

#### 前台页面

```shell
├── ai.html //项目主文件
├── main.jpg //背景图片
```

## 项目部署

### 服务端

项目后端环境

- JDK1.8
- Mysql5.7
- Mybatis 2.1
- Eclipse编译器

部署步骤：

1. 创建数据库scenic，并导入所有sql文件
2. 修改src/main/resource里的application.properties的数据库连接、redis连接、
3. 导入项目，并且运行src/main/java里的ScenicApplication.java方法

### 前端

前端环境：

- Node.js 8.0+
- SubLime编辑器

部署步骤：

1. 在Chorme中安装Moesif Orign & CORS Changer 跨域软件，开启跨域开关
2. 启动项目：右键浏览器中直接访问html文件



## 算法训练

### 环境配置

安装jupyter book，载入代码点击Run即可运行



## 界面预览





![RUNOOB 图标](https://wx2.sinaimg.cn/mw690/006f6eXoly1g908sxg5nkj31di0u01kz.jpg)

![RUNOOB 图标](https://wx4.sinaimg.cn/mw690/006f6eXoly1g908stqvu4j31e30u0kjn.jpg)



![页面](https://wx2.sinaimg.cn/mw690/006f6eXoly1g908su6x65j31bi0u01kz.jpg)





## 碎碎念

这是我们的一次不成功的实验，欢迎大家star～