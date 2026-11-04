# DREAM BUY 梦想购

一个适配安卓、iPhone、iPad 和 Mac 浏览器的 PWA 虚拟购物模拟器。

## 当前功能
- 商品分类、搜索、商品详情、规格选择
- 购物车、数量调整、虚拟优惠券、模拟付款
- 订单状态：待发货 → 运输中 → 已签收 → 拆箱
- 虚拟钱包、今日/本周/本月模拟消费统计
- 每日消费克制挑战、快乐值、成就
- 心愿清单
- localStorage 本地保存；Service Worker 离线缓存
- 不连接真实支付、不产生真实订单

## 最简单的发布方式：GitHub Pages
1. 在 GitHub 创建一个公开仓库，例如 `dream-buy`。
2. 将本文件夹中的 `index.html`、`manifest.webmanifest`、`sw.js`、`icon.svg`、`icon-192.png`、`icon-512.png`、`apple-touch-icon.png` 上传到仓库根目录。
3. 打开仓库 Settings → Pages。
4. 在 Build and deployment 中选择 Deploy from a branch。
5. Branch 选择 `main`，目录选择 `/ (root)`，保存。
6. 等待部署完成，GitHub 会给出 `https://你的用户名.github.io/dream-buy/` 网址。

注意：PWA 和离线缓存需要 HTTPS。GitHub Pages 默认提供 HTTPS。

## 手机/电脑安装
### Android（Chrome）
打开部署网址 → 浏览器菜单 → 安装应用 / 添加到主屏幕。

### iPhone / iPad（Safari）
用 Safari 打开网址 → 分享 → 添加到主屏幕 → 添加。
iOS 通常需要通过 Safari 安装；部分安装提示和能力随系统版本变化。

### Mac（Chrome / Edge）
打开网址 → 地址栏安装图标或菜单 → 安装页面为应用。
Safari 可将网页添加到 Dock（取决于 macOS 版本）。

## 数据与备份
所有订单、钱包、心愿清单和成就保存在当前浏览器的 localStorage 中。
清理浏览器网站数据、换浏览器或换设备可能导致数据丢失；当前版本没有云同步。
建议在升级前不要清除浏览器数据。下一阶段可增加导出/导入 JSON 备份。

## 本地预览
不要直接双击 HTML 期待离线安装功能。建议在项目目录运行：
`python3 -m http.server 8000`
然后访问 `http://localhost:8000`。本地 http 的 Service Worker 仅在 localhost 等安全环境可用。

## 说明
这是一个前端单机 PWA 原型。没有账号系统、服务器数据库或应用商店上架配置。
