
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
