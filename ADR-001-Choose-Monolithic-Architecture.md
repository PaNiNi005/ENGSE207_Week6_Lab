# 📄ADR-001: Monolithic for Dormitory System

**Date:** 2026-01-11  
**Status:** Accepted  
**Deciders:** นางสาวรัฐจิกาลณ์ กวงคำ 67543210063-3 

---

## 📝Context

### Background
ระบบบริหารจัดการหอพัก (Dormitory Management System) 

มีวัตถุประสงค์เพื่อช่วยผู้ดูแลหอพักในการจัดการข้อมูลห้องพัก ผู้เช่า การชำระค่าเช่า ค่าน้ำ ค่าไฟ และการแจ้งซ่อมบำรุง ระบบถูกออกแบบมาสำหรับการใช้งานในองค์กรขนาดเล็ก มีจำนวนผู้ใช้งานไม่มาก และมีขอบเขตการทำงานที่ชัดเจน

### Problem Statement
จำเป็นต้องเลือกสถาปัตยกรรมซอฟต์แวร์ที่เหมาะสมกับระบบบริหารจัดการหอพัก โดยต้องคำนึงถึง:
- ความง่ายในการพัฒนา  
- การดูแลรักษา  
- ต้นทุนและระยะเวลาในการพัฒนา  
ภายใต้ข้อจำกัดของทีมและทรัพยากรที่มีอยู่

### Key Drivers
**Functional:**
- จัดการข้อมูลผู้เช่า ห้องพัก และสัญญาเช่า
- บันทึกและตรวจสอบการชำระเงินค่าเช่า ค่าน้ำ และค่าไฟ
- รองรับการแจ้งซ่อมและติดตามสถานะการซ่อมบำรุง

**Quality Attributes:**
- **Maintainability:** ระบบต้องแก้ไขและดูแลรักษาได้ง่าย  
- **Performance:** ระบบต้องตอบสนองได้รวดเร็วสำหรับจำนวนผู้ใช้งานปกติ  
- **Simplicity:** โครงสร้างระบบไม่ซับซ้อนเกินความจำเป็น  

**Constraints:**
- งบประมาณและเวลาพัฒนามีจำกัด  
- ทีมพัฒนามีขนาดเล็ก  

---

## Decision

เราเลือกใช้ **Monolithic Web Application Architecture**

### Components
- **Web UI:** ส่วนติดต่อผู้ใช้สำหรับผู้ดูแลหอพักและผู้เช่า  
- **Application Logic:** ประมวลผลกฎทางธุรกิจ เช่น การคำนวณค่าใช้จ่ายและสถานะการชำระเงิน  
- **Database Access Layer:** จัดการการเชื่อมต่อและการจัดเก็บข้อมูล  
- **Database:** จัดเก็บข้อมูลผู้เช่า ห้องพัก การชำระเงิน และการซ่อมบำรุง  

### Technologies
- **Frontend:** HTML, CSS, JavaScript  
- **Backend:** Python (Flask หรือ Django)  
- **Database:** MySQL  
- **Others:** REST API, Web Browser  

### Architectural Patterns
- Monolithic Architecture  
- Layered Architecture  

---

## Rationale

### Why this decision?
1. ระบบมีขอบเขตชัดเจนและจำนวนผู้ใช้งานไม่สูงมาก  
2. Monolithic มีความซับซ้อนต่ำ เหมาะสำหรับทีมขนาดเล็ก  
3. ลดต้นทุนและระยะเวลาในการพัฒนา  
4. ง่ายต่อการดูแลและแก้ไขในระยะเริ่มต้น  

### Alternatives Considered
1. **Client–Server Architecture**  
   - Pros: ขยายระบบได้ง่าย รองรับผู้ใช้งานจำนวนมาก  
   - Cons: โครงสร้างซับซ้อนขึ้น ต้องใช้ทรัพยากรมาก  
   - Why not chosen: เกินความจำเป็นสำหรับระบบปัจจุบัน  

2. **Microservices Architecture**  
   - Pros: Scalability และ flexibility สูง  
   - Cons: ซับซ้อนสูง ต้นทุนและภาระการดูแลมาก  
   - Why not chosen: เกินความจำเป็นสำหรับระบบขนาดเล็ก  

---

## Consequences

### Positive (ข้อดี)
- ✅ พัฒนาและดูแลรักษาได้ง่าย  
- ✅ ลดต้นทุนและเวลาในการพัฒนา  
- ✅ โครงสร้างระบบเข้าใจง่าย  

### Negative (ข้อเสีย)
- ❌ ขยายระบบได้จำกัด → Mitigation: ปรับโครงสร้างเป็น Client–Server ในอนาคต  
- ❌ การเปลี่ยนแปลงใหญ่ต้อง deploy ทั้งระบบ → Mitigation: วางโครงสร้างโค้ดแบบ Layered ให้ชัดเจน  

### Risks
- ⚠️ หากจำนวนผู้ใช้งานเพิ่มขึ้นอย่างรวดเร็ว  
  - Impact: Medium  
  - Probability: Low  
  - Mitigation: เตรียมแผน migrate architecture ในอนาคต  

### Trade-offs
- ความง่ายในการพัฒนา vs ความสามารถในการขยายระบบ  
- ต้นทุนต่ำ vs ความยืดหยุ่นระยะยาว  

---

## Compliance

### Constraints Met
- ✅ งบประมาณจำกัด: ใช้เทคโนโลยีที่ไม่ซับซ้อนและต้นทุนต่ำ  
- ✅ ทีมขนาดเล็ก: Monolithic เหมาะกับทีมพัฒนาขนาดเล็ก  

### Quality Attributes Addressed
- ✅ Maintainability: โครงสร้างแบบ Layered ทำให้แก้ไขง่าย  
- ✅ Performance: ลด overhead จากการสื่อสารระหว่างบริการ  

---

## Notes

### Assumptions
- จำนวนผู้ใช้งานไม่เกินหลักร้อย  
- ระบบใช้งานภายในองค์กรเป็นหลัก  

### Future Considerations
- หากระบบขยายตัว อาจพิจารณาเปลี่ยนเป็น Client–Server หรือ Microservices  

### References
- *Software Architecture in Practice* – Len Bass  
- [ADR GitHub](https://adr.github.io)  
- [C4 Model](https://c4model.com)



