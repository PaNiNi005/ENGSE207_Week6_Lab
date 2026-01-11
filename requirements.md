# Step 1: System Selection

## 🏢 Selected System
Dormitory Management System (ระบบบริหารจัดการหอพัก)

## 📖 System Description
ระบบบริหารจัดการหอพักช่วยให้นักศึกษาและผู้ดูแลหอพักสามารถจัดการข้อมูลห้องพักได้อย่างเป็นระบบ  
- นักศึกษา: ดูข้อมูลห้องว่าง, จองห้อง, แจ้งซ่อม, ตรวจสอบค่าน้ำค่าไฟ  
- ผู้ดูแล: จัดการห้องพัก, อนุมัติ/ปฏิเสธการจอง, บันทึกค่าใช้จ่ายของแต่ละห้อง

## 🎯 Reason for Selection
- ใกล้ตัวและเข้าใจง่าย  
- ขอบเขตชัดเจน เหมาะสมกับการฝึก ADR  
- ระบบมีความซับซ้อนระดับเหมาะสม

---

# Step 2: Requirements Analysis

### 🛠️ Functional Requirements
1. นักศึกษาดูข้อมูลห้องพักและสถานะห้องว่างได้  
2. นักศึกษาจองห้องพักออนไลน์ได้  
3. ผู้ดูแลสามารถอนุมัติ/ปฏิเสธการจองได้  
4. นักศึกษาสามารถแจ้งซ่อมหรือแจ้งปัญหาเกี่ยวกับห้องพักได้  
5. ผู้ดูแลบันทึกและจัดการค่าน้ำค่าไฟของแต่ละห้องได้  
6. นักศึกษาตรวจสอบประวัติการชำระเงินของตนเองได้  

### ⚙️ Non-Functional Requirements
1. **Performance:** ระบบแสดงข้อมูลห้องพักและยืนยันการจองภายใน 3 วินาที  
2. **Availability:** ระบบพร้อมใช้งาน ≥ 99% ต่อเดือน  
3. **Security:** มีการยืนยันตัวตนและแยกสิทธิ์นักศึกษา/ผู้ดูแลชัดเจน  

### 📌 Constraints
1. **Technology:** พัฒนาเป็น Web Application  
2. **Budget:** ใช้เทคโนโลยี Open-source  
3. **Time:** MVP ต้องพัฒนาเสร็จภายใน 1 ภาคการศึกษา  

### 🏷️ Quality Attribute Scenarios

#### Scenario 1: Room Booking Performance
- **Quality Attribute:** Performance  
- **Source:** นักศึกษา  
- **Stimulus:** นักศึกษาค้นหาและจองห้องพัก  
- **Artifact:** ระบบบริหารจัดการหอพัก  
- **Environment:** ช่วงมีผู้ใช้งานพร้อมกันมาก (เปิดภาคเรียน)  
- **Response:** ระบบแสดงข้อมูลห้องพักและยืนยันการจอง  
- **Response Measure:** ตอบสนอง ≤ 3 วินาที  

#### Scenario 2: System Availability
- **Quality Attribute:** Availability  
- **Source:** ผู้ดูแลหอพัก  
- **Stimulus:** ผู้ดูแลเข้าใช้งานระบบ  
- **Artifact:** ระบบบริหารจัดการหอพัก  
- **Environment:** การใช้งานปกติ  
- **Response:** ระบบให้บริการต่อเนื่อง  
- **Response Measure:** Downtime ≤ 1% ต่อเดือน
