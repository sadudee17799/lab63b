# การทดลองที่ 7 ผสมแลป
## วัตถุประสงค์
1.เพื่อวิเคราะห์และผสมแลปต่างๆเข้าด้วยการ และใช้ในชีวิตได้จริง(ไฟข้างทาง)

## อุปกรณ์ที่ใช้
1.ไมโครคอนโทรลเลอร์
2.CPU
3.อุปกรณ์ต่อUSB
4.เอ้าพุท อินพุทพอร์ต
5.adapter
6.relay
7.หลอดไฟ
8.censorแสง

## ศึกษาข้อมูลเบื้องต้น
1.คลิป youtube ขออาจารย์

## วิธีการทำการทดลอง
1.
```javascript
#include <Arduino.h>
#include <ESP8266WiFi.h>

int cnt = 1;

void setup()
{
	Serial.begin(115200);
	pinMode(0, OUTPUT);
	pinMode(2, INPUT);
	Serial.println("\n\n\n");
}

void loop()
{
	int val = digitalRead(0);
	Serial.printf("======= read %d\n", val);
	if(val!=0) {
		digitalWrite(2, HIGH);
	} else {
		digitalWrite(2, LOW);
	}
	a=50
  b=50
  delay(a+b);
}
```
2.นำโปรแกรมไปอัปโหลดโดยใช้คำสั่ง pio run -t upload

## การบันทึกผลการทดลอง
สายไฟเส้นสีขาวจิ้มไปที่0โวลต์ ให้สัญญาณinputเป็น1แล้วoutputจะREAD1ไฟจะติด
เมื่อกดปุ่มสีดำไฟก็จะติด
ในกรณีที่นำcensorมาใช้ เมื่อแสงน้อยจะหลอดไฟจะติด แสงมากหลอดไฟจะดับ

## อภิปรายผลการทดลอง
สามารถนำไปใช้ในชีวิตประจำวันดังเช่นไฟข้างทาง



