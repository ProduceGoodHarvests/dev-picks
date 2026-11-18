# 精选项目索引

收录我常用技术栈里值得读源码的开源项目。**只放链接与阅读要点，不复制源码** —— 版权归各作者，使用时按其许可证执行。

数据时间：2026-11-18（星数、许可证、最后推送均由 GitHub API 读取）

## 怎么用这份清单

- 想快速找轮子：看「许可」列，优先 MIT / Apache-2.0，商用无忧
- 想读实现：看「看什么」列，那是一句话的入口，不是泛泛介绍
- 想抄结构：先读 `LICENSE` 与 `NOTICE`，再决定是引用依赖还是借鉴思路

> 「自定义」表示 GitHub 识别为 `NOASSERTION`（非标准 SPDX 标识），使用前需要读一遍许可证原文。

---

## Vue 生态

| 项目 | 星 | 语言 | 许可 | 看什么 |
|---|---:|---|---|---|
| [vuejs/core](https://github.com/vuejs/core) | 55.0k | TypeScript | MIT | 响应式与渲染器分层，`packages/reactivity` 可独立读懂 |
| [nuxt/nuxt](https://github.com/nuxt/nuxt) | 61.1k | TypeScript | MIT | 约定式路由与 SSR 的工程组织方式 |
| [vueuse/vueuse](https://github.com/vueuse/vueuse) | 22.4k | TypeScript | MIT | 组合式函数的实现范式，单文件即可读完 |
| [element-plus/element-plus](https://github.com/element-plus/element-plus) | 27.9k | TypeScript | MIT | 组件库工程化、主题变量、按需加载 |
| [vuetifyjs/vuetify](https://github.com/vuetifyjs/vuetify) | 41.0k | TypeScript | 自定义 | Material 设计体系的组件与主题实现 |
| [unovue/shadcn-vue](https://github.com/unovue/shadcn-vue) | 10.8k | TypeScript | MIT | 「源码放进项目里」的组件思路，改起来无负担 |
| [antfu-collective/vitesse](https://github.com/antfu-collective/vitesse) | 9.4k | TypeScript | MIT | 现代 Vue 工程模板：目录约定、自动导入、按需加载 |

## 微信小程序

| 项目 | 星 | 语言 | 许可 | 看什么 |
|---|---:|---|---|---|
| [youzan/vant-weapp](https://github.com/youzan/vant-weapp) | 18.5k | JavaScript | MIT | 组件样式隔离与交互细节，点单类页面可直接借鉴 |
| [Tencent/weui-wxss](https://github.com/Tencent/weui-wxss) | 15.3k | Less | 自定义 | 微信官方视觉规范在小程序里的落地方式 |
| [wechat-miniprogram/miniprogram-demo](https://github.com/wechat-miniprogram/miniprogram-demo) | 7.3k | JavaScript | MIT | 官方组件、API、云开发示例，查用法最快 |
| [Tencent/tdesign-miniprogram](https://github.com/Tencent/tdesign-miniprogram) | 1.8k | Vue | MIT | 小程序与 UniApp 双端共用组件的组织方式 |

## 桌面端

| 项目 | 星 | 语言 | 许可 | 看什么 |
|---|---:|---|---|---|
| [tauri-apps/tauri](https://github.com/tauri-apps/tauri) | 113.0k | Rust | Apache-2.0 | 用系统 WebView 打包桌面应用，产物只有几 MB |
| [electron/electron](https://github.com/electron/electron) | 124.0k | C++ | MIT | 成熟但体积大，适合需要完整 Node 能力的场景 |
| [TomSchimansky/CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) | 13.6k | Python | MIT | 给 Tkinter 套现代外观，最贴近现有桌面倒计时的技术栈 |
| [r0x0r/pywebview](https://github.com/r0x0r/pywebview) | 6.2k | Python | BSD-3-Clause | Python + HTML 做界面，比 Electron 轻一个量级 |

## 工程化

| 项目 | 星 | 语言 | 许可 | 看什么 |
|---|---:|---|---|---|
| [vitejs/vite](https://github.com/vitejs/vite) | 84.0k | TypeScript | MIT | 开发态 ESM 与生产态打包的双轨设计、插件机制 |
| [pnpm/pnpm](https://github.com/pnpm/pnpm) | 37.1k | Rust | MIT | 内容寻址存储与 workspace 依赖管理 |
| [unocss/unocss](https://github.com/unocss/unocss) | 19.0k | TypeScript | 自定义 | 原子化 CSS 的引擎实现，预设与规则可扩展 |

## 学习与清单

| 项目 | 星 | 语言 | 许可 | 看什么 |
|---|---:|---|---|---|
| [sindresorhus/awesome](https://github.com/sindresorhus/awesome) | 538.7k | — | CC0-1.0 | 各类清单的总入口，先搜再自己翻 |
| [nilbuild/developer-roadmap](https://github.com/nilbuild/developer-roadmap) | 372.3k | TypeScript | 自定义 | 学习路径图，用来定位自己的知识缺口 |

---

## 和 desktop-countdown 的关系

现有实现是 Python + Tkinter 自绘卡片（渐变、圆角、发光进度条）。往下走有三条路：

1. **留在 Tkinter**：读 CustomTkinter 的控件绘制方式，借鉴它对 DPI 与主题的处理，把自绘卡片做得更稳，体积不变
2. **换成 Web 界面**：pywebview 起步最快（产物 10 MB 级），Tauri 更极致（几 MB，但要引入 Rust 工具链）
3. **只换设置面板**：现有设置是手写 Tk 表单，可内嵌一个 WebView 页面用 Vue 写，交互上线更省事

## 说明

- 不收录 fork、镜像与已归档仓库；星数低于 1k 的小工具默认不进表
- 收录前逐个核对：是否仍在维护、是否有明确许可证、仓库是否为正主（曾遇到同名空壳仓库冒充分发仓库）
- 清单会随技术栈变化更新，新增条目遵循同样的核对流程
