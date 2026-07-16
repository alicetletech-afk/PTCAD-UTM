# API Deploy Checklist

1. เปิด Google Apps Script และวางไฟล์ `apps-script/Code.gs`
2. รัน `setupPTCADSalesHub` หนึ่งครั้ง และอนุญาตสิทธิ์
3. Deploy > New deployment > Web app
4. Execute as: Me
5. Who has access: Anyone
6. คัดลอก URL ที่ลงท้าย `/exec`
7. เปิด `js/config.js`
8. ใส่ URL ใน `apiUrl`
9. เปลี่ยน `demoMode: true` เป็น `demoMode: false`
10. อัปโหลดเว็บทั้งหมดขึ้น Hosting เดิม

ตัวอย่าง:

```javascript
window.PTCAD_CONFIG = {
  apiUrl: "https://script.google.com/macros/s/DEPLOYMENT_ID/exec",
  logoUrl: "https://ptcad.alicetletech.com/assets/images/ptcad-logo.png",
  siteName: "PTCAD Sales Hub",
  demoMode: false,
  adminDemoPassword: "ptcad2026"
};
```
