### TumTop โปรแกรม
เป็นโปรแกรม ที่เอาไว้ generate keyword แล้ว เก็บเป็น csv file ให้ และสามารถ เขียนลง meta data ของรูปได้ด้วย
> <p>ข้อดี</p>
> 1. สามารถเลือก model ของ openai เองได้ 
> 2. คุณเป็นคนคุมค่าใช้จ่ายของ api_key ด้วยตัวเอง
> 3. สามารถขยายรูปได้ ถ้ารูปต้นทางเจนมาจาก AI (ดูตัวอย่าง รูป original vs รูปขยาย resized ได้ในตัวอย่างด้านล่าง)
>    ขอเพียงคุณมี User_Secret_Key โปรแกรมจะเจนอัตโนมัติ ตอนที่ทำการฝัง meta data ลงไปที่รูป
>    การขยายรูป จะขยายแบบไม่ได้ใช้ AI ดังนั้น ฟรีต้นทุน ไม่ถูกตัดงานวงเงินของ api_key
> 4. การส่งรูปไปถาม keyword จาก AI ทางเราใช้ algorithm ที่ลด prompt ให้มากที่สุด ทำให้ต้นทุนถูกกว่าหลายๆเจ้า แม้คุณจะส่งภาพใหญ่ มาให้โปรแกรมเจนก็ตาม
> 5. สามารถกดปุ่ม save ที่หน้าโปรแกรมได้ เพื่อจะได้ไม่ต้องคอยกรอก api_key ทุกๆครั้งที่ใช้โปรแกรม
> 6. ทดลองใช้งานได้ 5 รูป 10 รูปแรกของแต่ละ folder **ฟรี** ถ้ารันมากกว่า 50 รูปขึ้นไป
> 7. สามารถใส่ input ได้ทั้ง PNG และ JPG ไฟล์
> 8. เสีย API cost แค่ 0.02 บาทต่อรูป (gpt-4o-mini) ถูกที่สุดในตลาดปัจจุบัน
> 9. รันได้ทั้ง Gemini และ OpenAI
> 10. User Friendly ใช้งานง่าย แล้ว เร็ว

