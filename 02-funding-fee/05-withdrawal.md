# 2.5 提现流程与费率

## 提现接口

- **方法**：`POST`
- **路径**：`/api/v1/withdraw/create`

---

## 核心请求字段

```json
{
  "account_id": "ACC_10001",
  "asset": "USDT",
  "amount": "1000",
  "address": "TXXXX",
  "network": "TRC20"
}
```

---

## 状态机

```
CREATED → REVIEWING → APPROVED → BROADCASTING → CONFIRMED → SUCCESS
```

---

## 费率说明

| 项目 | 说明 |
|------|------|
| 平台费 | 0.2% ~ 0.5% |
| 最低费用 | 1 ~ 3 USDT |
| 网络费 | 动态计算 |
