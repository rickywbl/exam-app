# 公考备考系统 - App 前端

## 项目说明

这是公考备考系统的移动 App 前端代码仓库（支持 iOS 和 Android）。

## 技术选型

推荐以下两种方案：

### 方案一：uni-app（推荐）
- 一套代码编译到 iOS/Android/H5/小程序
- 基于 Vue.js，学习成本低
- 丰富的插件生态

### 方案二：React Native
- 原生性能体验
- React 技术栈
- 社区活跃

## 功能规划

- [ ] 用户登录/注册
- [ ] 题目练习（单选/多选/判断）
- [ ] 专项练习
- [ ] 错题本
- [ ] 练习记录/统计
- [ ] 收藏题目
- [ ] 个人中心
- [ ] VIP 会员

## 开发环境

### uni-app
```bash
# 安装依赖
npm install

# 开发模式
npm run dev:app-plus

# 构建
npm run build:app-plus
```

### React Native
```bash
# 安装依赖
npm install

# iOS
cd ios && pod install && cd ..
npm run ios

# Android
npm run android
```

## API 配置

开发环境：`http://localhost:8080/api/v1`
生产环境：`http://122.51.210.141:8080/api/v1`

## 目录结构（uni-app）

```
├── pages/              # 页面
│   ├── index/         # 首页
│   ├── practice/      # 练习
│   ├── wrong/         # 错题本
│   ├── statistics/    # 统计
│   └── user/          # 个人中心
├── components/         # 组件
├── static/            # 静态资源
├── utils/             # 工具函数
├── store/             # 状态管理
├── styles/            # 全局样式
├── App.vue            # 应用配置
├── main.js            # 入口文件
└── manifest.json      # 应用配置
└── pages.json         # 页面配置
```

## 待开发

当前项目尚未开始开发，等待后续实现。

## 相关仓库

- 后端 API：https://github.com/rickywbl/exam-backend.git
- 管理后台：https://github.com/rickywbl/exam-manager.git
- 小程序：https://github.com/rickywbl/exam-front.git
