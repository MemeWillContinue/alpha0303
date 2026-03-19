# PinkWallet 技术文档

## 目录

- [一、系统概述](01-system-overview.md)
- [二、资金费率体系](02-funding-fee/README.md)
- [三、VA 虚拟账户体系](03-va/README.md)
- [四、BaaS 钱包即服务](04-baas/README.md)
- [五、风控与安全体系](05-risk-security.md)
- [六、系统特性](06-system-features.md)

## 主要内容

### 1) 系统概述
- 统一账户模型：多资产统一管理与清算。
- 支持资产：USDT、BTC、ETH 及链上代币。

### 2) 资金费率体系
- 费率构成：平台费、网络费、风控费。
- 提供费率计算、充值、提现相关接口与流程。

### 3) VA 虚拟账户体系
- 支持独立地址与归集地址 + Memo 两种模式。
- 覆盖创建、入账状态机、回调通知与费率。

### 4) BaaS 钱包即服务
- 覆盖钱包创建、转账接口与计费模型。
- 支持 Custodial、MPC、Smart Contract 钱包类型。

### 5) 风控与安全体系
- 黑名单检测、异常识别、高频监控。
- API 签名、时效校验、幂等控制。
