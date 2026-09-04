# Mori QA archive

หลักฐานจากการสร้าง Mori วันที่ 2026-09-05 รายงานเหล่านี้บันทึกผลตรวจของ atlas ที่อยู่ใน `pets/mori/spritesheet.webp`

## รายงานหลัก

- [run-summary.json](run-summary.json): สรุปรอบสร้างและสถานะการติดตั้ง
- [validation-extended.json](validation-extended.json): โครงสร้าง atlas และความโปร่งใส
- [final-visual-qa.json](final-visual-qa.json): ผลตรวจภาพและการเคลื่อนไหวแยกอิสระ
- [direction-blind-validation.json](direction-blind-validation.json): ผลรวมจากผู้ตรวจทิศแบบไม่เห็นป้าย 3 คน
- [direction-semantics.json](direction-semantics.json): ผลตรวจทิศทั้ง 16 แบบมีป้ายกำกับ
- [look-continuity.json](look-continuity.json): ค่าความต่อเนื่องระหว่างทิศ
- [chroma-despill-extended.json](chroma-despill-extended.json): ผลทำความสะอาดสีฉากหลังที่ขอบสไปรต์
- [timing.json](timing.json): ขั้นตอนซ่อมและเวลาของรอบสร้าง

ไฟล์ที่เหลือเก็บผลตรวจ cardinal anchor, คำตอบรายคนของ blind review, การตรวจเฟรม และกลไกการหันมอง ส่วน `previews/` เก็บ GIF ของ animation มาตรฐานทั้ง 9 แถว

## ความหมายของพาธ

- `pets/mori/...` อ้างจากรากของ repo
- `references/mori/...` คือภาพอ้างอิงที่เก็บใน repo
- `archived-run/mori/...` และ `archived-generation/mori/...` คือไฟล์ระหว่างสร้างที่ล้างออกหลังส่งมอบ
- `~/.codex/pets/mori` คือปลายทางติดตั้งบนเครื่องที่สร้าง

`installed_bytes_verified: true` หมายถึงไฟล์ที่ติดตั้งมี SHA-256 ตรงกับไฟล์ใน repo ส่วน `runtime_selection_tested: false` หมายถึงยังไม่ได้ตรวจการเลือกและแสดง Mori ผ่าน Codex UI
