# Challenge : Movie Ticket Machine
แบบทดสอบสร้างระบบซื้อตั๋วหนังผ่านตู้ขายตั๋วอัตโนมัติ

## การตรวจรับ
1. ทำการ Clone หรือ Download และนำขึ้น Github ของตัวเอง และส่ง URL มาในอีเมล `arada@thinknet.co.th`
2. ในโฟลเดอร์ `exercise` จะต้องมี **Source code** และเขียนอธิบายตามหัวข้อต่างๆ ใน **Readme.md** ดังนี้   
   2.1. **Technologies** :  ลิสต์ Technology และ Library ต่างๆ พร้อมเหตุผลที่เลือกมาใช้   
   2.2. **Architecture Design** : อธิบายการออกแบบ Architecture ที่นำมาใช้   
   2.3. **Installation** : อธิบายขั้นตอนการติดตั้ง   
   2.4. **Deployment** : อธิบายว่าในแต่ละส่วนถูกนำไป Deploy ขึ้นไปที่ไหนบ้าง และเหตุผลที่เลือกใช้ พร้อมทั้งแปะ URL ของแอพพลิเคชั่น  

3. Push Code ขึ้น Branch `Master` เป็นระยะตามความคืบหน้า
4. ระหว่างวันเวลาที่กำหนด จะมีโจทย์ย่อยเพิ่มเติม โดยจะเปิดไปให้ใน Issue ของ Repo ที่ส่งมา
5. ตรวจรับบน `Public URL` เท่านั้น (เช่น Heroku, Google AppEngine, Firebase, Amazon EC2, Digital Ocean เป็นต้น)
6. การวางมาตรการความปลอดภัยของ web 
7. Code quality 

## Frontend
### Technology
   - ใช้ React หรือ Framework ที่ใช้กับ React เช่น Next.js
   - CSS สามารถใช้ Third party ได้
### Spec
ให้พัฒนาเว็บไซต์จำลองการขายตั๋วหนัง ผ่านตู้ขายตั๋วหนังอัตโนมัติ โดยมีเงื่อนไขดังนี้
- ไม่ต้องมีเลือกที่นั่ง โดยจะสามารถซื้อได้แค่ตั๋วหนังได้ทีละเรื่อง เรื่องละกี่ที่นั่งก็ได้
- สามารถรองรับการเรียงรายชื่อหนังตามวันเวลาหรือราคาได้
- ค้นหาหนังจากชื่อหนังได้
- รายละเอียดและราคาของตั๋วหนัง จะมีข้อมูลเบื้องต้นดังนี้
   - ชื่อ
   - รูปภาพโปสเตอร์หนัง
   - ราคา/ใบ
   - คำโปรย
- ตู้ต้องสามารถทอนเงินได้โดยเรียงจากแบงค์และเหรียญตามลำดับ 1000, 500, 100, 50, 20, 10, 5, 2, 1 บาท

## Backend
### Technology 
- ใช้ Node.js และสามารถใช้ Framework/library ต่าง ๆ ของ Node.js ได้
- ใช้ RESTful API หรือ GraphQL 
- ใช้ Database เป็น NoSQL
### Spec
- ให้พัฒนา API สำหรับรองรับการใช้งานได้ตาม Frontend
- มีการเก็บข้อมูลของระบบไว้ในฐานข้อมูล
- จำนวนของหนังใน database ต้องไม่น้อยกว่า 20 เรื่องไม่ซ้ำกัน
- ต้องตรวจสอบความถูกต้องของทุก input 
## ตัวอย่าง Test Case
| | ชื่อหนังที่เลือก | ราคาตั๋วหนังต่อใบ | จำนวนการซื้อ | ราคาสุทธิ | เงินที่ใส่เข้าตู้ | เงินทอน  | แบงค์และเหรียญที่ทอน |
|---|-------|------------------|------------|-----------|----------|------------|-------|
| 1 |Deadpool 2|100|1|100|100|0|-|
| 2 |Ghostland|182|1|182|200|18|10,5,2,1|
|3|Avengers : Infinity War|355|3|1065|2000|935|500,100,100,100,100,20,10,5|
|4|Ghostland|182|4|728|1000|272|100,100,50,20,2|
|5|Midnight Sun|167|1|167|1000|833|500,100,100,100,20,10,2,1|
|6|Avengers : Infinity War|355|5|1775|5000|3225|1000,1000,1000,100,100,20,5|

## Bonus(คะแนนพิเศษ)
   - สามารถคิดฟีเจอร์เพิ่มเติมจากโจทย์ด้านบน
   - ส่งอีเมลรายละเอียดการซื้อตั๋วไปให้แก่ผู้ซื้อได้
   - ทำให้ UX/UI สวยงามและใช้ง่าย
   - ออกแบบและทำ Automate testing (Unit test, Integration test, System test)

## ข้อสงสัยอื่น ๆ

สามารถส่งอีเมลมาที่ `arada@thinknet.co.th` เพื่อสอบถามหรือแนะนำเพิ่มเติมเกี่ยวกับโจทย์นี้ได้
