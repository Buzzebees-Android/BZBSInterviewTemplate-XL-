# ข้อสอบ Android Developer 2020


## รายละเอียดข้อสอบ
* ระยะเวลาทำข้อสอบ 2 วัน
* สร้างแอปพลิเคชันตาม Requirements ที่กำหนดให้
* ผู้สมัครต้องสร้าง Project ด้วยตนเอง
* แอปพลิเคชันจะต้องใช้งานได้อย่างสมบูรณ์ ไม่ crash
* อนุญาตให้ใช้ Third Party Library ได้ตามสะดวก
* อนุญาตให้ใช้ Pattern MVP/MVVM ในการเขียนเท่านั้น
* หากสามารถใช้ Library เหล่านี้จะได้ จะพิจารณาเป็นพิเศษ 
    * Kotlin Coroutine
    * Koin
    * Dagger
    * Jetpack Components ต่าง ๆ
* หากสามารถเขียน Unit test ได้ จะพิจารณาเป็นพิเศษ (หากเวลาเหลือ)
* ผู้สมัครควรมีความเข้าใจใน Code ที่ตนเองเขียน


## Requirement

แอปพลิเคชันประกอบไปด้วย
* Login Screen
* Dashboard Screen
* Campaign List Screen
* Favourite Screen
* Detail Screen

### Login Screen

ประกอบด้วย

1. Username - ต้องกรอก
2. Password - ต้องกรอก
3. Login - หาก username และ password เป็นค่าว่าง จะต้อง alert ออกมาด้วย

อนุญาติให้ทำ Fake Login ได้ แต่หาก Login เข้าไปแล้ว หลังจากเปิดแอปมาใหม่ต้องไม่ผ่านหน้า Login อีกต่อไปแล้ว

### Dashboard Screen

เป็น Dynamic Content โดยรเรียก JSON จาก url 

https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/dashboard.json?alt=media&token=48371953-a998-4613-8791-e00c976335a2

ประกอบไปด้วย 

* small campaign rotate
* big campaign rotate
* header
* small campaign 
* big campaign

คลิกที่ไอเทมแต่ละอันจะเปิดหน้า Detail

### Campaign List Screen

เป็น Dynamic Content โดยรเรียก JSON จาก url 

https://xxxxxxxxxxxxxx

คลิกที่ไอเทมแต่ละอันจะเปิดหน้า Detail

### Detail Screen

แสดงรายละเอียด Campaign ที่คลิกมาจากหน้า Dashboard หรือ Campaign List
สามารถกด Favourite ได้

Campaign ที่เป็น Favourite จะไปปรากฎที่หน้า Favourite Screen

### Favourite Screen

แสดงรายการ Campaign ทีเป็น Favourite
