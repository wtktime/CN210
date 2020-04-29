#Linkความรู้ต่างๆ

- คลิปที่ 1
เป็นคลิปที่อธิบายคำสั่ง Jump ในภาษา MIPS(million instructions per second)
  ปกติการทำงานของโปรแกรมจะทำงานตามเรียงลำดับคำสั่งจนจบโปรแกรม ในบางกรณี อาจะมีความต้องการให้โปรแกรมกระโดดข้ามบางบรรทัดคำสั่ง หรือให้ย้อนกลับไปทำบางคำสั่งซ้ำใหม่ในลักษณะวนรอบ คำสั่งกระโดดจึงเป็นคำสั่งที่สั่งให้หน่วยประมวลผลกระโดดไปทำงานที่ตำแหน่งอื่นๆ รูปแบบทั่วไปของคำสั่งกระโดด

-https://youtu.be/0736qy-U0ZM
- คลิปที่ 2
เป็นคลิปยกตัวอย่างการทำงานของ CPU ในภาษา MIPS(million instructions per second)
  หน่วยประมวลผลกลางหรือ CPU นั้น เป็นศูนย์กลางในการทำงานของระบบคอมพิวเตอร์ ทุกสิ่งที่กล่าวถึงในสถาปัตยกรรมชุดคำสั่งนั้น หน่วยประมวลผลกลางจะต้องมีความสามารถทำงานได้ตามที่ระบุไว้ หากเปรียบเทียบร่างกายเราอาจกล่าวได้ว่าหน่วยประมวลผลกลางเป็นสมองมนุษย์เรา ทั้งนี้ภายในหน่ววยประมวลผลกลางจะประกอบไปด้วย 
-หน่วยประมวลผลทางคณิตศาสตร์และทางตรรกะ(ALU)
-หน่วยควบคุม(Control Unit)
-หน่วยความจำชั่วคราว(Register)


-https://youtu.be/8yq_oa1HVa0
- คลิปที่ 3
เป็นคลิปอธิบายความแตกต่างระหว่าง Single Cycle กับ Multi Cycle
  Single Cycle จะทำงานจบภายใน CyCle เดียว ส่วน Multi Cycle จะทำงานจบในหลาย CyCle
  Single Cycle มี ALU ได้หลายตัว ส่วน Multi CyCle จะมี ALU เพียงตัวเดียว
  Single Cycle มี Memmoryตัวเดียว เป็นแบบ Harvard Architecture ส่วน MultiCycle มี Memmoryหลายตัวเป็นแบบ Von Numen 

-https://www.youtube.com/watch?v=FVBvfoPVggo&feature=share
- คลิปที่ 4
เป็นคลิปอธิบายคำสั่ง lw(load word)

![รูปที่1](lwCN210.gif)

ขั้นตอนการทำงานของLoad word ( lw rt,offset(rs) )
1. คำสั่งจะถูกFetch จาก Memory และ จะเพิ่มค่าPC (program counter) เพื่อไปชี้
Address ถัดไปของคำสั่งถัดไป
2. อ่านค่า register (rs)
3. ALU จะคำนวณหาผลรวมของค่าRegister ที่อ่านได้กับค่าOffset
(16 bits จึงต้องทำให้เป็น32 bits)
4. ผลลัพธ์จากALU จะใช้เป็น Addressสำหรับ Data Memory
5. data จาก Memory unit จะถูกเขียนลงในRegister ปลายทาง (rt)

-https://www.youtube.com/watch?v=Wrj4nHQCamU&feature=share
- คลิปที่ 5
เป็นคลิปอธิบายคำสั่ง beq(branch equal)

-https://youtu.be/X2lB1ZSHdHE
- คลิปที่ 6
เป็นคลิปอธิบาย R type
พวก R-type Instruction, จะทำการอ่าน2 Register นำมาทำ ALU Operationแล้วเก็บค่าที่ได้ใน
Register 
ขั้นตอนการทำงานของR-Type Instruction Set
1. คำสั่งจะถูกFetch จาก Memory และ จะเพิ่มค่าPC (program counter) เพื่อไปชี้
Address ถัดไปของคำสั่งถัดไป
2. Register 2 ตัว จะถูกอ่าน, ตัว Main Control Unit จะ set controlline
3. ALU operate data ที่เข้ามาโดยใช้ Function Code(bits 5-0) ของคำสั่งในการเลือกใช้ALU Function
4. เขียนผลลัพธ์ที่ได้ลงในRegister (bits 15-11)
-https://youtu.be/MKwHdwCq7HY
- คลิปที่ 7
เป็นคลิปอธิบาย Pipelining

-https://youtu.be/x1Z5_TWaLLM
