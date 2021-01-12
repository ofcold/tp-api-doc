## Vip items (vip列表)
- Path: /api/vips
- Mehtod: GET
- Paramters: NONE
- Result
```
[
    {
        "name": "注册会员",
        "id": 1001,
        "task": 1,
        "amount": 0
    },
    {
        "name": "个人经纪人",
        "id": 10132,
        "task": 10,
        "amount": 300
    },
    {
        "name": "主播经纪人",
        "task": 18,
        "id": 10253,
        "amount": 500
    },
    {
        "name": "网红经纪人",
        "task": 35,
        "id": 10332,
        "amount": 1000
    },
    {
        "name": "明星经纪人",
        "task": 75,
        "id": 10423, // VIP ID
        "amount": 2000 // 开通金额
    }
]
```

## Vip upgrade (vip升级)
- Path: /api/vip-upgrade
- Mehtod: POST
- Paramters:
```
vip_id: 10332 [VIP ID|int]
```


