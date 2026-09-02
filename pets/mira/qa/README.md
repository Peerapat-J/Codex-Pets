# Mira QA archive

หลักฐานจากการสร้าง Mira วันที่ 2026-09-02 ย้ายเข้ามาพร้อมไฟล์ pet ที่มีไบต์ตรงกับผลงานเดิม รายงานเหล่านี้เป็นผลของรอบสร้างเดิม ไม่ได้หมายความว่ามีการรันทดสอบใหม่เมื่อ clone repo

## รายงานหลัก

- [run-summary.json](run-summary.json): สรุปรอบสร้างและสถานะการติดตั้งเดิม
- [validation-extended.json](validation-extended.json): โครงสร้าง atlas และความโปร่งใส
- [final-visual-qa.json](final-visual-qa.json): ผลตรวจภาพและการเคลื่อนไหว
- [direction-blind-validation.json](direction-blind-validation.json): ผลรวมการตรวจทิศโดยไม่เห็นชื่อทิศ
- [blind-review-resolution.json](blind-review-resolution.json): ข้อสรุปความกำกวมเล็กน้อยที่ 315°
- [look-continuity.json](look-continuity.json): ค่าความต่อเนื่องระหว่างทิศ
- [repository-import.json](repository-import.json): SHA-256 ของไฟล์หลักและรายละเอียดการย้ายเข้า repo

รายงานที่เหลือเก็บการตรวจ anchor, chroma despill, ขอบเขตเฟรม, คำตอบผู้ตรวจ และเวลาในการสร้าง ส่วน `previews/` เก็บ GIF ของแต่ละ animation

## ความหมายของพาธ

พาธใน JSON ถูกปรับให้อ่านได้ข้ามเครื่อง โดยตัวเลข ผลตรวจ และคำตัดสินเดิมคงไว้:

- `pets/mira/...` และ `references/mira/...` อ้างจากรากของ repo
- `archived-run/mira/...` เป็นชื่อไฟล์ระหว่างสร้างในรอบเดิม ไฟล์เหล่านี้ถูกล้างหลังส่งมอบและไม่ได้รวมอยู่ใน repo
- `~/.codex/pets/mira` คือปลายทางการติดตั้งเดิม ไม่ใช่โฟลเดอร์ใน repo

`installed_bytes_verified: true` เป็นผลยืนยันจากเครื่องที่สร้าง Mira เท่านั้น ส่วน `runtime_selection_tested: false` หมายถึงยังไม่ได้ตรวจการเลือกและแสดง pet ผ่าน Codex UI
