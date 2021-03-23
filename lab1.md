# การทดลองที่1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

# วัตถุประสงค์
* 1.เพื่อทราบว่าเป็นผลิตภัณฑ์ของบริษัทใด
* 2.บอร์ดที่ใช้ชื่ออะไร
* 3.ใช้วิธีเขียนโปรแกรมแบบไหน
* 4.ใช้พอร์ตที่ติดต่อพอร์ตอะไร

# อุปกรณ์ที่ใช้
* 1.CPU
* 2.เสาอากาศสำหรับไวไฟ
* 3.อุปกรณืต่อUSB
* 4.ไมโครคอนโทรลเลอร์

# ศึกษาข้อมูลเบื้องต้น
* จะศึกษาโดยใช้ข้อมูลจาก platformio.ini
* คลิปyoutubeของอาจาร์ย https://youtu.be/NLIUsWLEpmg

# วิธีการทำการทดลอง
* 1.ต่อไมโครคอนโทรลเลอร์
 ![image](https://user-images.githubusercontent.com/80879678/112148884-facc7200-8c10-11eb-901b-463e050c2d46.jpg)
* 2.ไปดูตัวอย่างโปรแกรมที่อยู่ในโฟลเดอร์9โปรแกรม
* 3.จะใช้ตัวอย่าง cd01_serial
 ![image](https://user-images.githubusercontent.com/80879678/112148981-15065000-8c11-11eb-8e73-479ec9fcaf44.jpg)

* 4.ใช้ configulation file platformio.ini
 ![image](https://user-images.githubusercontent.com/80879678/112149059-2c453d80-8c11-11eb-85ea-86c60257f23f.jpg)
* 5.อัปโหลดโปรแกรมเข้าไมโครคอนโทรลเลอร์โดยใช้คำสั่ง pio run -t upload
 ![image](https://user-images.githubusercontent.com/80879678/112149152-441cc180-8c11-11eb-890f-e0eec96896ac.jpg)
* 6.เพื่อให้รันโปรแกรมใหม่ ต้องกดปุ่มรีเซ็ต
 ![image](https://user-images.githubusercontent.com/80879678/112149241-572f9180-8c11-11eb-95e8-2c0c878792fb.jpg)
* 7.ใช้คำสั่งpio device monitor เพื่อดูผลลัพท์
  ![image](https://user-images.githubusercontent.com/80879678/112149295-66aeda80-8c11-11eb-8cb9-fe93a27b7bff.jpg)

# การบันทึกผลการทดลอง
* ทราบว่าเป็น platform ของ espressif8266
* มีบอร์ดชื่อ esp01_1m
* ใช้วิธีเขียนโปรแกรมแบบarduino
* พอร์ตที่ใช้ติดต่อคือ COM3
 ![image](https://user-images.githubusercontent.com/80879678/112150178-6236f180-8c12-11eb-9a6e-d880700f3421.jpg)

# อภิปรายผลการทดลอง
* สามารถดูข้อมูลของไมโครคอนโทรเลอร์ได้
* pio run -t upload นั้นใช้ในการอัพโหลดข้อมูลไปยัง microcontroller โดยสามารถกดปุ่มซึ่งอยู่ภายนอก microcontroller เพื่อทำการโหลดและรีเซ็ตการรันโปรแกรมได้

# คำถามหลังการทดลอง
* ปัจจุบันมีBoard,Platform,Framework อยู่เท่าไหร่
 * ตอบ 998 Board,44 Platform,24 Frameworks







