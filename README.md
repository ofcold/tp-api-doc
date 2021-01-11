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
```

# Task

## Tasks (任务列表)
- Path: /api/tasks
- Method: Get
- Paramters
```
q: [string|search text]
task_type: [jd|wechat_comment|tiktok|taobao|all]
order_by: [string|(field)[tiitle]]
```

- Result
```
{
    "current_page": 1,
    "data": [
        {
            "id": 2,
            "task_type": "wechat_comment",
            "title": "微信朋友圈",
            "claim": "要求用户下载的图片或给用户看的示例图",
            "url": "https://tp.com/tasks/create",
            "amount": "8.0000",
            "inventory": 2000,
            "compose": "<h1 jstcache=\"0\" style=\"color: var(--heading-color); font-size: 1.6em; font-weight: normal; line-height: 1.25em; margin-bottom: 16px; overflow-wrap: break-word; font-family: system-ui, sans-serif;\"><span jsselect=\"heading\" jsvalues=\".innerHTML:msg\" jstcache=\"10\">This site can’t be reached</span></h1><p jsselect=\"summary\" jsvalues=\".innerHTML:msg\" jstcache=\"2\" style=\"display: inline; color: rgb(95, 99, 104); font-family: system-ui, sans-serif; font-size: 15px;\"><strong jscontent=\"hostName\" jstcache=\"23\" style=\"overflow-wrap: break-word;\">www.android.com</strong>&nbsp;took too long to respond.</p><span style=\"color: rgb(95, 99, 104); font-family: system-ui, sans-serif; font-size: 15px;\"></span><div id=\"error-information-popup-container\" jstcache=\"0\" style=\"color: rgb(95, 99, 104); font-family: system-ui, sans-serif; font-size: 15px;\"><div id=\"error-information-popup\" jstcache=\"0\"><div id=\"error-information-popup-box\" jstcache=\"0\"><div id=\"error-information-popup-content\" jstcache=\"0\"><div id=\"suggestions-list\" jsdisplay=\"(suggestionsSummaryList &amp;&amp; suggestionsSummaryList.length)\" jstcache=\"17\"><p jsvalues=\".innerHTML:suggestionsSummaryListHeader\" jstcache=\"19\" style=\"margin-block-end: 0px;\">Try:</p><ul jsvalues=\".className:suggestionsSummaryList.length == 1 ? 'single-suggestion' : ''\" jstcache=\"20\" class=\"\"><li jsselect=\"suggestionsSummaryList\" jsvalues=\".innerHTML:summary\" jstcache=\"22\" jsinstance=\"0\">Checking the connection</li><li jsselect=\"suggestionsSummaryList\" jsvalues=\".innerHTML:summary\" jstcache=\"22\" jsinstance=\"*1\"><a href=\"chrome-error://chromewebdata/#buttons\" jstcache=\"0\" style=\"text-decoration: none;\">Checking the proxy and the firewall</a></li></ul></div><div class=\"error-code\" jscontent=\"errorCode\" jstcache=\"18\" style=\"color: var(--error-code-color); font-size: 0.8em; text-transform: uppercase; margin-top: 12px;\">ERR_CONNECTION_TIMED_OUT</div></div></div></div></div>",
            "tags": [
                "a",
                "b",
                "c"
            ],
            "images": [
                {
                    "ext": "jpg",
                    "disk": "qiniu",
                    "path": "task-images/VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz.jpg",
                    "uuid": "VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz",
                    "zise": 1134596,
                    "mime_type": "image/jpeg"
                },
                {
                    "ext": "jpg",
                    "disk": "qiniu",
                    "path": "task-images/l6ADjH7KNo3PNi6Vu23sSqFE3XNya0u1Dqg9gMnJ.jpg",
                    "uuid": "l6ADjH7KNo3PNi6Vu23sSqFE3XNya0u1Dqg9gMnJ",
                    "zise": 1263529,
                    "mime_type": "image/jpeg"
                }
            ],
            "status": "release",
            "release_at": "2021-01-10 18:49:21",
            "storage_type": "qiniu",
            "created_at": "2021-01-10 10:49:21",
            "updated_at": "2021-01-10 10:49:21",
            "image_host": "http://qm6tgfk67.hn-bkt.clouddn.com/",
            "task_type_name": {
                "name": "微信朋友圈",
                "slug": "wechat_comment",
                "icon": "wechat_comment"
            }
        },
        {
            "id": 1,
            "task_type": "wechat_comment",
            "title": "微信朋友圈",
            "claim": "要求用户下载的图片或给用户看的示例图",
            "url": "https://tp.com/tasks/create",
            "amount": "8.0000",
            "inventory": 2000,
            "compose": "<h1 jstcache=\"0\" style=\"color: var(--heading-color); font-size: 1.6em; font-weight: normal; line-height: 1.25em; margin-bottom: 16px; overflow-wrap: break-word; font-family: system-ui, sans-serif;\"><span jsselect=\"heading\" jsvalues=\".innerHTML:msg\" jstcache=\"10\">This site can’t be reached</span></h1><p jsselect=\"summary\" jsvalues=\".innerHTML:msg\" jstcache=\"2\" style=\"display: inline; color: rgb(95, 99, 104); font-family: system-ui, sans-serif; font-size: 15px;\"><strong jscontent=\"hostName\" jstcache=\"23\" style=\"overflow-wrap: break-word;\">www.android.com</strong>&nbsp;took too long to respond.</p><span style=\"color: rgb(95, 99, 104); font-family: system-ui, sans-serif; font-size: 15px;\"></span><div id=\"error-information-popup-container\" jstcache=\"0\" style=\"color: rgb(95, 99, 104); font-family: system-ui, sans-serif; font-size: 15px;\"><div id=\"error-information-popup\" jstcache=\"0\"><div id=\"error-information-popup-box\" jstcache=\"0\"><div id=\"error-information-popup-content\" jstcache=\"0\"><div id=\"suggestions-list\" jsdisplay=\"(suggestionsSummaryList &amp;&amp; suggestionsSummaryList.length)\" jstcache=\"17\"><p jsvalues=\".innerHTML:suggestionsSummaryListHeader\" jstcache=\"19\" style=\"margin-block-end: 0px;\">Try:</p><ul jsvalues=\".className:suggestionsSummaryList.length == 1 ? 'single-suggestion' : ''\" jstcache=\"20\" class=\"\"><li jsselect=\"suggestionsSummaryList\" jsvalues=\".innerHTML:summary\" jstcache=\"22\" jsinstance=\"0\">Checking the connection</li><li jsselect=\"suggestionsSummaryList\" jsvalues=\".innerHTML:summary\" jstcache=\"22\" jsinstance=\"*1\"><a href=\"chrome-error://chromewebdata/#buttons\" jstcache=\"0\" style=\"text-decoration: none;\">Checking the proxy and the firewall</a></li></ul></div><div class=\"error-code\" jscontent=\"errorCode\" jstcache=\"18\" style=\"color: var(--error-code-color); font-size: 0.8em; text-transform: uppercase; margin-top: 12px;\">ERR_CONNECTION_TIMED_OUT</div></div></div></div></div>",
            "tags": [],
            "images": [
                {
                    "ext": "jpg",
                    "disk": "qiniu",
                    "path": "task-images/VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz.jpg",
                    "uuid": "VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz",
                    "zise": 1134596,
                    "mime_type": "image/jpeg"
                },
                {
                    "ext": "jpg",
                    "disk": "qiniu",
                    "path": "task-images/l6ADjH7KNo3PNi6Vu23sSqFE3XNya0u1Dqg9gMnJ.jpg",
                    "uuid": "l6ADjH7KNo3PNi6Vu23sSqFE3XNya0u1Dqg9gMnJ",
                    "zise": 1263529,
                    "mime_type": "image/jpeg"
                }
            ],
            "status": "release",
            "release_at": "2021-01-10 14:37:06",
            "storage_type": "qiniu",
            "created_at": "2021-01-10 06:37:06",
            "updated_at": "2021-01-10 06:37:06",
            "image_host": "http://qm6tgfk67.hn-bkt.clouddn.com/",
            "task_type_name": {
                "name": "微信朋友圈",
                "slug": "wechat_comment",
                "icon": "wechat_comment"
            }
        }
    ],
    "first_page_url": "https://tp.com/api/tasks?page=1",
    "from": 1,
    "last_page": 1,
    "last_page_url": "https://tp.com/api/tasks?page=1",
    "links": [
        {
            "url": null,
            "label": "&laquo; Previous",
            "active": false
        },
        {
            "url": "https://tp.com/api/tasks?page=1",
            "label": 1,
            "active": true
        },
        {
            "url": null,
            "label": "Next &raquo;",
            "active": false
        }
    ],
    "next_page_url": null,
    "path": "https://tp.com/api/tasks",
    "per_page": 15,
    "prev_page_url": null,
    "to": 2,
    "total": 2
}
```

## Task Type (任务类型)
- Path: /api/task-types
- Method: Get
- Paramters
- Result
```
[
    {
        "name": "全部",
        "slug": "all",
        "icon": "all"
    },
    {
        "name": "京东",
        "slug": "jd",
        "icon": "jd"
    },
    {
        "name": "微信朋友圈",
        "slug": "wechat_comment",
        "icon": "wechat_comment"
    },
    {
        "name": "抖音",
        "slug": "tiktok",
        "icon": "tiktok"
    },
    {
        "name": "淘宝",
        "slug": "taobao",
        "icon": "taobao"
    }
]
```
