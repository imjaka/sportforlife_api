URL: https://www.sportforlife.co.th/api/member/historypoint <br>
Method: POST <br> 

### Header
| Field         | Type          | Description  |
| ------------- |---------------| -------------|
| Apikey        | String        | Your API Key |

### ตัวอย่าง Request header
```json
{
   "Apikey": "Your API Key",
}
```

### Body
| Field         | Type            | Mandatory     |Description           |
| ------------- |-----------------| ------------|------------------------|
| phone         | String          | M           | เบอร์มือถือสมาชิก           |

M=Mandatory, O=Optional

### ตัวอย่าง Request
```json
{
    "phone": "0873574494"
}
```



### ตัวอย่าง Response
```json
{
    "status": "success",
    "data": {
       {
            "id": "5815",
            "type": "redeemed",
            "shop": "1",
            "amount": null,
            "points": "100",
            "detail": "แลกพ้อยท์",
            "user": "1",
            "user_ref": "0873574494",
            "bill_no": "INV24010001",
            "note": "ทดสอบการแลกคะแนนจาก API",
            "ref": "R5395041_21MAR1749",
            "by": null,
            "on": "2024-03-21 17:49:51",
            "status": "1"
        },
    }
}
```

