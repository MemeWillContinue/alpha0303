# 自定义域名配置指南

将 PinkWallet 技术文档绑定到你购买的域名（如 `docs.pinkwallet.com`）。

---

## 一、在域名服务商处添加解析

在你的域名 DNS 管理后台添加以下记录：

| 类型 | 主机记录 | 记录值 |
|------|----------|--------|
| **CNAME** | `docs`（或 `www`、`@`） | `memewillcontinue.github.io` |

- 若使用 `docs.pinkwallet.com`：主机记录填 `docs`
- 若使用 `www.pinkwallet.com`：主机记录填 `www`
- 若使用根域名 `pinkwallet.com`：主机记录填 `@`，且需使用 A 记录（见下文）

**根域名 A 记录（可选）：**

| 类型 | 主机记录 | 记录值 |
|------|----------|--------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

---

## 二、在 GitHub 配置自定义域名

1. 打开：https://github.com/MemeWillContinue/alpha0303/settings/pages  
2. 在 **Custom domain** 中填写你的域名，如：`docs.pinkwallet.com`  
3. 点击 **Save**  
4. 等待 DNS 生效后，勾选 **Enforce HTTPS**（启用 HTTPS）

---

## 三、在仓库中创建 CNAME 文件（可选）

若 GitHub 未自动生成，可在仓库根目录创建 `CNAME` 文件，内容为：

```
docs.pinkwallet.com
```

（将域名替换为你的实际域名）

---

## 四、生效时间

DNS 解析通常 10 分钟到 48 小时内生效。生效后访问你的域名即可看到文档。
