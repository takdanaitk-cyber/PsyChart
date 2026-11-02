# PsyChart – โปรเจกต์ Android

แอปทำงานออฟไลน์ทั้งหมด (WebView + ไฟล์ในแอป) ข้อมูลโปรเจกต์เก็บในเครื่อง
PDF/JPG/CSV/XLSX ที่ส่งออกจะบันทึกที่ `Downloads/Psychrometric/` (ต้องใช้ Android 10 ขึ้นไป)

## วิธีสร้าง APK ด้วย GitHub (ไม่ต้องลงโปรแกรมอะไร)
1. สมัคร/ล็อกอิน github.com → New repository (ตั้งเป็น Private ได้)
2. อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ (รวมโฟลเดอร์ `.github`) ขึ้น repository
   - ถ้าลากอัปโหลดบนเว็บ ให้แน่ใจว่าโฟลเดอร์ `.github/workflows/build-apk.yml` ขึ้นไปด้วย
3. ไปที่แท็บ **Actions** → เลือก **Build APK** → **Run workflow** (ใช้เวลาประมาณ 3–6 นาที)
4. เมื่อเสร็จ เปิดรอบที่รัน → หัวข้อ **Artifacts** → ดาวน์โหลด `PsyChart-apk` (เป็น zip ข้างในคือ `PsyChart.apk`)
5. ส่งไฟล์ .apk เข้ามือถือ → เปิดไฟล์ → อนุญาต "ติดตั้งจากแหล่งที่ไม่รู้จัก" ตามที่เครื่องถาม

## วิธีสร้างด้วย Android Studio
เปิดโฟลเดอร์นี้ → รอ Gradle sync → Build > Build APK(s)

## แก้ไขแอป
ตัวแอปคือไฟล์ `app/src/main/assets/index.html` (ไฟล์เดียว) แก้แล้ว build ใหม่ได้เลย
