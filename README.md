### TumTop โปรแกรม
เป็นโปรแกรม ที่เอาไว้ generate keyword แล้ว เก็บเป็น csv file ให้ และสามารถ เขียนลง meta data ของรูปได้ด้วย  
#### ข้อดี
1. สามารถเลือก model ของ openai เองได้ 
2. คุณเป็นคนคุมค่าใช้จ่ายของ api_key ด้วยตัวเอง
3. สามารถขยายรูปได้ ถ้ารูปต้นทางเจนมาจาก AI (ดูตัวอย่าง รูป original vs รูปขยาย resized ได้ในตัวอย่างด้านล่าง)
    ขอเพียงคุณมี User_Secret_Key โปรแกรมจะเจนอัตโนมัติ ตอนที่ทำการฝัง meta data ลงไปที่รูป
    การขยายรูป จะขยายแบบไม่ได้ใช้ AI ดังนั้น ฟรีต้นทุน ไม่ถูกตัดงานวงเงินของ api_key
4. การส่งรูปไปถาม keyword จาก AI ทางเราใช้ algorithm ที่ทำให้ต้นทุนถูกกว่าหลายๆเจ้า แม้คุณจะส่งภาพใหญ่ มาให้โปรแกรมเจนก็ตาม
  โดยจากการทดลอง คุณเสีย API cost แค่ 0.02 บาทต่อรูปเท่านั้น (gpt-4o-mini) ถูกที่สุดในตลาดปัจจุบัน
5. สามารถกดปุ่ม save ที่หน้าโปรแกรมได้ เพื่อจะได้ไม่ต้องคอยกรอก api_key ทุกๆครั้งที่ใช้โปรแกรม
6. ทดลองใช้งานได้ 5 รูป และ สำหรับผู้มี usk => 10 รูปแรกของแต่ละ folder **ฟรี** ถ้ารันมากกว่า 50 รูปขึ้นไป
7. สามารถใส่ input ได้ทั้ง PNG, JPG, SVG, AI, MP4, MOV ไฟล์  <br>
8. รันได้ทั้ง Gemini และ OpenAI  <br>
9. User Friendly ใช้งานง่าย แล้ว เร็ว  <br>
10. ได้ คีย์เวิร์ดสีม่วงเยอะมาก
11. มี Developer คอยอัพเดต แก้ไข Program อยู่ตลอด
12. คุยปรึกษากันได้ เรามีไลน์กลุ่ม Openchat.

