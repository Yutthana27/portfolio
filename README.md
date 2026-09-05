# Portfolio — Yutthana Satorn

React + Vite. Static build, no backend.

## Run locally

```bash
npm install
npm run dev        # http://localhost:5173
```

## Build

```bash
npm run build      # -> dist/
npm run preview    # ดู dist/ ก่อนขึ้นจริง
```

## Deploy — Vercel

Vercel ตรวจเจอ Vite เองอัตโนมัติ ไม่ต้องตั้งค่าอะไรเพิ่ม
(Framework Preset: Vite / Build Command: `npm run build` / Output: `dist`)

**ผ่าน GitHub (แนะนำ — push แล้วเว็บอัปเดตเอง)**

```bash
git init
git add .
git commit -m "portfolio"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

จากนั้นเข้า vercel.com → Add New → Project → เลือก repo → Deploy

**ผ่าน CLI (เร็วกว่า ถ้าอยากลองก่อน)**

```bash
npm i -g vercel
vercel          # preview URL
vercel --prod   # production
```

## โครงไฟล์

```
index.html            meta tags, og:image, preload พอร์ตเทรต
src/main.jsx          จุดเริ่ม React
src/Portfolio.jsx     ทั้งหน้าอยู่ในไฟล์นี้
public/               เสิร์ฟตรงที่ root — path ขึ้นต้นด้วย / ได้เลย
  portrait.webp
  sut-logo.webp
  nangrong-logo.webp
  favicon.svg
  shots/              สกรีนช็อตโปรเจกต์ 13 รูป
  files/              เรซูเม่ PDF
```

## แก้เนื้อหา

ข้อมูลทั้งหมดรวมอยู่ด้านบนของ `src/Portfolio.jsx` เป็นค่าคงที่:
`ME`, `PROJECTS`, `EDUCATION`, `SKILLS`, `SKILL_ICONS`

เปลี่ยนรูป: วางไฟล์ทับใน `public/shots/` โดยใช้ชื่อเดิม ไม่ต้องแตะโค้ด
