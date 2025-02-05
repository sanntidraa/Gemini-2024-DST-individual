# Gemini Project Use Case Diagram

## Use Case Diagram
![Usecase Diagram](https://github.com/ICT-Mahidol/2024-ITDS361-Gemini7/blob/master/2024-ITDS361-Gemini7__D2_Usecase_diagram.png)

## Use Case Description

### **Astronomer (นักดาราศาสตร์)**:
   - **Use Case 1 : **Create Science Plan สร้างแผนวิทยาศาสตร์เพื่อกำหนดการสังเกตการณ์ในอนาคต (โหมด Planning)
   - **Use Case 2 : **Submit Science Plan to System ส่งแผนเข้าสู่ระบบเพื่อให้สามารถดำเนินการได้ (โหมด Planning)
   - **Use Case 3 : **Check System Status ตรวจสอบสถานะของระบบเพื่อให้แน่ใจว่าพร้อมใช้งาน (โหมด Monitoring)
   - **Use Case 4 : **Test Science Program ทดสอบแผนวิทยาศาสตร์กับตัวจำลองก่อนใช้งานจริง (โหมด Planning) [Extend จาก Create Science Plan]
   - **Use Case 5 : **Validate Science Plan ตรวจสอบความถูกต้องของแผนก่อนแปลงเป็นโปรแกรมที่สามารถปฏิบัติการได้ (โหมด Planning) [Include ในการส่งแผน]
### **Science Observer**:
   - **Use Case 6 : **Transform Science Plan into Executable Observing Program แปลงแผนที่ได้รับการอนุมัติเป็นโปรแกรมที่สามารถดำเนินการจริงได้ (โหมด Observing)
   - **Use Case 7 : **Manage Observation ควบคุมและจัดการการสังเกตการณ์ที่กำลังดำเนินอยู่ (โหมด Observing)
   - **Use Case 8 : **Remote Observation ทำการสังเกตการณ์และติดตามข้อมูลจากระยะไกล โดยไม่รบกวนกระบวนการที่ดำเนินอยู่ (โหมด Observing & Monitoring)
### **Developer**:
   - **Use Case 9 : **Upgrade System Software อัปเกรดซอฟต์แวร์ของระบบเพื่อปรับปรุงประสิทธิภาพและความสามารถใหม่ (โหมด Test & Maintenance) [Include Test Upgraded System]
   - **Use Case 10 : **Access Test Environment เข้าถึงสภาพแวดล้อมทดสอบเพื่อพัฒนาหรือทดสอบระบบโดยไม่กระทบต่อการปฏิบัติงานจริง (โหมด Test)
   - **Use Case 11 : **Test Upgraded System ทดสอบระบบหลังจากการอัปเกรดเพื่อให้แน่ใจว่าไม่มีข้อผิดพลาด (โหมด Test)
### **Telescope Operators**:
   - **Use Case 12 : **Monitor Telescope Status ตรวจสอบสถานะกล้องโทรทรรศน์เพื่อให้แน่ใจว่าพร้อมใช้งาน (โหมด Monitoring)
   - **Use Case 13 : **Monitor Telescope Performance ตรวจสอบประสิทธิภาพของกล้องเพื่อตรวจหาปัญหาหรือความผิดปกติ (โหมด Maintenance)
   - **Use Case 14 : **Control Telescope in Operation Mode ควบคุมการทำงานของกล้องโทรทรรศน์เมื่อดำเนินการสังเกตการณ์ (โหมด Operation) [Extend Adjust Telescope Settings]
   - **Use Case 15 : **Adjust Telescope Settings ปรับการตั้งค่ากล้องให้เหมาะสมกับการสังเกตการณ์แต่ละประเภท (โหมด Operation)
   - **Use Case 16 : **Execute Telescope Command ส่งคำสั่งให้กล้องทำงานตามที่กำหนด เช่น เล็งไปที่เป้าหมาย (โหมด Operation)[Include Diagnostic System]
### **Support**:
   - **Use Case 17 : **Monitor System ตรวจสอบระบบให้แน่ใจว่าทำงานได้อย่างถูกต้อง (โหมด Monitoring)
   - **Use Case 18 : **Maintain System ดำเนินการบำรุงรักษาและปรับปรุงระบบเป็นระยะ (โหมด Maintenance)
   - **Use Case 19 : **Troubleshoot Hardware Issue แก้ไขปัญหาฮาร์ดแวร์ที่อาจทำให้ระบบทำงานผิดปกติ (โหมด Maintenance)
   - **Use Case 20 : **Troubleshoot Software Issues แก้ไขปัญหาซอฟต์แวร์เพื่อให้ระบบสามารถทำงานได้อย่างราบรื่น (โหมด Maintenance)
### **Administrator**:
   - **Use Case 21 : **Manage User Privileges จัดการสิทธิ์ของผู้ใช้เพื่อควบคุมการเข้าถึงระบบ (โหมด Administrative)
   - **Use Case 22 : **Config System กำหนดค่าต่างๆ ของระบบเพื่อให้รองรับการทำงานของทุกผู้ใช้ (โหมด Administrative)
