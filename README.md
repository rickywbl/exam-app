# 公考备考系统 - App 前端（Flutter）

## 项目说明

这是公考备考系统的移动 App 前端代码仓库（支持 iOS 和 Android），基于 Flutter 开发。

## 技术栈

- **框架：** Flutter 3.x
- **语言：** Dart
- **状态管理：** Provider / Riverpod
- **网络请求：** Dio
- **本地存储：** SharedPreferences / Hive
- **路由管理：** GoRouter

## 环境要求

- Flutter SDK >= 3.0
- Dart >= 3.0
- Android Studio / VS Code
- Xcode（iOS 开发）
- Android SDK（Android 开发）

## 快速开始

### 1. 克隆项目

```bash
git clone git@github.com:rickywbl/exam-app.git
cd exam-app
```

### 2. 安装依赖

```bash
flutter pub get
```

### 3. 运行项目

```bash
# iOS
flutter run -d ios

# Android
flutter run -d android
```

### 4. 构建发布

```bash
# iOS
flutter build ios

# Android APK
flutter build apk --release

# Android App Bundle
flutter build appbundle --release
```

## 目录结构

```
lib/
├── main.dart              # 应用入口
├── app.dart               # 应用配置
├── config/                # 配置文件
│   ├── routes.dart       # 路由配置
│   └── constants.dart    # 常量配置
├── models/                # 数据模型
│   ├── user.dart         # 用户模型
│   ├── question.dart     # 题目模型
│   └── practice.dart     # 练习模型
├── services/              # 服务层
│   ├── api.dart          # API 服务
│   ├── auth.dart         # 认证服务
│   └── storage.dart      # 存储服务
├── providers/             # 状态管理
│   ├── user_provider.dart
│   └── practice_provider.dart
├── screens/               # 页面
│   ├── splash/           # 启动页
│   ├── login/            # 登录页
│   ├── home/             # 首页
│   ├── practice/         # 练习
│   │   ├── list.dart     # 题目列表
│   │   └── detail.dart   # 题目详情
│   ├── wrong/            # 错题本
│   ├── statistics/       # 统计
│   └── user/             # 个人中心
├── widgets/               # 组件
│   ├── question_card.dart    # 题目卡片
│   ├── answer_card.dart      # 答案卡片
│   ├── loading.dart          # 加载组件
│   └── empty_state.dart      # 空状态
├── utils/                 # 工具函数
│   ├── validators.dart   # 表单验证
│   ├── formatters.dart   # 格式化
│   └── helpers.dart      # 辅助函数
└── theme/                 # 主题
    ├── colors.dart       # 颜色
    ├── text_styles.dart  # 文本样式
    └── theme.dart        # 主题配置
```

## API 配置

修改 `lib/config/constants.dart`：

```dart
class ApiConfig {
  // 开发环境
  static const String baseURL = 'http://localhost:8080/api/v1';
  
  // 生产环境
  // static const String baseURL = 'http://122.51.210.141:8080/api/v1';
  
  static const Duration timeout = Duration(seconds: 30);
}
```

## 功能规划

- [ ] 用户登录/注册（手机号 + 密码）
- [ ] 题目练习（单选/多选/判断）
- [ ] 专项练习（按模块/知识点）
- [ ] 错题本（自动记录错题）
- [ ] 练习记录/统计
- [ ] 收藏题目
- [ ] 个人中心
- [ ] VIP 会员
- [ ] 离线下载

## 开发规范

1. 遵循 Dart 代码规范
2. 使用 Flutter 最佳实践
3. 组件化和模块化开发
4. 使用 `flutter_lints` 进行代码检查
5. 编写单元测试和 Widget 测试

## 常用命令

```bash
# 检查 Flutter 环境
flutter doctor

# 清理构建缓存
flutter clean

# 获取依赖
flutter pub get

# 代码格式化
dart format .

# 代码分析
flutter analyze

# 运行测试
flutter test

# 构建 iOS
flutter build ios

# 构建 Android APK
flutter build apk --release

# 构建 Android App Bundle
flutter build appbundle --release
```

## 依赖包

主要依赖（`pubspec.yaml`）：

```yaml
dependencies:
  flutter:
    sdk: flutter
  
  # 状态管理
  provider: ^6.0.0
  # 或 riverpod: ^2.0.0
  
  # 网络请求
  dio: ^5.0.0
  
  # 本地存储
  shared_preferences: ^2.0.0
  hive: ^2.0.0
  
  # 路由
  go_router: ^9.0.0
  
  # UI 组件
  cached_network_image: ^3.0.0
  flutter_svg: ^2.0.0
  
  # 工具
  intl: ^0.18.0
  json_annotation: ^4.8.0

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^2.0.0
  build_runner: ^2.0.0
  json_serializable: ^6.0.0
```

## 相关仓库

- 后端 API：https://github.com/rickywbl/exam-backend.git
- 管理后台：https://github.com/rickywbl/exam-manager.git
- 小程序：https://github.com/rickywbl/exam-front.git

## 待开发

当前项目尚未开始开发，等待后续实现。

## 许可证

MIT License
