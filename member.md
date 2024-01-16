URL: https://www.sportforlife.co.th/api/member <br>
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
| Field         | Type          | Description             |
| ------------- |---------------| ------------------------|
| keyword       | String        | เบอร์มือถือสมาชิก           |

### ตัวอย่าง Request
```json
{
    "keyword": "0873574494"
}
```


### Response
| Field            | Type          | Description             |
| -----------------|---------------| ------------------------|
| id               | Number        | รหัสสมาชิก                |
| username         | String        | ชื่อผู้ใช้                   |
| email            | String        | อีเมลสมาชิก               |
| activation_email | Number        | 1=ยืนยันอีเมลแล้ว 0=ยังไม่ยืนยัน |
| first_name       | String        | ชื่อจริงสมาชิก              |
| last_name        | String        | นามสกุลสมาชิก            |
| gender           | String        | M=เพศชาย F=เพศหญิง      |
| phone            | String        | เบอร์โทรศัพท์มือถือสมาชิก    |
| birthday         | String        | วันเดือนปีเกิด (YYYY-mm-dd) |
| member_class     | String        | ระดับสมาชิกปัจจุบัน         |
| points           | String        | คะแนนคงเหลือ             |

### ตัวอย่าง Response
```json
{
    "status": "success",
    "data": {
        "id": "1",
        "username": "admin",
        "email": "imjaka.pk@gmail.com",
        "activation_email": "1",
        "first_name": "SPORT FOR LIFE",
        "last_name": "ADMIN",
        "gender": "M",
        "phone": "0873574494",
        "birthday": null,
        "member_class": "Exclusive",
        "member_class_by": "exclusive",
        "points": 109
    }
}
```
