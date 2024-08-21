### TumTop โปรแกรม
เป็นโปรแกรม ที่เอาไว้ generate keyword แล้ว เก็บเป็น csv file ให้ และสามารถ เขียนลง meta data ของรูปได้ด้วย
ข้อดี
1. สามารถเลือก model ของ openai เองได้ 
2. คุณเป็นคนคุมค่าใช้จ่ายของ api_key ด้วยตัวเอง
3. สามารถขยายรูปได้ ถ้ารูปต้นทางเจนมาจาก AI (ดูตัวอย่าง รูป original vs รูปขยาย resized ได้ในตัวอย่างด้านล่าง)
    ขอเพียงคุณมี User_Secret_Key โปรแกรมจะเจนอัตโนมัติ ตอนที่ทำการฝัง meta data ลงไปที่รูป
    การขยายรูป จะขยายแบบไม่ได้ใช้ AI ดังนั้น ฟรีต้นทุน ไม่ถูกตัดงานวงเงินของ api_key
4. การส่งรูปไปถาม keyword จาก AI ทางเราใช้ algorithm ที่ลด prompt ให้มากที่สุด ทำให้ต้นทุนถูกกว่าหลายๆเจ้า แม้คุณจะส่งภาพใหญ่ มาให้โปรแกรมเจนก็ตาม
5. สามารถกดปุ่ม save ที่หน้าโปรแกรมได้ เพื่อจะได้ไม่ต้องคอยกรอก api_key ทุกๆครั้งที่ใช้โปรแกรม
6. 10 รูปแรกของแต่ละ folder **ฟรี** ทุกๆครั้งที่เจน แต่ถ้ามี secret user key เราจะใส่ meta data ลงไปใน 10 รูปนั้นให้ด้วย (ถ้าไม่มี user_secret_key เราจะเจนไฟล์ csv ให้เท่านั้น)
7. สามารถใส่ input ได้ทั้ง PNG และ JPG ไฟล์

