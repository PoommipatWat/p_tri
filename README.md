# การหา Equations of Motion จาก Lagrangian โดยละเอียด

## Lagrangian ที่กำหนดให้

$$L = \frac{m_1}{2}(R_1^2\dot{\theta}_1^2 - 2r_1R_1\dot{\theta}_1^2\cos(\theta_1) + r_1^2\dot{\theta}_1^2) + \frac{\dot{\theta}_1^2R_1^2m_1}{4} + \frac{R_2^2m_2}{4}(\dot{\theta}_1^2 + 2\dot{\theta}_1\dot{\theta}_2 + \dot{\theta}_2^2)$$

$$+ \frac{m_2}{2}\left[(R_1\dot{\theta}_1 + R_2(\dot{\theta}_2\cos(\theta_1) - \theta_2\dot{\theta}_1\sin(\theta_1) + \dot{\theta}_1\cos(\theta_1)) - r_2(\dot{\theta}_1 + \dot{\theta}_2)\cos(\theta_1 + \theta_2))^2\right.$$

$$\left. + (-R_2(\dot{\theta}_2\sin(\theta_1) + \theta_2\dot{\theta}_1\cos(\theta_1) + \theta_1\sin(\theta_1)) + r_2(\dot{\theta}_1 + \dot{\theta}_2)\sin(\theta_1 + \theta_2))^2\right]$$

$$- gm_1(R_1 - r_1\cos\theta_1) - gm_2(R_1 - r_2\cos(\theta_1 + \theta_2) + R_2\cos\theta_1 - R_2\theta_2\sin\theta_1)$$

## สมการ Euler-Lagrange

เพื่อหาสมการการเคลื่อนที่ เราจะใช้สมการ Euler-Lagrange สำหรับระบบที่มีตัวแปรอิสระ $\theta_1$ และ $\theta_2$:

$$\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{\theta}_i}\right) - \frac{\partial L}{\partial \theta_i} = 0$$

เราจะแยกคำนวณสมการสำหรับ $\theta_1$ และ $\theta_2$ ตามลำดับ

## 1. การหาอนุพันธ์สำหรับตัวแปร $\theta_1$

### 1.1 คำนวณ $\frac{\partial L}{\partial \dot{\theta}_1}$

เพื่อความสะดวกในการคำนวณ เราจะแยกพิจารณาทีละเทอม:

1. เทอมแรก: $\frac{m_1}{2}(R_1^2\dot{\theta}_1^2 - 2r_1R_1\dot{\theta}_1^2\cos(\theta_1) + r_1^2\dot{\theta}_1^2)$
   $$\frac{\partial}{\partial \dot{\theta}_1}\left[\frac{m_1}{2}(R_1^2\dot{\theta}_1^2 - 2r_1R_1\dot{\theta}_1^2\cos(\theta_1) + r_1^2\dot{\theta}_1^2)\right]$$
   $$= m_1(R_1^2\dot{\theta}_1 - 2r_1R_1\dot{\theta}_1\cos(\theta_1) + r_1^2\dot{\theta}_1)$$
   $$= m_1\dot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2)$$

2. เทอมที่สอง: $\frac{\dot{\theta}_1^2R_1^2m_1}{4}$
   $$\frac{\partial}{\partial \dot{\theta}_1}\left[\frac{\dot{\theta}_1^2R_1^2m_1}{4}\right] = \frac{R_1^2m_1\dot{\theta}_1}{2}$$

3. เทอมที่สาม: $\frac{R_2^2m_2}{4}(\dot{\theta}_1^2 + 2\dot{\theta}_1\dot{\theta}_2 + \dot{\theta}_2^2)$
   $$\frac{\partial}{\partial \dot{\theta}_1}\left[\frac{R_2^2m_2}{4}(\dot{\theta}_1^2 + 2\dot{\theta}_1\dot{\theta}_2 + \dot{\theta}_2^2)\right]$$
   $$= \frac{R_2^2m_2}{4}(2\dot{\theta}_1 + 2\dot{\theta}_2)$$
   $$= \frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)$$

