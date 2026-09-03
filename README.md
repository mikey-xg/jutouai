# 剧透 AI · 法务页（隐私政策 / 用户协议）

静态 HTML，用于部署到 GitHub Pages（`github.io`），并把链接填进 App Store Connect 的
**App 隐私政策 URL** 与 App 内「隐私政策 / 服务协议」入口。

## 文件

| 文件 | 说明 |
|---|---|
| `index.html` | 落地页，链到下面两份 |
| `privacy.html` | 隐私政策 |
| `terms.html` | 用户协议（服务条款） |
| `style.css` | 共用样式（浅色 / 自动适配深色，移动端友好） |

## 部署到 GitHub Pages

1. 新建仓库（如 `jutou-legal`），把本目录 4 个文件放到仓库根目录。
2. 仓库 Settings → Pages → Source 选 `main` 分支、`/ (root)`，保存。
3. 几分钟后可访问：
   - `https://<用户名>.github.io/jutou-legal/privacy.html`
   - `https://<用户名>.github.io/jutou-legal/terms.html`
4. 把上述两个 URL 分别填入：
   - App Store Connect → App 信息 → **隐私政策 URL**（填 `privacy.html` 的地址）
   - App 内「关于 / 我的」里的隐私政策、服务协议入口（当前 App 内嵌的是
     `jutouAI/Resources/legal-privacy.html` / `legal-terms.html` 本地副本，内容已与本目录一致；
     如需改成跳转线上版，改 `LegalWebViewController` 用 `WKWebView` 加载该 URL 即可）。

## ⚠️ 上线前必须替换的占位

文中所有黄色 `占位` 标记（`<span class="placeholder">`）都要替换成真实值，并把占位的样式类去掉：

- **开发者 / 运营方名称**：与 App Store Connect 上的销售者名称一致
- **联系邮箱**：隐私相关 `privacy@…`、支持相关 `support@…`（可为同一个）
- **所在地 / 国家地区**
- **生效日期 / 最近更新日期**：正式提交那天的日期
- **云服务提供商名称**：后端实际托管商（阿里云 / AWS / …）
- **大模型服务商**：目前为 DeepSeek（深度求索），服务器位于中华人民共和国；如更换需同步改
- **DeepSeek 隐私政策链接**：填其官网隐私政策页地址
- **数据保留天数**：服务日志滚动清除周期（默认写了 30 天）、请求响应时限（默认 15 个工作日）
- **适用法律与管辖机构**（`terms.html` 第 12 节）：建议咨询法律顾问确定

## 建议

- 美区上架建议**额外提供英文版** `privacy.en.html` / `terms.en.html`，并在 App Store Connect
  对应语言下填英文 URL。本目录先提供简体中文版。
- 内容与 App 实际行为保持一致：本文档已按当前实现撰写（自建后端、无第三方广告 / 分析 SDK、
  仅 AI 选剧涉及第三方与跨境、注销账号一键删除、本地通知不走服务器）。若功能变化需同步更新。
