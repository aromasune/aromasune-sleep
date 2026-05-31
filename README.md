# AROMA SUNÉ · 非药物睡眠健康服务体系

**官网**: [www.aromasune.com](https://www.aromasune.com) | **类型**: 非药物 · 健康促进 · 数据驱动

## 📌 项目定位

专注 **40-60岁女性** 的情绪睡眠健康，提供基于 PSQI 评估的连续行为记录与轻量干预方案。

> 本项目为 **P0 阶段**（观察与验证期），目标是积累行为数据 + 跑通完整链路，不做自动化运营与积分兑换。

---

## 🌍 线上入口

| 页面 | 用途 | 链接 |
|------|------|------|
| 品牌首页 (B端) | 酒店/企业合作 | [aromasune.com](https://www.aromasune.com) |
| PSQI 问卷 + 报告 | 核心数据采集 | [servey.html](https://www.aromasune.com/servey.html) |
| 睡眠健康指南 | 4语言非药物建议 | [sleep_guide.html](https://www.aromasune.com/sleep_guide.html) |
| 隐私政策 | PDPA 合规披露 | [privacy.html](https://www.aromasune.com/privacy.html) |
| 电子名片 | 联系人 + 合作入口 | [card.html](https://www.aromasune.com/card.html) |
| 社区活动入口 | 教会/社区专用 | [community.html](https://www.aromasune.com/community.html) |

---

## 📁 文件结构

```
aromasune-sleep/
├── index.html              # 品牌主页 (四语切换，B端)
├── servey.html             # PSQI 问卷 + 自动报告 (四语)
├── sleep_guide.html        # 睡眠健康指南 (四语)
├── privacy.html            # 隐私政策 (四语)
├── card.html               # 电子名片 (四语)
├── community.html          # 社区/教会活动入口 (英文)
├── assets/                 # (可选) 图片/样式
└── README.md               # 本文件
```

---

## 🛠 技术栈

- **前端**: 原生 HTML/CSS/JS，无框架依赖
- **多语言**: 前端 i18n 变量切换（中/英/马来/印尼）
- **数据存储**: Airtable (后端代理隐藏)
- **部署**: GitHub Pages + 自定义域名 `www.aromasune.com`
- **域名 DNS**: A 记录指向 GitHub Pages IP

---

## 📊 数据资产

| 资产 | 状态 | 说明 |
|------|------|------|
| PSQI 记录 | ✅ 正在积累 | Airtable 入库，可导出 |
| 区块链存证 | ✅ 已完成 | 北京市方圆公证处 + 蚂蚁链 (19项文档 + 1份效果数据) |
| 酒店试点案例 | ✅ 已脱敏 | PSQI 平均下降 4.2 分，入睡缩短 31 分钟，满意度 96% |
| 商标申请 | ⏳ 受理中 | `AROMA SUNÉ` 文字 + Logo (pending) |
| IPOS 版权登记 | ⏳ 待申请 | 核心代码 `servey.html` 建议申请 |

---

## 🚀 部署维护

### 本地测试
```bash
# 任意静态服务器，例如
npx serve .
# 或直接打开浏览器预览 HTML
```

### 更新线上版本
1. 修改本地文件
2. `git add . && git commit -m "描述"`
3. `git push origin main`
4. GitHub Pages 自动生效 (几分钟内)

### 环境变量 / 后端代理 (可选)
- 如需隐藏 Airtable 写入 URL，可在 Vercel/Cloudflare 配置代理接口
- 前端 `servey.html` 中 `BACKEND_PROXY` 变量指向代理地址

---

## 🔐 合规与安全

- ✅ 新加坡 PDPA 合规 (DPO 邮箱、数据保留期、删除请求)
- ✅ 非医疗声明 (所有页面显著标注)
- ✅ 数据出境披露 (Airtable 美国服务器)
- ✅ 商标使用规范 (pending 阶段统一用 `™`)

---

## 📈 P0 阶段成功标准

- [x] 链路闭环: 表单 → 问卷 → 入库 → 报告
- [x] 真实数据提交 ≥1 条
- [ ] 观察期 ≥2 周
- [ ] 真实提交 ≥5 条
- [ ] 至少 1 人完成首次参与

---

## 📬 联系与商业合作

| 渠道 | 信息 |
|------|------|
| 官网 | [www.aromasune.com](https://www.aromasune.com) |
| 邮箱 | `hello@aromasune.com` (业务) / `privacy@aromasune.com` (数据权利) |
| WhatsApp | `+65 8169 3808` |
| WeChat | `jlan_aroma` |

合作模式：产品采购 · 营收分成 (20%-25%起) · 托管服务

---

## © 版权与知识产权

- **代码与设计**: 未经授权不得复制或商用
- **商标**: `AROMA SUNÉ`™ 及 Logo 已提交新加坡商标申请 (pending)
- **存证**: 核心设计文档、效果数据已做区块链存证 (蚂蚁链 + 方圆公证处)

---

**维护者**: Jin Lan  
**法律主体**: Royal Trade & Consultancy Pte. Ltd. (UEN: 201923477E)  
**最后更新**: 2026-05-31
```

这份 `README.md` 已经涵盖了项目的关键信息，包括定位、线上入口、文件结构、技术栈、数据资产、部署方法、合规状态、P0 目标和联系方式。如果您需要调整任何部分，请随时告诉我。