### การใช้งาน
1. unzip and install app. สำหรับ MacOS สามารถเปิดตัว DMG แล้วลากลง Application ได้เลย
2. สำหรับ Windows สามารถ unzip และเปิดตัว TumTop.exe ได้เลย
3. ขอ api_key ของ openai มากรอกช่อง API_KEY คุณสามารถ ควบคุม รายจ่ายค่า API ได้ด้วยตัวเอง
    [วิธีขอ API_KEY ภาษาไทย](https://data-espresso.com/%e0%b8%a7%e0%b8%b4%e0%b8%98%e0%b8%b5%e0%b8%81%e0%b8%b2%e0%b8%a3%e0%b8%82%e0%b8%ad-api-key-%e0%b8%88%e0%b8%b2%e0%b8%81-openai/#:~:text=%E0%B9%80%E0%B8%82%E0%B9%89%E0%B8%B2%E0%B8%AA%E0%B8%B9%E0%B9%88%E0%B8%A3%E0%B8%B0%E0%B8%9A%E0%B8%9A%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93%20%E0%B9%80%E0%B8%A1%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93%E0%B9%84%E0%B8%94%E0%B9%89%E0%B8%A3%E0%B8%B1%E0%B8%9A%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%A2%E0%B8%B7%E0%B8%99%E0%B8%A2%E0%B8%B1%E0%B8%99%E0%B9%81%E0%B8%A5%E0%B9%89%E0%B8%A7%20%E0%B8%81%E0%B8%A5%E0%B8%B1%E0%B8%9A%E0%B9%84%E0%B8%9B%E0%B8%97%E0%B8%B5%E0%B9%88%20https%3A%2F%2Fplatform.openai.com%2F%20%E2%80%9CLog%20In%E2%80%9D%20%E0%B8%81%E0%B8%A3%E0%B8%AD%E0%B8%81%E0%B8%8A%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%9C%E0%B8%B9%E0%B9%89%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B8%A3%E0%B8%AB%E0%B8%B1%E0%B8%AA%E0%B8%9C%E0%B9%88%E0%B8%B2%E0%B8%99%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%84%E0%B8%B8%E0%B8%93%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B9%83%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%AA%E0%B8%A1%E0%B8%B1%E0%B8%84%E0%B8%A3%E0%B8%AB%E0%B8%A5%E0%B8%B1%E0%B8%87%E0%B8%88%E0%B8%B2%E0%B8%81%E0%B9%80%E0%B8%82%E0%B9%89%E0%B8%B2%E0%B8%AA%E0%B8%B9%E0%B9%88%E0%B8%A3%E0%B8%B0%E0%B8%9A%E0%B8%9A,%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%A1%E0%B8%B8%E0%B8%A1%E0%B8%82%E0%B8%A7%E0%B8%B2%E0%B8%9A%E0%B8%99%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%AB%E0%B8%99%E0%B9%89%E0%B8%B2%E0%B8%88%E0%B8%AD%20%E0%B8%84%E0%B8%B8%E0%B8%93%E0%B8%88%E0%B8%B0%E0%B9%80%E0%B8%AB%E0%B9%87%E0%B8%99%E0%B9%84%E0%B8%AD%E0%B8%84%E0%B8%AD%E0%B8%99%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%A1%E0%B8%B5%E0%B8%8A%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93%20%E0%B8%84%E0%B8%A5%E0%B8%B4%E0%B8%81%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%99%E0%B8%B1%E0%B9%89%E0%B8%99%E0%B9%80%E0%B8%9E%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B9%80%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B9%80%E0%B8%A1%E0%B8%99%E0%B8%B9%E0%B9%81%E0%B8%9A%E0%B8%9A%E0%B9%80%E0%B8%A5%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%99%E0%B8%A5%E0%B8%87%20%E0%B8%88%E0%B8%B2%E0%B8%81%E0%B8%99%E0%B8%B1%E0%B9%89%E0%B8%99%E0%B8%84%E0%B8%A5%E0%B8%B4%E0%B8%81%20%E2%80%9CView%20API%20keys%E2%80%9D)
4. กรอก User Secret Key (ถ้ามี) ถ้าไม่มี สามารถติดต่อ Line ID ด้านล่าง
5. กดปุ่ม Browse เพื่อเปิด Folder ที่มีรูปอยู่ "**เพียงคลิก ที่ไฟล์ใดไฟล์หนึ่งที่อยู่ใน Folder นั้น**" โปรแกรมจะดึงไฟล์รูปทั้งหมดมาดำเนินการอัตโนมัติ
8. เลือก model ของ AI ที่ใช้เจน ปกติคือ 4o-mini จะถุกที่สุด ตกรูปละประมาณ 0.08 บาท (ไม่รวมค่า user_secret_key) หรืออาจจะเลือก 4o ที่แพงขึ้น แต่แลกกับคีย์เวิร์ดดที่น่าจะหาได้และครอบคลุมมากขึ้น ก็ได้
9. กด Run
10. โปรแกรมจะสร้าง Folder  ขึ้นมาใหม่ ข้างใน Folder ที่เลือกจากข้อ 5 ใน Folder นั้น จะมีรูปที่ ฝัง Meta data ให้แล้ว (ถ้ามี User Secret key ในข้อ 4) และมีไฟล์ csv จะถูกสร้างขึ้น อยู่ใน folder นั้นอีกด้วย

### เรทราคา
1. ต้องมี api_key คุณสามารถควบคุม การใช้งานของ api_key ได้ด้วยตนเอง
   จากการทดลอง ถ้าใช้ โมเดล 4o-mini สามารถรันคีย์เวิร์ดได้ถูกกว่า 0.1 บาท ต่อรูป
    แต่ โมเดล 4o นั้นแพงกว่า แต่ก็ได้ คีย์เวิร์ดที่ดีกว่าเช่นกัน 
2. ถ้ามี api_key สามารถใช้โปรแกรมเราได้ โดยจะเจนแค่ csv ให้ และใช้ได้ครั้งละ 10ไฟล์
3. ถ้ามีทั้ง api_key และ user secret key สามารถเจนได้ unlimited ตราบใดที่ api_key และ user_secret_key ยังไม่หมด
   ถ้ามี User Secret key โปรแกรมจะสร้างทั้ง csv และ meta data ลงรูปภาพให้ด้วย ทั้ง 2 ขั้นตอน
   โดยสามารถติดต่อ Line ID ด้านล่าง เพื่อ ซื้อ User Secret Key ได้
    User Secret Key จะคิดราคาที่ 1 บาท ต่อการเจน 10 รูป และสามารถเก็บไว้ใช้คราวหน้าได้ ถ้ายังมีมูลค่าเหลือใน key
4. 10 รูปแรกของ ทุกๆ folder ที่เจน ถ้ารันรอบนั้นๆมากกว่า 10 รูป เราไม่ตัดเงินจาก user_secret_key ถือว่าเป็น bonus แต่ยัง api_key ของ openai คิดเงินปกติ
5. กรณี รูปภาพบางรูป ทาง AI ไม่สามารถคิด keywords ให้ได้ เราจะไม่ตัดเงินจาก user_secret_key ถือว่าโปรแกรมเจนรูปนั้นๆไม่สำเร็จ

### พบเจอบั๊ก
สามารถแจ้งได้ที่ [bugtracker](https://github.com/Pjumpod/TumTop_download/issues) เรามีรางวัลให้ด้วย

# Line ID
Line ID : foolstop หรือ pjumpod 

### v1.0.1 ####
1. better look for the GUI buttons for MacOSx.
2. fix cannot run the program if "user_secret_key" is missing.
3. show/hide the api_key, author name and secret key button.
