# edge-extends-types

## 0.0.9 (9 月 24 日 2024 年)

- 完善 `tabs` 相关的其他方法
- 完善 `runtime` 相关的方法与属性

## 0.0.9 (9 月 19 日 2024 年)

- 刚才提交的时候遗忘了将 `bin` 文加入导出列表，干了个尬

## 0.0.9 (9 月 19 日 2024 年)

使用 `@types/chrome` 模式发现必须将包放在 `@types` 下才能用，所有又花了一天折腾，最后又改回 `version: 0.0.7` 了，
不过现在是使用在根目录添加文件 `chrome.d.ts` 文件完成全局的注入（可能还需要在 `tsconfig.json` 文件完成 `include`）

_chrome.d.ts 文件内容_

```ts
import { Chrome } from 'a-edge-extends-types';

declare global {
  interface Window {
    chrome: Chrome;
  }

  const chrome: Chrome;
}
```

## 0.0.8 (9 月 17 日 2024 年)

- 查了下，居然有 `@types/chrome` 这么好的东西，那还更新个屁
- 使用 `@types/chrome` 的模式重新了该包，这样就不用
- 修复已知 bug

## 0.0.7 (9 月 16 日 2024 年)

- 遗漏了 `contextMenu` 的类型导出

## 0.0.6 (9 月 16 日 2024 年)

- 进一步完善了注释内容
- 添加了 `contextMenus`

## 0.0.5 (9 月 16 日 2024 年)

- 完善了部分注释内容
- 添加了 `tts` 及 `i18n`

## 0.0.4 (9 月 15 日 2024 年)

- `runtime` 添加 `onload` 方法，用于测试时重新加载扩展
- 修复 `runtime` 的 `onMessage.addListener` 类型错误
- 添加了 `keepChrome` rollup 插件，这也是我的第一款 rollup 插件，值的庆贺，一个煮面加根火腿肠

## 0.0.3 (9 月 13 日 2024 年)

- 修复已知 bug

## 0.0.2 (9 月 13 日 2024 年)

- 完善了自述文档

## 0.0.0 (9 月 12 日 2024 年)

- 初始化项目
