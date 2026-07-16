# Installation Guide

## เปิด Demo
เปิด `index.html` เพื่อใช้ Sales Hub และ `login.html` เพื่อเข้า CMS

รหัส Demo: `ptcad2026`

## ต่อ Google Apps Script
1. สร้าง Google Sheet ใหม่
2. เปิด Extensions > Apps Script
3. วางโค้ดจาก `apps-script/Code.gs`
4. ใส่ Google Sheet ID ที่ตัวแปร `SHEET_ID`
5. Run ฟังก์ชัน `setupSheets()` หนึ่งครั้ง
6. ตั้ง Script Property ชื่อ `ADMIN_PASSWORD`
7. Deploy > New deployment > Web app
8. Execute as: Me
9. Who has access: Anyone with the link หรือจำกัดตามนโยบายบริษัท
10. Copy Web App URL
11. แก้ `js/config.js`

```js
apiUrl: "YOUR_WEB_APP_URL",
demoMode: false
```

## Deploy เว็บ
นำทั้งโฟลเดอร์ขึ้น GitHub Pages, Vercel, Netlify หรือ Hosting เดิมของ alicetletech.com ได้
