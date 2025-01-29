# Gemini Project Requirements

## Functional Requirements

1. **Operational Levels**:
   - The system must provide support for three operational levels: **Observing**, **Maintenance**, and **Test**.

2. **Access Modes**:
   - The system must allow users to collect and analyze data in Observing mode.
   - The system must enable read-only access to system status in Monitoring mode.
   - The system must provide direct control of the telescope in Operation mode.
   - The system must support the preparation of science programs in Planning mode.
   - The system must facilitate subsystem diagnostics and installations in Testing mode.
   - The system must allow status and scheduling control in Administrative mode.

3. **User Authentication**:
   - The system must require login-based access with role-based privileges, such as those for astronomers, observers, and support staff.

4. **Science Plan Workflow**:
   - The system must enable astronomers to create and test science plans.
   - The system must allow science observers to validate and convert science plans into executable observing programs.
   - The system must permit operation staff to execute and monitor these plans during observations.

5. **Flexible Scheduling**:
   - The system must support dynamic mode and instrument switching based on weather conditions or scientific priorities.

6. **Remote Operations**:
   - The system must allow users to perform remote observing, monitoring, and diagnostics without interrupting ongoing observations.

7. **Data Management**:
   - The system must automate data archiving into the Gemini archive.
   - The system must maintain at least two copies of raw data for security and quality assessment.

8. **Error Handling**:
   - The system must provide real-time fault notifications and error logging.
   - The system must categorize issues into **Fatal**, **Serious**, and **Warning** levels.

---

## Non-Functional Requirements

1. **Usability**:
   - The system must feature a simple and intuitive user interface designed for astronomers, operators, and support staff.
   - The system must provide clear and responsive feedback on system status and errors.

2. **Reliability**:
   - The system must ensure high reliability to avoid interruptions during planned operations.

3. **Scalability and Expandability**:
   - The system must employ a modular design to support future upgrades and visitor instruments.

4. **Security**:
   - The system must implement robust access controls to protect the telescope and its data.

---

## Additional Notes
### User-Level Access

1. **Astronomers**:
   - Astronomers must have access to Planning, Observing, and Monitoring modes.
   - Astronomers must use telescope simulators for testing science programs.

2. **Science Observers**:
   - Astronomers must use telescope simulators for testing science programs.
   - Science observers must validate science plans and manage observations.

3. **Telescope Operators**:
   - Telescope operators must have access to Observing, Maintenance, and Test levels.
   - Telescope operators must execute commands, monitor performance, and ensure operational safety.

4. **Support Staff**:
   - Support staff must have access to Maintenance and Test levels for hardware and software troubleshooting.

5. **Developers**:
   - Developers must have access to test environments and must adhere to strict guidelines when implementing upgrades.

# Gemini Project Requirements

## Functional Requirements

1. **ระดับการปฏิบัติงาน**:
   - ระบบต้องสนับสนุน 3 ระดับการปฏิบัติงาน ได้แก่ **Observing**, **Maintenance**, และ **Test**

2. **โหมดการเข้าถึง**:
   - ระบบต้องอนุญาตให้ผู้ใช้เก็บรวบรวมและวิเคราะห์ข้อมูลในโหมด สังเกตการณ์ (Observing)
   - ระบบต้องอนุญาตการเข้าถึงแบบอ่านอย่างเดียวเพื่อดูสถานะของระบบในโหมด การตรวจสอบ (Monitoring)
   - ระบบต้องอนุญาตการควบคุมกล้องโทรทรรศน์โดยตรงในโหมด การปฏิบัติการ (Operation)
   - ระบบต้องสนับสนุนการเตรียมโปรแกรมวิทยาศาสตร์ในโหมด การวางแผน (Planning)
   - ระบบต้องอำนวยความสะดวกในการตรวจวินิจฉัยและติดตั้งระบบย่อยในโหมด การทดสอบ (Testing)
   - ระบบต้องอนุญาตให้ควบคุมสถานะและตารางการปฏิบัติงานในโหมด การบริหารจัดการ (Administrative)

3. **การยืนยันตัวตนของผู้ใช้งาน**:
   - ระบบต้องรองรับการเข้าถึงผ่านการเข้าสู่ระบบ และจัดการสิทธิ์ตามบทบาท เช่น นักดาราศาสตร์ ผู้สังเกตการณ์ และเจ้าหน้าที่สนับสนุน

