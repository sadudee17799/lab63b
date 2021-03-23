# การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์(Wifi AP)

# วัตถุประสงค์
เพื่อเขียนโปรมแกรมที่จะสร้าไวไฟแอคเซสพอยต์ขึ้นมาเองที่จะสามารถนำไวไฟของตัวเองเชื่อมกับอุปกรณือื่น

# อุปกรณ์ที่ใช้
* 1.CPU
* 2.อุปกรณ์ต่อUSB
* 3.ไมโครคอนโทรเลอร์ESP-01

# ศึกษาข้อมูลเบื้องต้น
* platformio.ini
* คลิป youtube อาจาร์ย

# วิธีการทำการทดลอง
* 1.กำหนดชื่อและตั้งพาสเวิด
 ![image](https://user-images.githubusercontent.com/80879678/112093962-ea92a380-8bcc-11eb-8b5d-9c367a3b9449.jpg)

* 2.กำหนดIPAdress,gateway,subnet
 ![image](https://user-images.githubusercontent.com/80879678/112094045-19107e80-8bcd-11eb-87a4-81398dc3a70c.jpg)

* 3.เตรียมเว็บเซิฟเวอร์1ตัว
 ![image](https://user-images.githubusercontent.com/80879678/112094082-32192f80-8bcd-11eb-9905-b37362433e7a.jpg)

* 4.รันคำสั่งsoftAPแล้วกำหนดssiadกับpassword
 ![image](https://user-images.githubusercontent.com/80879678/112094155-537a1b80-8bcd-11eb-9f3f-7429cc1003ca.jpg)
* 5.อัปโหลดโปรแกรมโดยใช้คำสั่งpio run -t upload
![image](https://user-images.githubusercontent.com/80879678/112094212-6ee52680-8bcd-11eb-963f-b78ec3414b97.jpg)
* 6.กดปุ่มรีเซ็ต
 ![image](https://user-images.githubusercontent.com/80879678/112094256-88866e00-8bcd-11eb-8bab-dc64b6cff485.jpg)

* 7.เช็คว่าไวไฟที่สร้างขึ้นนั้นมีจริงมั้ยโดยใช้คำสั่งpio device monitor
 ![image](https://user-images.githubusercontent.com/80879678/112094298-9cca6b00-8bcd-11eb-84ab-2dc865285aca.jpg)
* 8.ใช็โทรศัพท์มือถือค้นหาไวไฟ

# การบันทึกผลการทดลอง
สามารถสร้างไวไฟแอคเซสพอยต์ขึ้นมาเองได้ โดยทดลองค้นหาด้วยโทรศัพท์แล้วว่ามีจริง
![image](https://user-images.githubusercontent.com/80879678/112094339-ad7ae100-8bcd-11eb-98da-a0eb09f63ef6.jpg)
# อภิปรายผลการทดลอง
# คำถามหลังการทดลอง