### การใช้งาน
1. unzip and install app. สำหรับ MacOS สามารถเปิดตัว DMG แล้วลากลง Application ได้เลย
2. สำหรับ Windows สามารถ unzip และเปิดตัว TumTop.exe ได้เลย
3. ขอ api_key ของ openai มากรอกช่อง API_KEY คุณสามารถ ควบคุม รายจ่ายค่า API ได้ด้วยตัวเอง
    [วิธีขอ API_KEY ภาษาไทย](https://data-espresso.com/%e0%b8%a7%e0%b8%b4%e0%b8%98%e0%b8%b5%e0%b8%81%e0%b8%b2%e0%b8%a3%e0%b8%82%e0%b8%ad-api-key-%e0%b8%88%e0%b8%b2%e0%b8%81-openai/#:~:text=%E0%B9%80%E0%B8%82%E0%B9%89%E0%B8%B2%E0%B8%AA%E0%B8%B9%E0%B9%88%E0%B8%A3%E0%B8%B0%E0%B8%9A%E0%B8%9A%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93%20%E0%B9%80%E0%B8%A1%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93%E0%B9%84%E0%B8%94%E0%B9%89%E0%B8%A3%E0%B8%B1%E0%B8%9A%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%A2%E0%B8%B7%E0%B8%99%E0%B8%A2%E0%B8%B1%E0%B8%99%E0%B9%81%E0%B8%A5%E0%B9%89%E0%B8%A7%20%E0%B8%81%E0%B8%A5%E0%B8%B1%E0%B8%9A%E0%B9%84%E0%B8%9B%E0%B8%97%E0%B8%B5%E0%B9%88%20https%3A%2F%2Fplatform.openai.com%2F%20%E2%80%9CLog%20In%E2%80%9D%20%E0%B8%81%E0%B8%A3%E0%B8%AD%E0%B8%81%E0%B8%8A%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%9C%E0%B8%B9%E0%B9%89%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B8%A3%E0%B8%AB%E0%B8%B1%E0%B8%AA%E0%B8%9C%E0%B9%88%E0%B8%B2%E0%B8%99%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%84%E0%B8%B8%E0%B8%93%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B9%83%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%AA%E0%B8%A1%E0%B8%B1%E0%B8%84%E0%B8%A3%E0%B8%AB%E0%B8%A5%E0%B8%B1%E0%B8%87%E0%B8%88%E0%B8%B2%E0%B8%81%E0%B9%80%E0%B8%82%E0%B9%89%E0%B8%B2%E0%B8%AA%E0%B8%B9%E0%B9%88%E0%B8%A3%E0%B8%B0%E0%B8%9A%E0%B8%9A,%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%A1%E0%B8%B8%E0%B8%A1%E0%B8%82%E0%B8%A7%E0%B8%B2%E0%B8%9A%E0%B8%99%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%AB%E0%B8%99%E0%B9%89%E0%B8%B2%E0%B8%88%E0%B8%AD%20%E0%B8%84%E0%B8%B8%E0%B8%93%E0%B8%88%E0%B8%B0%E0%B9%80%E0%B8%AB%E0%B9%87%E0%B8%99%E0%B9%84%E0%B8%AD%E0%B8%84%E0%B8%AD%E0%B8%99%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%A1%E0%B8%B5%E0%B8%8A%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93%20%E0%B8%84%E0%B8%A5%E0%B8%B4%E0%B8%81%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%99%E0%B8%B1%E0%B9%89%E0%B8%99%E0%B9%80%E0%B8%9E%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B9%80%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B9%80%E0%B8%A1%E0%B8%99%E0%B8%B9%E0%B9%81%E0%B8%9A%E0%B8%9A%E0%B9%80%E0%B8%A5%E0%B8%B7%E0%B9%88%E0%B8%AD%E0%B8%99%E0%B8%A5%E0%B8%87%20%E0%B8%88%E0%B8%B2%E0%B8%81%E0%B8%99%E0%B8%B1%E0%B9%89%E0%B8%99%E0%B8%84%E0%B8%A5%E0%B8%B4%E0%B8%81%20%E2%80%9CView%20API%20keys%E2%80%9D)
   ขอ api_key ของ gemini มากรอกช่อง Gemini API_KEY คุณสามารถ ควบคุมรายจ่ายค่าใช้ API ได้ด้วยตัวเองที่
   [Link ขอ api_key ของ Gemini](https://aistudio.google.com/app/apikey?hl=th )
5. กรอก User Secret Key (ถ้ามี) ถ้าไม่มี สามารถติดต่อ Line ID ด้านล่าง
6. กดปุ่ม Browse เพื่อเปิด Folder ที่มีรูปอยู่ "**เพียงคลิก ที่ไฟล์ใดไฟล์หนึ่งที่อยู่ใน Folder นั้น**" โปรแกรมจะดึงไฟล์รูปทั้งหมดมาดำเนินการอัตโนมัติ
8. เลือก model ของ AI ที่ใช้เจน ปกติคือ 4o-mini จะถุกที่สุด ตกรูปละประมาณ 0.08 บาท (ไม่รวมค่า user_secret_key) หรืออาจจะเลือก 4o ที่แพงขึ้น แต่แลกกับคีย์เวิร์ดดที่น่าจะหาได้และครอบคลุมมากขึ้น ก็ได้
9. กด Run
10. โปรแกรมจะสร้าง Folder  ขึ้นมาใหม่ ข้างใน Folder ที่เลือกจากข้อ 5 ใน Folder นั้น จะมีรูปที่ ฝัง Meta data ให้แล้ว (ถ้ามี User Secret key ในข้อ 4) และมีไฟล์ csv จะถูกสร้างขึ้น อยู่ใน folder นั้นอีกด้วย

### เรทราคา
1. ต้องมี api_key คุณสามารถควบคุม การใช้งานของ api_key ได้ด้วยตนเอง
   จากการทดลอง ถ้าใช้ โมเดล 4o-mini สามารถรันคีย์เวิร์ดได้ถูกกว่า 0.1 บาท ต่อรูป
    แต่ โมเดล 4o นั้นแพงกว่า แต่ก็ได้ คีย์เวิร์ดที่ดีกว่าเช่นกัน 
2. ถ้ามี api_key สามารถใช้โปรแกรมเราได้ โดยจะเจนแค่ csv ให้ และใช้ได้ครั้งละ 5ไฟล์
3. ถ้ามีทั้ง api_key และ user secret key สามารถเจนได้ unlimited ตราบใดที่ api_key และ user_secret_key ยังไม่หมด
   ถ้ามี User Secret key โปรแกรมจะสร้างทั้ง csv และ meta data ลงรูปภาพให้ด้วย ทั้ง 2 ขั้นตอน
   โดยสามารถติดต่อ Line ID ด้านล่าง เพื่อ ซื้อ User Secret Key ได้
    User Secret Key จะคิดราคาที่ 1 บาท ต่อการเจน 10 รูป และสามารถเก็บไว้ใช้คราวหน้าได้ ถ้ายังมีมูลค่าเหลือใน key
4. 10 รูปแรกของ ทุกๆ folder ที่เจน ถ้ารันรอบนั้นๆมากกว่า 50 รูป เราไม่ตัดเงินจาก user_secret_key ถือว่าเป็น bonus แต่ยัง api_key ของ openai คิดเงินปกติ
5. กรณี รูปภาพบางรูป ทาง AI ไม่สามารถคิด keywords ให้ได้ เราจะไม่ตัดเงินจาก user_secret_key ถือว่าโปรแกรมเจนรูปนั้นๆไม่สำเร็จ

### พบเจอบั๊ก
สามารถแจ้งได้ที่ [bugtracker](https://github.com/Pjumpod/TumTop_download/issues) เรามีรางวัลให้ด้วย

# Line ID
Line ID : foolstop หรือ pjumpod 

สามารถ ดาวโหลดโปรแกรมเวอชั่นล่าสุดได้ที่ : [ดูเวอชั่นล่าสุด](https://github.com/Pjumpod/TumTop_download/releases)
### v1.0.1 ####
1. better look for the GUI buttons for MacOSx.
2. fix cannot run the program if "user_secret_key" is missing.
3. show/hide the api_key, author name and secret key button.

### v1.1.1 ####
1. **แก้ algorithm เพื่อให้ราคาของ openai ถูกลงกว่าเวอร์ชั่นก่อนๆ และ เมื่อยิ่งรันภาพมากขึ้นในคราวเดียว ราคาจะยิ่งถูกลง**
2. **สามารถเลือกจำนวน keywords เองได้** 
3. **ลดค่าใช้จ่ายในการให้ Ai ค้นหา Category ให้กับภาพ**
4. **แก้ไขให้สามารถขยายรูปภาพที่เป็นสี่เหลี่ยมจัสตุรัสได้**
5. ปรับ prompt เพื่อลด ERROR จาก AI
6. รูป output สามารถเลือกที่จะเปลี่ยนให้เป็น 300 dpi ได้ (beta function)
7. Input ภาพได้ทั้ง JPG และ PNG
8. ใช้งานใน MacOS ได้แบบไหลลื่นทั้ง Intel chip และ M chip
9. สามารถขยายภาพได้สูงสุดมากถึง 4.5x ถ้าภาพ original มีขนาด 900-3000px โดย output จะได้ไฟล์ขนาด 4500px

### v1.2.0 ####
1. **เพิ่มตัวเลือก Gemini AI** สามารถใช้ทั้ง OPENAI และ GEMINI AI ได้ในแอพเดียว
2. เพิ่มความสามารถในการอ่านชื่อไฟล์ของภาพ(filename) แล้วให้ AI ดึงคำในชื่อไฟล์มาเป็น keywords ได้ (แต่ต้องมีความเกี่ยวข้องกับภาพ)
    เหมาะกับสาย AI มีในชื่อไฟล์ จะมี prompt ติดมาบน ชื่อของไฟล์ภาพด้วย
3. **แก้ไขให้สามารถฝัง metadata ซัพพอร์ตการส่งงานเว็บอื่นๆ** นอกเหนือจาก adobe stock 
      เช่นเว็บ shutterstock, freepik, depositphotos, 123rf, pixta, etc

### v1.2.1 ####
1. **Model ใหม่ของ openai 'chatgpt-4o-latest'** 
2. แก้ปัญหาที่ description ไม่ขึ้นเมื่อในเว็บ depositphoto, 123rf

### v1.2.2 ####
1. แก้เรื่อง Error 429 จาก OPENAI การทำงานจะช้าลงเล็กน้อย แต่ โอกาส Error น้อยลงมาก
2. แก้เรื่อง Error 500 ของ Gemini การทำงานจะช้าลงเล็กน้อย แต่ โอกาส Error น้อยลงมาก
3. เพิ่ม Free Tier mode
สำหรับ User ที่เติมเงินแล้วของ OPENAI แต่ระบบยังไม่เปลี่ยนเลเวลมาอยู่ Tier1
หรือ User Free ของ Gemini สามารถใช้งานได้ โดย limit ที่ จำนวนของการรีเควซไว้
FREE TIER ไม่ได้หมายถึง คนที่ได้เครดิตฟรีจาก Gemini นะครับ <br/>
<b>PS:</b> สำหรับ Free Tier ความเร็วสูงสุดคือ 2 รูปต่อนาที หรือ 1รูปต่อนาทีถ้าเลือก Category ด้วย

### v1.3.0 ###
1. ปรับปรุง algorithm ในการส่งข้อมูลกับ AI ให้ดีขึ้น prompt เดิม แต่ใช้เงินน้อยลง เหลือแค่ 0.02 บาทต่อรูปเท่านั้น (คิดที่ gpt-4o-mini ถูกลงกว่าเวอร์ชั่นก่อนถึง 75%) และไม่มีผลกับคุณภาพคีย์เวิร์ด จะเจอสีม่วงเยอะเหมือนเดิม
  
> สำหรับราคาที่ gpt-4o-mini
> - คนมี USK ราคารวม USK ต่อรูป จะอยู่ที่ ** 0.1 + 0.02 = **<span style="color:green">0.12 บาท</span>**  ต่อ 1 รูป (USK + API)
> - คนที่ไม่มี USK (ทดลองใช้) **จะใช้ algorithm ส่งข้อมูลแบบเก่า** ราคาต่อรูปอยู่ที่ **<span style="color:red">0.21 บาท</span>** ต่อ 1 รูป

2. เพิ่มเมนูสำหรับ แตกคีย์เวิร์ด
3. เพิ่มเมนูสำหรับผู้ที่ต้องการ title ไม่เกิน 100 ตัวอักษร (สำหรับบางเวปเช่น Freepik)
4. เพิ่มเมนูให้สามารถเลือกได้ว่าจะไม่เอา "-" ใน keywords (สำหรับบางเวปเช่น Vecteezy)
5. แก้เรื่อง Error 429 บน openai และ 500 บน Gemini
6. New model ของ Gemini "gemini-flash-exp-0827", "gemini-pro-exp-0827" และ "gemini-flash-8b-exp-0827"
7. อัพเป็น 300DPI สำเร็จมากขึ้น
8. เปลี่ยนการแสดงสถานะการทำงานเป็นแบบ progress bar.
9. เพิ่ม Support metadata สำหรับเวป Vecteezy
10. เพิ่มประสิทธิภาพทั่วๆไปของโปรแกรม
11. เพิ่มคำอธิบายส่วนต่างๆของโปรแกรมเป็นภาษาไทยเมื่อเอา mouse ไปชี้ (Tool Tip)
