# Content Intake — urbanROOM website

วางไฟล์ตามโครงสร้างนี้ แล้วบอก Claude ให้ wire ขึ้น code ได้เลย

---

## 1. รูปภาพ Hero (rotating background)

**โฟลเดอร์:** `assets/images/hero/`

วางรูปโปรเจกต์หรือรูป field work ที่อยากให้หมุนใน hero section
ตอนนี้ rotate 4 สไลด์ — วางได้ 4–6 รูป

| ชื่อไฟล์แนะนำ | เนื้อหา |
|---|---|
| `hero-01.jpg` | รูปแรกที่เห็นเมื่อเปิดเว็บ — เลือกรูปที่ดีที่สุด |
| `hero-02.jpg` | สไลด์ที่สอง |
| `hero-03.jpg` | สไลด์ที่สาม |
| `hero-04.jpg` | สไลด์ที่สี่ |

**spec รูป:**
- อัตราส่วน landscape (16:9 หรือกว้างกว่า)
- ขนาดแนะนำ: 2400px กว้าง
- Format: JPG, คุณภาพสูง (ไม่ต้อง compress มาก เพราะเป็น hero)

---

## 2. รูปโปรเจกต์

**โฟลเดอร์:** `assets/images/projects/[ชื่อโปรเจกต์]/`

แต่ละโปรเจกต์ต้องการ:
- **cover.jpg** — รูปหลักที่แสดงใน grid (อัตราส่วน 4:5 portrait)
- **01.jpg, 02.jpg, ...** — รูปเพิ่มเติมในหน้า detail (ใส่ได้เท่าที่มี)

| โฟลเดอร์ | โปรเจกต์ | สถานะข้อมูลใน code |
|---|---|---|
| `khon-kaen-innovation-district/` | Khon Kaen Innovation District | ✓ ครบ |
| `walkable-kangsadan/` | Walkable Kangsadan | ✓ ครบ |
| `isan-showcase/` | ISAN Showcase | ✓ ครบ |
| `sukhothai-learning-center/` | Sukhothai Learning Center | ✓ ครบ |
| `eco-innovation-park/` | Eco Innovation Park | ✓ ครบ |
| `pocket-park/` | Pocket Park | ✓ ครบ |
| `phetchabun-city/` | Phetchabun City | ✓ ครบ |
| `lam-luk-ka-city/` | Lam Luk Ka City | ✓ ครบ |

**spec รูป:**
- cover: อัตราส่วน 4:5 (portrait), ขนาด 1200×1500px
- detail: อะไรก็ได้ แต่ landscape ดูดีกว่า

---

## 3. ข้อมูล YouTube

**ไฟล์:** `content/videos.json`

เปิดไฟล์นี้แล้วกรอก:
- `youtube_url` — link video จริง
- `youtube_id` — ID ท้าย URL (ส่วน `v=XXXXX`)
- แก้ `title`, `meta`, `duration`, `desc` ให้ตรงกับ video จริง

ตอนนี้ใน code มี 4 video placeholder — เพิ่มหรือลดจำนวนได้

---

## 4. ข้อมูลโปรเจกต์ (ตรวจสอบ)

ข้อมูลโปรเจกต์ที่ใส่ไว้ใน `index.html` แล้ว — ตรวจสอบว่าถูกต้อง:

- ชื่อ client
- ปี (year)
- พื้นที่ (area)
- Role ที่ทำ
- คำอธิบาย (desc)

ถ้าต้องแก้ บอก Claude หรือแก้ใน `index.html` ที่ section `const PROJECTS = [...]`

---

## 5. Partners (ถ้ามี logo)

**โฟลเดอร์:** `assets/images/partners/`

ตอนนี้แสดงแค่ชื่อ 3 บริษัท:
- 3DOT DESIGN
- Z56
- Open partner slot

ถ้าต้องการเพิ่ม logo หรือแก้รายชื่อ บอก Claude

---

## สิ่งที่ทำได้เลยหลังจากวางไฟล์แล้ว

บอก Claude ว่า:
- "wire รูป hero" → ใส่รูปจริงใน slideshow
- "wire รูป projects" → ใส่รูปใน project grid และ detail view
- "wire videos.json" → เอา YouTube จริงใส่ channel section
- "ตรวจโปรเจกต์" → เช็คข้อมูลทั้งหมดใน code
