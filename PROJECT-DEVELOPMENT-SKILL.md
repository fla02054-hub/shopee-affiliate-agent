# PROJECT DEVELOPMENT SKILL

> This Skill must be read completely before ANY development work.

## 1. Project Goal

พัฒนาโปรเจกต์ใหม่สำหรับงาน Shopee Affiliate
โดยใช้ Hermes Agent ผ่าน CLI

Repository:
fla02054-hub/shopee-affiliate-agent

โปรเจกต์นี้เริ่มใหม่จากศูนย์

---

## 2. Mandatory Development Protocol

ก่อนพัฒนา แก้โค้ด เพิ่มฟีเจอร์ แก้บั๊ก
เปลี่ยน dependency หรือ architecture ทุกครั้ง:

1. อ่าน Skill นี้ทั้งหมด
2. ตรวจ repository ปัจจุบัน
3. ตรวจโค้ดที่เกี่ยวข้องก่อนแก้
4. เปรียบเทียบสถานะจริงกับ Skill
5. เข้าใจระบบเดิมก่อนตัดสินใจ
6. เลือกวิธีที่ง่ายที่สุดที่แก้ปัญหาได้
7. ลงมือแก้เฉพาะส่วนที่จำเป็น
8. ทดสอบผลจริง
9. ตรวจว่าไม่ได้ทำระบบเดิมเสีย
10. อัปเดต Skill นี้หลังงานสำเร็จ

ห้ามเริ่มเขียนโค้ดก่อนทำข้อ 1-5

---

## 3. Development Principles

- เริ่มจากระบบที่ง่ายที่สุด
- เพิ่มความซับซ้อนเมื่อจำเป็นจริง
- ไม่สร้างระบบซ้ำ
- ไม่สร้าง abstraction ล่วงหน้าโดยไม่มีการใช้งาน
- ไม่เพิ่ม dependency โดยไม่มีเหตุผล
- ทุกฟีเจอร์ต้องสามารถตรวจสอบการทำงานจริง
- ห้ามรายงานว่าสำเร็จถ้ายังไม่ได้ตรวจสอบ
- ใช้ repository จริงเป็น source of truth

---

## 4. Greenfield Rule

โปรเจกต์นี้เป็นโปรเจกต์ใหม่

ห้าม ChatGPT นำสิ่งต่อไปนี้จากโปรเจกต์เก่ามาใช้เอง:

- architecture
- workflow
- Agent structure
- database structure
- API integration
- naming
- SCOUT / ORBIT / PULSE
- AFFLUX
- assumptions จากระบบเก่า

ใช้ได้เฉพาะเมื่อผู้ใช้สั่งให้นำกลับมาใช้โดยตรง

---

## 5. Hermes Rule

Hermes Agent เป็น Agent หลักของระบบ

หลักการ:

- ใช้ Hermes ผ่าน CLI ก่อน
- ตรวจความสามารถที่ Hermes มีอยู่แล้วก่อนสร้างระบบเพิ่ม
- ไม่สร้าง custom Agent framework มาซ้อน Hermes โดยไม่มีเหตุผล
- Hermes Skills/Tools เป็นคนละส่วนกับ Development Skill นี้
- Runtime Skill ของ Hermes ให้สร้างเมื่อ requirement จำเป็นจริง

---

## 6. Confirmed Requirements

บันทึกเฉพาะ requirement ที่ผู้ใช้ตกลงแล้ว

Current:

- ระบบเกี่ยวข้องกับงาน Shopee Affiliate
- ใช้ Hermes Agent
- CLI-first
- เริ่มพัฒนาใหม่จากศูนย์
- พัฒนาทีละขั้น
- ทุกส่วนต้องใช้งานได้จริง
- ไม่ออกแบบระบบใหญ่ล่วงหน้า

เมื่อมี requirement ใหม่:
เพิ่มตรงนี้ทันที

---

## 7. Current Architecture

บันทึก architecture ที่มีอยู่จริงเท่านั้น

ห้ามเขียน architecture ที่ยังไม่ได้สร้างเป็นของปัจจุบัน

Current:
- ยังไม่มี Shopee application architecture
- Hermes Agent เป็น external CLI runtime ของโปรเจกต์ ไม่ได้ vendor หรือสร้าง agent framework ซ้อนใน repository
- Repository ใช้ `AGENTS.md` เป็น workspace instruction และ `PROJECT-DEVELOPMENT-SKILL.md` เป็น development source of truth

---

## 8. Repository Structure

บันทึกโครงสร้างสำคัญของ repository ตามของจริง

Current:
- `AGENTS.md` — กฎระดับ repository บังคับให้อ่าน Development Skill ก่อนพัฒนา
- `PROJECT-DEVELOPMENT-SKILL.md` — Development Skill หลักของ repository
- `README.md` — ขั้นตอนติดตั้ง/ตรวจ Hermes CLI และ project smoke test ขั้นแรก
- `PROJECT_DEVELOPMENT_SKILL.md` — Development Skill รุ่นแรกที่มีอยู่ก่อนเปลี่ยนชื่อหลัก; ไม่ใช่กฎหลัก

เมื่อเพิ่ม/ลบ/ย้ายส่วนสำคัญ:
อัปเดตส่วนนี้

---

## 9. Important Components

บันทึก component สำคัญเมื่อเริ่มมีการพัฒนา

สำหรับแต่ละ component ระบุ:

- หน้าที่
- อยู่ไฟล์/โฟลเดอร์ไหน
- เชื่อมกับอะไร
- สถานะ

ห้ามสร้างรายการล่วงหน้าสำหรับ component ที่ยังไม่มี