4. **ขั้นตอนการทำงานของแผนวิทยาศาสตร์**:
   - ระบบต้องรองรับให้นักดาราศาสตร์สามารถสร้างและทดสอบแผนวิทยาศาสตร์ได้
   - ระบบต้องอนุญาตให้ผู้สังเกตการณ์ทางวิทยาศาสตร์ตรวจสอบและแปลงแผนวิทยาศาสตร์ให้เป็นโปรแกรมการสังเกตการณ์ที่ปฏิบัติได้
   - ระบบต้องสนับสนุนเจ้าหน้าที่ปฏิบัติการในการดำเนินการและติดตามแผนเหล่านี้ระหว่างการสังเกตการณ์

5. **การกำหนดตารางเวลาแบบยืดหยุ่น**:
   - ระบบต้องรองรับการสลับโหมดและเครื่องมืออย่างยืดหยุ่นตามสภาพอากาศหรือความสำคัญทางวิทยาศาสตร์

6. **การปฏิบัติงานระยะไกล**:
   - ระบบต้องอนุญาตให้ผู้ใช้สามารถสังเกตการณ์ ติดตาม และตรวจวินิจฉัยระบบจากระยะไกลได้โดยไม่รบกวนการสังเกตการณ์ที่กำลังดำเนินอยู่

7. **การจัดการข้อมูล**:
   - ระบบต้องเก็บถาวรข้อมูลโดยอัตโนมัติในคลังข้อมูล Gemini
   - ระบบต้องรักษาสำเนาข้อมูลดิบอย่างน้อย 2 ชุด เพื่อความปลอดภัยและการประเมินคุณภาพ

8. **การจัดการข้อผิดพลาด**:
   - ระบบต้องแจ้งเตือนข้อผิดพลาดแบบเรียลไทม์และบันทึกข้อผิดพลาด
   - ระบบต้องจำแนกปัญหาเป็น 3 ระดับ ได้แก่ **Fatal**, **Serious**, และ **Warning**

---

## Non-Functional Requirements

1. **ความง่ายต่อการใช้งาน**:
   - ระบบต้องออกแบบส่วนติดต่อผู้ใช้ให้เรียบง่ายและใช้งานง่าย โดยเหมาะสำหรับนักดาราศาสตร์ ผู้ปฏิบัติการ และเจ้าหน้าที่สนับสนุน
   - ระบบต้องแสดงสถานะและข้อผิดพลาดของระบบอย่างชัดเจนและตอบสนองได้อย่างรวดเร็ว

2. **ความน่าเชื่อถือ**:
   - ระบบต้องมีความน่าเชื่อถือสูง เพื่อให้การสังเกตการณ์ดำเนินไปได้อย่างไม่สะดุดในระหว่างการปฏิบัติงานตามแผน

3. **ความสามารถในการขยายและพัฒนา**:
   - ระบบต้องมีโครงสร้างแบบแยกส่วนเพื่อรองรับการอัปเกรดในอนาคตและการใช้งานเครื่องมือเพิ่มเติม

4. **ความปลอดภัย**:
   - ระบบต้องมีการควบคุมการเข้าถึงอย่างเข้มงวดเพื่อป้องกันกล้องโทรทรรศน์และข้อมูล

---

## Additional Notes
### User-Level Access

1. **นักดาราศาสตร์**:
   - นักดาราศาสตร์ต้องสามารถเข้าถึงโหมด Planning, Observing และ Monitoring
   - นักดาราศาสตร์ต้องสามารถใช้ตัวจำลองกล้องโทรทรรศน์เพื่อทดสอบโปรแกรมวิทยาศาสตร์ได้

2. **ผู้สังเกตการณ์**:
   - ผู้สังเกตการณ์ต้องสามารถเข้าถึงโหมด Observing และ Monitoring
   - ผู้สังเกตการณ์ต้องสามารถตรวจสอบและจัดการแผนวิทยาศาสตร์ได้

3. **ผู้ควบคุมกล้องโทรทรรศน์**:
   - ผู้ปฏิบัติการต้องสามารถเข้าถึงระดับ Observing, Maintenance และ Test
   - ผู้ปฏิบัติการต้องดำเนินคำสั่ง ติดตามประสิทธิภาพ และรับรองความปลอดภัยของระบบ

4. **เจ้าหน้าที่สนับสนุน**:
   - เจ้าหน้าที่สนับสนุนต้องสามารถเข้าถึงระดับ Maintenance และ Test เพื่อแก้ไขปัญหาฮาร์ดแวร์และซอฟต์แวร์

5. **นักพัฒนา**:
   - นักพัฒนาต้องสามารถเข้าถึงสภาพแวดล้อมการทดสอบ และต้องปฏิบัติตามแนวทางที่เข้มงวดเมื่ออัปเกรดระบบ
