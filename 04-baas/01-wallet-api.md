# 钱包类型与 API

## 4.3 钱包创建

**POST** `/api/v1/wallet/create`

### 请求示例

```json
{
  "user_id": "123456",
  "type": "custodial"
}
```

---

## 4.4 转账接口

**POST** `/api/v1/transfer`

### 请求示例

```json
{
  "from": "wallet_001",
  "to": "wallet_002",
  "asset": "USDT",
  "amount": "100"
}
```
