## Candidate Architecture 2: Client–Server with REST API

### Overview
สถาปัตยกรรมแบบ Client–Server แยกส่วนการทำงานระหว่าง Frontend และ Backend อย่างชัดเจน Frontend ติดต่อกับ Backend ผ่าน REST API เหมาะสำหรับระบบที่มีแนวโน้มขยายในอนาคตและรองรับผู้ใช้งานจำนวนมากขึ้น

### Components
Web Client (Frontend)
API Gateway / Backend Service
Authentication Service
Room & Booking Service
Maintenance Service
Billing Service
Database

### Technology Stack
- Frontend: [React.js]
- Backend: [Node.js (Express) หรือ Spring Boot]
- Database: [PostgreSQL]
- Others: [REST API, JWT, Docker]

### Architectural Patterns
- [Client–Server Architecture]
- [Service-Oriented Architecture (SOA)]
- [RESTful Architecture]


### Diagram


### Pros & Cons
**Pros:**
- ✅ [ขยายระบบและเพิ่มฟีเจอร์ได้ง่ายกว่า]
- ✅ [รองรับผู้ใช้งานพร้อมกันจำนวนมาก]
- ✅ [แยกความรับผิดชอบของแต่ละส่วนชัดเจน]

**Cons:**
- ❌ [ออกแบบและพัฒนาซับซ้อนกว่าแบบ Monolithic]
- ❌ [ต้องดูแลหลายส่วนของระบบ]

---
