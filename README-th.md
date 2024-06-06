## นำรูปจากกล้อง Esp32-S3 ขึ้นบนจอ TFT
 [For English version](https://github.com/San279/Esp32-camera-to-tft)
 <br/>
 <br/>
 โปรเจ็คนี้ถูกออกแบบมาใช้กับ [FOMO](https://docs.edgeimpulse.com/docs/edge-impulse-studio/learning-blocks/object-detection/fomo-object-detection-for-constrained-devices) AI ตรวจจับวัตถุ ในส่วนของการเซ็ทอัพจอ TFT กับกล้อง AIoT บอร์ด หรือ Esp32
<br/>
## สิงที่ต้องมี
 - [AIoT](https://wirelesssolution.asia/) บอร์ด Esp32-S3 หรือ Esp32 ที่มี PSRAM
 - กล้อง OV 2640
 - ST7789 หรือ จอ TFT แบบไหนก้ได้ <br/> <br/>
 - [Arduino IDE](https://www.arduino.cc/en/software) อันเก่าหรือใหม่ก้ได้
   รูปแผงวงจรของกล้องกับจอ TFT ใน AIot บอร์ด <br/> <br/>
  ![alt_text](/images-for-readme/pinout.PNG)
## โครงสร้าง
 - camera-to-tft - ในแฟ้มมี c++ โค้ดสำหรับ Arduino เพื่อแสดงรูปภาพขึ้นบนหน้าจอ TFT.
 - User_Setup.h - เฮเด้อไฟล์สำหรับ c++ นำไฟล์นี่ไปใส่ใน TFT_eSPI ไลบรารี่.  <br/> <br/>
## วิธีรันโปรเจ็ค
<strong> 1. ดาวน์โหลดไลบราลี่เป็น zip และแตกไฟล์ในแฟ้ม Arduino. </strong>
<br /><br />
![alt_text](/images-for-readme/download_directory.PNG)
<br /><br /><br /><br />
<strong> 2. เปิดไฟล์ camera-to-tft.ino Arduino ในแฟ้มที่พึ่งแยกออก และในช่องด้ายซ้านมือให้กดไปที่ library และค้นหา TFT_eSPI เพื่อกดโหลดไลบรารี่นั้น</strong>
<br /><br />
![alt_text](/images-for-readme/library_manager.PNG)
<br /><br /><br /><br />
<strong> 3. หลังจากโหลด TFT_eSPI เสร็จแล้ว นำไฟล์ User_Setup.h ไปใว้แทนในแฟ้ม TFT_eSPI </strong> 
 - จากแฟ้ม Arduino ให้ไปที่ library และ กดเข้าไปใน TFT_eSPI และนำไฟล์ User_Setup.h มาใว้แทนไฟล์ของเดิมในไลบรารี่นี้
<br/><br/>
![alt_text](/images-for-readme/replace.PNG)
<strong> 4. กดไปที่ tools ตรงตัวเลือกด้านบนและเปลี่ยน Board เป็น "ESP32S3 Dev Module" และเปลี่ยน PSRAM เป็น "OPI PSRAM".  </strong>
<br /><br />
![alt_text](/images-for-readme/library_manager.PNG)
<br /><br /><br /><br />
<strong> 5. อัพโหลดโค้ดขึ้นบน ESP32-S3 เพียงแค่นี่เราสามารถเห็นรูปจากกล้องบนจอ TFT.  </strong> <br/> <br/>
![alt_text](/images-for-readme/AIOT.PNG)
<br /><br /><br /><br />
## เครดิต
ต้องขอขอบคุณ [WIRELESS SOLUTION ASIA CO.,LTD](https://wirelesssolution.asia/) สำหรับการสนับสนุนโปรเจ็คนี้ และ [Bodmer / TFT_eSPI](https://github.com/Bodmer/TFT_eSPI/blob/master/README.md)
สำหรับโค้ดส่วนจอ TFT