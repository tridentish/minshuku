# minshuku
# 🏡 闽韵雅舍民宿web网站 

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Vue](https://img.shields.io/badge/Vue-3.3.4-brightgreen)](https://vuejs.org/)
[![SpringBoot](https://img.shields.io/badge/SpringBoot-3.1.5-green)](https://spring.io/projects/spring-boot)

> 一个集成住宿、餐饮、旅游服务的沉浸式Web平台，提供流畅的动态交互体验

---

## ✨ 功能特性

### **核心功能**
- 🏠 3D房源展示：WebGL实现的360°全景看房
- 🛎️ 多业务集成：住宿/餐饮/旅游服务一键式预订
- 🧩 动态交互：悬浮菜单、视差滚动等现代Web交互
- 📊 智能推荐：基于用户行为的个性化服务推荐

### **特色亮点**
```diff
+ 浮动式支付窗口：支付过程不中断浏览
+ 拖拽式服务组合：自由搭配旅游套餐
+ 离线PWA支持：弱网环境下仍可访问基础功能
```

---

## 🛠️ 技术栈

| 模块       | 技术选型                                                                 |
|------------|--------------------------------------------------------------------------|
| **前端**   | Vue3 + TypeScript + Pinia + Three.js + Element Plus                      |
| **后端**   | Spring Boot 3.x + Spring Cloud + MySQL 8 + Redis 7                       |
| **运维**   | Docker + Kubernetes + Prometheus + Grafana                               |
| **工具链** | Vite + Swagger + Jenkins                                                 |

---

## 🚀 快速开始

### 环境要求
- Node.js 18+
- JDK 17+
- MySQL 8.0
- Redis 7.0

### 本地开发
```bash
# 克隆仓库
git clone https://github.com/your-repo/floating-bnb.git
cd floating-bnb

# 前端启动
cd frontend
npm install
npm run dev

# 后端启动
cd ../backend
mvn spring-boot:run

# 初始化数据库（需提前创建bnb数据库）
mysql -u root -p bnb < db/schema.sql
```

---

## 🌍 部署指南

### Docker Compose部署
```yaml
# docker-compose.prod.yml
services:
  backend:
    image: your-registry/bnb-backend:latest
    environment:
      SPRING_DATASOURCE_URL: jdbc:mysql://mysql:3306/bnb
    depends_on:
      - mysql
      - redis
```

### Kubernetes配置示例
```yaml
# deployment.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: bnb-frontend
spec:
  replicas: 3
  template:
    spec:
      containers:
        - name: frontend
          image: your-registry/bnb-frontend:latest
          ports:
            - containerPort: 80
```

---

## 🤝 贡献指南

### 开发流程
1. Fork本仓库
2. 创建特性分支 (`git checkout -b feature/your-feature`)
3. 提交代码 (`git commit -m 'Add some feature'`)
4. 推送分支 (`git push origin feature/your-feature`)
5. 发起Pull Request

### 代码规范
- 前端：遵循[Vue风格指南](https://vuejs.org/style-guide)
- 后端：遵守[Google Java代码规范](https://google.github.io/styleguide/javaguide.html)
- 提交信息：采用[Conventional Commits](https://www.conventionalcommits.org)

---

## 📄 许可证

[MIT License](LICENSE) © 2023 Your Name

---

## 📮 联系我们

- 📧 Email: dev@bnb.com  
- 💬 WeChat: BNB_TechTeam  
- 🌐 Website: https://bnb-tech.com  
```

---

<div align="center">
  <sub>Built with ❤️ by 民宿技术团队 | 让旅行更温暖</sub>
</div>
```

### 文档亮点说明：
1. **徽章系统**：使用Shields.io徽章直观展示技术栈和许可证
2. **功能特性可视化**：采用图标+颜色标记突出核心功能
3. **代码块分层**：通过bash/yaml等语法高亮提升可读性
4. **移动端适配**：Markdown表格和模块化布局确保移动端友好
5. **贡献引导**：明确的开发流程+代码规范链接降低协作门槛
6. **情感化设计**：结尾的团队标语增强项目温度感
