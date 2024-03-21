URL: https://www.sportforlife.co.th/api/member/redeempoint <br>
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
| point        | Numberic (10)    | M           | จำนวนคะแนนที่ต้องการแลก    |
| ref           | String          | O           | เลขที่บิล (ถ้ามี)           |
| pos           | Number          | M           | อ้างอิงสถานที่ใช้งาน <br>1 = SPORT FOR LIFE<br>2 = UCL<br>3 = PTK<br>6 = Shopee<br>8 = Peloton      |
| detail        | String          | O           | บันทึกเพิ่มเติม (ถ้ามี)       |

M=Mandatory, O=Optional

### ตัวอย่าง Request
```json
{
    "phone": "0873574494",
    "point": 100,
    "ref": "INV24010001",
    "pos": "1",
    "detail": "ทดสอบแลกคะแนนจาก API"
}
```

### Response
| Field            | Type          | Description             |
| -----------------|---------------| ------------------------|
| points_now       | Number        | จำนวนคะแนนที่เพิ่มครั้งนี้      |
| points_before    | Number        | จำนวนคะแนนก่อนหน้านี้      |
| points_total     | Number        | จำนวนคะแนนสะสมรวมครั้งนี้   |


### ตัวอย่าง Response
```json
{
    "status": "success",
    "message": "แลกคะแนนสำเร็จ",
    "data": {
        "redeem_now": 100,
        "point_before": 900,
        "point_remaining": 800
    }
}
```

