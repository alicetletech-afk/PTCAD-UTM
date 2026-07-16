# PTCAD Sales Hub

ระบบสร้างลิงก์ UTM สำหรับทีมขาย พร้อม Campaign Cards, Caption, QR Code, Link History และหน้า CMS

## ไฟล์หลัก

- `index.html` หน้าสำหรับทีมขาย
- `login.html` หน้าเข้าสู่ CMS
- `admin.html` หน้า CMS
- `js/config.js` ตั้งค่า API และ Demo Mode
- `apps-script/Code.gs` Backend สำหรับ Google Apps Script
- `setup/installation-guide.md` คู่มือติดตั้ง

## ติดตั้งฐานข้อมูลแบบอัตโนมัติ

นำ `apps-script/Code.gs` ไปวางใน Google Apps Script แล้วรัน:

```text
setupPTCADSalesHub
```

ระบบจะสร้าง Google Spreadsheet, ทุกแท็บ, หัวคอลัมน์ และข้อมูลตัวอย่างให้อัตโนมัติ ไม่ต้องสร้าง Sheet เอง

## Demo Login

Password: `ptcad2026`

## หมายเหตุ

หน้าเว็บอ้างอิงโลโก้จาก URL ที่ให้มาโดยตรง หากใช้งาน Internal แบบ Offline ให้ดาวน์โหลดโลโก้มาไว้ใน `assets/images/` แล้วแก้ค่า `logoUrl` ใน `js/config.js`


## รูปแบบลิงก์เวอร์ชันนี้

ระบบสร้าง `ref` เป็นพารามิเตอร์แรกเสมอ:

```text
https://ptcadthailand.com/pricing/?ref=ball&utm_source=line&utm_medium=sales&utm_campaign=ptcad_lite_2026
```

ชื่อเซลล์เก็บใน `ref` ส่วน `utm_content` ใช้เฉพาะ Content Variant ที่กรอกเพิ่มเติมเท่านั้น