4. สำหรับเทอมที่สี่ เรากำหนดให้:
   $$X = R_1\dot{\theta}_1 + R_2(\dot{\theta}_2\cos(\theta_1) - \theta_2\dot{\theta}_1\sin(\theta_1) + \dot{\theta}_1\cos(\theta_1)) - r_2(\dot{\theta}_1 + \dot{\theta}_2)\cos(\theta_1 + \theta_2)$$
   
   ดังนั้น:
   $$\frac{\partial X}{\partial \dot{\theta}_1} = R_1 + R_2(-\theta_2\sin(\theta_1) + \cos(\theta_1)) - r_2\cos(\theta_1 + \theta_2)$$
   
   และสำหรับเทอม $\frac{m_2}{2}X^2$:
   $$\frac{\partial}{\partial \dot{\theta}_1}\left[\frac{m_2}{2}X^2\right] = m_2 X \cdot \frac{\partial X}{\partial \dot{\theta}_1}$$

5. สำหรับเทอมที่ห้า เรากำหนดให้:
   $$Y = -R_2(\dot{\theta}_2\sin(\theta_1) + \theta_2\dot{\theta}_1\cos(\theta_1) + \theta_1\sin(\theta_1)) + r_2(\dot{\theta}_1 + \dot{\theta}_2)\sin(\theta_1 + \theta_2)$$
   
   ดังนั้น:
   $$\frac{\partial Y}{\partial \dot{\theta}_1} = -R_2\theta_2\cos(\theta_1) + r_2\sin(\theta_1 + \theta_2)$$
   
   และสำหรับเทอม $\frac{m_2}{2}Y^2$:
   $$\frac{\partial}{\partial \dot{\theta}_1}\left[\frac{m_2}{2}Y^2\right] = m_2 Y \cdot \frac{\partial Y}{\partial \dot{\theta}_1}$$

รวมทุกเทอมเข้าด้วยกัน:

$$\frac{\partial L}{\partial \dot{\theta}_1} = m_1\dot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2) + \frac{R_1^2m_1\dot{\theta}_1}{2} + \frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)$$
$$+ m_2 X [R_1 + R_2(-\theta_2\sin(\theta_1) + \cos(\theta_1)) - r_2\cos(\theta_1 + \theta_2)]$$
$$+ m_2 Y [-R_2\theta_2\cos(\theta_1) + r_2\sin(\theta_1 + \theta_2)]$$

### 1.2 คำนวณ $\frac{\partial L}{\partial \theta_1}$

1. เทอมแรก:
   $$\frac{\partial}{\partial \theta_1}\left[\frac{m_1}{2}(R_1^2\dot{\theta}_1^2 - 2r_1R_1\dot{\theta}_1^2\cos(\theta_1) + r_1^2\dot{\theta}_1^2)\right]$$
   $$= \frac{m_1}{2} \cdot 2r_1R_1\dot{\theta}_1^2\sin(\theta_1)$$
   $$= m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1)$$

2. เทอมที่สองและสามไม่มี $\theta_1$ โดยตรง:
   $$\frac{\partial}{\partial \theta_1}\left[\frac{\dot{\theta}_1^2R_1^2m_1}{4} + \frac{R_2^2m_2}{4}(\dot{\theta}_1^2 + 2\dot{\theta}_1\dot{\theta}_2 + \dot{\theta}_2^2)\right] = 0$$

3. สำหรับเทอม X:
   $$\frac{\partial X}{\partial \theta_1} = R_2(-\dot{\theta}_2\sin(\theta_1) - \theta_2\dot{\theta}_1\cos(\theta_1) - \dot{\theta}_1\sin(\theta_1)) + r_2(\dot{\theta}_1 + \dot{\theta}_2)\sin(\theta_1 + \theta_2)$$
   
   และ:
   $$\frac{\partial}{\partial \theta_1}\left[\frac{m_2}{2}X^2\right] = m_2 X \cdot \frac{\partial X}{\partial \theta_1}$$

