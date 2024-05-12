# OnlineExamSystem
OnlineExamSystem, Software Testing and Quality Assurance course, 2020 Spring, NENU

## 项目描述
- 此项目为一个基于 `Vue + SpringBoot` 的 **前后端分离** 的在线考试系统
- 前端方面：使用了 `Vue 全家桶 + Webpack` 等前端新技术 
- 后端方面：基于 `SpringBoot` 搭建 `SSM` 框架
- 包括学生端、教师端和管理员端 
- 采用模块化、组件化、工程化的模式开发 

## 项目功能
### 基本功能
>学生端
- 注册登录
- 在线考试
- 考试有起止时间限制
    - 若未到考试开始时间，学生无法查看试卷
    - 学生在考试时超过答题时长，则自动交卷
    - 若当前时间已超过，教师设置的可查看试卷时间，则学生无法查看试卷
- 在个人中心查看分数

>教师端
- 登录
- 试题管理功能：增删改，模糊查询
    - 试题种类包括： 选择（单选）题、判断题、填空题，主观题（简答题） 可选择。
- 试卷管理功能：增删改，模糊查询
- 两种方式生成试卷
    - 教师在线出题并生成试卷，试卷存入“试卷库”，然后发布并考试
    - 教师事先在线录入试题，试题分类存入试题库。教师生成试卷时从题库抽取各类试题组卷
- 在线发布试卷
- 学生成绩管理功能

>管理员端
- 登录
- 试题管理功能
- 试卷管理功能
- 学生成绩管理功能
- 用户管理功能（修改用户权限，删除用户）

### 关于错误输入的处理
- **登录注册**：输入为空，用户名不存在，密码输入有误等非法提示
- **考试时长**：输入字母，负数等非法提示
- **权限判断**：防止入侵者非法从 `URL` 进入后台系统

### 附加功能
- **自动批改简答题**：在计算成绩时，系统不仅可自动批改选择题，判断题及填空题，还可以自动批改简答题
- **公告管理**：在基础需求上，添加公告管理功能，教师和管理员均可在线发布考试公告，发布的公告显示在学生端
- **错题集功能**：在系统批改学生试卷时，若该学生在某道题上没有得到满分，系统自动会将该题收录到该学生的错题集中
- **密码 `MD5` 加密**：为确保安全，将用户密码 `MD5` 明文加密后存入数据库
- **权限判断**：防止非法进入系统操作数据

### 部分页面展示
![online-exam-01](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/online-exam-01.png)
![online-exam-02](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/online-exam-02.png)
![online-exam-07](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/online-exam-07.png)

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
- 日志截图：[前端操作日志截图](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/online-exam-08.jpg)

### 后端仓库
- 仓库地址：https://github.com/NENU-ST2020-TEAM/OnlineExamBackEnd
- 日志截图：[后端操作日志截图](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/online-exam-09.jpg)

### 项目总仓库
>2020.06.30-2020.07.05：项目组处于代码测试优化阶段。将前后端仓库合并，进行项目分阶段测试。
- 仓库地址：https://github.com/NENU-ST2020-TEAM/OnlineExamSystem
- 日志截图：[测试阶段日志截图](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/online-exam-10.jpg)