Current:

Component: Repository development instructions
- หน้าที่: กำหนดให้ Agent อ่าน Development Skill และตรวจ repository ก่อนพัฒนา
- ไฟล์: `AGENTS.md`
- เชื่อมกับ: Hermes workspace context / development agents
- สถานะ: สร้างและตรวจไฟล์แล้ว

Component: Hermes CLI foundation documentation
- หน้าที่: กำหนด minimum setup และ smoke test ก่อนเริ่ม Shopee logic
- ไฟล์: `README.md`
- เชื่อมกับ: external `hermes` CLI
- สถานะ: สร้างและตรวจเนื้อหาใน repository แล้ว; ยังไม่ได้ยืนยัน runtime บนเครื่องผู้ใช้

---

## 10. Decisions

บันทึกการตัดสินใจทางเทคนิคที่สำคัญ

รูปแบบ:

Decision:
Reason:
Date/Stage:

ห้ามเปลี่ยน Decision เดิมโดยไม่ตรวจเหตุผลเดิมก่อน

Current Decisions:

Decision: ใช้ `PROJECT-DEVELOPMENT-SKILL.md` เป็น Development Skill หลักของ repository
Reason: ผู้ใช้กำหนดให้ไฟล์นี้เป็นกฎกลางที่ ChatGPT/Agent ต้องอ่านก่อนพัฒนาและอัปเดตหลังการพัฒนาทุกครั้ง
Date/Stage: Project initialization

Decision: Hermes Agent เป็น Agent หลัก และเริ่มผ่าน CLI
Reason: เป็น requirement ที่ผู้ใช้ยืนยัน
Date/Stage: Project initialization

Decision: ใช้ Hermes CLI โดยตรงเป็น foundation แทนการสร้าง custom agent wrapper/framework ในขั้นแรก
Reason: Hermes มี CLI, setup/model/tool configuration, one-shot chat และ workspace instruction support อยู่แล้ว; ตรงกับกฎให้ตรวจ capability ที่มีอยู่ก่อนสร้างระบบเพิ่ม
Date/Stage: Hermes CLI foundation

Decision: ใช้ one-shot `hermes chat --oneshot -q` เป็น smoke test ขั้นแรกของ repository
Reason: เป็นวิธีเล็กที่สุดในการยืนยันว่า Hermes รันได้และอ่าน context ของ repository ได้ก่อนสร้าง Shopee-specific code
Date/Stage: Hermes CLI foundation

---

## 11. Completed

บันทึกเฉพาะงานที่:

- สร้างแล้ว
- ตรวจแล้ว
- ทำงานได้จริงในขอบเขตที่ระบุ

ห้ามบันทึกงานที่ยังไม่ได้ทดสอบว่า Completed

Current:
- ตรวจ repository ก่อนงานครั้งนี้แล้ว
- ยืนยันว่า repository เข้าถึงและเขียนได้
- สร้าง Development Skill หลัก `PROJECT-DEVELOPMENT-SKILL.md`
- ตรวจ official Hermes Agent documentation สำหรับ installation, setup, CLI และ one-shot chat capability
- สร้าง `README.md` สำหรับ minimum Hermes CLI foundation และตรวจว่าไฟล์ถูกบันทึกใน repository แล้ว

---

## 12. Current Problems

บันทึก:

- bugs
- blockers
- technical debt ที่สำคัญ
- สิ่งที่ยังทำไม่ได้

เมื่อแก้สำเร็จให้อัปเดตสถานะ

Current:
- ยังไม่มี Shopee application code
- ยังไม่สามารถยืนยันได้จาก GitHub repository ว่าเครื่อง development ของผู้ใช้ติดตั้ง/configure Hermes CLI แล้ว
- project smoke test ต้องรันใน environment ที่มี Hermes CLI และ model/provider credentials จริง
- มีไฟล์ Development Skill รุ่นแรก `PROJECT_DEVELOPMENT_SKILL.md` อยู่ร่วมกับไฟล์หลักใหม่; ห้ามถือไฟล์เดิมเป็นกฎหลัก

---

## 13. Next Step

ต้องมี Main Next Step เพียงหนึ่งอย่าง

Current Next Step:

รันและยืนยัน Hermes CLI project smoke test ใน development environment จริงจาก root ของ repository ให้ผ่านก่อนสร้าง Shopee-specific application code

ห้ามกระโดดไปสร้างระบบขั้นถัดไป
ถ้า Main Next Step ปัจจุบันยังไม่ผ่าน

---

## 14. End-of-Work Protocol

หลังพัฒนาแต่ละครั้ง:

1. ทดสอบสิ่งที่เปลี่ยน
2. ตรวจ repository state
3. อัปเดต Completed
4. อัปเดต Architecture ถ้าเปลี่ยน
5. อัปเดต Repository Structure ถ้าเปลี่ยน
6. บันทึก Decision ใหม่ถ้ามี
7. อัปเดต Problems
8. กำหนด Main Next Step ใหม่
9. อัปเดต Skill นี้ใน repository

---

# DEVELOPMENT LOOP

READ SKILL
↓
INSPECT REPOSITORY
↓
UNDERSTAND CURRENT SYSTEM
↓
DECIDE
↓
BUILD
↓
TEST
↓
VERIFY
↓
UPDATE SKILL
↓
SET NEXT STEP

---

# PRIMARY RULE

ห้ามพัฒนาโปรเจกต์จากความจำของ ChatGPT เพียงอย่างเดียว

ทุกครั้งต้องอ่าน Skill นี้
และตรวจ repository จริงก่อนพัฒนา