4. สำหรับเทอม Y:
   $$\frac{\partial Y}{\partial \theta_1} = -R_2(\dot{\theta}_2\cos(\theta_1) - \theta_2\dot{\theta}_1\sin(\theta_1) + \theta_1\cos(\theta_1) + \sin(\theta_1)) + r_2(\dot{\theta}_1 + \dot{\theta}_2)\cos(\theta_1 + \theta_2)$$
   
   และ:
   $$\frac{\partial}{\partial \theta_1}\left[\frac{m_2}{2}Y^2\right] = m_2 Y \cdot \frac{\partial Y}{\partial \theta_1}$$

5. สำหรับเทอมพลังงานศักย์:
   $$\frac{\partial}{\partial \theta_1}\left[-gm_1(R_1 - r_1\cos\theta_1) - gm_2(R_1 - r_2\cos(\theta_1 + \theta_2) + R_2\cos\theta_1 - R_2\theta_2\sin\theta_1)\right]$$
   $$= gm_1r_1\sin\theta_1 + gm_2(r_2\sin(\theta_1 + \theta_2) - R_2\sin\theta_1 - R_2\theta_2\cos\theta_1)$$

รวมทุกเทอมเข้าด้วยกัน:

$$\frac{\partial L}{\partial \theta_1} = m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1) + m_2 X \cdot \frac{\partial X}{\partial \theta_1} + m_2 Y \cdot \frac{\partial Y}{\partial \theta_1}$$
$$+ gm_1r_1\sin\theta_1 + gm_2(r_2\sin(\theta_1 + \theta_2) - R_2\sin\theta_1 - R_2\theta_2\cos\theta_1)$$

### 1.3 คำนวณ $\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{\theta}_1}\right)$

เราจะหาอนุพันธ์ตามเวลาของ $\frac{\partial L}{\partial \dot{\theta}_1}$ โดยแยกพิจารณาทีละเทอม:

1. เทอมแรก: $m_1\dot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2)$
   $$\frac{d}{dt}[m_1\dot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2)]$$
   $$= m_1\ddot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2) + m_1\dot{\theta}_1 \cdot \frac{d}{dt}(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2)$$
   $$= m_1\ddot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2) + m_1\dot{\theta}_1 \cdot 2r_1R_1\sin(\theta_1)\dot{\theta}_1$$
   $$= m_1\ddot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2) + 2m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1)$$

2. เทอมที่สอง: $\frac{R_1^2m_1\dot{\theta}_1}{2}$
   $$\frac{d}{dt}\left[\frac{R_1^2m_1\dot{\theta}_1}{2}\right] = \frac{R_1^2m_1\ddot{\theta}_1}{2}$$

3. เทอมที่สาม: $\frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)$
   $$\frac{d}{dt}\left[\frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)\right] = \frac{R_2^2m_2}{2}(\ddot{\theta}_1 + \ddot{\theta}_2)$$

4. สำหรับเทอมที่เกี่ยวกับ X:
   $$\frac{d}{dt}[m_2 X \cdot \frac{\partial X}{\partial \dot{\theta}_1}] = m_2 \frac{d}{dt}(X) \cdot \frac{\partial X}{\partial \dot{\theta}_1} + m_2 X \cdot \frac{d}{dt}\left(\frac{\partial X}{\partial \dot{\theta}_1}\right)$$

5. สำหรับเทอมที่เกี่ยวกับ Y:
   $$\frac{d}{dt}[m_2 Y \cdot \frac{\partial Y}{\partial \dot{\theta}_1}] = m_2 \frac{d}{dt}(Y) \cdot \frac{\partial Y}{\partial \dot{\theta}_1} + m_2 Y \cdot \frac{d}{dt}\left(\frac{\partial Y}{\partial \dot{\theta}_1}\right)$$

รวมทุกเทอมแล้วย้ายไปด้านขวา:

$$\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{\theta}_1}\right) - \frac{\partial L}{\partial \theta_1} = 0$$

$$m_1\ddot{\theta}_1(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2) + 2m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1) + \frac{R_1^2m_1\ddot{\theta}_1}{2} + \frac{R_2^2m_2}{2}(\ddot{\theta}_1 + \ddot{\theta}_2)$$
$$+ m_2 \frac{d}{dt}(X) \cdot \frac{\partial X}{\partial \dot{\theta}_1} + m_2 X \cdot \frac{d}{dt}\left(\frac{\partial X}{\partial \dot{\theta}_1}\right) + m_2 \frac{d}{dt}(Y) \cdot \frac{\partial Y}{\partial \dot{\theta}_1} + m_2 Y \cdot \frac{d}{dt}\left(\frac{\partial Y}{\partial \dot{\theta}_1}\right)$$
$$- m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1) - m_2 X \cdot \frac{\partial X}{\partial \theta_1} - m_2 Y \cdot \frac{\partial Y}{\partial \theta_1}$$
$$- gm_1r_1\sin\theta_1 - gm_2(r_2\sin(\theta_1 + \theta_2) - R_2\sin\theta_1 - R_2\theta_2\cos\theta_1) = 0$$

## 2. การหาอนุพันธ์สำหรับตัวแปร $\theta_2$

### 2.1 คำนวณ $\frac{\partial L}{\partial \dot{\theta}_2}$

1. เทอมแรกและเทอมที่สองไม่มี $\dot{\theta}_2$ จึงมีค่าเป็น 0

2. เทอมที่สาม: $\frac{R_2^2m_2}{4}(\dot{\theta}_1^2 + 2\dot{\theta}_1\dot{\theta}_2 + \dot{\theta}_2^2)$
   $$\frac{\partial}{\partial \dot{\theta}_2}\left[\frac{R_2^2m_2}{4}(\dot{\theta}_1^2 + 2\dot{\theta}_1\dot{\theta}_2 + \dot{\theta}_2^2)\right]$$
   $$= \frac{R_2^2m_2}{4}(2\dot{\theta}_1 + 2\dot{\theta}_2)$$
   $$= \frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)$$

3. สำหรับเทอม X:
   $$\frac{\partial X}{\partial \dot{\theta}_2} = R_2\cos(\theta_1) - r_2\cos(\theta_1 + \theta_2)$$
   
   และ:
   $$\frac{\partial}{\partial \dot{\theta}_2}\left[\frac{m_2}{2}X^2\right] = m_2 X \cdot \frac{\partial X}{\partial \dot{\theta}_2}$$

4. สำหรับเทอม Y:
   $$\frac{\partial Y}{\partial \dot{\theta}_2} = -R_2\sin(\theta_1) + r_2\sin(\theta_1 + \theta_2)$$
   
   และ:
   $$\frac{\partial}{\partial \dot{\theta}_2}\left[\frac{m_2}{2}Y^2\right] = m_2 Y \cdot \frac{\partial Y}{\partial \dot{\theta}_2}$$

รวมทุกเทอมเข้าด้วยกัน:

$$\frac{\partial L}{\partial \dot{\theta}_2} = \frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2) + m_2 X \cdot \frac{\partial X}{\partial \dot{\theta}_2} + m_2 Y \cdot \frac{\partial Y}{\partial \dot{\theta}_2}$$

### 2.2 คำนวณ $\frac{\partial L}{\partial \theta_2}$

1. เทอมแรก เทอมที่สอง และเทอมที่สามไม่มี $\theta_2$ โดยตรง จึงมีค่าเป็น 0

2. สำหรับเทอม X:
   $$\frac{\partial X}{\partial \theta_2} = -r_2(\dot{\theta}_1 + \dot{\theta}_2)\sin(\theta_1 + \theta_2)$$
   
   และ:
   $$\frac{\partial}{\partial \theta_2}\left[\frac{m_2}{2}X^2\right] = m_2 X \cdot \frac{\partial X}{\partial \theta_2}$$

