# Gemini Project Use Case Diagram

## Use Case Diagram
![screenshot](https://github.com/sanntidraa/muict-gitaction-demo1/blob/main/Gemini.png)

## Use Case Description

### **Astronomer**:
   - Create Science Plan สร้างแผนวิทยาศาสตร์
   - Submit Science Plan to System ส่งแผนเข้าสู่ระบบ
   - Check System Status ตรวจสอบสถานะของระบบ
   - Test Science Program ทดสอบโปรแกรมวิทยาศาสตร์ (Extend จาก Create Science Plan)
   - Validate Science Plan ตรวจสอบความถูกต้องของแผน (Include ในการส่งแผน)
### **Science Observer**:
   - Transform Science Plan into Executable Observing Program แปลงแผนเป็นโปรแกรมสำหรับการสังเกตการณ์
   - Manage Observation จัดการกระบวนการสังเกตการณ์
   - Remote Observation ทำการสังเกตการณ์จากระยะไกล
### **Developer**:
   - Upgrade System Software อัปเกรดซอฟต์แวร์ของระบบ (Include Test Upgraded System)
   - Access Test Environment เข้าถึงสภาพแวดล้อมทดสอบ
   - Test Upgraded System ทดสอบระบบที่อัปเกรดแล้ว
### **Telescope Operators**:
   - Monitor Telescope Status เฝ้าติดตามสถานะของกล้องโทรทรรศน์
   - Monitor Telescope Performance เฝ้าติดตามประสิทธิภาพการทำงานของกล้อง
   - Control Telescope in Operation Mode ควบคุมกล้องในโหมดปฏิบัติการ (Extend Adjust Telescope Settings)
   - Adjust Telescope Settings ปรับการตั้งค่ากล้องโทรทรรศน์
   - Execute Telescope Command ดำเนินการคำสั่งของกล้อง (Include Diagnostic System)
### **Support**:
   - Monitor System เฝ้าติดตามระบบ
   - Maintain System บำรุงรักษาระบบ
   - Troubleshoot Hardware Issue แก้ไขปัญหาฮาร์ดแวร์
   - Troubleshoot Software Issues แก้ไขปัญหาซอฟต์แวร์
### **Administrator**:
   - Manage User Privileges จัดการสิทธิ์การใช้งานของผู้ใช้
   - Config System กำหนดค่าระบบ
