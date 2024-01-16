URL: https://www.sportforlife.co.th/api/member/addpoint <br>
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
| phone         | String          | M           | เบอร์มือถือสมาชิก          |
| amount        | Numberic (10,2) | M           | ยอดซื้อ                 |
| ref           | String          | M           | เลขที่บิล                |
| pos           | Number          | M           | อ้างอิงสถานที่ใช้งาน <br>1 = SPORT FOR LIFE<br>2 = UCL<br>3 = PTK<br>6 = Shopee<br>8 = Peloton      |
| detail        | String          | O           | ชื่อรายการ defult = ซื้อสินค้า-บริการ                |

M=Mandatory, O=Optional

### ตัวอย่าง Request
```json
{
    "phone": "0873574494",
    "amount": "10000",
    "ref": "INV24010001",
    "pos": "1",
    "detail": "ทดสอบการเพิ่มคะแนนจาก API"
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
    "message": "เพิ่มคะแนนสำเร็จ",
    "data": {
        "points_now": 400,
        "points_before": 589,
        "points_total": 989
    }
}
```

