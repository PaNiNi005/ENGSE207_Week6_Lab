## Candidate Architecture 1: Monolithic Web Application

### Overview
สถาปัตยกรรมแบบ Monolithic เป็นระบบที่รวมทุกฟังก์ชันการทำงานไว้ในแอปพลิเคชันเดียว
เหมาะสำหรับระบบบริหารจัดการหอพักที่มีขอบเขตชัดเจนและจำนวนผู้ใช้งานไม่สูงมาก
ช่วยให้การพัฒนาและการดูแลระบบทำได้ง่ายในระยะเริ่มต้น

### Components
User Interface (Web UI)
Authentication & Authorization
Room Management
Booking Management
Maintenance / Issue Reporting
Billing & Payment Management
Database


### Technology Stack
- Frontend: [HTML, CSS, JavaScript (Bootstrap)]
- Backend: [Node.js (Express) หรือ Django]
- Database: [MySQL หรือ PostgreSQL]
- Others: [REST API, JWT Authentication]

### Architectural Patterns
- [Monolithic Architecture]
- [Layered Architecture (Presentation, Business, Data)]

### Diagram


### Pros & Cons
**Pros:**
- ✅ [ออกแบบและพัฒนาได้ง่าย]
- ✅ [ดูแลและดีบักระบบสะดวก]
- ✅ [เหมาะสำหรับระบบขนาดเล็กถึงกลาง]

**Cons:**
- ❌ [ขยายระบบ (Scalability) ได้จำกัด]
- ❌ [หากส่วนใดส่วนหนึ่งมีปัญหา อาจกระทบทั้งระบบ]

---
