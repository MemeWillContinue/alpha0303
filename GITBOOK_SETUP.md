# GitBook 发布配置说明

本文档说明如何将 PinkWallet 技术文档发布至 GitBook，并隐藏发布时间与版本历史。

---

## 一、导入至 GitBook

1. 登录 [GitBook](https://app.gitbook.com/o/DzMFHUSafAeVlhtyL22n/home)
2. 进入目标 Space
3. 在 **Integrations** 中配置 Git Sync，连接本仓库
4. 或通过 **Import** 上传本目录中的文档

---

## 二、隐藏发布时间和版本历史

### 方式一：Space 设置（推荐）

1. 进入 Space 的 **Settings** / **设置**
2. 找到 **Customization** / **自定义** 或 **Site settings** / **站点设置**
3. 查找以下选项并关闭：
   - **Show last updated date** / **显示最后更新时间** → 关闭
   - **Show version history** / **显示版本历史** → 关闭（如有）
   - **Page actions** 中如有「显示更新时间」等相关选项，同样关闭

### 方式二：访问控制

若版本历史仅需对编辑者可见：

1. 在 Space 设置中配置 **Permissions**
2. 将版本历史的查看权限限定为编辑/管理员

### 方式三：自定义主题（高级）

若平台支持自定义 CSS，可添加：

```css
/* 隐藏页面底部更新时间 */
[data-testid="page-updated"],
.page-updated,
.last-updated {
  display: none !important;
}
```

---

## 三、目录结构说明

- `README.md`：文档首页
- `SUMMARY.md`：GitBook 目录索引
- `01-system-overview.md`：系统概述
- `02-funding-fee/`：资金费率体系
- `03-va/`：VA 虚拟账户体系
- `04-baas/`：BaaS 钱包即服务
- `05-risk-security.md`：风控与安全
- `06-system-features.md`：系统特性
- `07-disclaimer.md`：免责声明
- `08-summary.md`：总结

---

## 四、同步与更新

- 通过 Git Sync 时，`SUMMARY.md` 将自动生成侧边栏目录
- 修改文档后推送至仓库，GitBook 将按同步策略自动更新
