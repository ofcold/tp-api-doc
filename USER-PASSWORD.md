## Password reset (密码重设)
- Path: /api/password-sms
- Method: POST
- Paramters
```
phone_number:18898726543 [require|exists|china phone number]
```


## Password store (密码重设)
- Path: /api/password-store
- Method: POST
- Paramters
```
phone_number:18898726543 [require|exists|china phone number]
password:password [string]
password_confirmation:password [string]
validate_code:18898726543 [require|exists|china phone number]
```
