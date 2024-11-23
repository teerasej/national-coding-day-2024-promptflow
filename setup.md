
# Preparing the computer for Workshop Day

สำหรับพวกเราที่สนใจ session Microsoft Promptflow วันที่ 29 พฤศจิกายน 2024 ครับ



## 1. ติดตั้งโปรแกรม

ติดตั้งโปรแกรมตามรายการนี้

1. [Python 3.11+](https://www.python.org/downloads/)
2. [Anaconda](https://www.anaconda.com/download) 
3. [Visual Studio Code](https://code.visualstudio.com/download)
   1. เสร็จแล้วติดตั้ง Extension ตามนี้
      1. [Python Extension](https://code.visualstudio.com/docs/languages/python) 
      2. [Prompt flow for VSCode](https://marketplace.visualstudio.com/items?itemName=prompt-flow.prompt-flow)

## 2. เตรียม environment สำหรับ workshop

### 2.1 Activate Conda

#### สำหรับคนที่ใช้ bash shell


```bash
conda init bash
```

#### สำหรับคนที่ใช้ zsh shell


```bash
conda init zsh
```

#### สำหรับคนที่ใช้ powershell


```bash
conda init powershell
```

### 2.2 สร้าง conda environment สำหรับใช้ในวันนี้

หลังจากติดตั้ง conda แล้ว ให้เปิด Terminal หรือ command prompt ขึ้นมา เพื่อรันคำสั่งด้านล่าง เพื่อสร้าง environment สำหรับใช้ในวัน workshop 

```bash
conda create --name ncd-promptflow
conda activate ncd-promptflow
```



### 2.3 เลือก activate conda environment

1. เปิดแอพ Visual Studio Code > เปิด Promptflow Activity ทางด้านซ้าย จะสังเกตเห็นว่า dependencies ของ package ยังไม่ถูกติดตั้ง ให้กดเลือก install dependencies

   <img width="508" alt="2024-11-23_20-47-53" src="https://github.com/user-attachments/assets/d025a713-a656-4c2f-a179-14aff01c4aa0">


2. เราจะเห็นหน้าจอสำหรับช่วยติดตั้ง และเช็คความพร้อมของ package ที่จำเป็น ส่วนแรกของเราคือ 
   1. **Python Interpreter** ที่ควรจะแสดงที่อยู่ของ python ที่เราติดตั้งไว้ในเครื่องจากขั้นตอนแรก
   2. กดปุ่ม **Select Python Interpreter** เพื่อไปเลือก python environment ที่เราสร้างไว้ด้วย conda ในขั้นตอนที่ 2.1

   <img width="955" alt="2024-11-23_20-50-40" src="https://github.com/user-attachments/assets/9b6c97f8-53e4-41e4-bfda-56ff7c395b87">

3. ให้ทำการเลือก environment ที่เราสร้างไว้ (สังเกตชื่อ และชื่อกำกับว่าเป็น conda)

   > ไม่จำเป็นต้องมีชื่อ path เพื่อกับในภาพตัวอย่างนะครับ

   <img width="850" alt="2024-11-23_20-59-34" src="https://github.com/user-attachments/assets/1a6c39e0-0997-4b8e-ab01-32773f5335d8">
   
4. รอสักพัก จะเห็นว่าชื่อของ Current Python Interpreter จะเปลี่ยนเป็น environment ที่เราเลือกไว้ (ถ้าไม่เปลี่ยน ให้ลองเปิดและเลือก interpreter ใหม่)

   <img width="863" alt="2024-11-23_20-59-47" src="https://github.com/user-attachments/assets/a08fae27-07b6-4b83-a506-048e0fb8f972">


### 2.4 เริ่มติดตั้ง package และเช็คความพร้อม

1. เลื่อนลงมาด้านล่าง จะเป็นส่วน **Install Status** ที่แสดงรายชื่อ dependencies ที่จำเป็นต่อการทำงานของ promptflow ตอนนี้จะเห็นว่าทุกอันไม่พร้อมใช้งาน เราจะกลับมาที่นี่ทีหลัง

   <img width="870" alt="2024-11-23_21-01-53" src="https://github.com/user-attachments/assets/a30d6c4e-8b6f-4ad1-ab5e-afb7f289d653">

2. เลื่อนลงมาด้านล่างจะเห็น step 1 และ step 2 จุดสำคัญของส่วนนี้คือการรันคำสั่งตามขั้นตอนใน terminal ซึ่งสามารถกดปุ่ม run ตามที่ชี้ลูกศรได้ หรือจะเปิด terminal แล้ว copy คำสั่งไปรันใน terminal เองก็ได้ 

   <img width="696" alt="2024-11-23_22-03-49" src="https://github.com/user-attachments/assets/aaf4247e-0854-4c7b-9c61-3a818cf358c1">


3. เลื่อนขึั้นมาที่ **Install Status** เพื่อกดปุ่ม refresh ของแต่ละ dependencies เพื่อเช็คว่าติดตั้งเรียบร้อยไหม

   <img width="842" alt="2024-11-23_21-02-31" src="https://github.com/user-attachments/assets/7f954ba3-3366-40c1-b8a7-074fd4fe17e0">

#### Note: หากการติดตั้งไม่สมบูรณ์

   สามารถเลื่อนลงมาใน option 2 และกดปุ่มรันคำสั่ง **Install** เพื่อติดตั้ง package ที่ไม่สมบูรณ์ เพื่อทำให้เช็คแล้ว สถานะของ **Install Status** สมบูรณ์

   <img width="816" alt="2024-11-23_21-02-47" src="https://github.com/user-attachments/assets/659cd7fe-f7ad-4cc9-90b2-50778b7f5160">


4. ถ้าติดตั้งสมบูรณ์ จะเห็นว่าทุกอันจะเป็นสีเขียว 

   <img width="847" alt="2024-11-23_21-03-12" src="https://github.com/user-attachments/assets/4e2e9840-e1c9-4466-9bb6-39fea8dd4242">




