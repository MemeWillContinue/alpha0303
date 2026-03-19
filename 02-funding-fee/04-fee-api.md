# 2.4 费率计算接口

## 接口信息

- **方法**：`GET`
- **路径**：`/api/v1/fee/calculate`

---

## 请求示例

```json
{
  "type": "withdrawal",
  "asset": "USDT",
  "network": "TRC20",
  "amount": "1000"
}
```

---

## 返回示例

```json
{
  "code": 0,
  "data": {
    "platform_fee": "3.000000",
    "network_fee": "1.200000",
    "risk_fee": "0.500000",
    "total_fee": "4.700000",
    "arrival_amount": "995.300000"
  }
}
```
