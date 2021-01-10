## Register
- Path: /api/register
- Mehtod: PUT
- Paramters:
```
name:add (require|max:10)
phone_number:18898726543 (require|unique|china phone number)
password:Admin123 (require|min:8|max:20)
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

## Activation
- Path: /api/activation
- Method: POST
- Paramters
```
phone_number:18898726543 (require|china phone number)
validate_code:114751 (require|must length:6)
```

## Register resend SMS
- Path: /api/resend-sms
- Method: POST
- Paramters
```
phone_number:18898726543 (require|china phone number)
```

## Password reset
- Path: /api/password-sms
- Method: POST
- Paramters
```
phone_number:18898726543 (require|unique|china phone number)