3. สำหรับเทอม Y:
   $$\frac{\partial Y}{\partial \theta_2} = r_2(\dot{\theta}_1 + \dot{\theta}_2)\cos(\theta_1 + \theta_2)$$
   
   และ:
   $$\frac{\partial}{\partial \theta_2}\left[\frac{m_2}{2}Y^2\right] = m_2 Y \cdot \frac{\partial Y}{\partial \theta_2}$$

4. สำหรับเทอมพลังงานศักย์:
   $$\frac{\partial}{\partial \theta_2}\left[-gm_2(R_1 - r_2\cos(\theta_1 + \theta_2) + R_2\cos\theta_1 - R_2\theta_2\sin\theta_1)\right]$$
   $$= gm_2r_2\sin(\theta_1 + \theta_2) + gm_2R_2\sin\theta_1$$

รวมทุกเทอมเข้าด้วยกัน:

$$\frac{\partial L}{\partial \theta_2} = m_2 X \cdot \frac{\partial X}{\partial \theta_2} + m_2 Y \cdot \frac{\partial Y}{\partial \theta_2} + gm_2r_2\sin(\theta_1 + \theta_2) + gm_2R_2\sin\theta_1$$

### 2.3 คำนวณ $\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{\theta}_2}\right)$

1. เทอมแรก: $\frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)$
   $$\frac{d}{dt}\left[\frac{R_2^2m_2}{2}(\dot{\theta}_1 + \dot{\theta}_2)\right] = \frac{R_2^2m_2}{2}(\ddot{\theta}_1 + \ddot{\theta}_2)$$

2. สำหรับเทอมที่เกี่ยวกับ X:
   $$\frac{d}{dt}[m_2 X \cdot \frac{\partial X}{\partial \dot{\theta}_2}] = m_2 \frac{d}{dt}(X) \cdot \frac{\partial X}{\partial \dot{\theta}_2} + m_2 X \cdot \frac{d}{dt}\left(\frac{\partial X}{\partial \dot{\theta}_2}\right)$$

3. สำหรับเทอมที่เกี่ยวกับ Y:
   $$\frac{d}{dt}[m_2 Y \cdot \frac{\partial Y}{\partial \dot{\theta}_2}] = m_2 \frac{d}{dt}(Y) \cdot \frac{\partial Y}{\partial \dot{\theta}_2} + m_2 Y \cdot \frac{d}{dt}\left(\frac{\partial Y}{\partial \dot{\theta}_2}\right)$$

รวมทุกเทอมแล้วย้ายไปด้านขวา:

$$\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{\theta}_2}\right) - \frac{\partial L}{\partial \theta_2} = 0$$

$$\frac{R_2^2m_2}{2}(\ddot{\theta}_1 + \ddot{\theta}_2) + m_2 \frac{d}{dt}(X) \cdot \frac{\partial X}{\partial \dot{\theta}_2} + m_2 X \cdot \frac{d}{dt}\left(\frac{\partial X}{\partial \dot{\theta}_2}\right) + m_2 \frac{d}{dt}(Y) \cdot \frac{\partial Y}{\partial \dot{\theta}_2} + m_2 Y \cdot \frac{d}{dt}\left(\frac{\partial Y}{\partial \dot{\theta}_2}\right)$$
$$- m_2 X \cdot \frac{\partial X}{\partial \theta_2} - m_2 Y \cdot \frac{\partial Y}{\partial \theta_2} - gm_2r_2\sin(\theta_1 + \theta_2) - gm_2R_2\sin\theta_1 = 0$$

## 3. สมการการเคลื่อนที่สุดท้าย

เราสามารถเขียนสมการการเคลื่อนที่ในรูปแบบที่แก้หา $\ddot{\theta}_1$ และ $\ddot{\theta}_2$ ได้ดังนี้:

### สมการที่ 1 สำหรับ $\ddot{\theta}_1$:

$$\left[m_1\left(R_1^2 - 2r_1R_1\cos(\theta_1) + r_1^2\right) + \frac{R_1^2m_1}{2} + \frac{R_2^2m_2}{2} + m_2 \text{(เทอมที่มี $\ddot{\theta}_1$)}\right] \ddot{\theta}_1$$
$$+ \left[\frac{R_2^2m_2}{2} + m_2 \text{(เทอมที่มี $\ddot{\theta}_2$)}\right] \ddot{\theta}_2$$
$$= m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1) - 2m_1r_1R_1\dot{\theta}_1^2\sin(\theta_1) + m_2 X \cdot \frac{\partial X}{\partial \theta_1} + m_2 Y \cdot \frac{\partial Y}{\partial \theta_1}$$
$$- m_2 \frac{d}{dt}(X) \cdot \frac{\partial X}{\partial \dot{\theta}_1} - m_2 X \cdot \frac{d}{dt}\left(\frac{\partial X}{\partial \dot{\theta}_1}\right) - m_2 \frac{d}{dt}(Y) \cdot \frac{\partial Y}{\partial \dot{\theta}_1} - m_2 Y \cdot \frac{d}{dt}\left(\frac{\partial Y}{\partial \dot{\theta}_1}\right)$$
$$+ gm_1r_1\sin\theta_1 + gm_2(r_2\sin(\theta_1 + \theta_2) - R_2\sin\theta_1 - R_2\theta_2\cos\theta_1)$$

### สมการที่ 2 สำหรับ $\ddot{\theta}_2$:

$$\left[\frac{R_2^2m_2}{2} + m_2 \text{(เทอมที่มี $\ddot{\theta}_1$)}\right] \ddot{\theta}_1$$
$$+ \left[\frac{R_2^2m_2}{2} + m_2 \text{(เทอมที่มี $\ddot{\theta}_2$)}\right] \ddot{\theta}_2$$
$$= m_2 X \cdot \frac{\partial X}{\partial \theta_2} + m_2 Y \cdot \frac{\partial Y}{\partial \theta_2} - m_2 \frac{d}{dt}(X) \cdot \frac{\partial X}{\partial \dot{\theta}_2} - m_2 X \cdot \frac{d}{dt}\left(\frac{\partial X}{\partial \dot{\theta}_2}\right) - m_2 \frac{d}{dt}(Y) \cdot \frac{\partial Y}{\partial \dot{\theta}_2} - m_2 Y \cdot \frac{d}{dt}\left(\frac{\partial Y}{\partial \dot{\theta}_2}\right)$$
$$+ gm_2r_2\sin(\theta_1 + \theta_2) + gm_2R_2\sin\theta_1$$

## 4. การตรวจสอบความถูกต้อง

โดยทั่วไป สมการการเคลื่อนที่ที่ได้จะอยู่ในรูปแบบ:

$$M_{11}\ddot{\theta}_1 + M_{12}\ddot{\theta}_2 = F_1(\theta_1, \theta_2, \dot{\theta}_1, \dot{\theta}_2)$$
$$M_{21}\ddot{\theta}_1 + M_{22}\ddot{\theta}_2 = F_2(\theta_1, \theta_2, \dot{\theta}_1, \dot{\theta}_2)$$

โดยที่ $M_{ij}$ คือสัมประสิทธิ์ของความเร่งเชิงมุม และ $F_i$ คือฟังก์ชันของตำแหน่ง ความเร็ว และแรงภายนอก

เราสามารถแก้ระบบสมการนี้เพื่อหา $\ddot{\theta}_1$ และ $\ddot{\theta}_2$ ในเทอมของตัวแปรอื่น ๆ ได้โดยใช้กฎของเครเมอร์:

$$\ddot{\theta}_1 = \frac{F_1 M_{22} - F_2 M_{12}}{M_{11}M_{22} - M_{12}M_{21}}$$
$$\ddot{\theta}_2 