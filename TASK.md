## Task Item (任务)
- Path: /api/task-entry
- Method: Get
- Paramters
```
taskid: [string|required]
```

- Result
```
{
    "id": 2,
    "task_type": "wechat_comment",
    "title": "微信朋友圈", // 名称
    "claim": "要求用户下载的图片或给用户看的示例图", // 要求
    "url": "https://tp.com/tasks/create",
    "amount": "8.0000",
    "inventory": 2000,
    "compose": "<h1 jstcache=\"0", // 文案
    "tags": [ //标签
        "a",
        "b",
        "c"
    ],
    "images": [ // 图片
        {
            "ext": "jpg",
            "disk": "qiniu",
            "path": "task-images/VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz.jpg",
            "uuid": "VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz",
            "zise": 1134596,
            "mime_type": "image/jpeg"
        }
    ],
    "status": "release", // 状态
    "release_at": "2021-01-10 18:49:21", // 发布时间
    "storage_type": "qiniu", // 存储类型 例如：七牛云
    "created_at": "2021-01-10 10:49:21", // 创建时间
    "updated_at": "2021-01-10 10:49:21", // 更新时间
    "image_host": "http://qm6tgfk67.hn-bkt.clouddn.com/", // 图片域名
    "task_type_name": { // 任务类型
        "name": "微信朋友圈", // 类型名称
        "slug": "wechat_comment", // slug
        "icon": "wechat_comment"
    }
},
```

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
            "title": "微信朋友圈", // 名称
            "claim": "要求用户下载的图片或给用户看的示例图", // 要求
            "url": "https://tp.com/tasks/create",
            "amount": "8.0000",
            "inventory": 2000,
            "compose": "<h1 jstcache=\"0", // 文案
            "tags": [ //标签
                "a",
                "b",
                "c"
            ],
            "images": [ // 图片
                {
                    "ext": "jpg",
                    "disk": "qiniu",
                    "path": "task-images/VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz.jpg",
                    "uuid": "VC2kdNZwth1m317DTY7rLNBYDryqluLMee7EjaLz",
                    "zise": 1134596,
                    "mime_type": "image/jpeg"
                }
            ],
            "status": "release", // 状态
            "release_at": "2021-01-10 18:49:21", // 发布时间
            "storage_type": "qiniu", // 存储类型 例如：七牛云
            "created_at": "2021-01-10 10:49:21", // 创建时间
            "updated_at": "2021-01-10 10:49:21", // 更新时间
            "image_host": "http://qm6tgfk67.hn-bkt.clouddn.com/", // 图片域名
            "task_type_name": { // 任务类型
                "name": "微信朋友圈", // 类型名称
                "slug": "wechat_comment", // slug
                "icon": "wechat_comment"
            }
        },
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
