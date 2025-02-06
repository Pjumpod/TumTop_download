![image](https://github.com/user-attachments/assets/1e5149d2-ff7d-4d3f-b089-4ad800bce6dd)

### TumTop: เครื่องมือฝัง Metadata สำหรับภาพออนไลน์ ###

> เป็นโปรแกรมที่ออกแบบมาเพื่อฝัง title, description, และ keywords ลงบนภาพถ่ายหรือภาพที่สร้างด้วย AI โดยเฉพาะ เป็นที่นิยมใช้กันในแพลตฟอร์มขายภาพออนไลน์ เช่น Shutterstock และ Adobe Stock รองรับการทำงานได้ทั้งบนระบบปฏิบัติการ Windows และ MacOS ทั้ง Intel chip และ M chip
> 
#### ข้อดี ###
- รองรับ Windows และ MacOS ทั้ง Intel และ M chip
- เลือกใช้ OpenAI, Gemini หรือ Claude ได้
- ควบคุมค่าใช้จ่าย API key เอง
- ขยายภาพได้ถึง 4.5x (900-3000px เป็น 4500px) โดยไม่ใช้ AI
- ฝัง metadata อัตโนมัติด้วย User Secret Key (USK)
- ปรับแต่งจำนวน keywords และความยาว Title ได้
- ค้นหา category อัตโนมัติสำหรับ Adobe Stock และ Shutterstock
- รองรับไฟล์หลายรูปแบบ ดังภาพ
 
| ไฟล์นามสกุล  |   CSV|  METADATA |   
|---|---|---|
| JPG  | <span style="color:green">รองรับ</span>  | <span style="color:green">ฝัง metadata ลงภาพได้</span>|   
|  JPEG | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงภาพได้</span> |   
| PNG | <span style="color:green">รองรับ</span>  | <span style="color:green">ฝัง metadata ลงภาพได้</span> <br/> จำแนกได้ว่ารูปไหนเป็น Background ใส หรือ ไม่<br/> ถ้าเป็นภาพพื้นหลังใส จะเขียน metadata ลงไฟล์ PNG เลย <br/> ถ้าเป็นภาพสีพื้น จะแปลงเป็น JPG ก่อน และเขียน Metadata ลง JPG <br/><br/> ตามกฏการส่งงาน|
|  TIFF | <span style="color:green">รองรับ</span>  |  <span style="color:green">แปลงเป็น JPG และ ฝัง metadata ลง JPG</span> |  
|  WEBP | <span style="color:green">รองรับ</span>  |  <span style="color:green">แปลงเป็น JPG และ ฝัง metadata ลง JPG</span> |  
|  HEIC | <span style="color:green">รองรับ</span>  |  <span style="color:green">แปลงเป็น JPG และ ฝัง metadata ลง JPG</span> |  
| AI| <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงเวคเตอร์ได้</span> |
| SVG | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงเวคเตอร์ได้</span> |
| EPS | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลงเวคเตอร์ได้</span> |
| MP4 | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
| MOV | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
| MPG | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
| AVI | <span style="color:green">รองรับ</span>  |  ไม่รองรับ |
- มีฟังก์ชัน Stop List of Keywords สำหรับคัดกรองคำที่ไม่ต้องการ หรือคำที่ติดลิขสิทธิ์เครื่องหมายการค้า
- มีฟังก์ชัน Title Style สำหรับกำหนดรูปแบบการเพิ่มคำใน Title และ Keywords ของแต่ละภาพ
- มีฟังก์ชัน PromptMJ สำหรับสร้าง Prompt เพื่อนำไปสร้างภาพในเว็บ Midjourney
- มีฟังก์ชัน Keyword Analysis สำหรับวิเคราะห์จำนวนภาพของคู่แข่งจากชุด Keywords ที่ต้องการ เพื่อค้นหาโอกาสทางการตลาด

---
## การติดตั้ง

### **สำหรับ MacOS**

1. โหลดตัว TumTop_Intel_Chip หรือ TumTop_M ตามเครื่องที่ใช้งาน
2. Unzip และเปิดตัว dmg แล้วลากไฟล์ลงไปไว้ในโฟลเดอร์ Application
    
    ![image](https://github.com/user-attachments/assets/bbe4d101-d3da-4e67-8fc4-62ce606da72f)

    
3. ให้เปิดการตั้งค่า Privacy & Security ใน setting
   
   ![image](https://github.com/user-attachments/assets/301adf47-ba14-461f-a3a5-ea439f834859)

4. ทำการเปิดโปรแกรมได้เลย
    
    ![image](https://github.com/user-attachments/assets/a34bb487-231f-477b-b0eb-ecdc04b4a026)


### **สำหรับ Windows**

1. ให้โหลดตัว TumTop_Windows
2. Unzip และรอจนเสร็จสิ้น
3. เปิดตัว TumTop.exe เพื่อรันโปรแกรมได้เลย
   ![image](https://github.com/user-attachments/assets/bc27e6cf-d580-4042-8579-319dcf02ecc4)

4. ถ้าอยากสร้าง Icon ที่หน้า Desktop ให้คลิกขวาแล้วเลือกคำสั่ง create shortcut
---
### การใช้งานเบื้องต้น ###
1. unzip and install app. สำหรับ MacOS สามารถเปิดตัว DMG แล้วลากลง Application ได้เลย
2. สำหรับ Windows สามารถ unzip และเปิดตัว TumTop.exe ได้เลย
3. ขอ api_key ของ openai มากรอกช่อง API_KEY คุณสามารถ ควบคุม รายจ่ายค่า API ได้ด้วยตัวเอง <br>
    [วิธีขอ API_KEY ภาษาไทย](https://th.extendoffice.com/documents/excel/7435-get-openai-api-key.html) <br>
   ขอ api_key ของ gemini มากรอกช่อง Gemini API_KEY คุณสามารถ ควบคุมรายจ่ายค่าใช้ API ได้ด้วยตัวเองที่ <br>
   [Link ขอ api_key ของ Gemini](https://aistudio.google.com/app/apikey?hl=th ) <br>
   ขอ api_key ของ claude มากรอกช่อง Claude API_KEY <br>
   [Link ขอ api_key ของ Claude ภาษาไทย](https://data-espresso.com/claude-ai-api-guide-for-beginners/)<br>
5. กรอก User Secret Key (ถ้ามี) ถ้าไม่มี สามารถติดต่อ Line ID ด้านล่าง
6. กดปุ่ม Browse เพื่อเปิด Folder ที่มีรูปอยู่ "**เพียงคลิก ที่ไฟล์ใดไฟล์หนึ่งที่อยู่ใน Folder นั้น**" โปรแกรมจะดึงไฟล์รูปทั้งหมดมาดำเนินการอัตโนมัติ
8. เลือก model ของ AI ที่ใช้เจน ปกติคือ 4o-mini จะถุกที่สุด ตกรูปละประมาณ 0.08 บาท (ไม่รวมค่า user_secret_key) หรืออาจจะเลือก 4o ที่แพงขึ้น แต่แลกกับคีย์เวิร์ดดที่น่าจะหาได้และครอบคลุมมากขึ้น ก็ได้
9. กด Run
10. โปรแกรมจะสร้าง Folder  ขึ้นมาใหม่ ข้างใน Folder ที่เลือกจากข้อ 5 ใน Folder นั้น จะมีรูปที่ ฝัง Meta data ให้แล้ว (ถ้ามี User Secret key ในข้อ 4) และมีไฟล์ csv จะถูกสร้างขึ้น อยู่ใน folder นั้นอีกด้วย

---
## ค่าใช้จ่ายในการใช้งานโปรแกรมแบ่งเป็น 2 ส่วน

1. ค่า **Api key** จาก AI ค่ายต่างๆ 
    
    > เช่น Api key ของ Open Ai เติมขั้นต่ำ $5 เพื่อเปิดการใช้งาน จะใช้งานได้ราวๆ 8,xxx-1x,xxx ภาพในโมเดล 4o mini ครับ
    > 
2. ค่าบริการ User Secret Key หรือ **USK**
    
    > คุณสามารถระบุได้เลยครับว่าจะซื้อเท่าไรครับ
    ทีมงานคิดที่ 1 บาท ได้จำนวน 10 ไฟล์ ครับ
    สมมุตซื้อ 100 บาท ทีมงานจะให้ **USK** ที่เจนได้ 1000 ไฟล์ครับ
    ถ้าเจนรอบนึงเกิน 50 ไฟล์ ทางเราจะไม่คิด USK 10 ไฟล์แรกครับ ถือว่าเป็นโบนัสให้ลูกค้า
    สามารถเติมได้ไม่มีขั้นต่ำครับ
    >
---
## ต้นทุนการใช้งานโปรแกรม TumTop

- ไฟล์ Photo, .eps และ .svg เสียค่า USK + API key = 0.1 + 0.02 = **0.12** บาทต่อไฟล์ (GPT-4 mini)
- ไฟล์ VDO เสียค่า USK + API key = 0.1 + 0.05 = **0.15** บาทต่อไฟล์ (GPT-4 mini)
- 10 ไฟล์แรกของ ทุกๆ folder ที่เจน ถ้ารันรอบนั้นๆมากกว่า 50 รูป เราไม่ตัดเงินจาก user_secret_key ถือว่าเป็น bonus แต่ยัง api_key ของ openai คิดเงินปกติ
- กรณี รูปภาพบางรูป ทาง AI ไม่สามารถคิด keywords ให้ได้ เราจะไม่ตัดเงินจาก user_secret_key ถือว่าโปรแกรมเจนรูปนั้นๆไม่สำเร็จ
---
## คำแนะนำและเทคนิคในการใช้งานโปรแกรม

- หากภาพถูกปรับขนาดมาจากโปรแกรมอื่นแล้ว โปรแกรมจะไม่เปลี่ยนแปลงขนาดภาพครับ
- หากไม่ได้ปรับขนาดภาพมาก่อน และภาพมีขนาดระหว่าง 900-3000px โปรแกรมจะขยายขนาดให้เป็น 4500px โดยอัตโนมัติครับ อย่างไรก็ตาม คุณภาพอาจไม่เทียบเท่า Topaz Gigapixel ที่ใช้ AI เพราะโปรแกรมของเราเป็นเพียงการขยายพิกเซลเท่านั้น ไม่ได้มีการเพิ่มความคมชัดหรือลดสัญญาณรบกวนในภาพครับ
- การสร้างคีย์เวิร์ดสำหรับไฟล์วิดีโอจะถูกบันทึกเป็นไฟล์ CSV ไว้ในโฟลเดอร์ output สำหรับแนบส่งครับ
- สำหรับไฟล์ .jpeg, .jpg, .png, .eps, .ai และ .svg โปรแกรมจะฝังข้อมูลลงในตัวไฟล์โดยตรงครับ
- ไฟล์ png ถ้าเป็น png ที่ต้องการแปลงเป็น jpeg ก็จะแปลงให้อัตโนมัติและถ้าไฟล์ png ที่เป็นฉากหลังใส หรืองาน di cut โปรแกรมก็จะฝังคีย์ให้ในภาพได้เลยครับ
- โปรแกรมสามารถแยกแยะได้ว่าไฟล์ PNG ใดเป็นภาพธรรมดา และไฟล์ใดเป็นภาพที่มีการตัดฉากหลังมาครับ
- โปรแกรมจะวิเคราะห์และอธิบายจากภาพเป็นหลัก โดยถ้าชื่อไฟล์เกี่ยวข้องกับภาพ จะใช้เป็นลำดับความสำคัญแรกในการค้นหาคีย์เวิร์ด แต่ถ้าชื่อไฟล์ไม่เกี่ยวข้องกับภาพ หรือเป็นเพียงตัวเลข โปรแกรมจะสร้างคีย์เวิร์ดตามหลัก SEO ทั่วไปครับ
- **แนะนำให้รันโปรแกรมของเราเป็นขั้นตอนสุดท้ายครับ เพราะถ้านำไฟล์ไปผ่านโปรแกรมอื่นต่อ metadata อาจถูกเขียนทับได้ครับ**
- คุณสามารถนำเมาส์ไปวางเหนือส่วนต่างๆ ของโปรแกรมเพื่อดูคำอธิบายแบบย่อได้ (Tooltip)
- ฟังชั่น **PromptMJ** ไม่เสียค่า USK แต่จะเสียค่า API key ในจำนวนที่น้อยมาก โดยการตอบกลับประมาณ 1 ล้านคำจาก AI จะมีค่าใช้จ่ายเพียง $0.65
- 10 รูปแรกของแต่ละโฟลเดอร์ที่เจนเนอเรต หากในโฟลเดอร์มีมากกว่า 50 รูป เราจะไม่หักค่า USK ถือเป็นโบนัส แต่ค่า API key ของ OpenAI จะยังคงคิดตามปกติ
- กรณีที่ AI ไม่สามารถสร้าง keywords ให้กับรูปภาพบางรูปได้ เราจะไม่หักค่า USK เนื่องจากถือว่าการเจนเนอเรตรูปนั้นไม่สำเร็จ
---
### พบเจอบั๊ก ###
- สามารถแจ้งได้ที่ [bugtracker](https://github.com/Pjumpod/TumTop_download/issues) เรามีรางวัลให้ด้วย

---
# Line ID #
- Line ID : foolstop หรือ pjumpod 
---
### ช่องทางการติดต่อ ###
- [Facebook Fan page](https://www.facebook.com/tumtopapp) <br>
- [Notion](https://supreme-archer-cdb.notion.site/TumTop-1916ff4a10ff808db65ccefdac2db727)

---
# Release #
- สามารถ ดาวโหลดโปรแกรมเวอชั่นล่าสุดได้ที่ : [ดูเวอชั่นล่าสุด](https://github.com/Pjumpod/TumTop_download/releases)
---
### [v2.3.0](https://github.com/Pjumpod/TumTop_download/releases/tag/2.3.0) ###
1. Keyword Analysis ที่เร็วมาก มีโหมด VIP (unlimited key set) และ free ให้เลือกใช้
2. แก้ไขปัญหา svg ไฟล์ ไม่สามารถรันได้ ซึ่งสาเหตุเกิดจาก การอัพเดต patch ของ os
3. เปลี่ยน Themes ของ Windows
4. เปลี่ยน algorithm ในการจัดการกับ prohibit list
5. รับมือกับสัญลักษณ์ _ จาก AI.
6. รับมือกับสัญลักษณ์ ' ตัวใหม่จาก AI

![KW Analysis](https://github.com/user-attachments/assets/8618536a-bf2c-48c8-b832-f0fe8a1cf4ee)
---
### [v2.2.9](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.9) ###
1. Manage การใช้งาน CPU/RAM ได้ดีขึ้น
2. มี option ให้เลือก ลบไฟล์ต้นฉบับ หลังเจน Title/KW อัตโนมัติ
3. แก้ปัญหาเวลาใช้งาน 2 จอ แล้ว ถอดจอออก ทำให้มีปัญหา
4. แก้บั๊ก Chocolate
5. สามารถใช้ model niji6 ได้ ใน gen prompt.
6. รองรับไฟล์นามสกุล WEBP, TIFF และ HEIC โดยจะแปลงเป็น JPG และเขียน meta ลงไปที่ JPG ไฟล์เลย
---
### [v2.2.8](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.8) ###
1. เพิ่มความสามารถให้โปรแกรมจำ model ล่าสุดที่ใช้งานได้ (จำเมื่อมีการ RUN หรือ GenPrompt)
2. เพิ่มความสามารถให้โปรแกรมจำ ratio ล่าสุดที่ใช้งานได้ (จำเมื่อมีการ GenPrompt)
3. ปรับปรุงแก้ไข เรื่อง csv
4. ลดการใช้ cpu/memory ของเครื่อง เพื่อให้ รัน vdo ได้ดีขึ้น
---
### [v2.2.7](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.7) ###
1. เพิ่มความสามารถให้โปรแกรมจำ ratio ที่เลือกไว้ก่อนกด Gen Prompt รอบล่าสุดได้
2. ปรับปรุงโปรแกรม เรื่อง csv
3. ลดการใช้ cpu/memory ของเครื่อง เพื่อให้ รัน vdo ได้ดีขึ้น
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
### [v2.2.4](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.4) ###
1. แก้ปัญหา csv file
2. OPENAI และ GEMINI สามารถอ่านรูปลายเส้นที่เป็นพื้นหลังใสได้แล้ว!!!
3. ปรับปรุงการสกรีน ตัวอักขระพิเศษใน keyword
---
### [v2.2.3](https://github.com/Pjumpod/TumTop_download/releases/tag/2.2.3) ###
1. ปรับปรุงเพิ่มประสิทธิภาพ เรื่อง การนำ title style มาใส่ใน keyword
2. ปรับปรุงให้รองรับ สามารถแปลงอักขระพิเศษได้มากขึ้น
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
### [v2.1.5](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.5) ###
1. สามารถย่อขยายหน้าจอของโปรแกรมได้
2. โปรแกรมจะจำขนาดและตำแหน่งสุดท้ายไว้ เมื่อเปิดโปรแกรมครั้งถัดไป จะอยู่ที่ตำแหน่ง และขนาดเท่าเดิม
3. แก้ไขปัญหา เวลารันแล้วเกิด Error แต่มีการตัด USK
4. วางลิ้งเรือง TradeMark ของ Adobe ในหน้าโปรแกรม
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
### [v2.1.1](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.1) ###
1. แก้ไขให้ลิ้งจากหน้าโปรแกรมสามารถกลับมากลับมากดได้
2. เพิ่มการเช็คว่าเวอชั่นใหม่มีอะไรเปลี่ยนบ้าง
---
### [v2.1.2](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.2) ###
1. เพิ่มฟังชั่น Multiple --ar สำหรับการเจน prompt MJ
2. เพิ่มความสามารถสำหรับไฟล์ SVG ที่ไม่ได้สร้างจาก Adobe Illustrator
---
### [v2.1.0](https://github.com/Pjumpod/TumTop_download/releases/tag/2.1.0) ###
1. เพิ่ม Support สำหรับ VDO นามสกุล mp4 และ mov
2. เพิ่ม Support สำหรับ Vector นามสกุล ai และฝัง metadata ให้ .ai ได้ด้วย
3. สามารถฝัง metadata ให้ Vector นามสกุล svg ได้แล้ว
4. เพิ่ม Gen Prompt สำหรับ MJ
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
### [v1.3.1 BETA](https://github.com/Pjumpod/TumTop_download/releases/tag/1.3.1) ###
1. แก้ปัญหาจาก AI bug (ไม่ใช่โปรแกรมเราบั๊กนะครับ) เนื่องจาก AI จะมอง รูป png ที่พื้นหลังใส ว่าเป็น black background เจอทั้ง Gemini และ OPENAI แต่โปรแกรมเรารับจบให้ครับ
2. แก้ไขรูปบางรูปถูก Gemini block เพราะเรื่องของ safety rate ให้โปรแกรมช่วยคุยให้ครับ
3. improve โปรแกรมเรื่อง error ต่างๆ ทั้ง gemini และ openai
4. กรณีเกิด ERROR จะมีไฟล์ ERROR.csv อยู่ใน folder Error เพื่อให้ลูกค้าสามารถส่งไฟล์นี้มาให้ Developer ได้เลย (ไม่ต้องค้นหาใน csv)

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

### [v1.2.2](https://github.com/Pjumpod/TumTop_download/releases/tag/1.2.2) ####
1. แก้เรื่อง Error 429 จาก OPENAI การทำงานจะช้าลงเล็กน้อย แต่ โอกาส Error น้อยลงมาก
2. แก้เรื่อง Error 500 ของ Gemini การทำงานจะช้าลงเล็กน้อย แต่ โอกาส Error น้อยลงมาก
3. เพิ่ม Free Tier mode
สำหรับ User ที่เติมเงินแล้วของ OPENAI แต่ระบบยังไม่เปลี่ยนเลเวลมาอยู่ Tier1
หรือ User Free ของ Gemini สามารถใช้งานได้ โดย limit ที่ จำนวนของการรีเควซไว้
FREE TIER ไม่ได้หมายถึง คนที่ได้เครดิตฟรีจาก Gemini นะครับ <br/>
<b>PS:</b> สำหรับ Free Tier ความเร็วสูงสุดคือ 2 รูปต่อนาที หรือ 1รูปต่อนาทีถ้าเลือก Category ด้วย

---
### [v1.2.1](https://github.com/Pjumpod/TumTop_download/releases/tag/1.2.1) ####
1. **Model ใหม่ของ openai 'chatgpt-4o-latest'** 
2. แก้ปัญหาที่ description ไม่ขึ้นเมื่อในเว็บ depositphoto, 123rf

---
### [v1.2.0](https://github.com/Pjumpod/TumTop_download/releases/tag/1.2.0) ####
1. **เพิ่มตัวเลือก Gemini AI** สามารถใช้ทั้ง OPENAI และ GEMINI AI ได้ในแอพเดียว
2. เพิ่มความสามารถในการอ่านชื่อไฟล์ของภาพ(filename) แล้วให้ AI ดึงคำในชื่อไฟล์มาเป็น keywords ได้ (แต่ต้องมีความเกี่ยวข้องกับภาพ)
    เหมาะกับสาย AI มีในชื่อไฟล์ จะมี prompt ติดมาบน ชื่อของไฟล์ภาพด้วย
3. **แก้ไขให้สามารถฝัง metadata ซัพพอร์ตการส่งงานเว็บอื่นๆ** นอกเหนือจาก adobe stock 
      เช่นเว็บ shutterstock, freepik, depositphotos, 123rf, pixta, etc
   
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
### [v1.0.1](https://github.com/Pjumpod/TumTop_download/releases/tag/1.0.1) ####
1. better look for the GUI buttons for MacOSx.
2. fix cannot run the program if "user_secret_key" is missing.
3. show/hide the api_key, author name and secret key button.
   
---

