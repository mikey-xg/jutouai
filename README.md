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

## 占位替换（已全部填写，如需变更按此清单改）

以下值已写入 `privacy.html` / `terms.html` / App 内嵌 `legal-*.html`：

- **开发者 / 运营方名称**：剧透AI团队
- **联系邮箱**：beyondbyterminal@gmail.com
- **所在地**：中国 / 山东
- **生效日期 / 最近更新日期**：2026 年 9 月 3 日
- **云服务提供商**：AWS
- **大模型服务商**：DeepSeek（杭州深度求索人工智能基础技术研究有限公司），服务器位于中华人民共和国；隐私政策 中文 https://cdn.deepseek.com/policies/zh-CN/deepseek-privacy-policy.html ，英文 https://cdn.deepseek.com/policies/en-US/deepseek-privacy-policy.html
- **服务日志滚动清除周期**：30 天；**请求响应时限**：15 个工作日
- **适用法律与管辖**（terms.html 第 12 节）：适用中华人民共和国法律，由开发者所在地（山东省）有管辖权的人民法院管辖，并保留用户所在地强制性消费者保护规定的优先适用条款


## 建议

- 美区上架建议**额外提供英文版** `privacy.en.html` / `terms.en.html`，并在 App Store Connect
  对应语言下填英文 URL。本目录先提供简体中文版。
- 内容与 App 实际行为保持一致：本文档已按当前实现撰写（自建后端、无第三方广告 / 分析 SDK、
  仅 AI 选剧涉及第三方与跨境、注销账号一键删除、本地通知不走服务器）。若功能变化需同步更新。
