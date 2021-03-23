# การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล


# วัตถุประสงค์
เพื่อนำสัญญาณอินพุทจากภายนอกเข้ามาในไมโครคอนโทรลเลอร์

# อุปกรณ์ที่ใช้
* 1.ไทโครลคอนโทรลเลอร์
* 2.เอ้าพุทพอร์ต-อินพุทพอร์ต
* 3.adapter
* 4.relay
* 5.หลอดLED
* 6.censorแสง

# ศึกษาข้อมูลเบื้องต้น
คลิปyoutubeของอาจารย์ https://youtu.be/pSAqgVDv8xU

# วิธีการทำการทดลอง
* 1.เซ็ตให้พอร์ต0เป็นinput(สีขาว)และให้พอร์ต2เป็นoutput(สีเหลือง)
 ![image](https://user-images.githubusercontent.com/80879678/112166877-9fa37b00-8c22-11eb-8c5e-971073125017.jpg)
* 2.ข้อมูลที่ได้จากพอร์ต0เป็นสัญญาณดิจิทัลคือไม่0ก็1
เขียนข้อมูลคือถ้าเป็น1(low)หลอดไฟจะดับที่พอร์ต2 ถ้าเป็น0(high)หลอดไฟติดที่พอร์ต2
![image](https://user-images.githubusercontent.com/80879678/112166985-b0ec8780-8c22-11eb-9248-f64372f73e97.jpg)
* 3.นำโปรแกรมไปอัปโหลดโดยใช้คำสั่งpio run -t upload
![image](https://user-images.githubusercontent.com/80879678/112167081-c661b180-8c22-11eb-8acc-2b0ab05803db.jpg) 
* 4.กดปุ่มอัปโหลด จะขึ้นread1 (จะเช็คที่พอร์ต0ว่ามีอินพุทมาหรือไม่ ถ้าเป็น1ไฟติด ถ้าเป็น0ไฟดับ)
*  ![image](https://user-images.githubusercontent.com/80879678/112167180-d5e0fa80-8c22-11eb-8241-d6d71b8da2a7.jpg)
* 5.นำสายไฟเส้นสีขาว(พอร์ต0)จิ้มไปที่0โวลต์ที่เส้นสีดำเอ้าพุทread0ไฟติด
 ![image](https://user-images.githubusercontent.com/80879678/112167286-ea24f780-8c22-11eb-8915-82df41b39a43.jpg)
* 6.นำไปต่อกับcensorแสง ขานึงต่อกับสีแดงอีกขาต่อกับสีดำ(ground)
 ![image](https://user-images.githubusercontent.com/80879678/112167356-f741e680-8c22-11eb-850c-1807248dc092.jpg)
* 7.นำเส้นสีขาวไปต่อกับ censor 
  ![image](https://user-images.githubusercontent.com/80879678/112167423-04f76c00-8c23-11eb-9dd9-947c58f7a6e1.jpg)
* โค้ดที่ใช้ในการเขียนโปรแกรม
 ```javascript
 #include <Arduino.h>
#include <ESP8266WiFi.h>

int cnt = 0;

void setup()
{
	Serial.begin(115200);
	pinMode(0, INPUT);
	pinMode(2, OUTPUT);
	Serial.println("\n\n\n");
}

void loop()
{
	int val = digitalRead(0);
	Serial.printf("======= read %d\n", val);
	if(val==1) {
		digitalWrite(2, LOW);
	} else {
		digitalWrite(2, HIGH);
	}
	delay(100);
}
```


# การบันทึกผลการทดลอง
* เมื่อนำสายไฟเส้นสีขาวจิ้มไปที่0โวลต์ที่เส้นสีดำจะเกิดเหตุการ์ณคือ ให้สัญญาณinputเป็น0แล้วoutputจะresd0ไฟก็จะติด
![image](https://user-images.githubusercontent.com/80879678/112167286-ea24f780-8c22-11eb-8915-82df41b39a43.jpg)
* เมื่อกดปุ่มสีดำที่ต่อกับพอร์ต0อยูแล้ว เมื่อกดพอร์ต0จะread0ไฟก็จะติด
 ![image](https://user-images.githubusercontent.com/80879678/112167517-18a2d280-8c23-11eb-82cd-f9b785b42f53.jpg)
* ในกรณีที่นำcensorมาใช้ เมื่อเอานิ้วปิดแสงจะน้อยไฟจะดับ เมื่อไม่บังแสงแสงจะมากไฟก็จะติด

# อภิปรายผลการทดลอง
* โค้ดที่ถูกอ่านมีค่าเท่ากับ0ไฟจะสว่าง1จะไฟจะดับ
* เมื่อต่อ censor เมื่อมีแสงกระทบค่าจะเป็น0แล้วสว่างและเมื่อเอามือบังค่าจะป็น1ไฟจะดับ
# คำถามหลังการทดลอง
* ในชีวิตประจำวันพบcensorลักษณะนี้ที่ใดบ้าง
* ตอบ ไฟหน้าบ้าน เมื่อตกเย็นแสงเริ่มหมดไก็จะติด
 
