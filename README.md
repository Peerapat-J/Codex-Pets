# Codex Pets

โปรเจคสำหรับสร้างและเก็บ custom pet ของ Codex หลายตัว โดยแยกไฟล์ใช้งานจริง รายละเอียดตัวละคร ภาพอ้างอิง และผลตรวจของแต่ละตัวไว้ด้วยกัน

## Pets

| Pet | สไตล์ | รูปแบบ |
| --- | --- | --- |
| [Mira](pets/mira/README.md) | สาวเอลฟ์อนิเมะ ผมบลอนด์หม่น แว่นดำ ชุดกรมท่า | v2 · 9 animations · 16 look directions |

![Mira waving](pets/mira/qa/previews/waving.gif)

## โครงสร้าง

```text
pets/
  mira/
    pet.json             # metadata สำหรับ Codex
    spritesheet.webp     # atlas ที่ใช้จริง
    brief.json           # รูปลักษณ์และข้อกำหนดของตัวละคร
    README.md            # วิธีใช้และสถานะการตรวจ
    qa/                  # รายงาน ภาพรวม และ GIF preview
references/
  mira/reference.png     # ภาพอ้างอิงต้นฉบับที่ผู้ใช้ให้มา
docs/adding-a-pet.md      # ขั้นตอนเพิ่มตัวใหม่
templates/pet-brief.md    # แบบฟอร์มเริ่มออกแบบ
```

ไฟล์ระหว่างสร้างเก็บใน `work/` และ ZIP สำหรับแจกเก็บใน `dist/` ซึ่งถูกยกเว้นจาก Git

## ใช้งาน Mira

นำ `pet.json` และ `spritesheet.webp` จาก `pets/mira/` ไปไว้ด้วยกันใน `~/.codex/pets/mira/` แล้วเลือก Mira จากตัวเลือก pet ใน Codex เมื่อมีให้ใช้งาน

Mira ผ่านการตรวจรูปแบบ atlas และภาพเคลื่อนไหวแล้ว การเลือกใช้งานใน Codex UI ยังไม่ได้ทดสอบ ดูรายละเอียดใน [หน้า Mira](pets/mira/README.md)

## สร้างตัวต่อไป

เริ่มจาก [แบบฟอร์มตัวละคร](templates/pet-brief.md) แล้วทำตาม [ขั้นตอนเพิ่ม pet](docs/adding-a-pet.md) แต่ละตัวใช้ ID และโฟลเดอร์ของตัวเอง จึงพัฒนาหลายสไตล์ใน repo เดียวได้

การสร้างภาพใช้ skill `hatch-pet` และเครื่องมือสร้างภาพที่มีใน Codex โดยติดตั้งแยกจาก repo นี้ ไฟล์ pet ที่เสร็จแล้วใช้งานได้โดยไม่ต้องมีเครื่องมือสร้างภาพ

## เชื่อม remote ภายหลัง

สร้าง remote repository เปล่าของคุณ แล้วรันจากโฟลเดอร์นี้ โดยแทน `YOUR_REPOSITORY_URL` ด้วย URL จริง:

```sh
git remote add origin YOUR_REPOSITORY_URL
git push -u origin main
```

Repo นี้เตรียมไว้ในเครื่องบน branch `main` และยังไม่มี remote
