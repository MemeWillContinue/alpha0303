# GitBook 部署说明

本仓库已配置为 GitBook 可直接同步：

- 首页：`README.md`
- 目录：`SUMMARY.md`
- 配置：`.gitbook.yaml`
- 同步分支：`main`

---

## 1) 在 GitBook 连接仓库

1. 进入 GitBook，打开目标 Space
2. `Integrations` -> `GitHub` -> `Connect repository`
3. 选择仓库：`MemeWillContinue/alpha0303`
4. 选择分支：`main`
5. Root 目录保持 `/`（仓库根目录）
6. 保存并触发首次同步

---

## 2) 发布站点

1. 进入 Space 的 `Share` 或 `Publish`
2. 打开 Public site（或按你的权限策略设置访问）
3. 完成后获得 GitBook 访问链接

---

## 3) 后续更新

- 只要继续推送到 `main`，GitBook 会自动同步更新
- 如果未自动更新，在 GitBook 的 Sync 页面手动点击 `Sync now`
