# OnlineExamSystem
OnlineExamSystem for Software Quality Assurance and Testing course, Spring 2020, NENU 

## 项目描述
- 此项目为一个基于 `Vue + SpringBoot` 的 **前后端分离** 的在线考试系统
- 前端方面：使用了 `Vue 全家桶 + Webpack` 等前端新技术 
- 后端方面：基于 `SpringBoot` 搭建 `SSM` 框架
- 包括学生端、教师端和管理员端 
- 采用模块化、组件化、工程化的模式开发 

## 项目功能


## 开发环境介绍
>远程服务器版本：Aliyun云服务器ECS、CentOS 7.3 64位

### 前端工具和环境
- 开发工具：Microsoft VS Code x64 1.44.2
- Node.js：V10.15.0
- Vue.js：V2.5.21
- 版本控制工具：Git

### 后端工具和环境
- 开发工具：IntelliJ IDEA 2020.1.1 x64
- Java版本：jdk1.8
- 本地服务器：Tomcat 9.0.6
- 数据库：MySQL 8.0
- 版本管理工具：Maven 3.5.4
- 版本控制工具：Git 2.18.0 x64

## 后端项目入口
- 本地：`localhost:8080`（本地跑需导入数据库文件，路径：`OnlineExamSystem\db_onlineexam.sql` ）
- 远程服务器：`120.26.186.88:8080`（前端Vue代码接口对接的是远程服务器端口）

## 关键技术
>框架组合：SpringBoot + Vue.js 前后端分离模式

### 前端：Vue 插件或第三方库
- Vue.js 框架
- vue-router 开发单页应用 
- 使用 vue-cli 脚手架初始化 Vue.js 项目
- 使用 axios/vue-resource 与后端进行数据交互
- 使用 mint-ui、muse-ui 和 element-ui 组件库构建界面
- 使用 mockjs 模拟后台数据接口 

### 后端
- SpringBoot 框架
- SpringMVC 开发模式
- MyBatis 数据库操作工具
- MySQL 数据库
- Maven 版本控制
- FastJson 解析Json数据
- Junit 单元测试
- 后台接口API: Swagger

## Git 提交日志
>2020.06.15-2020.06.29：项目组处于开发阶段。由于项目采用前后端分离模式，为了便于代码管理，前后端小组在各自仓库进行协同开发。

### 前端仓库
- 仓库地址：https://github.com/NENU-ST2020-TEAM/OnlineExamFrontEnd
- 日志截图：[前端仓库日志操作](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/1.jpg)

### 后端仓库
- 仓库地址：https://github.com/NENU-ST2020-TEAM/OnlineExamBackEnd
- 日志截图：[后端仓库日志操作](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/2.jpg)

>2020.06.30-2020.07.05：项目组处于代码测试阶段。将前后端仓库合并，进行项目分阶段测试。