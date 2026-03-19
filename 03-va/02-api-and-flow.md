# VA 创建与入账

## 3.3 VA 创建接口

**POST** `/api/v1/va/create`

### 请求示例

```json
{
  "user_id": "123456",
  "asset": "USDT"
}
```

### 返回示例

```json
{
  "va_id": "VA_10001",
  "address": "TXXXX",
  "network": "TRC20"
}
```

---

## 3.4 入账处理流程

```
DETECTED → PENDING_CONFIRM → CONFIRMED → CREDITED
```

| 状态 | 说明 |
|------|------|
| DETECTED | 检测到链上交易 |
| PENDING_CONFIRM | 等待确认 |
| CONFIRMED | 达到确认数 |
| CREDITED | 记入账户 |

---

## 3.5 回调通知（Webhook）

```json
{
  "event": "deposit.confirmed",
  "va_id": "VA_10001",
  "amount": "500",
  "tx_hash": "0xabc"
}
```
