# Hrt位置 - 小米手表地理位置应用

<div align="center">
  <img src="./src/common/logo.png" alt="项目Logo" width="120" height="120">
  <h3>基于小米快应用Vela平台开发的地理位置显示应用</h3>
</div>

## 项目简介

Hrt位置是一个专为小米手表设计的快应用，主要功能是实时显示当前地理位置坐标和对应的网格坐标（Maidenhead Locator System）。该应用利用手表的GPS功能获取实时位置信息，并将经纬度坐标转换为业余无线电爱好者常用的网格坐标格式。

## 功能特性

- 📍 实时显示经纬度坐标
- 🔍 自动转换为网格坐标（Maidenhead Locator）
- ⏰ 显示当前时间
- ⌚ 针对小米手表屏幕优化的界面
- 🌐 支持中英文国际化
- <div align="center">
  <img src="1762954409103.png" alt="应用截图" width="300" />
</div>

## 快速上手

### 1. 开发

```bash
npm install
npm run start -- --watch
```

执行以上命令安装依赖并启动开发服务器（带有监视模式）。

### 2. 构建

```bash
npm run build
```

执行构建命令生成生产环境代码。

### 3. 发布

```bash
npm run release
```

将应用发布到快应用平台。

### 4. 代码规范化配置

代码规范化可以帮助开发者在git commit前进行代码校验、格式化、commit信息校验。

**使用前提**：必须先关联git仓库

macOS 或 Linux 系统：
```bash
sh husky.sh
```

Windows 系统：
```bash
./husky.sh
```

## 使用说明

1. 应用启动后会自动请求位置权限
2. 获取位置成功后，将显示：
   - 当前时间（顶部）
   - 网格坐标（大号字体居中显示）
   - 经纬度坐标（小号字体显示）
3. 应用会定期自动更新位置信息

## 技术实现

- 基于小米快应用Vela平台开发
- 使用系统定位API获取地理位置
- 实现网格坐标转换算法
- 定时更新机制，优化电量消耗

## 项目结构

```
src/
├── app.ux             # 应用入口文件
├── common/            # 公共资源
│   └── logo.png       # 项目Logo
├── i18n/              # 国际化资源
│   ├── defaults.json  # 默认语言配置
│   ├── en.json        # 英文配置
│   └── zh-CN.json     # 中文配置
├── manifest.json      # 应用配置文件
└── pages/             # 页面目录
    ├── detail/        # 详情页（示例）
    │   └── detail.ux
    └── index/         # 首页（主功能页面）
        └── index.ux
```

## 开发规范

- 遵循 ESLint 和 Prettier 规范进行代码风格控制
- 使用 commitlint 进行提交信息校验
- 使用 husky 进行 git hooks 管理
- 代码提交前会自动进行格式化和语法检查



## 了解更多

你可以通过小米的[官方文档](https://iot.mi.com/vela/quickapp)熟悉和了解快应用。
