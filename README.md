# Codex Pets

**ภาษาไทย** | [English](README.en.md)

รวม pet แบบเคลื่อนไหวสำหรับ Codex พร้อมภาพอ้างอิง ตัวอย่างแอนิเมชัน และขั้นตอนสร้างตัวละครใหม่ ปัจจุบันมี pet 2 ตัว

โปรเจคนี้แยกไฟล์ใช้งานจริง รายละเอียดตัวละคร ภาพอ้างอิง และผลตรวจของแต่ละตัวไว้ด้วยกัน เพื่อให้สร้างและดูแล pet หลายสไตล์ใน repo เดียวได้

## Pets

| Pet | สไตล์ | รูปแบบ |
| --- | --- | --- |
| [Mira](pets/mira/README.md) | สาวเอลฟ์อนิเมะ ผมบลอนด์หม่น แว่นดำ ชุดกรมท่า | v2 · 9 แอนิเมชัน · 16 ทิศการมอง |
| [Mori](pets/mori/README.md) | Humanoid 3D toy ชุด techwear โทนเขียว เสื้อกั๊กขน และกระเป๋า utility | v2 · 9 แอนิเมชัน · 16 ทิศการมอง |

![Mira waving](pets/mira/qa/previews/waving.gif)
![Mori waving](pets/mori/qa/previews/waving.gif)

## โครงสร้าง

```text
pets/
  <pet-id>/
    pet.json             # metadata สำหรับ Codex
    spritesheet.webp     # atlas ที่ใช้จริง
    brief.json           # รูปลักษณ์และข้อกำหนดของตัวละคร
    README.md            # วิธีใช้และสถานะการตรวจ
    qa/                  # รายงาน ภาพรวม และ GIF preview
references/
  <pet-id>/              # ภาพอ้างอิงและคอนเซปต์ของแต่ละตัว
docs/adding-a-pet.md      # ขั้นตอนเพิ่มตัวใหม่
templates/pet-brief.md    # แบบฟอร์มเริ่มออกแบบ
```

ไฟล์ระหว่างสร้างเก็บใน `work/` และ ZIP สำหรับแจกเก็บใน `dist/` ซึ่งถูกยกเว้นจาก Git

## ใช้งาน Pet

เลือกโฟลเดอร์จาก `pets/` แล้วนำ `pet.json` และ `spritesheet.webp` ไปไว้ด้วยกันใน `~/.codex/pets/<pet-id>/` จากนั้นเลือก pet จากตัวเลือกใน Codex เมื่อมีให้ใช้งาน

Mira และ Mori ผ่านการตรวจรูปแบบ atlas และภาพเคลื่อนไหวแล้ว การเลือกใช้งานใน Codex UI ยังไม่ได้ทดสอบ ดูรายละเอียดในหน้าของ [Mira](pets/mira/README.md) และ [Mori](pets/mori/README.md)

## สร้างตัวต่อไป

เริ่มจาก [แบบฟอร์มตัวละคร](templates/pet-brief.md) แล้วทำตาม [ขั้นตอนเพิ่ม pet](docs/adding-a-pet.md) แต่ละตัวใช้ ID และโฟลเดอร์ของตัวเอง จึงพัฒนาหลายสไตล์ใน repo เดียวได้

การสร้างภาพใช้ skill `hatch-pet` และเครื่องมือสร้างภาพที่มีใน Codex โดยติดตั้งแยกจาก repo นี้ ไฟล์ pet ที่เสร็จแล้วใช้งานได้โดยไม่ต้องมีเครื่องมือสร้างภาพ
