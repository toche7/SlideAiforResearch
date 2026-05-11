# Day 2 Lab Manual — ML for Research & Mini Proposal
## AI for Research Workshop | Mahidol University × BDI

> **วิธีใช้คู่มือนี้**  
> คู่มือนี้ออกแบบให้ใช้คู่กับ slides ของวันที่ 2  
> แต่ละ lab มีเนื้อหาละเอียดกว่าที่แสดงใน slide  
> รวมถึง prompt, template code และ checklist ที่ copy ไปใช้ได้ทันที

---

## สารบัญ

| # | กิจกรรม | เวลา | ช่วง |
|---|---|---|---|
| Lab 1 | Python Lab — Regression with Google Colab | 15 นาที | เช้า |
| Lab 2 | Python Lab — Classification with Google Colab | 15 นาที | เช้า |
| Lab 3 | ML Analysis Plan Design | 20 นาที | เช้า |
| Lab 4 | Literature Lab — Scholar → NotebookLM → Gemini | 20 นาที | บ่าย |
| **Workshop** | Mini Research Proposal Development | 60 นาที | บ่าย |

---

## §1 Lab 1 — Python Lab: Regression (15 นาที)

### เป้าหมาย
รัน Linear Regression บน Google Colab เพื่อทำนายค่าตัวเลขต่อเนื่อง และตีความ coefficient และ R² ได้

### ขั้นตอน

**Step 1 — เปิด Google Colab**

