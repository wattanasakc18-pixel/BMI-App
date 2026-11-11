# BMI Calculator

เว็บแอปคำนวณดัชนีมวลกาย (BMI) รองรับการแสดงผลบนมือถือ ใช้เกณฑ์ที่แตกต่างกันตามกลุ่มอายุและเพศ

## Features

- เลือกเพศ ชาย / หญิง
- กรอกน้ำหนัก (กก.), ส่วนสูง (ซม.) และอายุ (ปี)
- คำนวณค่า BMI พร้อมแสดงผลเกณฑ์สุขภาพและคำแนะนำ
- แบ่งเกณฑ์การประเมินตาม 3 กลุ่มอายุ
  - **เด็ก/วัยรุ่น (2–19 ปี)** — BMI-for-age Percentile (WHO) แยกตามเพศ
  - **ผู้ใหญ่ (20–59 ปี)** — Asian BMI cutoff (WHO สำหรับประชากรเอเชีย)
  - **ผู้สูงอายุ (60+ ปี)** — เกณฑ์เฉพาะวัยสูงอายุ

## Tech Stack

- HTML5 / CSS3 / Vanilla JavaScript
- Google Fonts — Prompt
- ไม่มี dependency หรือ build step ใด ๆ

## Project Structure

```
BMI/
├── index.html       # ไฟล์หลักของแอป
└── README.md        # เอกสารนี้
```

## การ Deploy

### Netlify Drop
1. เข้า [netlify.com/drop](https://app.netlify.com/drop)
2. ลากโฟลเดอร์ `BMI/` ไปวาง
3. ได้ URL ทันที ไม่ต้องตั้งค่าอะไรเพิ่ม

### GitHub Pages
1. Push โค้ดขึ้น GitHub repository
2. ไปที่ Settings → Pages → Source: `main` branch
3. แอปจะพร้อมใช้งานที่ `https://<username>.github.io/<repo>/`

### Vercel
```bash
npx vercel --prod
```

### ใช้งาน Local
เปิดไฟล์ `index.html` ในเบราว์เซอร์ได้เลย ไม่ต้องติดตั้งอะไร

## BMI Criteria Reference

| กลุ่ม | เกณฑ์ที่ใช้ | อ้างอิง |
|---|---|---|
| เด็ก 2–19 ปี | BMI-for-age Percentile | WHO Child Growth Standards |
| ผู้ใหญ่ 20–59 ปี | Asian cutoff (< 18.5 / 18.5–22.9 / 23–24.9 / ≥ 25) | WHO Expert Consultation 2004 |
| ผู้สูงอายุ 60+ ปี | ผ่อนปรน (< 20 / 20–23.9 / 24–27.4 / ≥ 27.5) | กรมอนามัย กระทรวงสาธารณสุข |
