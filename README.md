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
| MP4 | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลง VDO ได้</span> |
| MOV | <span style="color:green">รองรับ</span>  |  <span style="color:green">ฝัง metadata ลง VDO ได้</span> |
| MPG | <span style="color:green">รองรับ</span>  |  - |
| AVI | <span style="color:green">รองรับ</span>  |  - |
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
### การตั้งค่า ###
1. จำเป็นต้องตั้งค่า ในครั้งแรกของการใช้งาน สิ่งที่ต้องเตรียมคือ API KEY และ User Secret Key (USK)
2. API Key เลือกมาอย่างน้อย 1 เจ้า เมื่อคุณมี API KEY ของผู้ให้บริการ AI เจ้าไหน คุณสามารถใช้งาน model ของ ผู้ให้บริการเจ้านั้นๆได้
   ขอ api_key ของ openai มากรอกช่อง API_KEY <br>
    [วิธีขอ API_KEY ภาษาไทย](https://th.extendoffice.com/documents/excel/7435-get-openai-api-key.html) <br>
   ขอ api_key ของ gemini มากรอกช่อง Gemini API_KEY <br>
   [Link ขอ api_key ของ Gemini](https://aistudio.google.com/app/apikey?hl=th ) <br>
   ขอ api_key ของ claude มากรอกช่อง Claude API_KEY <br>
   [Link ขอ api_key ของ Claude ภาษาไทย](https://data-espresso.com/claude-ai-api-guide-for-beginners/)<br>
3. กรอก User Secret Key (ถ้ามี) ถ้าไม่มี สามารถติดต่อ Line ID ด้านล่าง
4. กดปุ่ม SAVE เพื่อให้โปรแกรม จำการตั้งค่าไว้
5. หลังกดปุ่ม SAVE ทุกครั้งที่โปรแกรมปิดแล้วเปิดขึ้นมาใหม่ จะเรียกการตั้งค่าล่าสุดมาใช้
6. คุณสามารเปลี่ยนแปลง API KEY หรือ USK ภายหลังได้ตลอดเวลา
### การใช้งานเบื้องต้น ###
1. กดปุ่ม Browse เพื่อเปิด Folder ที่มีรูปอยู่ "**เพียงคลิก ที่ไฟล์ใดไฟล์หนึ่งที่อยู่ใน Folder นั้น**" โปรแกรมจะดึงไฟล์รูปทั้งหมดมาดำเนินการอัตโนมัติ
2. เลือก model ของ AI ที่ใช้เจน โดยค่าย openai จะมี 4o-mini ถูกที่สุด ตกรูปละประมาณ 0.015-0.02 บาท (ไม่รวมค่า user_secret_key) หรืออาจจะเลือก 4o ที่แพงขึ้น แต่แลกกับคีย์เวิร์ดดที่น่าจะหาได้และครอบคลุมมากขึ้น ก็ได้
3. กด Run
4. โปรแกรมจะสร้าง Folder  ขึ้นมาใหม่ ข้างใน Folder ที่เลือกจากข้อ 5 ใน Folder นั้น จะมีรูปที่ ฝัง Meta data ให้แล้ว (ถ้ามี User Secret key ในข้อ 4) และมีไฟล์ csv จะถูกสร้างขึ้น อยู่ใน folder นั้นอีกด้วย

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
- ไฟล์ png ถ้าเป็น png ที่ต้องการแปลงเป็น jpeg ก็จะแปลงให้อัตโนมัติและถ้าไฟล์ png ที่เป็นฉากหลังใส หรืองาน di cut โปรแกรมก็จะฝังคีย์ให้ในภาพ png ได้เลยโดยไม่แปลงเป็น JPG ครับ
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
- Line ID : @tumtop
---
### ช่องทางการติดต่อ ###
- [Facebook Fan page](https://www.facebook.com/tumtopapp) <br>
- [Notion](https://fan-bank-49f.notion.site/TumTop-19248f4e66e58129ac76de3dc7ca07da)

---
# Release #
- สามารถ ดาวโหลดโปรแกรมเวอชั่นล่าสุดได้ที่ : [ดูเวอชั่นล่าสุด](https://github.com/Pjumpod/TumTop_download/releases)
  
---

### [V5.2.0](https://github.com/Pjumpod/TumTop_download/releases/tag/5.2.0) ###
<ol>
<li>สร้าง csv ของ envato</li>
<li>เพิ่ม model ใหม่ GPT-5.2 จาก openai</li>
<li>เพิ่ม model ใหม่ gemini-3-flash จาก Gemini</li>
<li>แก้ปัญหาที่เจอบน GPT-5.1</li>
<li>ฟังชั่น gen รูปด้วย OPENAI อัพเกรด model ไปใช้ gpt-image-1.5</li>
<li>เพิ่มให้โปรแกรมรู้จัก ERROR MESSAGE ใหม่ๆของ Gemini โดยเฉพาะที่เกี่ยวกับ RPD </li>
<li>เพิ่มความเร็วในการเปิดโปรแกรม</li>
<li>จัดหมวดหมู่ folder ของ CSV ให้เป็นระเบียบมากขึ้น</li>
<li>อัพเดต Tool Tip ช่องของการเลือก AI model</li>
<li>เปลี่ยน default model เมื่อ usk หมด จาก gpt-4o เป็น gpt-4.1</li>
</ol>

---

### [V5.1.1](https://github.com/Pjumpod/TumTop_download/releases/tag/5.1.1) ###
<ol>
<li>สร้าง csv ของ istock</li>
<li>เพิ่ม model ใหม่ GPT 5.1 และ GPT 5.1 TumTop</li>
<li>เพิ่ม model ใหม่ Gemini 3.0 pro และ Gemini 3.0 TumTop</li>
<li>เพิ่ม model ใหม่ Claude Opus 4.5</li>
<li>ปรับปรุง Title/Keyword ให้มีผลลัพท์ที่ดียิ่งขึ้น</li>
<li>เปลี่ยน link ของ Gemini ที่เข้าไปเช็ค TIER & Rate Limit</li>
<li>ลบ model เก่าๆ ของ Gemini 
<ul>gemini-2.0-flash-thinking-exp-01-21</ul><ul>gemini-2.0-flash-lite-001</ul><ul>gemini-2.0-flash-lite-preview-02-05</ul></li>
<li>เพิ่มให้โปรแกรมรู้จัก ERROR MESSAGE ใหม่ๆของ Gemini โดยเฉพาะที่เกี่ยวกับ RPD </li>
</ol>

---

### [V5.1.0](https://github.com/Pjumpod/TumTop_download/releases/tag/5.1.0) ###
<ol>
<li>แก้ปัญหารันไม่ได้เนื่องจาก Security Upgrade</li>
<li>สร้าง VDO จาก prompt ด้วย VEO3.1 จาก Gemini API </li>
</ol>

---

### [V5.0.2](https://github.com/Pjumpod/TumTop_download/releases/tag/5.0.2) ###
<ol>
<li>เพิ่ม Claude Sonnet 4.5</li>
<li>เพิ่ม Gemini 2.5 Flash preview และ Flash-Lite preview 09-2025</li>
<li>ลบ Claude Sonnet 3.5 ออก</li>
<li>ลบ Gemini 1.5 ออก</li>
<li>สร้าง csv ของ 123rf</li>
<li>ปรับปรุง Title/Keyword ให้มีผลลัพท์ที่ดียิ่งขึ้น</li>
</ol>

---

### [V5.0.1](https://github.com/Pjumpod/TumTop_download/releases/tag/5.0.1) ###
<ol>
<li>เจอว่า VDO จากบางแอพไม่สามารถแก้ไข title/keyword แบบ manual ผ่านหน้าต่าง live ได้ <ul><li>ปรับปรุงโปรแกรมให้สามารถแก้ไขด้วยมือผ่านหน้าต่าง live ได้</li></ul></li>
<li>ปรับปรุงการฝัง metadata ลงบน VDO ไฟล์ให้ดีขึ้นกว่าเดิม</li>
<li>เพิ่ม Error code ใหม่ๆของ Gemini</li>
</ol>

---

### [V5.0.0](https://github.com/Pjumpod/TumTop_download/releases/tag/5.0.0) ###

<ol>
<li>เพิ่ม model ใหม่ของ OpenAI<ul><li>gpt-5</li><li>gpt-5-mini</li></ul><mark>GPT-5 คือ reasoning model ที่ราคาถูก แต่อย่างไรก็ตาม ราคาจะแพงกว่า gpt-4.1 เล็กน้อย แต่ถูกกว่า ตระกูล O ทั้งหลาย</mark></li>
<li>ลบ model ของ OpenAI ที่ใช้งานไม่ได้แล้ว<ul><li>gpt-4.5-preview</li></ul></li>
<li>เพิ่ม model ใหม่ของ Gemini <ul><li>gemini-2.5-flash-lite-preview-06-17</li><li>gemini-2.5-flash-lite</li></ul></li>
<li>เพิ่มฟังชั่นการตรวจสอบตัวสะกด</li>
<li>โปรแกรมจะจำ AI ที่ใช้งานรอบล่าสุด และ ตั้งค่าอัตโนมัตเป็น AI ตัวนั้น ในการเปิดโปรแกรมรอบถัดไป</li>
<li>เพิ่มฟังชั่นใหม่ ปุ่ม "Runway Gen" สำหรับเจนภาพจาก Runway API</li>
<li>เพิ่มปุ่มให้สามารถส่งผ่าน prompt ที่ได้จาก genPrompt ทั้งหมดไปที่ Runway Gen</li>
<li>เพิ่ม Theme สำหรับ Windows<ul><li>DarkGlass</li><li>LightGlass</li><li>SunGlass</li></ul></li>
<li>เพิ่ม style ใหม่ evening light ลงใน ReCraft Gen</li>
<li>เปลี่ยนแปลงวิธีการแจ้งเตือน เมื่อมี version ใหม่</li>
<li>แก้ปัญหา Runway gen VDO แล้วเจอ ERR 400 (เกิดจาก backend ของ Runway เอง มีการเปลี่ยนแปลง)</li>
</ol>

---

### [V4.4.1](https://github.com/Pjumpod/TumTop_download/releases/tag/4.4.1) ###

<ol>
<li>เพิ่มแนวทางป้องกันปัญหา ที่อาจจะเกิดได้เวลา openai server overload</li>
<li>ฟังชั่น VDO Gen ของเรา สามารถใส่พร้อมพ์ได้แล้ว เราสามารถสร้าง VDO โดยใช้รูปอย่างเดียว หรือ รูป+พร้อมพ์ก็ได้</li>
<li>เพิ่มลิ้ง เช็คสถานะ ของ Gemini API server</li>
<li>ปรับปรุงคุณภาพของ title/keyword</li>
<li>แก้ไขปัญหา ที่ openai ชอบค้าง</li>
<li>ปรับปรุง UI เล็กน้อย</li>
<li>เพิ่ม Theme ใหม่<ul><li>Chocolate</li><li>Forest</li><li>Lime</li><li>Yogurt</li></ul>
</ol>

---

### [V4.3.2](https://github.com/Pjumpod/TumTop_download/releases/tag/4.3.2) ###

<ol>
<li>Gemini 2.5 official model release ทั้ง flash และ pro</li>
<li>ปรับปรุง Title/Keyword ให้ดียิ่งขึ้น</li>
<li>เพิ่มการนับตัวอักษรในฟังชั่น key concept <ul><li>คำแนะนำ: เพื่อให้ title ที่ได้สวยงาม ควรตั้ง Title ให้ยาวกว่า key concept อย่างน้อยๆ 2 เท่า</li></ul></li>
<li>เพิ่ม checkbox สำหรับทำให้ title และ description ไม่เหมือนกัน</li>
</ol>

---

### [V4.3.1](https://github.com/Pjumpod/TumTop_download/releases/tag/4.3.1) ###

<ol>
<li>แก้ไข error message เมื่อ api key ผิด</li>
</ol>

---

### [V4.3.0](https://github.com/Pjumpod/TumTop_download/releases/tag/4.3.0) ###
<ol>
<li>เพิ่ม Gemini โมเดล<ul><li>Gemini 2.5 flash thinking</li><li>Gemini 2.5 flash 05-20</li><li>Gemini 2.5 pro 06-05</li></ul></li>
<li>เพิ่ม Claude โมเดล <ul><li>Claude Opus 4</li><li>Claude Sonnet 4</li></ul></li>
<li>ลดค่าใช้จ่าย API ให้น้อยลง ในการคิด category</li>
<li>ปรับปรุง Title/Keyword ให้ดียิ่งขึ้น</li>
</ol>

---

### [V4.2.0](https://github.com/Pjumpod/TumTop_download/releases/tag/4.2.0) ###
<ol>
<li>Auto gen image ด้วย OpenAI. (เจน PNG แบบ auto!!)</li>
<li>Theme ใหม่ Cosmo, White, Viper และ SuperHero.</li>
<li>แก้ปัญหา title เพี้ยน ที่ Vecteezy</li>
<li>Model ใหม่จาก Gemini "gemini-2.5-pro-preview-05-06"</li>
</ol>

---

### [v4.1.0](https://github.com/Pjumpod/TumTop_download/releases/tag/4.1.0) ###
<ol>
<li>ปรับปรุง คุณภาพ ของ title, description และ keywords ให้ดีขึ้น</li>
<li>แก้ปัญหาที่ฝัง metadata ของ mp4 จากกล้องบางรุ่นไม่ได้</li>
<li>MJ version 7 ใน genprompt.</li>
<li>Gemini โมเดลใหม่</li>
<ul>
<li>Gemini-2.5-pro-preview-03-25</li>
<li>Gemini-2.5-flash-preview-04-17</li>
</ul>
<li>OpenAI โมเดลใหม่</li>
<ul>
<li>GPT-4.1</li>
<li>GPT-4.1-nano</li>
<li>GPT-4.1-mini</li>
<li>o4-mini</li>
</ul>
<li>Auto Gen VDO โดยใช้ รูปภาพ (Image to VDO) ด้วย model "Runway Gen4 turbo"</li>
<li>เอา model ที่ outdated แล้วทั้งของ Openai และ Gemini ออก</li>
<li>แก้ปัญหาปุ่มลูกศรขึ้นลง เวลา review รูป หลังเจน metadata</li>
</ol>

---

### [v3.1.2](https://github.com/Pjumpod/TumTop_download/releases/tag/3.1.2) ###
<ol>
<li>ปรับปรุง คุณภาพ ของ description และ keywords ให้ดีขึ้น</li>
<li>เพิ่ม screening message เพื่อรองรับ openai หลังอัพเดต</li>
<li>ปรับปรุง GUI เล็กน้อย ในส่วนของ progress bar</li>
<li>Prompt helper สำหรับเจน Text to VDO (BETA)</li>
<li>Gemini โมเดลใหม่ gemini-2.5-pro-exp-03-25</li>
</ol>

---

### [v3.1.1](https://github.com/Pjumpod/TumTop_download/releases/tag/3.1.1) ###
<ol>
<li>เพิ่ม model ใน Claude</li>
<ul>
<li>claude-3-5-haiku-20241022</li>
</ul>
<li>แก้บั๊กที่เมื่อใช้ model gpt-4o-mini แล้วมีโอกาสที่จะมี , คั่นระหว่างคำ ใน title ของรูปบางรูป</li>
<li>ปรับปรุง title ที่ได้ให้ตัดจบประโยคได้สวยงามมากขึ้น</li>
</ol>

---
### [v3.1.0](https://github.com/Pjumpod/TumTop_download/releases/tag/3.1.0) ###
<ol>
<li> แก้ปัญหาใน live function ที่ไฟล์ SVG สามารถดูได้แค่ครั้งเดียว</li>
<li>ฟังชั่นใหม่ Key Concept</li>
<li>เลือกฝัง metadata บน VDO แบบเลือก on/off ได้ สำหรับนามสกุล MOV/MP4 <br> * เทสด้วยไฟล์ ProRess422 ไฟล์ละประมาณ 1 gb 10 ไฟล์ รวม 10 gb ใช้เวลาประมาณ 59 วินาที <br> **ขึ้นอยู่กับความไวของ hdd และ ssd ของคอมพิวเตอร์ด้วย ถ้า HDD M2 หรือ SSD ก็จะไวกว่า SATA และ แบบเก่า</li>
<li>เพิ่ม model ใน openai (ข้อควรระวัง แพงมาก เหมาะกับผู้ที่ต้องการความ Luxury.) </li>
<ul>
<li>o1</li>
<li>o1-2024-12-17</li>
<li>gpt-4.5-preview</li>
<li>gpt-4.5-preview-2025-02-27</li>
</ul>
<li>เพิ่ม model ใน gemini</li>
<ul>
<li>gemini-2.0-flash-lite-001</li>
<li>gemini-2.0-pro-exp</li>
<li>gemini-2.0-flash-thinking-exp-01-21</li>
<li>gemini-2.0-flash-thinking-exp</li>
</ul>
</ol>

---

### [v3.0.0](https://github.com/Pjumpod/TumTop_download/releases/tag/3.0.0) ###
1. ฟังชั่น Theme โดยตอนนี้มี 6 Themes (Dark, Light, Blue, Valentine, Hacker, AI)
2. model ใหม่ Claude Sonnet 3.7
3. ปรับปรุงประสิทธิภาพ การคิด title/keyword ให้กับ ไฟล์นามสกุล SVG.
4. **AUTO GEN RECRAFT** สามารถ เจนภาพจาก Recraft ได้ เลือกได้ว่าจะเจน photo, illustrator หรือ vector
5. **AUTO GEN RECRAFT** สามารถเลือกได้ตั้งแต่ 1-4 ว่าจะเจนพร้อมพ์ละกี่ภาพ
6. **AUTO GEN RECRAFT** มี style ให้เลือกว่าจะใช้แบบไหนเจน ในเวอชั่นแรกนี้ แอดมิน เอาแค่ที่ แอดมินชอบใช้มาใส่ก่อนนะครับ
7. **AUTO GEN RECRAFT** สามารถเรียก txt หรือ csv ที่ทำพร้อมพ์ไว้สำหรับ MJ ได้เลย
8. **AUTO GEN RECRAFT** สามารถเลือกขนาดรูปได้ โดยจะดู --ar จาก prompt เป็นหลักก่อน ถ้าไม่มี หรือ ratio นั้นๆทาง recraft ไม่ support จะใช้ ขนาดของไฟล์ที่เลือกไว้
9. **AUTO GEN RECRAFT** สามารถโหลด csv/txt หรือ เลือกจากปุ่ม "Gen Recraft" ที่หน้า GenPrompt ได้เลย โดยโปรแกรมจะดึง prompt ที่ได้จาก genPrompt มาไว้ในหน้าของ Auto Gen Recraft ด้วย
10. **AUTO GEN RECRAFT** ตอนนี้ฟรี เสียแค่ค่า API ของ recraft

![image](https://github.com/user-attachments/assets/455d6a24-584e-47da-9c28-0af8e448fea6)

![image](https://github.com/user-attachments/assets/b54be705-6c01-4fc5-b7b5-9e7ffe5d7905)

NOTE: AUTO GEN RECRAFT จะได้ รูปเป็น WEBP กับ SVG
- [WEBP] สามารถ convert เป็น JPG ด้วย GIGAPIXEL ตอนขยายได้ แต่ถ้าลืม หรือทำไม่เป็น 
ทาง TumTop รองรับไฟล์นามสกุล WEBP ด้วยเช่นกัน โดยจะแปลงเป็น JPG ให้ และ ฝัง Metadata ให้อัตโนมัต
- [ SVG] ทาง TumTop รองรับอยู่แล้ว
---
### [v2.3.1](https://github.com/Pjumpod/TumTop_download/releases/tag/2.3.1) ###
<ol>
<li>คำที่อยู่ใน prohibit list ถ้าใส่รูปเอกพจน์มา จะถูกแบนทั้ง เอกพจน์ และ รูปพหูพจน์</li>
<li>Added new Gemini model.</li>
<ul>
 <li>Gemini 2.0 Flash "gemini-2.0-flash-001"</li>
 <li>Gemini 2.0 Flash Lite "gemini-2.0-flash-lite-preview-02-05"</li>
<li>Gemini 2.0 Pro Experiment. "gemini-2.0-pro-exp-02-05"</li>
 </ul>
<li>มีแถบ progress bar แสดง status ตอนรัน keyword analysis.</li>
<li>ในตารางแสดงผลของ keyword analysis ถ้าคลิกเลือกช่อง และ double click จะ copy ข้อมูลของ cell นั้นๆ (ช่องเดียว)</li>
<li>ในตารางแสดงผลของ keyword analysis ถ้าคลิกเลือกหลายๆช่อง และ right click จะ copy ข้อมูลทั้งหมดของทุกช่องที่เลือกไว้ (หลายช่อง)</li>
<li>ในตารางแสดงผลของ keyword analysis เมื่อรันเสร็จ จะเรียงลำดับ จาก น้อยไปมากให้อัตโนมัต</li>
<li>ตำแหน่งแสดง usk คงเหลือ จะแสดงสีได้</li>
<ul>
<li>สีเขียว เมื่อ usk > 500</li>
<li>สีส้ม เมื่อ 500 > usk > 100</li>
<li>สีแดง เมื่อ 100 > usk </li>
</ul>
<li>Keyword Analysis สามารถกดที่ Heading ของตารางเพื่อเรียงค่าได้ตามแถวที่ต้องการได้</li>
<li>เพิ่มลิ้งไป Notion เพื่ออ่านวิธีการใช้งานเบื้องต้น **มีประโยชน์มาก สำหรับผู้เริ่มต้นใช้งาน**</li>
</ol>

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