1. ไปที่ [https://colab.research.google.com](https://colab.research.google.com)
2. Log in ด้วย Google account
3. เปิด Notebook จาก link: [Basic Regression Notebook](https://github.com/toche7/MLPython1Day/blob/main/BasicRegression.ipynb)
   - คลิก **Open in Colab** หรือ **File → Open notebook → GitHub → วาง URL**

**Step 2 — ข้อมูลที่ใช้ใน Lab**

ข้อมูลตัวอย่างความพึงพอใจผู้รับบริการ (5 ราย):

| ผู้รับบริการ | เวลารอ (นาที) | คะแนน Staff (1–10) | ความพึงพอใจ (0–10) |
|:---:|:---:|:---:|:---:|
| คนที่ 1 | 10 | 9 | 8.5 |
| คนที่ 2 | 30 | 6 | 5.0 |
| คนที่ 3 | 5 | 10 | 9.5 |
| คนที่ 4 | 45 | 5 | 4.0 |
| คนที่ 5 | 20 | 8 | 7.0 |

- **Features (X):** เวลารอ, คะแนน Staff
- **Target (y):** ความพึงพอใจ

**Step 3 — รัน Code และดูผลลัพธ์**

รัน cell ตามลำดับจากบนลงล่าง แล้วสังเกตผลลัพธ์:

```python
import pandas as pd
from sklearn.linear_model import LinearRegression
from sklearn.metrics import r2_score, mean_absolute_error

data = {
    "waiting_time":  [10, 30, 5, 45, 20],
    "staff_score":   [9,  6, 10,  5,  8],
    "satisfaction":  [8.5, 5.0, 9.5, 4.0, 7.0]
}
df = pd.DataFrame(data)
X = df[["waiting_time", "staff_score"]]
y = df["satisfaction"]

model = LinearRegression()
model.fit(X, y)

print("Coef:", model.coef_)   # น้ำหนักของแต่ละ feature
print("R2 :", round(r2_score(y, model.predict(X)), 3))
print("MAE:", round(mean_absolute_error(y, model.predict(X)), 3))
```

**Step 4 — อ่านผลลัพธ์**

| ผลลัพธ์ | ความหมาย |
|---|---|
| `Coef[0]` (waiting_time) ติดลบ | รอนานขึ้น → คะแนนความพึงพอใจลดลง |
| `Coef[1]` (staff_score) เป็นบวก | staff ดีขึ้น → คะแนนความพึงพอใจเพิ่มขึ้น |
| **R²** ใกล้ 1.0 | โมเดลอธิบายความแปรปรวนของข้อมูลได้สูง |
| **MAE** ต่ำ | ค่าทำนายคลาดเคลื่อนน้อยเฉลี่ย X หน่วย |

ผลที่ควรได้ (จากข้อมูลตัวอย่าง):
```
Coef: [-0.0009,  1.1036]
R²  : 0.996
MAE : 0.07
```

> ⚠️ R² = 0.996 สูงมากเนื่องจากข้อมูลมีเพียง 5 ราย — อาจเกิด **overfitting** ได้ในข้อมูลจริง

**Step 5 — ทดลองปรับค่า**

ลองเปลี่ยนค่าใน `data` เพื่อดูว่าผล R² และ Coef เปลี่ยนอย่างไร:
- เพิ่ม/ลดจำนวน data point
- เพิ่ม feature ใหม่ เช่น `facility_score`

### เชื่อมกับงานวิจัย

| ส่วน ML | เทียบกับงานวิจัย |
|---|---|
| Features (X) | ตัวแปรอิสระ / predictors |
| Target (y) | ตัวแปรตาม / outcome |
| Coef (β) | ขนาดความสัมพันธ์ของแต่ละ predictor |
| R² | สัดส่วนความแปรปรวนที่โมเดลอธิบายได้ |
| MAE | ค่าความผิดพลาดเฉลี่ยในหน่วยเดียวกับ target |

### Checklist ✅

- [ ] เปิด Google Colab และรัน Notebook สำเร็จ
- [ ] เห็น Coef, R², MAE ใน output
- [ ] อธิบายความหมายของ coefficient แต่ละตัวได้
- [ ] รู้ว่าจะใช้ Regression เมื่อใด (target เป็นตัวเลขต่อเนื่อง)

---

## §2 Lab 2 — Python Lab: Classification (15 นาที)

### เป้าหมาย
รัน Logistic Regression บน Google Colab เพื่อจำแนกกลุ่ม และตีความ Precision, Recall, F1-score ได้

### ขั้นตอน

**Step 1 — เปิด Notebook**

เปิด Notebook จาก link: [Basic Classification Notebook](https://github.com/toche7/MLPython1Day/blob/main/BasicClassification.ipynb)

**Step 2 — ข้อมูลที่ใช้ใน Lab**

ข้อมูลตัวอย่างนักเรียน: ผ่าน/ไม่ผ่านการสอบ (6 คน):

| นักเรียน | ชั่วโมงอ่านหนังสือ | คะแนนเก่า (0–100) | ผ่านสอบ (1=ใช่, 0=ไม่) |
|:---:|:---:|:---:|:---:|
| คนที่ 1 | 1 | 40 | 0 |
| คนที่ 2 | 2 | 55 | 0 |
| คนที่ 3 | 3 | 60 | 1 |
| คนที่ 4 | 4 | 70 | 1 |
| คนที่ 5 | 5 | 80 | 1 |
| คนที่ 6 | 1 | 50 | 0 |

- **Features (X):** ชั่วโมงอ่านหนังสือ, คะแนนสอบเก่า
- **Target (y):** ผ่านสอบ (1) หรือไม่ผ่าน (0)

**Step 3 — รัน Code และดูผลลัพธ์**

```python
import pandas as pd
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report

data = {
    "hours_studied": [1, 2, 3, 4, 5, 1],
    "prev_score":    [40, 55, 60, 70, 80, 50],
    "passed":        [0, 0, 1, 1, 1, 0]
}
df = pd.DataFrame(data)
X = df[["hours_studied", "prev_score"]]
y = df["passed"]

model = LogisticRegression()
model.fit(X, y)
y_pred = model.predict(X)

print(classification_report(y, y_pred,
      target_names=["ไม่ผ่าน", "ผ่าน"]))
```

**Step 4 — อ่าน Classification Report**

```
              precision    recall  f1-score   support
     ไม่ผ่าน       1.00      1.00      1.00         3
        ผ่าน       1.00      1.00      1.00         3
    accuracy                           1.00         6
```

| Metric | ความหมาย | ใช้เมื่อ |
|---|---|---|
| **Precision** | ในจำนวนที่ทำนายว่า Positive ถูกต้องกี่ % | FP มีต้นทุนสูง (เช่น รักษาโดยไม่จำเป็น) |
| **Recall** | จากทั้งหมดที่เป็น Positive จริง จับได้กี่ % | FN มีต้นทุนสูง (เช่น พลาดผู้ป่วยเสี่ยงสูง) |
| **F1-score** | Harmonic mean ของ Precision + Recall | ต้องการสมดุลทั้งสอง |
| **Accuracy** | ความถูกต้องโดยรวม | class สมดุล |

> **งานวิจัยด้านสุขภาพส่วนใหญ่เน้น Recall** — เพราะการพลาดกรณี Positive มีผลกระทบสูง

**Step 5 — เพิ่มความซับซ้อน: Random Forest**

ลองเปลี่ยนจาก `LogisticRegression()` เป็น `RandomForestClassifier()`:

```python
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(random_state=42)
model.fit(X, y)
y_pred = model.predict(X)
print(classification_report(y, y_pred, target_names=["ไม่ผ่าน", "ผ่าน"]))
```

สังเกตว่า metrics เปลี่ยนอย่างไรเมื่อเปลี่ยน algorithm

### Checklist ✅

- [ ] รัน Classification Notebook สำเร็จ
- [ ] อ่านค่า Precision, Recall, F1-score ได้
- [ ] อธิบายได้ว่า Recall สำคัญกว่า Precision เมื่อไร
- [ ] รู้ว่าจะใช้ Classification เมื่อใด (target เป็น class/กลุ่ม)

---

## §3 Lab 3 — ML Analysis Plan Design (20 นาที)

### เป้าหมาย
แปลง Research Question เป็น ML Analysis Plan ที่มีองค์ประกอบครบถ้วน พร้อมนำต่อยอดเป็น Proposal ช่วงบ่าย

### เลือก Dataset

เลือก 1 dataset ก่อนเริ่ม Lab:

| # | Dataset | ML Task | Target Variable |
|---|---|---|---|
| **1** | Patient Readmission (500 ราย) | Binary Classification | กลับมาใน 30 วัน: Yes/No |
| **2** | Nurse Burnout (200 คน) | Regression | คะแนน Burnout (0–100) |
| **3** | Health Screening (300 ราย) | Multi-class Classification | กลุ่มเสี่ยง: High/Medium/Low |
| **4** | Patient Satisfaction (300 ชุด) | NLP | Theme / Sentiment |

> หรือใช้ข้อมูลของท่านเอง — กำหนด ML task ให้ชัดเจนก่อน

### Template: ML Analysis Plan Canvas

กรอก canvas นี้ตามหัวข้อที่เลือก:

| องค์ประกอบ | Dataset ของท่าน |
|---|---|
| **Research Topic** | |
| **Research Question** | |
| **Data Science Objective** | |
| **ML Task** | Classification / Regression / NLP |
| **Target Variable** | |
| **Features (ตัวแปรอิสระ)** | |
| **Data Source** | |
| **Sample Size** | n = |
| **Candidate Models** | |
| **Evaluation Metrics** | |
| **Known Limitations** | |

### ตัวอย่าง Analysis Plan ตาม Dataset

**Dataset 1 — Patient Readmission:**

| องค์ประกอบ | ค่า |
|---|---|
| Research Question | Can ML predict 30-day readmission from routine clinical data? |
| ML Task | Binary Classification |
| Target | Readmission: Yes / No |
| Features | age, gender, diagnosis, comorbidities, length of stay |
| Models | Logistic Regression, Random Forest |
| Metrics | Recall, F1-score |
| Limitation | Class imbalance, single-site data |

**Dataset 2 — Nurse Burnout:**

| องค์ประกอบ | ค่า |
|---|---|
| Research Question | Which workload factors best predict burnout severity? |
| ML Task | Regression |
| Target | Burnout Score (0–100) |
| Features | weekly hours, patient load, organizational support |
| Models | Linear Regression, Random Forest Regressor |
| Metrics | MAE, R² |
| Limitation | Self-report bias, n=200 |

**Dataset 3 — Health Screening:**

| องค์ประกอบ | ค่า |
|---|---|
| Research Question | How accurately can ML classify disease risk from health screening data? |
| ML Task | Multi-class Classification |
| Target | Risk Group: High / Medium / Low |
| Features | BMI, fasting glucose, blood pressure, exercise, family history |
| Models | Decision Tree, Random Forest |
| Metrics | Accuracy, macro F1-score |
| Limitation | Self-reported lifestyle data, cross-sectional |

**Dataset 4 — Patient Satisfaction:**

| องค์ประกอบ | ค่า |
|---|---|
| Research Question | What themes emerge from patient satisfaction open-ended responses? |
| ML Task | NLP / Text Mining |
| Target | Themes & Sentiment direction |
| Features | Free-text survey responses |
| Models | LDA topic modeling, sentiment analysis |
| Metrics | Topic coherence score, human validation |
| Limitation | Language variation, subjectivity |

### Prompt สำหรับ AI ช่วย Design Analysis Plan

ถ้าต้องการให้ Gemini ช่วยออกแบบ — copy prompt นี้:

```
Act as a research methodology advisor for ML-based health research.
I want to design an ML analysis plan for the following:
- Research topic: [ระบุหัวข้อ]
- Dataset description: [ระบุข้อมูลที่มี — จำนวนราย, ตัวแปร, แหล่งที่มา]
- Research question: [ระบุ RQ]

Please suggest:
1. The appropriate ML task (Classification / Regression / Clustering / NLP)
2. Target variable and key features
3. Candidate ML models (list 2–3 options)
4. Recommended evaluation metrics with justification
5. Potential limitations and biases to address

Keep the response practical and aligned with the research question.
```

### Formula: Research Question → ML Task

```
RQ ถามเรื่อง          →   ML Task ที่เหมาะ
─────────────────────────────────────────────
"predict / ทำนาย"      →   Regression (ถ้า target ต่อเนื่อง)
                           Classification (ถ้า target เป็น class)
"classify / จำแนก"     →   Classification
"group / cluster"       →   Clustering (Unsupervised)
"theme / pattern"       →   NLP / Text Mining
"factor / ปัจจัย"       →   Regression + Feature importance
```

### Checklist ✅

- [ ] เลือก dataset แล้ว
- [ ] กรอก Analysis Plan Canvas ครบทุกช่อง
- [ ] เลือก ML task ที่สอดคล้องกับ RQ
- [ ] ระบุ target variable และ features ชัดเจน
- [ ] เลือก evaluation metrics พร้อมเหตุผล
- [ ] พร้อมนำ plan นี้ต่อยอดเป็น proposal ช่วงบ่าย

---

## §4 Lab 4 — Literature Lab: Google Scholar → NotebookLM → Gemini (20 นาที)

### เป้าหมาย
ค้นหาเปเปอร์ที่เกี่ยวข้อง สกัด research gap และร่าง Background paragraph พร้อมอ้างอิง

### ภาพรวม 3 ขั้นตอน

```
Step 1: ค้นหา + ดาวน์โหลด PDF
   Google Scholar
Step 2: สกัดความรู้จาก paper
   NotebookLM
Step 3: ร่าง Background paragraph
   Gemini
```

**เป้าหมายของ Lab นี้:**
- ได้เปเปอร์ที่เกี่ยวข้อง **3–5 บทความ**
- เข้าใจ gap ของงานที่มีอยู่
- ได้ **draft Background paragraph** พร้อมอ้างอิงเบื้องต้น

---

### Step 1 — ค้นหาและดาวน์โหลดเปเปอร์ (Google Scholar)

**เปิด [scholar.google.com](https://scholar.google.com)**

**วิธีค้นหา:**
1. พิมพ์ keyword ตาม Dataset ที่เลือก (ดูตารางด้านล่าง)
2. กรองปี: **2020–2025** (คลิก "Custom range" ด้านซ้าย)
3. เลือกบทความที่มี **[PDF]** ปรากฏ
4. ดาวน์โหลด **3–5 บทความ** ที่เกี่ยวข้องมากที่สุด

**Keyword ตาม Dataset:**

| Dataset | Keyword ที่แนะนำ |
|---|---|
| 1 Readmission | `hospital readmission prediction machine learning` |
| 2 Burnout | `nurse burnout workload regression prediction` |
| 3 Health Screening | `chronic disease risk classification machine learning BMI` |
| 4 Satisfaction | `patient satisfaction NLP topic modeling survey` |

> ถ้าบทความไม่มี PDF ฟรี — ลองค้นใน [PubMed Central](https://pmc.ncbi.nlm.nih.gov) หรือ [Unpaywall](https://unpaywall.org)

**Keyword Strategy เพิ่มเติม:**
- ใช้ `"` ครอบคำหลัก เช่น `"nurse burnout" machine learning`
- เพิ่ม `Thailand` หรือ `Southeast Asia` ถ้าต้องการบริบทท้องถิ่น
- ดู **Related articles** ใต้บทความที่เกี่ยวข้องมากที่สุด

---

### Step 2 — สกัดความรู้ด้วย NotebookLM

**เปิด [notebooklm.google.com](https://notebooklm.google.com)**

**ขั้นตอน:**
1. สร้าง **Notebook ใหม่** ตั้งชื่อตามหัวข้อวิจัยของท่าน
2. คลิก **Add Source → Upload PDF**
3. อัปโหลดเปเปอร์ทั้งหมดที่ดาวน์โหลดมา
4. รอให้ NotebookLM วิเคราะห์ (1–2 นาที)

**คำถามที่ควรถาม NotebookLM (Phase 1 — Overview):**
```
Based on all the papers I uploaded:
1. What are the key findings across these papers?
2. What methods were used to [predict/classify/analyze] [topic]?
3. What are the main datasets and sample sizes used?
4. What are the most common evaluation metrics reported?
```

**คำถามสำหรับสกัด Research Gap (Phase 2 — Gap):**
```
Based on all the papers I uploaded:
1. What is the most common research gap mentioned by the authors?
2. Which populations or settings are underrepresented?
3. What ML methods have NOT been applied to this topic yet?
4. What outcome variables are rarely studied?

Summarize in 3–5 bullet points with the paper title as source.
```

> NotebookLM อ้างอิงเฉพาะเนื้อหาจาก PDF ที่อัปโหลด — **ไม่สร้าง citation ปลอม**  
> ทุก claim สามารถตรวจสอบย้อนกลับกับ paper ต้นฉบับได้

**บันทึก output จาก NotebookLM:**
- สรุป key findings จากเปเปอร์
- รายการ research gap พร้อมระบุ paper ที่อ้างถึง
- นำไปใส่ใน Proposal Canvas ช่อง Research Gap

---

### Step 3 — ร่าง Background ด้วย Gemini

**เปิด [gemini.google.com](https://gemini.google.com)**

**Prompt สำหรับเขียน Background:**

```
I am writing a research proposal on [topic].
My research question is: [RQ].

Based on findings from related literature, here is what I found:
[วาง key findings จาก NotebookLM ที่นี่]

The research gap identified is:
[วาง gap จาก NotebookLM ที่นี่]

Please write a Background/Rationale paragraph (150–200 words) that:
1. Introduces the problem and its significance
2. Summarizes what previous studies have found
3. Identifies the research gap clearly
4. Justifies why ML is appropriate for this study
5. Ends with the purpose of this study

Use academic English. Include in-text citations in APA format
using the paper titles I described.
I will verify and update all citations manually.
```

**ปรับ Prompt ถ้าผลยังไม่ตรงกับงาน:**
```
The background is too general.
Please make it more specific to [ML task] for [population/setting].
Emphasize the gap related to [specific gap from NotebookLM].
Keep the length to 150–200 words.
```

---

### ตรวจสอบ Background ก่อนนำไปใช้

หลังได้ draft จาก Gemini ต้องตรวจสอบทุกครั้ง:

- [ ] Citation ทุกตัวมีอยู่จริงใน paper ที่อัปโหลด
- [ ] ตัวเลขและสถิติถูกต้อง ไม่ใช่ค่า hallucinated
- [ ] Gap ที่ระบุสอดคล้องกับ RQ ของท่าน
- [ ] ไม่กล่าวเกินจริงกว่าที่ paper ระบุ
- [ ] ความยาวเหมาะสม 150–200 คำ

---

### ตัวอย่าง Background ที่สมบูรณ์ ตาม Dataset

**Dataset 1 — 30-Day Readmission:**

> *Hospital readmission within 30 days is a major quality indicator and cost burden globally. Studies have shown that 15–20% of patients are readmitted within 30 days of discharge (Jencks et al., 2009). Machine learning models have demonstrated promising results in predicting readmission risk, with Logistic Regression and Random Forest achieving AUC > 0.70 in several studies (Frizzell et al., 2017; Mortazavi et al., 2016). However, most existing models rely on EHR data from large academic hospitals in high-income countries, limiting their applicability to community hospital settings. This study aims to address this gap by developing a prediction model using routinely available clinical data from [setting].*

**Gap:** งานส่วนใหญ่ทำในโรงพยาบาลใหญ่ในประเทศรายได้สูง — ขาดหลักฐานในบริบทโรงพยาบาลชุมชน

---

**Dataset 2 — Nurse Burnout:**

> *Nurse burnout is a persistent challenge affecting healthcare quality and workforce retention. High patient-to-nurse ratios and excessive working hours have been consistently linked to elevated burnout scores (Aiken et al., 2014). Predictive models using regression techniques have begun to explore which workload factors most strongly predict burnout severity (Dall'Ora et al., 2020). Despite this, few studies have examined the combined effect of workload and organizational support on burnout in Southeast Asian hospital settings. This study addresses this gap using regression modeling on survey data from [setting].*

**Gap:** ขาดการศึกษาในบริบทเอเชียตะวันออกเฉียงใต้ที่พิจารณาทั้ง workload และ organizational support

---

**Dataset 3 — Health Screening:**

> *Annual health screenings provide an opportunity for early identification of chronic disease risk. Studies have applied machine learning to classify individuals into risk groups using BMI, glucose, and blood pressure (Zou et al., 2018; Islam et al., 2020). However, exercise behavior and family history are rarely integrated as predictors in existing models. This study proposes a multi-class risk classification model incorporating these underexplored variables to improve early identification of at-risk individuals in community health settings.*

**Gap:** โมเดลส่วนใหญ่ใช้เพียงตัวแปรทางคลินิก — ขาดการรวมพฤติกรรมสุขภาพและประวัติครอบครัว

---

**Dataset 4 — Patient Satisfaction:**

> *Patient satisfaction is increasingly recognized as a key dimension of healthcare quality and a driver of service improvement. Open-ended survey responses contain rich qualitative data, but are often underanalyzed due to the limitations of manual review. NLP approaches such as LDA topic modeling have been used to extract recurring themes from patient feedback (Doing-Harris et al., 2017; Greaves et al., 2013). However, few studies have applied NLP to Thai-language patient feedback in hospital settings. This study applies topic modeling and sentiment analysis to identify key themes and satisfaction patterns from survey data at [setting].*

**Gap:** ยังขาดการนำ NLP ไปใช้กับข้อมูลความคิดเห็นภาษาไทยในบริบทโรงพยาบาล

---

### Checklist ✅ Lab 4

- [ ] ดาวน์โหลดเปเปอร์ 3–5 บทความจาก Google Scholar
- [ ] อัปโหลด PDF ใน NotebookLM สำเร็จ
- [ ] ถาม NotebookLM เพื่อสกัด key findings และ gap ได้
- [ ] ได้ Background draft จาก Gemini (150–200 คำ)
- [ ] ตรวจสอบ citation และตัวเลขเบื้องต้นแล้ว
- [ ] พร้อมนำ Background + Gap ไปใส่ใน Mini Proposal Canvas

---

## §5 Workshop — Mini Research Proposal Development (60 นาที)

### เป้าหมาย
นำผลจาก Lab 3 (ML Analysis Plan) และ Lab 4 (Literature Lab) มาพัฒนาเป็น Mini Research Proposal ที่มี 10 องค์ประกอบครบถ้วน

---

### Mini Proposal Canvas

**Dataset ที่เลือก:** ☐ 1-Readmission  ☐ 2-Burnout  ☐ 3-Health Screening  ☐ 4-Satisfaction  ☐ ข้อมูลเอง

| Section | Draft ของท่าน |
|---|---|
| 1. Title | |
| 2. Background / Rationale | *(ใช้จาก Lab 4)* |
| 3. Research Gap | *(ใช้จาก Lab 4 — NotebookLM)* |
| 4. Research Question | |
| 5. Objectives (2 ระดับ) | |
| 6. Methodology | |
| 7. AI/ML Application | *(ใช้จาก Lab 3)* |
| 8. Preliminary Findings | |
| 9. Ethical Considerations | |
| 10. Limitations | |

---

### Workshop Task 1 — เตรียม Input

ก่อนเริ่มร่าง Proposal ต้องมี:

| สิ่งที่ต้องเตรียม | มาจาก |
|---|---|
| Background paragraph | Lab 4 (Gemini) |
| Research gap | Lab 4 (NotebookLM) |
| ML Analysis Plan | Lab 3 |
| Dataset ที่เลือก | Lab 1/2 หรือข้อมูลเอง |

---

### Workshop Task 2 — ร่าง Title

Title ที่ดีต้องมีครบ:
- บอก **population / context**
- ระบุ**ตัวแปรหรือประเด็นหลัก**
- สะท้อน **predictive / classification / analysis aim**
- **ไม่กว้างเกินไป**

**โครงสร้าง Title ที่ใช้บ่อย:**
```
[ML Method] for [Outcome] [Prediction/Classification/Analysis]:
A [Study Design] Study in [Setting/Population]
```

**ตัวอย่าง:**
```
Dataset 1: Machine Learning-Based Prediction of 30-Day Hospital
           Readmission Using Routine Clinical Data: A Retrospective
           Study in a Community Hospital Setting

Dataset 2: Predictors of Nurse Burnout Severity: A Regression Analysis
           of Workload and Organizational Support Factors

Dataset 3: Multi-class Disease Risk Classification from Annual Health
           Screening Data Using Machine Learning

Dataset 4: Identifying Patient Satisfaction Themes from Open-ended
           Survey Responses Using NLP Topic Modeling
```

---

### Workshop Task 3 — ร่าง Research Question และ Objectives

**Research Question — โครงประโยคที่ใช้บ่อย:**

```
Classification:  How accurately can a ML model classify [outcome]
                 from [dataset]?
Regression:      Which factors are most strongly associated with
                 [outcome] in [population]?
NLP:             What themes emerge from [text data] regarding
                 [topic]?
```

**Objectives — ต้องมี 2 ระดับเสมอ:**

```
Research Objective:
To examine / investigate / identify [research aim]
in [population/setting].

Data Science Objective:
To develop / compare / evaluate a [ML task] model
for [prediction/classification/analysis] of [target]
using [data source].
```

**ตัวอย่าง Objectives — Dataset 1:**
- **Research Objective:** To identify factors associated with 30-day hospital readmission in community hospital patients.
- **Data Science Objective:** To develop and evaluate a binary classification model for predicting readmission risk using routinely collected clinical data.

---

### Workshop Task 4 — ร่าง Methodology

**Template Methodology Paragraph:**

```
This study will use a [ML task] approach to [predict/classify/analyze]
[target variable]. The dataset includes [n] [patient records /
participants] with features such as [feature list]. Candidate models
will include [model 1] and [model 2]. The dataset will be split into
80% training and 20% testing sets. Model performance will be evaluated
using [metrics]. Potential limitations include [limitations].
```

**Prompt สำหรับ Gemini ช่วยเขียน Methodology:**

```
Write a Methods paragraph for a research proposal (150–200 words).
Use the following:
- ML task: [regression / binary classification / multi-class / NLP]
- Dataset: [description, n=XXX]
- Setting: [hospital / community / survey]
- Target variable: [target]
- Features: [feature list]
- Candidate models: [model 1, model 2]
- Evaluation metrics: [metrics with justification]
- Limitations: [list]

Use future tense (will be developed). Keep academic tone.
```

---

### Workshop Task 5 — ร่าง Preliminary Findings

Preliminary findings แสดงความเป็นไปได้ของงานวิจัย — ยังไม่ใช่ final results

**ประเภท Preliminary Findings ที่ยอมรับได้:**

| ประเภท | ตัวอย่าง |
|---|---|
| Literature-based | สรุปแนวโน้มจากงานที่ผ่านมา |
| ML Lab-based | ผล performance เบื้องต้นจาก Colab |
| Conceptual | กรอบแนวคิดหรือ pattern ที่คาดไว้ |

**ตัวอย่าง Preliminary Findings ตาม Dataset:**

| Dataset | Preliminary Finding ตัวอย่าง |
|---|---|
| **1 Readmission** | Initial classification model achieved Recall = 0.78, suggesting feasibility of early high-risk identification |
| **2 Burnout** | Regression analysis indicates working hours and patient load are strongly associated with burnout (preliminary R² = 0.61) |
| **3 Health Screening** | Pilot classification model shows BMI and fasting glucose as top predictors; accuracy = 0.74 |
| **4 Satisfaction** | Topic modeling identified 4 recurring themes: waiting time, staff communication, facility, and follow-up care |

**การเขียน Preliminary Findings อย่างปลอดภัย:**

✅ ควรใช้:
- Preliminary results **suggest** that …
- Initial analysis **indicates** that …
- Simulated analysis **demonstrates the feasibility** of …
- Further validation **is required** …

❌ ไม่ควรใช้:
- This study **proves** that …
- The model **confirms** that …
- Results **show the true cause** of …

> ⚠️ ถ้าใช้ข้อมูลจำลอง ต้องระบุ "simulated data" ในทุกที่ที่อ้างถึงผล

---

### Workshop Task 6 — ร่าง Proposal ด้วย AI

**Prompt หลักสำหรับร่าง Proposal ทั้งหมด:**

```
Act as a research methodology advisor. I am developing a mini research 
proposal. Please help me draft the following sections using the 
information below.

Dataset: [Dataset 1/2/3/4 — description]
Research Question: [RQ จาก Task 3]
Data Science Objective: [Objective จาก Task 3]
ML Task: [classification / regression / NLP]
Target Variable: [target]
Key Features: [feature list]

Verified Background paragraph (do NOT rewrite this):
[วาง Background จาก Lab 4 ที่นี่]

Research Gap identified from literature:
[วาง gap จาก NotebookLM ที่นี่]

Please draft:
1. A concise research title
2. Research question (one sentence)
3. Research objective + Data science objective
4. Methodology paragraph (150 words)
5. Preliminary findings (2–3 bullet points)
6. Ethical considerations (2–3 sentences)
7. Limitations (3–5 bullet points)

Do NOT rewrite the Background — use it as provided above.
```

---

### Workshop Task 7 — ตรวจ Alignment ด้วย AI

**Prompt สำหรับตรวจความสอดคล้องของ Proposal:**

```
Please review the following mini research proposal.
Check whether Title, Research Gap, Research Question, Objectives,
Methodology, ML Application, and Preliminary Findings are 
logically aligned with each other.
Identify any inconsistencies and suggest specific improvements.

[วาง proposal draft ทั้งหมดที่นี่]
```

---

### Proposal Alignment Checklist

| Checkpoint | ✓ |
|---|---|
| Title สะท้อน ML task และ target ที่ชัดเจน | |
| Background มีอ้างอิงจากเปเปอร์จริง (≥ 3 บทความ) | |
| Gap ที่ระบุมาจาก literature ไม่ใช่ความเห็นส่วนตัว | |
| Research Question ตอบได้ด้วย method ที่เลือก | |
| Objectives มีทั้ง Research + Data Science objective | |
| ML task เหมาะกับประเภทของ target variable | |
| Metrics เลือกให้เหมาะกับโจทย์วิจัย พร้อมเหตุผล | |
| Preliminary findings ไม่กล่าวเกินจริง | |
| Ethics และ limitation ระบุชัดเจน | |
| ทุก section เชื่อมต่อกันอย่างสอดคล้อง | |

---

### Workshop Checklist ✅

| Section | เสร็จ | AI ช่วย | ตรวจสอบแล้ว |
|---|---|---|---|
| Title | ☐ | ☐ | ☐ |
| Background (จาก Lab 4) | ☐ | ☐ | ☐ |
| Research Gap | ☐ | ☐ | ☐ |
| Research Question | ☐ | ☐ | ☐ |
| Research Objective | ☐ | ☐ | ☐ |
| Data Science Objective | ☐ | ☐ | ☐ |
| Methodology | ☐ | ☐ | ☐ |
| AI/ML Application | ☐ | ☐ | ☐ |
| Preliminary Findings | ☐ | ☐ | ☐ |
| Ethical Considerations | ☐ | ☐ | ☐ |
| Limitations | ☐ | ☐ | ☐ |
| Alignment ตรวจสอบแล้ว | ☐ | — | — |

---

## ภาคผนวก A — AI Prompts สรุป

### Prompts สำหรับ Lab 3 (ML Analysis Plan)

**ออกแบบ Analysis Plan:**
```
Design an ML analysis plan for [topic].
Dataset: [description, n=XXX].
Research question: [RQ].
Suggest: ML task, target variable, features,
candidate models, evaluation metrics, and limitations.
```

### Prompts สำหรับ Lab 4 (Literature Lab)

**NotebookLM — สกัด Gap:**
```
Based on all papers uploaded:
1. Most common research gap?
2. Underrepresented populations/settings?
3. Unapplied ML methods?
4. Rarely studied outcomes?
Summarize in 3–5 bullets with paper source.
```

**Gemini — ร่าง Background:**
```
Write a Background paragraph (150–200 words) for a proposal on [topic].
RQ: [RQ]. Key findings from literature: [findings].
Research gap: [gap].
Cover: problem significance, prior studies, gap, ML justification, purpose.
Academic English. APA citation format. I will verify all citations.
```

### Prompts สำหรับ Workshop (Proposal)

**ร่าง Proposal ทั้งหมด:**
```
Draft a mini proposal for [topic] using:
Dataset: [n=XXX], ML task: [task], Target: [target],
Features: [list], Models: [list], Metrics: [metrics].
Background (do not rewrite): [background].
Gap: [gap].
Draft: title, RQ, 2 objectives, methodology (150w),
preliminary findings (3 bullets), ethics, limitations.
```

**ตรวจ Alignment:**
```
Review this proposal for logical alignment between
title, gap, RQ, objectives, methodology, ML, and findings.
Identify inconsistencies and suggest improvements.
[paste proposal]
```

**แปลไทย → Academic English:**
```
Translate this Thai text to academic English suitable for a
research proposal. Preserve technical terms in English.
Adjust for formal academic register.
"[ข้อความภาษาไทย]"
```

---

## ภาคผนวก B — Quick Reference: ML Task Selection

| Research Question type | ML Task | Target type | Metrics |
|---|---|---|---|
| Predict a score / value | **Regression** | Continuous | MAE, RMSE, R² |
| Predict yes/no | **Binary Classification** | 2 classes | Recall, F1, AUC |
| Predict one of 3+ groups | **Multi-class Classification** | 3+ classes | Accuracy, macro F1 |
| Find hidden groups | **Clustering** | No target | Silhouette score |
| Analyze text data | **NLP** | Text | Coherence, F1, human validation |

---

## ภาคผนวก C — Evaluation Metrics Quick Guide

### Regression
$$MAE = \frac{1}{n}\sum|y_i - \hat{y}_i|$$
$$RMSE = \sqrt{\frac{1}{n}\sum(y_i - \hat{y}_i)^2}$$
$$R^2 = 1 - \frac{\sum(y_i - \hat{y}_i)^2}{\sum(y_i - \bar{y})^2}$$

| Metric | ตีความ | ใช้เมื่อ |
|---|---|---|
| **MAE** | ผิดพลาดเฉลี่ย X หน่วย | ข้อมูลมี outlier มาก |
| **RMSE** | คล้าย MAE แต่ลงโทษ error ใหญ่หนักกว่า | error ขนาดใหญ่มีผลกระทบสูง |
| **R²** | อธิบายความแปรปรวนได้ X% | เปรียบเทียบโมเดลหลายตัว |

### Classification

$$Precision = \frac{TP}{TP+FP}, \quad Recall = \frac{TP}{TP+FN}$$
$$F1 = 2 \times \frac{Precision \times Recall}{Precision + Recall}$$

| สถานการณ์ | Metric ที่เน้น |
|---|---|
| อย่าพลาดผู้ป่วยเสี่ยงสูง | **Recall** |
| ลด false alarm / รักษาโดยไม่จำเป็น | **Precision** |
| สมดุลทั้งคู่ | **F1-score** |
| class สมดุล เน้นภาพรวม | **Accuracy** |

---

## หมายเหตุสำคัญ

> ⚠️ **Research Integrity**  
> - Preliminary findings จาก simulated data ต้องระบุว่า "simulated" ทุกครั้ง  
> - Citation ทุกอันต้องตรวจสอบจากเปเปอร์ต้นฉบับ — อย่าเชื่อ AI โดยไม่ตรวจ  
> - Methodology ที่เขียนต้องทำได้จริงในบริบทของท่าน  
> - Proposal วันนี้คือ **draft เริ่มต้น** — ยังต้องผ่านการตรวจสอบและปรับปรุง

> ⚠️ **AI-Assisted Writing**  
> - AI เขียนได้ดีระดับประโยค แต่ยังอ่อนแอระดับภาพรวม  
> - มนุษย์ต้องรับผิดชอบ: ตรวจ logic, flow, citation, และ factual accuracy  
> - ให้ AI ช่วยร่าง — แต่ขัดเกลาขั้นสุดท้ายเป็นหน้าที่ของท่าน

---

*Day 2 Lab Manual | AI for Research Workshop | Version 1.0 | May 2026*
