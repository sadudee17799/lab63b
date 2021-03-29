# การทดลองที่ 7
## วัตถุประสงค์
1.เพื่อวิเคราะห์และผสมแลปต่างๆเข้าด้วยการ และใช้ในชีวิตได้จริง
2.เพื่อให้เข้าใจการทำงานของไมโครคอนโทรลเลอร์
3.เพื่อควบคุมการเปิด/ปิดLED 

## อุปกรณ์ที่ใช้
1.ไมโครคอนโทรลเลอร์
2.CPU
3.USB adapter 
4.เอ้าพุท อินพุทพอร์ต
5.adapter
6.relay
7.หลอดไฟ
8.censorแสง

## ศึกษาข้อมูลเบื้องต้น
1.คลิป youtube ขออาจารย์
2.ศึกษาข้อมูลเพิ่มเติมทางอินเตอร์เน็ต

## วิธีการทำการทดลอง
1.
```javascript
#include <Arduino.h>
#include <ESP8266WiFi.h>

void setup() {
  // initialize digital pin 13 as an output.
  pinMode(2, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(2, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second
  digitalWrite(2, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);              // wait for a second
}


```
2.นำโปรแกรมไปอัปโหลดโดยใช้คำสั่ง pio run -t upload

## การบันทึกผลการทดลอง
เมื่อกดปุ่มสีดำที่ไมโครคอนโทรลเลอร์ไฟก็จะติด
ในกรณีที่นำcensorมาใช้ เมื่อแสงน้อยจะหลอดไฟจะติด แสงมากหลอดไฟจะดับ

## อภิปรายผลการทดลอง
สามารถนำไปใช้ในชีวิตประจำวันดังเช่นไฟข้างทาง



