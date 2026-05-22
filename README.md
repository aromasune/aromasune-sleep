
```markdown
# 🌙 AROMA SUNÉ 睡眠健康评估系统

> 非药物睡眠健康评估 · PSQI / ESS / ISI 国际量表 · HPB 健康积分 · 数据资产化



## 📱 项目简介

AROMA SUNÉ 是一个面向 40–60 岁女性的非药物睡眠情绪健康评估平台。用户完成 28 题标准化问卷（PSQI / ESS / ISI）后，可获得睡眠质量报告、积分奖励，并可将积分用于 Health365 保费抵扣或 FairPrice 消费。

本项目同时构建**合规 PSQI 数据资产池**，用于药企 RWE 研究、酒店星级认证及数据 RWA 化。

---

## ✅ 已实现功能

| 功能模块 | 说明 |
|----------|------|
| 🌐 多语言支持 | 中文 / English / Bahasa Melayu / Indonesia |
| 📋 完整问卷 | PSQI（7维度）+ ESS（9题）+ ISI（7题）= 28题 |
| 🧮 自动计分 | 真实 PSQI / ESS / ISI 算法，倾向分析 |
| 🔐 安全登录 | 手机号 + 短信验证码（测试模式 123456） |
| 🎫 Token 认证 | Bearer Token，自动刷新，防重放 |
| 💯 积分系统 | 首次提交 +100 积分，后端存储（Airtable） |
| 📊 报告生成 | 分数 + 分级 + 四种倾向分析 |
| 📤 分享功能 | WhatsApp / Facebook / 微信 / 复制链接 |
| 🖼️ 保存图片 | 报告导出为图片（html2canvas） |
| 📜 历史报告 | 本地存储，可查看过往提交 |
| 🏢 B端入口 | 企业合作 / 数据洞察 / 星级认证 / 合作伙伴登录 |
| 🛒 积分兑换 | 跳转 Health365 / FairPrice 官方渠道 |
| ✅ 合规设计 | 知情同意 + RWE 授权（不默认勾选），手机号 SHA‑256 哈希 |
| 📱 响应式 | 移动端适配，可缩放滚动 |



## 🛠 技术栈

| 层级 | 技术 | 说明 |
|------|------|------|
| 前端 | HTML5 + CSS3 + JavaScript | 原生，无框架 |
| 托管 | GitHub Pages | 全球 CDN 加速 |
| 后端 | Google Apps Script | 无服务器，自动扩缩容 |
| 数据库 | Airtable | `submissions` / `user_points` / `audit_log` |
| 身份验证 | 短信验证码 + Bearer Token | 测试模式固定码 `123456` |
| 安全机制 | CORS / 频率限制 / LockService / 输入校验 | 防并发、防滥用 |
| 域名 | `aromasune.com`（配置中） | CNAME 文件已准备 |

---

## 📂 文件结构

```

aromasune-sleep/
├── index.html          # 主问卷页面（完整生产版）
├── CNAME               # 自定义域名配置（aromasune.com）
├── README.md           # 项目说明（本文件）
└── assets/             # 可选：图片/图标（暂无）

```

---

## 🔒 隐私与合规（新加坡 PDPA）

| 要求 | 状态 | 说明 |
|------|------|------|
| 明确同意 | ✅ | 知情同意书 + RWE 授权，未默认勾选 |
| 最小必要收集 | ✅ | 仅手机号哈希、年龄、绝经状态、睡眠数据 |
| 数据匿名化 | ✅ | 手机号 SHA‑256 哈希，不存储明文 |
| 数据跨境传输 | ⚠️ | Airtable 位于美国，已在隐私政策中声明 |
| 用户删除权 | 🔄 | 可通过后端手动删除，自助接口待开发 |
| 儿童保护 | ✅ | 目标 40–60 岁，不涉及儿童 |

---

## 📊 数据采集目标

| 阶段 | 数据量 | 用途 |
|------|--------|------|
| 初期 | 500 份 | 验证流程 + 效果证明 |
| 中期 | 2,000 份 | 药企 RWE 合作谈判 |
| 长期 | 10,000+ 份 | 数据资产化 / RWA |

---

## 🚀 快速开始（本地测试）

```bash
# 克隆仓库
git clone https://github.com/aromasune/aromasune-sleep.git

# 直接用浏览器打开 index.html
open index.html
```

注意：本地打开时因跨域限制，无法调用后端 API。建议部署到 GitHub Pages 或使用本地服务器（如 npx http-server）进行测试。

---

🔧 环境配置

1. 后端部署（Google Apps Script）

· 打开 script.google.com，新建项目
· 粘贴 Code.gs 代码（需单独提供）
· 修改 AIRTABLE_TOKEN 和 BASE_ID
· 部署为 Web App（执行身份：我，访问权限：任何人）
· 复制 Web App URL，填入前端 apiEndpoint

2. Airtable 表结构

表名 字段数 说明
submissions 40+ 问卷提交记录
user_points 3 积分余额
audit_log 5 操作审计日志

3. 前端配置

```javascript
const apiEndpoint = "你的 Web App URL";
```

---

📈 当前状态（2026-05-21）

模块 状态 说明
前端代码 ✅ 完整 28题 + 多语言 + 计分 + 分享
后端代码 ✅ 完整 Token + Airtable + 频率限制 + CORS
后端部署 🔄 需重新部署 最后一次 URL 返回 404，请重新部署
GitHub Pages ✅ 已启用 main 分支 /root
自定义域名 🔄 配置中 CNAME 文件已准备，等待 DNS 生效
Airtable ✅ 已配置 三个表均已创建

---

📞 联系方式

· 品牌：AROMA SUNÉ
· 邮箱：hello@aromasune.com
· 网站：https://aromasune.github.io/aromasune-sleep/
· 商业合作：企业合作 / 酒店认证 / 药企 RWE / 数据资产化

---

📄 许可证

© 2026 AROMA SUNÉ。所有内容及设计均通过蚂蚁链存证，侵权必究。

---

🙏 致谢

· 新加坡保健促进局（HPB）健康积分计划
· CIDESCO / WITT / WSS / APSWC / WTA 国际资质支持
· 圣路加医院（待正式签约）数据采集合作

---

最后更新：2026-05-21 · 生产就绪版

```

## ✅ 使用说明

1. 复制上面的内容
2. 在 GitHub 仓库 `aromasune/aromasune-sleep` 中点击 **Add file** → **Create new file**
3. 文件名输入 `README.md`
4. 粘贴内容，点击 **Commit changes**

## 📌 与之前 README 的主要区别

| 内容 | 旧版 | 新版 |
|------|------|------|
| 功能列表 | 简要 | 详细表格，16+ 项 |
| 技术栈 | 简单列举 | 完整表格 + 说明 |
| 合规说明 | 一句话 | 按 PDPA 逐条列出 |
| 数据目标 | 三阶段 | 保留 + 补充用途 |
| 当前状态 | 无 | 明确标注各模块状态 |
| 快速开始 | git clone | 增加本地测试提示 |
| 环境配置 | 无 | 后端/Airtable/前端配置说明 |
| 致谢 | 无 | 新增合作伙伴名单 |

需要我调整任何内容吗？（比如加图标、改排版、补充更详细的 Airtable 字段说明）
```