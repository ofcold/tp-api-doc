## Login/Log In (登入)
- Path: /api/login
- Mehtod: POST
- Paramters:
```
phone_number:18898726543 [require|unique|china phone number]
password:Admin123 [require|min:8|max:20]
```

- Result:
```
{
    type: 'Bearer',
    token: '8|8AL1mwqbE5n3QNLMGSnjWlfWcBSXMee4uVieSPnt'
}
```

- Example: Bearer 8|8AL1mwqbE5n3QNLMGSnjWlfWcBSXMee4uVieSPnt


## Logout
- Path: /api/logout
- Mehtod: GET
- Headers:
```
Authorization: Bearer 8|8AL1mwqbE5n3QNLMGSnjWlfWcBSXMee4uVieSPnt
```

- Paramters: NONE

```
