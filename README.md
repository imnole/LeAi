# Le-AI 智能助手

Le-AI 是一个基于智谱AI大模型的智能对话助手系统，提供多种专业领域的对话支持。

## 功能特点

- 多领域智能对话
  - 通用助手：回答各类常见问题
  - 代码助手：专注编程开发问题
  - 文档助手：协助文档处理工作
  - 办公助手：处理日常办公事务

- 用户系统
  - 支持用户注册和登录
  - JWT token认证
  - 本地/数据库双模式存储

- 历史记录管理
  - 保存对话历史
  - 查看历史对话
  - 删除历史记录

- 响应式设计
  - 支持PC和移动端
  - 优化的移动端交互体验

## 技术栈

### 前端
- Vue 3
- Vite
- Pinia
- Vue Router
- Element Plus
- Axios
- Marked (Markdown渲染)
- Highlight.js (代码高亮)
- SCSS

### 后端
- Spring Boot
- Spring Security
- MyBatis Plus
- MySQL
- JWT
- Lombok
- FastJSON

## 项目结构 
Le-AI/
├── Leai-Vue/ # 前端项目
│ ├── src/
│ │ ├── api/ # API请求
│ │ ├── stores/ # Pinia状态管理
│ │ │ ├── chat.js # 聊天状态
│ │ │ └── user.js # 用户状态
│ │ ├── views/ # 页面组件
│ │ │ ├── Chat.vue # 聊天页面
│ │ │ ├── History.vue # 历史记录页面
│ │ │ └── Login.vue # 登录页面
│ │ └── router/ # 路由配置
│ └── package.json
│
└── Leai-Server/ # 后端项目
├── src/main/java/com/leai/
│ ├── config/ # 配置类
│ │ ├── SecurityConfig.java
│ │ ├── CorsConfig.java
│ │ └── ZhipuConfig.java
│ ├── controller/ # 控制器
│ │ ├── ChatController.java
│ │ ├── AuthController.java
│ │ └── ChatHistoryController.java
│ ├── service/ # 服务层
│ │ ├── ChatService.java
│ │ └── UserService.java
│ ├── entity/ # 实体类
│ │ ├── User.java
│ │ └── ChatHistory.java
│ ├── mapper/ # MyBatis映射
│ │ ├── UserMapper.java
│ │ └── ChatHistoryMapper.java
│ └── util/ # 工具类
│ └── JwtUtil.java
└── pom.xml
## 快速开始

### 环境要求
- JDK 11+
- Node.js 16+
- MySQL 8.0+

### 数据库配置
1. 创建数据库sql
CREATE DATABASE leai CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
2. 执行SQL脚本sql
source /path/to/schema.sql
source /path/to/data.sql
### 后端配置
1. 修改`application.yml`配置yaml
spring:
datasource:
url: jdbc:mysql://localhost:3306/leai
username: your_username
password: your_password
zhipu:
api:
key: your_zhipu_api_key
2. 启动后端服务bash
cd Leai-Server
./mvnw spring-boot:run
### 前端配置
1. 安装依赖bash
cd Leai-Vue
npm install
2. 启动开发服务器bash
npm run dev
3. 访问应用http://localhost:3000
4. 
## 主要功能

### 1. 智能对话
- 支持多种专业领域的对话
- Markdown格式渲染
- 代码高亮显示
- 实时响应

### 2. 用户管理
- 用户注册和登录
- JWT token认证
- 安全的密码加密存储

### 3. 历史记录
- 自动保存对话历史
- 支持查看完整对话
- 历史记录管理
- 本地/数据库双模式存储

### 4. 移动端适配
- 响应式布局设计
- 触摸友好的交互
- 优化的移动端显示

## 开发说明

### API接口
- `/api/auth/login`: 用户登录
- `/api/auth/register`: 用户注册
- `/api/chat`: 发送对话消息
- `/api/chat-history`: 历史记录管理

### 数据库表
- `users`: 用户信息表
- `chat_history`: 对话历史记录表

## 部署说明

### 生产环境配置
1. 修改数据库配置
2. 配置正式环境的API密钥
3. 配置跨域设置
4. 设置JWT密钥

### 打包部署
bash
前端打包
cd Leai-Vue
npm run build
后端打包
cd Leai-Server
./mvnw package

## 贡献指南
1. Fork 项目
2. 创建功能分支
3. 提交变更
4. 发起 Pull Request

## 许可证
[MIT License](LICENSE)

## 联系方式
- 作者：[nole]
- 邮箱：[noleit@icloud.com]
- 项目地址：[[GitHub Repository URL](https://github.com/imnole/LeAi)]
