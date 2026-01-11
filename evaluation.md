## Evaluation

### Comparison Table

เกณฑ์ให้คะแนน: 1 = แย่, 5 = ดีมาก  
Weighted = Score × Weight

| Criteria        | Weight | Arch 1: Monolithic (Score) | Arch 1 (Weighted) | Arch 2: Client–Server (Score) | Arch 2 (Weighted) |
|-----------------|--------|----------------------------|-------------------|-------------------------------|-------------------|
| Performance     | 20%    | 4                          | 0.8               | 4                             | 0.8               |
| Scalability     | 20%    | 2                          | 0.4               | 5                             | 1.0               |
| Maintainability | 20%    | 3                          | 0.6               | 4                             | 0.8               |
| Complexity      | 20%    | 5                          | 1.0               | 3                             | 0.6               |
| Cost            | 20%    | 5                          | 1.0               | 3                             | 0.6               |
| **Total**       | **100%** |                            | **3.8**           |                               | **3.8**           |

💡 *หมายเหตุ:* คะแนนรวมใกล้เคียงกัน แสดงให้เห็นว่าแต่ละ Architecture มีจุดเด่นและข้อจำกัดที่แตกต่างกันอย่างชัดเจน

---

### Selected Architecture

**Decision:** Candidate Architecture 1 – Monolithic Web Application

**Reasons:**
1. ระบบบริหารจัดการหอพักมีขอบเขตชัดเจนและจำนวนผู้ใช้งานไม่สูงมาก  
   ทำให้สถาปัตยกรรมแบบ Monolithic เพียงพอต่อความต้องการในปัจจุบัน
2. สถาปัตยกรรมแบบ Monolithic มีความซับซ้อนต่ำ  
   เหมาะสำหรับการพัฒนาและการดูแลระบบในระยะเริ่มต้น
3. ช่วยลดต้นทุนและระยะเวลาในการพัฒนา  
   ซึ่งสอดคล้องกับข้อจำกัดด้านงบประมาณและระยะเวลา (Constraints)
