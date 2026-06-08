<div align="center">

# 🔥 Phoenix Flow

**AI Block-based Platform — สร้าง AI workflow แบบลากวาง ไม่ต้องเขียนโค้ด**

ลากบล็อกมาต่อกันบน canvas → เชื่อมเป็น pipeline → รันได้ทันที
เทรนโมเดล AI ของตัวเองได้ในเครื่อง (ใช้ CPU/GPU ของคุณเอง · ทำงาน offline)

### [⬇️ ดาวน์โหลดล่าสุด (Releases)](https://github.com/whitephoenixrobotics/PhoenixFlow-Releases/releases/latest)

</div>

---

## ⬇️ ดาวน์โหลด

เลือกแบบที่ตรงกับเครื่องของคุณ — ตัวติดตั้งเล็กมาก (~730 KB) แล้วดาวน์โหลดส่วนที่เหลืออัตโนมัติ

| แบบ | เหมาะกับ | ดาวน์โหลดตอนติดตั้ง | ลิงก์ |
|-----|----------|---------------------|-------|
| 🖥️ **CPU Installer** | เครื่อง Windows ทั่วไป (ไม่มีการ์ดจอก็ได้) | ~490 MB | [`Phoenix-Flow-CPU-Setup-0.2.0.exe`](https://github.com/whitephoenixrobotics/PhoenixFlow-Releases/releases/latest) |
| 🚀 **GPU Installer** | เครื่องที่มีการ์ดจอ NVIDIA (AI เร็วกว่ามาก) | ~2 GB | [`Phoenix-Flow-GPU-Setup-0.2.0.exe`](https://github.com/whitephoenixrobotics/PhoenixFlow-Releases/releases/latest) |
| 📦 **Portable (CPU)** | ไม่อยากติดตั้ง — แตก zip แล้วเปิดได้เลย | — (662 MB ในตัว) | [`Phoenix-Flow-CPU-0.2.0-win-x64.zip`](https://github.com/whitephoenixrobotics/PhoenixFlow-Releases/releases/latest) |

> **ไม่แน่ใจ?** เลือก **CPU** — รันได้ทุกเครื่อง · GPU จะช่วยก็ต่อเมื่อมีการ์ดจอ NVIDIA เท่านั้น

---

## 📥 วิธีติดตั้ง

1. ดาวน์โหลดตัวติดตั้ง (CPU หรือ GPU)
2. ดับเบิลคลิก → ตัวติดตั้งจะดาวน์โหลด + ติดตั้ง + เพิ่มเข้า Start Menu ให้อัตโนมัติ
3. ถ้า Windows ขึ้น **"Windows protected your PC"** (SmartScreen) → กด **More info → Run anyway**
4. เปิด Phoenix Flow → **Sign in with Google**
5. ผู้ใช้ใหม่จะอยู่สถานะ **รออนุมัติ** — แอดมินอนุมัติแล้วถึงเริ่มใช้งานได้

> 💡 แบบ Portable: แตก zip แล้วดับเบิลคลิก `Phoenix Flow.exe` ได้เลย ไม่ต้องติดตั้ง

---

## Phoenix Flow คืออะไร

แพลตฟอร์มสร้าง AI แบบ **block-based** (คล้าย Scratch / Node-RED แต่เน้น AI/Computer Vision) —
ลากบล็อกมาต่อกันบน canvas เพื่อสร้าง workflow เช่น *กล้อง → ตรวจจับวัตถุ → แสดงผล* โดยไม่ต้องเขียนโปรแกรม

- 🎨 **Visual editor** — ลากวางบล็อก เชื่อมเส้น เห็นผล real-time
- 🧠 **เทรน AI เองได้** — สอนโมเดลจำแนกภาพ/ตรวจจับวัตถุจากรูปของคุณเอง
- 💻 **ใช้เครื่องตัวเอง** — ประมวลผล/เทรนบน CPU/GPU ในเครื่อง (offline · ไม่ส่งข้อมูลขึ้น cloud)
- 🔐 **ควบคุมผู้ใช้** — ล็อกอิน Google + ระบบอนุมัติโดยแอดมิน
- 🖥️ **Desktop App** — Electron พร้อม auto-update

---

## ✨ ฟีเจอร์หลัก (v0.2)

- **Flow Editor** — สร้าง/บันทึก/รัน workflow บน canvas, รันสด (live) ผ่าน WebSocket
- **TrainAI** — เทรนโมเดลเอง 2 แบบ:
  - 🏷️ **จำแนกภาพ** (Classification) — ถ่าย/อัปโหลดรูปแยกคลาส แล้วเทรน
  - 🎯 **ตรวจจับวัตถุ** (Detection) — ตีกรอบ (วาดเอง/ให้ AI ช่วย) แล้วเทรน YOLO
  - มี Data Augmentation, เลือก base model, ทดสอบโมเดล, ดาวน์โหลด `.pt`
- **Speech to Text** — ถอดเสียงเป็นข้อความแบบ offline (ภาษาไทย, faster-whisper, โหมดถอดสด/อัดแล้วถอด)
- **Auth & ผู้ใช้** — ล็อกอิน Google, ผู้ใช้ใหม่รอแอดมิน **อนุมัติ**, หน้าจัดการผู้ใช้สำหรับแอดมิน

---

## 🧰 เครื่องมือ (บล็อก) ที่ใช้ได้ — รวม ~56 บล็อก ใน 11 หมวด

### 📥 Input — รับข้อมูลเข้า
Upload Image · Webcam · Text · Switch · Button · Hotkey · Speech to Text · Color · HTTP Fetch · วาดรูป

### 🔍 ข้อมูล · 🔢 คณิตศาสตร์ · ⏰ เวลา
JSON Extract · ตัวเลข · สุ่ม · คำนวณ (+ − × ÷ %) · หน่วงเวลา · ตั้งเวลา

### 🔀 ตรรกะ & Logic Gates
If/Else · Compare · Counter · Toggle · Trigger Once · Hold · AND · OR · NOT · NAND · NOR · XOR · XNOR

### 🤖 AI
Detect (YOLO) · Image Classifier · Pose (ท่าทาง) · นับวัตถุ · ตรวจจับสี · OCR (ไทย+อังกฤษ) · อ่านตัวเลขเขียนมือ (MNIST)

### 🎭 AI · ใบหน้า
โครงใบหน้า (478 จุด) · นับใบหน้า · รอยยิ้ม · จดจำใบหน้า · อารมณ์

### 🧠 Deep Learning
DeepDetect · DeepClassifier — รันโมเดลที่เทรนเอง (`.pt` / `.onnx`)

### 🎨 แก้ไขภาพ
Brightness · Contrast · Saturation · Sharpen · Blur · Grayscale · Invert · RGB Adjust · Style Transfer · แยกฉากหลัง

### 📤 Output — แสดงผล
Display · Light Bulb · Text to Speech

---

## 💻 ความต้องการของระบบ

- **Windows 10 (1809+) หรือ 11 · 64-bit**
- เชื่อมต่ออินเทอร์เน็ต (ตอนติดตั้ง + ล็อกอิน)
- **CPU build:** พื้นที่ว่าง ~2 GB
- **GPU build:** พื้นที่ว่าง ~5 GB + การ์ดจอ NVIDIA (CUDA 12.4)

---

## 🔧 ภายใต้ฝากระโปรง (Tech Stack)

| ส่วน | เทคโนโลยี |
|------|-----------|
| Frontend | Next.js 16 + React 19 + React Flow + Tailwind |
| Backend | FastAPI + SQLAlchemy (async) + SQLite |
| Desktop | Electron + electron-updater |
| Auth | Google OAuth (ผ่าน Supabase) + ระบบอนุมัติแอดมิน |
| AI / ML | PyTorch, Ultralytics YOLOv8, OpenCV, EasyOCR, MediaPipe, faster-whisper |

ทุกอย่างรวมอยู่ในตัวติดตั้ง — **ไม่ต้องลง Python / Node / Docker เอง**

---

<div align="center">
<sub>🔥 Phoenix Flow · v0.2 · ใช้งานบนเครื่องของคุณเอง · ข้อมูลไม่ออกจากเครื่อง</sub>
</div>
