# Common Header
- X-Requested-With: XMLHttpRequest [string]
- Authorization: You login token (Example: Bearer 8|8AL1mwqbE5n3QNLMGSnjWlfWcBSXMee4uVieSPnt) [string]

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

## Password reset (密码重设)
- Path: /api/password-sms
- Method: POST
- Paramters
```
phone_number:18898726543 [require|unique|china phone number]
