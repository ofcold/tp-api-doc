# Common Header
```
- X-Requested-With: XMLHttpRequest [string]
- Authorization: You login token (Example: Bearer 8|8AL1mwqbE5n3QNLMGSnjWlfWcBSXMee4uVieSPnt) [string]
```
- Host: http://tikplus.cn:9200/

## Register
- Path: /api/register
- Mehtod: PUT
- Paramters:
```
name:add [nullable|max:10]
phone_number:18898726543 [require|unique|china phone number]
password:Admin123 [require|min:8|max:20]
password_confirmation:Admin123
invite_code: (optional)
```

- Validate form fail
```
{
    "message": "The given data was invalid.",
    "errors": {
        "name": [
            "The name field is required."
        ],
        "phone_number": [
            "The phone number field is required."
        ],
        "password": [
            "The password field is required."
        ]
    }
}
```

## Activation (验证手机短信/激活账户)
- Path: /api/activation
- Method: POST
- Paramters
```
phone_number:18898726543 [require|china phone number]
validate_code:114751 [require|must length:6]
```

## Register resend SMS (注册短信重发)
- Path: /api/resend-sms
- Method: POST
- Paramters
```
phone_number:18898726543 [require|china phone number]
```

## Login/Log Up (登入)
- Path: /api/login
- Mehtod: POST
- Paramters:
```
phone_number:18898726543 [require|unique|china phone number]
password:Admin123 [require|min:8|max:20]
```

## Auth information (用户信息)
- Path: /api/user
- Mehtod: GET
- Paramters: NONE
- Result
```
{
    "name": "188****6543", // user name
    "first_name": null,
    "last_name": null,
    "phone_number": 18898726543,
    "balance": 0,
    "parent_id": null,
    "vip_expired_at": null,
    "enabled": true,
    "last_active_at": null,
    "created_at": "2020-12-25 03:04:56",
    "updated_at": "2020-12-25 03:06:20",
    "profile_photo_url": "https://ui-avatars.com/api/?name=188%2A%2A%2A%2A6543&color=7F9CF5&background=EBF4FF",
    "created_ago": "4天前",
    "full_name": " ",
    "vip": {
        "name": "注册会员",
        "id": 1001,
        "task": 1,
        "amount": 0
    },
    "team_count": 202,
    "invite_code": "00000h"
}
```

## Auth Childrens (我的团队)
- Path: /api/childrens
- Mehtod: GET
- Paramters: NONE
- Result
```
{
    "current_page": 1,
    "data": [
        {
            "name": "廉鹰",
            "created_at": "2020-12-27 05:38:18",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E5%BB%89%E9%B9%B0&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "全志强",
            "created_at": "2020-12-27 05:38:18",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E5%85%A8%E5%BF%97%E5%BC%BA&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "任建华",
            "created_at": "2020-12-27 05:38:18",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E4%BB%BB%E5%BB%BA%E5%8D%8E&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "蔺欢",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E8%94%BA%E6%AC%A2&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "金佳",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E9%87%91%E4%BD%B3&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "贺毅",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E8%B4%BA%E6%AF%85&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "习晨",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E4%B9%A0%E6%99%A8&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "计涛",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E8%AE%A1%E6%B6%9B&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "高静",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E9%AB%98%E9%9D%99&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "冯志强",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E5%86%AF%E5%BF%97%E5%BC%BA&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "栾君",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E6%A0%BE%E5%90%9B&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "赵宁",
            "created_at": "2020-12-27 05:38:19",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E8%B5%B5%E5%AE%81&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "毛帅",
            "created_at": "2020-12-27 05:38:20",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E6%AF%9B%E5%B8%85&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "贺智明",
            "created_at": "2020-12-27 05:38:20",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E8%B4%BA%E6%99%BA%E6%98%8E&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        },
        {
            "name": "谭红梅",
            "created_at": "2020-12-27 05:38:20",
            "profile_photo_url": "https://ui-avatars.com/api/?name=%E8%B0%AD%E7%BA%A2%E6%A2%85&color=7F9CF5&background=EBF4FF",
            "created_ago": "2周前",
            "full_name": " ",
            "vip": {
                "name": "注册会员",
                "id": 1001,
                "task": 1,
                "amount": 0
            },
            "team_count": 1,
            "invite_code": "000000"
        }
    ],
    "first_page_url": "https://tp.com/api/childrens?page=1",
    "from": 1,
    "last_page": 14,
    "last_page_url": "https://tp.com/api/childrens?page=14",
    "links": [
        {
            "url": null,
            "label": "&laquo; Previous",
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=1",
            "label": 1,
            "active": true
        },
        {
            "url": "https://tp.com/api/childrens?page=2",
            "label": 2,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=3",
            "label": 3,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=4",
            "label": 4,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=5",
            "label": 5,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=6",
            "label": 6,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=7",
            "label": 7,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=8",
            "label": 8,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=9",
            "label": 9,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=10",
            "label": 10,
            "active": false
        },
        {
            "url": null,
            "label": "...",
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=13",
            "label": 13,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=14",
            "label": 14,
            "active": false
        },
        {
            "url": "https://tp.com/api/childrens?page=2",
            "label": "Next &raquo;",
            "active": false
        }
    ],
    "next_page_url": "https://tp.com/api/childrens?page=2",
    "path": "https://tp.com/api/childrens",
    "per_page": 15,
    "prev_page_url": null,
    "to": 15,
    "total": 202
}
```

## Password reset (密码重设)
- Path: /api/password-sms
- Method: POST
- Paramters
```
phone_number:18898726543 [require|unique|china phone number]
