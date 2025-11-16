# 🤖 n8n Job TTS Automation Workflow (ElevenLabs & Discord)

## 📌 Project Overview / ภาพรวมโครงการ

**[EN]** This n8n workflow is designed to **convert job description data into spoken audio (Text-to-Speech - TTS)** using the **ElevenLabs** service. The resulting audio file and a summary are then automatically sent to a designated **Discord** channel.

**[TH]** โปรเจกต์นี้คือ n8n workflow ที่สร้างขึ้นเพื่อ **แปลงข้อมูลรายละเอียดงาน/อาชีพให้เป็นเสียงพูด (Text-to-Speech - TTS)** โดยใช้บริการ **ElevenLabs** จากนั้นจึงส่งไฟล์เสียงพร้อมข้อมูลสรุปไปยังช่องทาง **Discord** โดยอัตโนมัติ

---

## 🛠️ Workflow Structure / โครงสร้าง Workflow

This workflow consists of four main stages: / Workflow นี้ประกอบด้วย 4 ส่วนหลัก:

1.  **Job Data Fetch/Input:** Retrieves the raw job description data (e.g., title, duties, qualifications). / รับข้อมูลดิบของรายละเอียดงาน (เช่น ชื่อตำแหน่ง, หน้าที่, คุณสมบัติ).
2.  **Script Generation/Processing:** Processes and formats the data into a script ready for TTS conversion (may use JavaScript or AI/LLM Nodes). / ประมวลผลและจัดรูปแบบข้อมูลให้เป็นสคริปต์ที่พร้อมสำหรับการแปลงเสียง (อาจใช้ Node JavaScript หรือ AI/LLM Node).
3.  **ElevenLabs TTS Conversion:** Converts the prepared script into an audio file (.mp3 or .wav). / แปลงสคริปต์ที่ได้ให้เป็นไฟล์เสียง (.mp3 หรือ .wav).
4.  **Discord Notification & File Upload:** Uploads the generated audio file and sends a notification message to the specified Discord channel. / อัปโหลดไฟล์เสียงที่สร้างเสร็จแล้ว พร้อมส่งข้อความแจ้งเตือนไปยังช่อง Discord ที่กำหนด.

---

## ⚙️ Prerequisites / ข้อกำหนดเบื้องต้น

To ensure the workflow runs correctly, you must have the following: / เพื่อให้ Workflow นี้ทำงานได้อย่างถูกต้อง คุณต้องมีสิ่งเหล่านี้:

* **n8n Instance:** Installed and running n8n Server (Self-hosted or Cloud). / ติดตั้งและใช้งาน n8n Server (Self-hosted หรือ Cloud).
* **ElevenLabs API Key:** An API key to access the ElevenLabs service. / คีย์ API สำหรับการเข้าถึงบริการ ElevenLabs.
* **Discord Webhook URL:** The Webhook URL for the target Discord channel. / Webhook URL สำหรับช่อง Discord ที่คุณต้องการให้ไฟล์เสียงถูกส่งไป.
* **Source Data:** A data source feeding job details into the Workflow (e.g., CSV, Google Sheets, or an API). / แหล่งข้อมูลที่ป้อนรายละเอียดงานเข้าสู่ Workflow (เช่น ไฟล์ CSV, Google Sheets, หรือ API).

---

## 🔑 Credential Setup / การตั้งค่า Credentials

You need to set up the necessary credentials in n8n for external connections: / คุณจำเป็นต้องตั้งค่า Credential ใน n8n สำหรับการเชื่อมต่อภายนอก:

| Service / บริการ | Credential Type / ประเภท Credential | Required Information / ข้อมูลที่จำเป็น |
| :--- | :--- | :--- |
| **ElevenLabs** | API Key | Your ElevenLabs API Key |
| **Discord** | Webhook URL | Your Discord Webhook URL |
| **Source Data** | (Depends on source) | e.g., Database Credentials or API Key |

---

## 🚀 How to Use / วิธีการใช้งาน

1.  **Import Workflow:** Copy the content of this `my-tts-workflow.json` file and **Import** it into your n8n Editor. / คัดลอกเนื้อหาทั้งหมดในไฟล์ `my-tts-workflow.json` นี้ ไปวาง (Import) ใน n8n Editor.
2.  **Connect Credentials:** Update the ElevenLabs and Discord Nodes to connect to the credentials you have set up. / อัปเดต Node ของ ElevenLabs และ Discord ให้เชื่อมต่อกับ Credentials ที่คุณได้สร้างไว้.
3.  **Configure Input:** Customize the Trigger or Input Node to pull job description data from your desired source. / ปรับแต่ง Node เริ่มต้นให้ดึงข้อมูลรายละเอียดงานจากแหล่งที่คุณต้องการ.
4.  **Test Run:** Execute the workflow manually to ensure the audio file is created and successfully sent to Discord. / รัน Workflow ด้วยตนเองเพื่อตรวจสอบว่าไฟล์เสียงถูกสร้างและส่งไปยัง Discord สำเร็จหรือไม่.
5.  **Activate:** Set the workflow to run automatically (e.g., daily or upon data changes). / ตั้งค่า Workflow ให้ทำงานอัตโนมัติ (เช่น ทุกวัน หรือตามการเปลี่ยนแปลงของข้อมูล).

---

## 🤝 Support / การสนับสนุน

If you have any questions or need assistance in customizing this workflow, please contact [Your Contact Channel, e.g., email or Discord ID]. / หากมีคำถามหรือต้องการความช่วยเหลือในการปรับแต่ง Workflow นี้ กรุณาติดต่อ [dream.seat1@outlook.com].