---
### การใช้งาน
1. unzip and install app. สำหรับ MacOS สามารถเปิดตัว DMG แล้วลากลง Application ได้เลย
2. สำหรับ Windows สามารถ unzip และเปิดตัว TumTop.exe ได้เลย
3. ขอ api_key ของ openai มากรอกช่อง API_KEY คุณสามารถ ควบคุม รายจ่ายค่า API ได้ด้วยตัวเอง <br>
    [วิธีขอ API_KEY ภาษาไทย](https://th.extendoffice.com/documents/excel/7435-get-openai-api-key.html) <br>
   ขอ api_key ของ gemini มากรอกช่อง Gemini API_KEY คุณสามารถ ควบคุมรายจ่ายค่าใช้ API ได้ด้วยตัวเองที่ <br>
   [Link ขอ api_key ของ Gemini](https://aistudio.google.com/app/apikey?hl=th )
5. กรอก User Secret Key (ถ้ามี) ถ้าไม่มี สามารถติดต่อ Line ID ด้านล่าง
6. กดปุ่ม Browse เพื่อเปิด Folder ที่มีรูปอยู่ "**เพียงคลิก ที่ไฟล์ใดไฟล์หนึ่งที่อยู่ใน Folder นั้น**" โปรแกรมจะดึงไฟล์รูปทั้งหมดมาดำเนินการอัตโนมัติ
8. เลือก model ของ AI ที่ใช้เจน ปกติคือ 4o-mini จะถุกที่สุด ตกรูปละประมาณ 0.08 บาท (ไม่รวมค่า user_secret_key) หรืออาจจะเลือก 4o ที่แพงขึ้น แต่แลกกับคีย์เวิร์ดดที่น่าจะหาได้และครอบคลุมมากขึ้น ก็ได้
9. กด Run
10. โปรแกรมจะสร้าง Folder  ขึ้นมาใหม่ ข้างใน Folder ที่เลือกจากข้อ 5 ใน Folder นั้น จะมีรูปที่ ฝัง Meta data ให้แล้ว (ถ้ามี User Secret key ในข้อ 4) และมีไฟล์ csv จะถูกสร้างขึ้น อยู่ใน folder นั้นอีกด้วย

---
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

---
### พบเจอบั๊ก
สามารถแจ้งได้ที่ [bugtracker](https://github.com/Pjumpod/TumTop_download/issues) เรามีรางวัลให้ด้วย

---
# Line ID
Line ID : foolstop หรือ pjumpod 

---
สามารถ ดาวโหลดโปรแกรมเวอชั่นล่าสุดได้ที่ : [ดูเวอชั่นล่าสุด](https://github.com/Pjumpod/TumTop_download/releases)
### [v1.0.1](https://github.com/Pjumpod/TumTop_download/releases/tag/1.0.1) ####
1. better look for the GUI buttons for MacOSx.
2. fix cannot run the program if "user_secret_key" is missing.
3. show/hide the api_key, author name and secret key button.
   
---
### [v1.1.1](https://github.com/Pjumpod/TumTop_download/releases/tag/1.1.1) ####
1. **แก้ algorithm เพื่อให้ราคาของ openai ถูกลงกว่าเวอร์ชั่นก่อนๆ และ เมื่อยิ่งรันภาพมากขึ้นในคราวเดียว ราคาจะยิ่งถูกลง**
2. **สามารถเลือกจำนวน keywords เองได้** 
3. **ลดค่าใช้จ่ายในการให้ Ai ค้นหา Category ให้กับภาพ**
4. **แก้ไขให้สามารถขยายรูปภาพที่เป็นสี่เหลี่ยมจัสตุรัสได้**
5. ปรับ prompt เพื่อลด ERROR จาก AI
6. รูป output สามารถเลือกที่จะเปลี่ยนให้เป็น 300 dpi ได้ (beta function)
7. Input ภาพได้ทั้ง JPG และ PNG
8. ใช้งานใน MacOS ได้แบบไหลลื่นทั้ง Intel chip และ M chip
9. สามารถขยายภาพได้สูงสุดมากถึง 4.5x ถ้าภาพ original มีขนาด 900-3000px โดย output จะได้ไฟล์ขนาด 4500px
    
---
### [v1.2.0](https://github.com/Pjumpod/TumTop_download/releases/tag/1.2.0) ####
1. **เพิ่มตัวเลือก Gemini AI** สามารถใช้ทั้ง OPENAI และ GEMINI AI ได้ในแอพเดียว
2. เพิ่มความสามารถในการอ่านชื่อไฟล์ของภาพ(filename) แล้วให้ AI ดึงคำในชื่อไฟล์มาเป็น keywords ได้ (แต่ต้องมีความเกี่ยวข้องกับภาพ)
    เหมาะกับสาย AI มีในชื่อไฟล์ จะมี prompt ติดมาบน ชื่อของไฟล์ภาพด้วย
3. **แก้ไขให้สามารถฝัง metadata ซัพพอร์ตการส่งงานเว็บอื่นๆ** นอกเหนือจาก adobe stock 
      เช่นเว็บ shutterstock, freepik, depositphotos, 123rf, pixta, etc
   
---
### [v1.2.1](https://github.com/Pjumpod/TumTop_download/releases/tag/1.2.1) ####
1. **Model ใหม่ของ openai 'chatgpt-4o-latest'** 
2. แก้ปัญหาที่ description ไม่ขึ้นเมื่อในเว็บ depositphoto, 123rf

---
### [v1.2.2](https://github.com/Pjumpod/TumTop_download/releases/tag/1.2.2) ####
1. แก้เรื่อง Error 429 จาก OPENAI การทำงานจะช้าลงเล็กน้อย แต่ โอกาส Error น้อยลงมาก
2. แก้เรื่อง Error 500 ของ Gemini การทำงานจะช้าลงเล็กน้อย แต่ โอกาส Error น้อยลงมาก
3. เพิ่ม Free Tier mode
สำหรับ User ที่เติมเงินแล้วของ OPENAI แต่ระบบยังไม่เปลี่ยนเลเวลมาอยู่ Tier1
หรือ User Free ของ Gemini สามารถใช้งานได้ โดย limit ที่ จำนวนของการรีเควซไว้
FREE TIER ไม่ได้หมายถึง คนที่ได้เครดิตฟรีจาก Gemini นะครับ <br/>
<b>PS:</b> สำหรับ Free Tier ความเร็วสูงสุดคือ 2 รูปต่อนาที หรือ 1รูปต่อนาทีถ้าเลือก Category ด้วย

---
### [v1.3.0](https://github.com/Pjumpod/TumTop_download/releases/tag/1.3.0) ###
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

---
### [v1.3.1 BETA](https://github.com/Pjumpod/TumTop_download/releases/tag/1.3.1) ###
1. แก้ปัญหาจาก AI bug (ไม่ใช่โปรแกรมเราบั๊กนะครับ) เนื่องจาก AI จะมอง รูป png ที่พื้นหลังใส ว่าเป็น black background เจอทั้ง Gemini และ OPENAI แต่โปรแกรมเรารับจบให้ครับ
2. แก้ไขรูปบางรูปถูก Gemini block เพราะเรื่องของ safety rate ให้โปรแกรมช่วยคุยให้ครับ
3. improve โปรแกรมเรื่อง error ต่างๆ ทั้ง gemini และ openai
4. กรณีเกิด ERROR จะมีไฟล์ ERROR.csv อยู่ใน folder Error เพื่อให้ลูกค้าสามารถส่งไฟล์นี้มาให้ Developer ได้เลย (ไม่ต้องค้นหาใน csv)

---
### [v2.0.0](https://github.com/Pjumpod/TumTop_download/releases/tag/2.0.0) ###
1. ***เพิ่มการเขียน meta ลงบน PNG ไฟล์*** โดยเขียนเฉพาะ เมื่อ PNG เป็นภาพที่พื้นหลังใส (ลบ Background แล้ว) แต่ ถ้า PNG พื้นหลังไม่ใส ยังแปลงเป็น JPG เหมือนเดิม
2. Gen Keyword/ Title/ Description ของ Vector file ได้ (เฉพาะ SVG ใน เวอชั่นนี้)
3. GUI ปรับปรุงใหม่
4. มีปุ่มยกเลิก ระหว่างที่รันได้
5. มีภาพ/title/keyword ให้ดู ระหว่างการรัน
6. ย้อนดูภาพ/title/keyword ได้ หลังรันเสร็จ
7. เพิ่มความแม่นยำ สำหรับ progress bar
8. เพิ่มความไวในการเจนอีกเล็กน้อย
9. เช็คเวอชั่น เมื่อเปิด และ ปิดโปรแกรม
10. เพิ่มลิ้งสำคัญๆ ด้านล่างโปรแกรม เช่นลิ้งขอ API_KEY ของ OPENAI และ GEMINI
---
### [v2.0.1](https://github.com/Pjumpod/TumTop_download/releases/tag/2.0.1) ###
1. เพิ่ม model ใหม่ของ Gemini
    - gemini-1.5-flash-latest
    - gemini-1.5-flash-002 (gemini-1.5-flash-latest จะลิ้งมาที่โมเดลตัวนี้ประมาณ 8 ตุลา)
    - gemini-1.5-flash-001 (gemini-1.5-flash-latest ตอนนี้ยังลิ้งมาที่โมเดลตัวนี้อยู่จนกว่าจะถึง 10 ตุลา และหลังจากนั้น ถ้าอยากใช้ model นี้ สามารถใช้ได้ในโปรแกรม TumTop)
    - gemini-1.5-pro-latest
    - gemini-1.5-pro-002 (gemini-1.5-pro-latest จะลิ้งมาที่โมเดลตัวนี้ประมาณ 8 ตุลา)
    - gemini-1.5-pro-001 (gemini-1.5-pro-latest ตอนนี้ยังลิ้งมาที่โมเดลตัวนี้อยู่จนกว่าจะถึง 10 ตุลา และหลังจากนั้น ถ้าอยากใช้ model นี้ สามารถใช้ได้ในโปรแกรม TumTop)
2. สามารถ แก้ไข Title และ Keyword ของรูปจากโปรแกรมได้เลย โปรแกรมจะแก้ไขทั้ง csv และฝังลงในรูปให้หลังแก้ไข
3. มี function สำหรับ Template Title 
    เช่น ตั้งไว้ว่า "**Vehicle of <AI> at night.**"
    และ Title ที่ได้จาก AI เป็น "**This is a cat**"
    โปรแกรมจะนำ "This is a cat" ไปแทน <AI> ใน template จะได้่ว่า Vehicle of **This is a cat** at night.
4. สามารถตั้ง คำต้องห้ามได้  โดยมีผลทั้ง keywords และ title (ยังเป็น BETA อยู่สำหรับ Title)
5. เพิ่มตัวนับพยัญชนะ ทั้ง Title และ description
6. เพิ่มตัวนับ Keywords
7. ปรับปรุง เพิ่มความเร็วของโปรแกรม.
---
### [v2.1.0](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.0) ###
1. เพิ่ม Support สำหรับ VDO นามสกุล mp4 และ mov
2. เพิ่ม Support สำหรับ Vector นามสกุล ai และฝัง metadata ให้ .ai ได้ด้วย
3. สามารถฝัง metadata ให้ Vector นามสกุล svg ได้แล้ว
4. เพิ่ม Gen Prompt สำหรับ MJ
---
### [v2.1.1](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.1) ###
1. แก้ไขให้ลิ้งจากหน้าโปรแกรมสามารถกลับมากลับมากดได้
2. เพิ่มการเช็คว่าเวอชั่นใหม่มีอะไรเปลี่ยนบ้าง
---
### [v2.1.2](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.2) ###
1. เพิ่มฟังชั่น Multiple --ar สำหรับการเจน prompt MJ
2. เพิ่มความสามารถสำหรับไฟล์ SVG ที่ไม่ได้สร้างจาก Adobe Illustrator
---
### [v2.1.3](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.3) ###
1. แก้ปัญหา Algorithm ใหม่ของ Dreamtime ทำให้ดึง description มาผิดพลาด
2. ปรับความเร็ว free tier ของ gemini หลังจากที่ google ปรับ RPM ของ Free Tier ให้รองรับได้มากขึ้น
3. แก้ไข font ใน prohibit popup และ title style popup.
4. เอา 's ออกจาก keyword ทั้งหมด
5. สามารถเช็ค openai server status ได้จากหน้าแอพ
6. เพิ่มลิ้งไป Claude AI (เตรียมตัวสำหรับเวอชั่นอนาคต 2.2.0)
7. ปรับปรุง prompt ของ openai และ gemini ให้ดีขึ้น
---
### [v2.1.5](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.5) ###
1. สามารถย่อขยายหน้าจอของโปรแกรมได้
2. โปรแกรมจะจำขนาดและตำแหน่งสุดท้ายไว้ เมื่อเปิดโปรแกรมครั้งถัดไป จะอยู่ที่ตำแหน่ง และขนาดเท่าเดิม
3. แก้ไขปัญหา เวลารันแล้วเกิด Error แต่มีการตัด USK
4. วางลิ้งเรือง TradeMark ของ Adobe ในหน้าโปรแกรม
---
### [v2.2.0](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.0) ###
1. สามารถ วิเคราะห์ Title และ Keywords ให้กับภาพเวคเตอร์ นามสกุล EPS ได้แล้ว โดยสามารถฝัง Metadata ได้ด้วย
2. สามารถ วิเคราะห์ Title และ Keywords ให้กับ VDO footage นามสกุล MPG และ AVI ได้แล้ว
3. ลด Token การวิเคราะห์ Title และ Keywords ของ VDO ทุกนามสกุลลงเหลือ 1 token จากเดิม 2 tokens.
4. สามารถคลิกขวาเลือก Select All, Copy, Paste, Cut ได้ บน Windows.
5. จัดเรียงตำแหน่งตัว checkbox ใหม่ เอา category นำไปไว้ด้านบนสุด
6. จัดการ การใช้ memory ให้ดีขึ้น
7. สามารถรันผ่าน External HDD ของ MacOS ได้อย่างไม่มีปัญหา
8. แก้ไขปัญหาของภาพที่ผ่านการ Up DPI มาจากโปรแกรมอื่นๆแล้ว ทำให้ภาพนั้นเวลาเปิดด้วยโปรแกรมทำภาพพวก Photoshop, GIMP จะไม่สามารถแสดงค่า DPI ที่ ถูกต้องได้
9. สามารถใช้ปุ่มลูกศรขึ้นลง บน keyboard เพื่อขึ้นลง ตอนรีวิว รูป/title/description/keyword จากตารางได้
---
### [v2.2.2](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.2) ###
1. เพิ่ม Claude AI เป็น AI ตัวที่ 3 ที่ใช้ใน program ของเราได้ (ก่อนหน้านี้มี 2 ตัวคือ OpenAI และ Gemini)
2. เพิ่ม model "gpt-4o-2024-11-20" ของ OpenAI ซึ่ง OpenAI บอกมาว่า เวอชั่นนี้ การเขียน จะได้สำนวนที่สวยขึ้น (จากที่ทดลอง ก็เห็นอารมณ์ความแตกต่างของ title ที่ได้จาก gpt-4o ตัวปัจจุบันจริงๆ)
3. เพิ่มโมเดล ใหม่จาก GEMINI ดังนี้ Gemini-EXP-1121, GEMINI-EXP-1114 และ LEARN-1.5-PRO
4. สามารถ ดู prompt จากรูป (BETA) อัตโนมัต และนำมาช่วยในการคิด title/keyword ได้ เพื่อให้ได้คำที่ตรงความต้องการของ user ที่สุด
5. ban คำว่า Vector หรือ Vectors ใน รูป jpg และ jpeg (automatic)
6. สามารถระบุจำนวนตัวอักษรของ title ได้หลากหลายขึ้น
7. ฟังชั่น GenPrompt [PromptMJ!] สามารถเลือกจำนวน prompt ที่ต้องการได้หลากหลายมากขึ้น
8. เพิ่มความแตกต่าง ระหว่าง title กับ description สำหรับ user ที่ต้องนำไปส่ง Dreamstime.
9. ปรับปรุงสำหรับฟังชั่น STOP list.
10. ปรับปรุงโปรแกรมให้รองรับ เวลา AI ส่งคำตอบผิดพลาด สำหรับ Error Message ของ AI ในเวอชั่นใหม่ๆ
11. Template ที่ถูกระบุไว้ใน Title Style จะถูกนำมา Damage และเอามาใส่ไว้ใน Keywords ด้วย
12. ใน กรณี เลือก เจนแบบมี category จะได้ csv ทั้ง 2 แบบ คือแบบปกติที่ไม่มี category และแบบมี category.
---
### [v2.2.3](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.3) ###
1. ปรับปรุงเพิ่มประสิทธิภาพ เรื่อง การนำ title style มาใส่ใน keyword
2. ปรับปรุงให้รองรับ สามารถแปลงอักขระพิเศษได้มากขึ้น
---
### [v2.2.4](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.4) ###
1. แก้ปัญหา csv file
2. OPENAI และ GEMINI สามารถอ่านรูปลายเส้นที่เป็นพื้นหลังใสได้แล้ว!!!
3. ปรับปรุงการสกรีน ตัวอักขระพิเศษใน keyword
---
### [v2.2.6](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.6) ###
1. Gemini โมเดลใหม่ Gemini Flash 2.0
2. เพิ่ม Max Prompt ใน Gen Prompt ถึง 120
3. เพิ่มการแตก Title style ไปที่ Keyword ให้กับ VDO
4. สามารถเลือกได้ว่าจะใส่ คำ ที่แตกมาจาก title style มาไว้คำที่เท่าไรของ keyword
5. ปรับปรุงปัญหาที่เกิดขึ้นกับ csv file
6. ลดการใช้ memory ของโปรแกรม
7. ปรับปรุง logfile
8. แก้ปัญหาบางครั้ง เมื่อ gen title/kw แล้วเกิด ERROR ตัวไฟล์ไม่เข้าไปอยู่ใน folder ERROR
9. ถ้าเลือก เจน title/kw แบบมี category จะได้ csv เพิ่มมาอีกไฟล์ เป็น csv ของ shuterstock แบบมี primary category (ss.csv)
---
### [v2.2.7](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.7) ###
1. เพิ่มความสามารถให้โปรแกรมจำ ratio ที่เลือกไว้ก่อนกด Gen Prompt รอบล่าสุดได้
2. ปรับปรุงโปรแกรม เรื่อง csv
3. ลดการใช้ cpu/memory ของเครื่อง เพื่อให้ รัน vdo ได้ดีขึ้น
---
#### ตอนนี้โปรแกรมเรารองรับนามสกุลดังนี้

| ไฟล์นามสกุล  |   CSV|  METADATA |   
|---|---|---|
| JPG  | <span style="color:green">รองรับ</span>  | <span style="color:green">ฝัง metadata ลงภาพได้</span>|   
|  JPEG | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงภาพได้</span> |   
| PNG | <span style="color:green">รองรับ</span>  | <span style="color:green">ฝัง metadata ลงภาพได้</span> <br/> จำแนกได้ว่ารูปไหนเป็น Background ใส หรือ ไม่<br/> ถ้าเป็นภาพพื้นหลังใส จะเขียน metadata ลงไฟล์ PNG เลย <br/> ถ้าเป็นภาพสีพื้น จะแปลงเป็น JPG ก่อน และเขียน Metadata ลง JPG <br/><br/> ตามกฏการส่งงาน|
| AI| <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงเวคเตอร์ได้</span> |
| SVG | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงเวคเตอร์ได้</span> |
| EPS | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงเวคเตอร์ได้</span> |
| MP4 | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
| MOV | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
| MPG | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
| AVI | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
