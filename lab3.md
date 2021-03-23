# การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล


# วัตถุประสงค์
เพื่อทดลองสัญญาณเอ้าพุทออกไปภายนอก

# อุปกรณ์ที่ใช้
* 1.ไมโครคอนโทรลเลอร์
* 2.เอ้าพุทพอร์ต-อินพุทพอร์ต คือ หมายเลข0(สีขาว)และ1(สีเหลือง)
* 3.adapter
* 4.relay
* 5.หลอดไฟLED

# ศึกษาข้อมูลเบื้องต้น
* จะใช้ข้อมูลจากplatformio.iniเพื่อศึกษาข้อมูลของไมโครคอนโทรลเลอร์
* คลิปการสอนในyoutubeของอาจาร https://youtu.be/9s2qB71o3Xc

# วิธีการทำการทดลอง
* 1.ต่อadapterเข้ากับ USB to sereal แล้วก็ต่อไมโครคอนโทรลเลอร์ข้างบน
 ![image](https://user-images.githubusercontent.com/80879678/112155062-8517d480-8c17-11eb-9d98-1142280b8d57.jpg)
* 2.เซ็ตให้พอร์ต 0 เป็นพอร์ตเอ้าพุท และมีการวนลูปทุก500ms
 ![image](https://user-images.githubusercontent.com/80879678/112155294-bc868100-8c17-11eb-8a6a-c3d2956f1f37.jpg)
* 3.นับ cnt(count)ไปเรื่อยๆ ถ้าcntเป็นเลขคี่ให้onเลขคู่ให้off 
 ![image](https://user-images.githubusercontent.com/80879678/112155343-cc05ca00-8c17-11eb-8a51-b1c21b9b851e.jpg)
* 4.อัปโหลดโปรแกรมโดยเขียนคำสั่ง pio run -t upload
 ![image](https://user-images.githubusercontent.com/80879678/112155404-daec7c80-8c17-11eb-8cd7-b36f0462bb6b.jpg)
* 5.เพื่อให้โปรแกรมถูกโหลดกดปุ่มอัปโหลด
* 6.กดปุ่มรีเซ็ต
 * 7.ดูผลลัพท์การรันโดยเขียน pio device monitor
 ![image](https://user-images.githubusercontent.com/80879678/112155485-edff4c80-8c17-11eb-9a36-fa88113ce316.jpg)
* 8.นำไมโครคอนโทรลเลอร์ที่เขียนโปรแกรมไว้แล้ว มาใช้เพื่อควบคุมrelayเพื่อเปิด/ปิดสวิทซ์
 ![image](https://user-images.githubusercontent.com/80879678/112156989-5a2e8000-8c19-11eb-8857-caf1f8547aa4.jpg)
* 9.ต่อเข้ากับขั้วชาร์ต
 ![image](https://user-images.githubusercontent.com/80879678/112157082-6c102300-8c19-11eb-8eae-e7906c577dfb.jpg)
* โค้ดที่ใช้ในการเขียนโปรแกรม
 ```javascript
 ; IOT for KIDS
;
; By Dr.Choompol Boonmee
; 

[env:exercise01]
platform = espressif8266
board = esp01_1m
framework = arduino
board_build.flash_mode = dout

upload_port = /dev/cu.usbserial-1420
;upload_port = COM3

monitor_port = /dev/cu.usbserial-1420
;monitor_port = COM3
monitor_speed = 115200
```
# การบันทึกผลการทดลอง
ทุกๆครึ่งวินาทีจะเป็นon/off
พอร์ตที่ต่อเส้นสีขาวจะเปล่งแสงตอนที่on
![image](https://user-images.githubusercontent.com/80879678/112155642-1424ec80-8c18-11eb-999a-79c9768e7b1b.jpg)
เมื่อต่อrelay จะควบคุมrelayให้เปิด/ปิดโดยจะได้ยินเสียง
![image](https://user-images.githubusercontent.com/80879678/112157082-6c102300-8c19-11eb-8eae-e7906c577dfb.jpg)

# อิปรายผลการทดลอง
* จากการทดลองก่อนที่จะต่อrelayสัญญาณจะเป็นon/offสลับกันไปทุกๆครึ่งวินาทีและเมื่อเป็นon LEDจะเปล่งแสง
* Relay จะไปควบคุมการเปิดปิดสวิทซ์

# คำถามหลังการทดลอง
* เราสามารถทำให้ไฟกระพริบเร็วขึ้นหรือช้าลงได้หรือไม่
* ตอบ ได้โดยการไปเขียนโค้ดใหม่ เลือกเวลาวนลูปที่เร็วขึ้นหรือช้าลงนั่นเอง
