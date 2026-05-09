---
marp: true
theme: mahidol-green
paginate: true
size: 16:9
footer: "From ML Lab to Research Proposal | AI for Research"
---

<!-- _class: lead -->

<style scoped>
.logo-bar { position: absolute; top: 36px; right: 64px; display: flex; align-items: center; gap: 16px; }
.logo-bar img { width: 100px; height: 100px; object-fit: contain; }
</style>

<div class="logo-bar">
  <img src="fig/logos/mahidol.svg" alt="Mahidol University">
  <img src="fig/logos/chulabhorn-circle.png" alt="BDI">
</div>

# From ML Lab to Research Proposal

<div class="subtitle">Day 2 Afternoon Session</div>

**จาก ML Analysis Plan สู่ Mini Research Proposal**

---

## ภาพรวมช่วงบ่าย

1. **Transition** — ต่อยอดจากช่วงเช้าสู่ proposal
2. **HIRF Framework** — ทบทวนบทบาท Human vs AI
3. **Mini Proposal Structure** — โครงสร้าง proposal 10 ส่วน
4. **Methodology & ML** — การเขียน methodology อย่างถูกต้อง
5. **Preliminary Findings** — การนำเสนอผลเบื้องต้น
6. **Workshop** — ลงมือทำ mini proposal
7. **Process Reflection** — สะท้อนกระบวนการทำงานกับ AI

---

<!-- _class: divider -->

## 01
## Transition from Morning

From ML Workflow to Proposal Development

---

<!-- _class: lead -->

# ช่วงเช้า → ช่วงบ่าย

- ช่วงเช้า: เข้าใจ **ML workflow**
- ช่วงบ่าย: นำ ML ไป**ออกแบบ proposal**
- เป้าหมาย: ได้ proposal พร้อมผลการศึกษาเบื้องต้น

---

## สิ่งที่ได้จากช่วงเช้า

ผู้เข้าอบรมควรมีครบ 7 อย่าง:

1. Research topic
2. Data science objective
3. ML task
4. Target variable
5. Features
6. Evaluation metrics
7. **Draft ML-based analysis plan**

---

## Output ช่วงเช้า → Proposal Section

| Output ช่วงเช้า | Section ใน Proposal |
|---|---|
| Research topic | Title |
| Research question | Research Question |
| Data science objective | Objective / Methodology |
| Target variable | Outcome / Dependent variable |
| Features | Predictors / Independent variables |
| ML task | Data analysis method |
| Evaluation metrics | Model evaluation |
| Bias / limitation | Limitation / Ethics |

---

## 4 Datasets จากช่วงเช้า

เลือก 1 dataset เพื่อพัฒนาต่อเป็น Proposal ช่วงบ่าย

| # | Dataset | ML Task | Target |
|---|---|---|---|
| 1 | **Patient Readmission** (500 ราย) | Classification | กลับมาใน 30 วัน (Yes/No) |
| 2 | **Nurse Burnout** (200 คน) | Regression | คะแนน Burnout (0–100) |
| 3 | **Health Screening** (300 ราย) | Classification | กลุ่มเสี่ยง (สูง/กลาง/ต่ำ) |
| 4 | **Patient Satisfaction** (300 ชุด) | NLP | Theme / Sentiment |

> หรือใช้ข้อมูลของท่านเอง — ให้เลือก **ก่อนเข้าสู่ Workshop**

---

<!-- _class: divider -->

## 02
## HIRF Framework

Applying Human Judgment and AI Assistance

---

## ทบทวน HIRF Framework

กรอบสำหรับการทำวิจัยร่วมกับ AI อย่างมีคุณภาพ

- **H** — Human judgment
- **I** — AI (Intelligent) assistance
- **R** — Research evidence
- **F** — Feedback and reflection

> ใช้ HIRF เชื่อมจาก Day 1 สู่การพัฒนา proposal

---

## ทำไมต้องใช้ HIRF กับ Proposal

- AI ช่วย**ร่างและสังเคราะห์**ได้รวดเร็ว
- นักวิจัยยังต้อง**ตัดสินใจเชิงวิชาการ**เอง
- Methodology ต้อง**ตรวจสอบได้**
- Evidence ต้อง**น่าเชื่อถือ**
- ต้องมี **reflection** ต่อ bias และ limitation

---

## Human Role vs AI Role

| ส่วนของงาน | Human | AI |
|---|---|---|
| เลือกหัวข้อ | ตัดสินใจจากปัญหาจริง | เสนอแนวทาง |
| หา gap | ประเมินความสำคัญ | ช่วยสรุป literature |
| ตั้ง RQ | ตรวจความเหมาะสม | ช่วยปรับถ้อยคำ |
| ออกแบบ method | รับผิดชอบความถูกต้อง | ช่วยเสนอทางเลือก |
| เขียน proposal | ตรวจตราความน่าเชื่อถือ | ช่วยร่างและปรับภาษา |

---

## AI Cannot Replace Research Judgment

⚠️ สิ่งที่ AI ทำได้ไม่ดีพอ:

- อาจให้ **citation ผิด**
- อาจ**สรุปเกินหลักฐาน**
- อาจสร้าง methodology ที่ **ดูดีแต่ทำจริงยาก**

✅ นักวิจัยต้องทำเอง:

- ตรวจสอบความเป็นไปได้
- แยก **"AI suggestion"** กับ **"research decision"**

---

<!-- _class: divider -->

## 03
## Mini Proposal Structure

10 Components of a Research Proposal

---

## Mini Proposal — 10 ส่วนหลัก

วันนี้ผู้เข้าอบรมจะสร้าง proposal สั้นที่มี:

1. Title
2. Background / Rationale
3. Research gap
4. Research question
5. Objectives
6. Methodology
7. AI/ML application
8. Preliminary findings
9. Ethical considerations
10. Limitations

---

## Flow ของ Mini Proposal

```
Title
  ↓
Background
  ↓
Research Gap
  ↓
Research Question
  ↓
Objectives → Methodology → AI/ML Analysis
                              ↓
                    Preliminary Findings
                              ↓
                         Contribution
```

---

## Research Title

หัวข้อที่ดีต้องมีครบ:

- บอก **population / context**
- ระบุ**ตัวแปรหรือประเด็นหลัก**
- สะท้อน **predictive / classification / analysis aim** (ถ้าใช้ ML)
- **ไม่กว้างเกินไป**

> **ตัวอย่าง:**
> Development of a Machine Learning Model for Predicting High-risk Patients Using Basic Health Indicators

---

## Background / Rationale

โครงเขียน 5 ส่วน:

1. **ปัญหา**หรือความสำคัญของเรื่อง
2. **สถานการณ์**หรือบริบท
3. **ช่องว่าง**ของความรู้
4. **เหตุผล**ที่ต้องใช้ AI/ML
5. **ประโยชน์**ที่คาดว่าจะเกิดขึ้น

> ✅ Background ที่ดีต้องมี **การทบทวนวรรณกรรม** เป็นฐานรองรับ — ไม่ใช่แค่ความเห็นส่วนตัว

---

## Background ต้องมี Literature Review ด้วย

**ทำไม Background ถึงต้องอ้างอิงงานวิจัย?**

| ถ้า Background ไม่มีอ้างอิง | ถ้า Background มี Literature |
|---|---|
| ดูเหมือนความเห็นส่วนตัว | มีน้ำหนักทางวิชาการ |
| ไม่รู้ว่ามีงานทำแล้วหรือยัง | แสดง gap ได้ชัดเจน |
| Reviewer / Committee ไม่เชื่อ | น่าเชื่อถือ ตรวจสอบได้ |
| ไม่รู้ว่าตัวเองอยู่ตรงไหนในสาขา | รู้ว่างานนี้ contribute อะไรใหม่ |

**ขั้นต่ำที่ควรมี:**
- อ้างอิงอย่างน้อย **3–5 บทความ** ที่เกี่ยวข้อง
- มีทั้ง **งานที่สนับสนุน** และ **งานที่ยังมีช่องว่าง**
- ระบุปี ผู้แต่ง และแหล่งที่มา

---

## วิธีหาเปเปอร์สำหรับ Background

**แหล่งค้นหาที่แนะนำ:**

| แหล่ง | เหมาะกับ | URL |
|---|---|---|
| **PubMed** | งานด้านสุขภาพ / คลินิก | pubmed.ncbi.nlm.nih.gov |
| **Google Scholar** | ทุกสาขา รวมถึงภาษาไทย | scholar.google.com |
| **IEEE Xplore** | งาน ML / AI เชิงเทคนิค | ieeexplore.ieee.org |
| **Semantic Scholar** | AI ช่วยค้นหาแบบ semantic | semanticscholar.org |

**Keyword Strategy:**
- ใช้คีย์เวิร์ดจาก **Research Topic + ML task**
- เช่น: `"hospital readmission" machine learning prediction`
- กรองปี: **2020–2025** สำหรับงานที่ยังทันสมัย


---

<!-- _class: divider -->

## 03.1
## Literature Lab

Google Scholar → NotebookLM → Gemini

---

## Literature Lab — ภาพรวม 3 ขั้นตอน

<div class="columns">

<div>

**ขั้นตอนการทำงาน:**

```
Step 1: ค้นหา + ดาวน์โหลด
   Google Scholar
        ↓
Step 2: จัดการความรู้
   NotebookLM (KM)
        ↓
Step 3: เขียน Background
   Gemini
```

</div>

<div>

**เป้าหมาย:**
- ได้เปเปอร์ที่เกี่ยวข้อง **3–5 บทความ**
- เข้าใจ gap ของงานที่มีอยู่
- ได้ **draft Background paragraph** พร้อมอ้างอิงที่ตรวจสอบแล้ว

**เวลา:** ~20 นาที

</div>

</div>

---

## Step 1 — ค้นหาและดาวน์โหลดเปเปอร์



<div class="columns">

<div>

**เปิด [scholar.google.com](https://scholar.google.com)**
**วิธีค้นหา:**

1. พิมพ์ keyword: `[topic] machine learning`  
   ตัวอย่าง: `"nurse burnout" machine learning prediction`
2. กรองปี: **2020 – 2025**
3. เลือกบทความที่มี **Full Text / PDF** 
4. คลิก **[PDF]** หรือ **Cite → Download**
5. ดาวน์โหลด **3–5 บทความ**

</div>

<div>

**Keyword ตาม Dataset:**

| Dataset | Keyword ตัวอย่าง |
|---|---|
| 1 Readmission | `hospital readmission prediction ML` |
| 2 Burnout | `nurse burnout workload regression` |
| 3 Health Screening | `chronic disease risk classification BMI` |
| 4 Satisfaction | `patient satisfaction NLP topic modeling` |

> 💡 ถ้าบทความไม่มี PDF ฟรี — ลองค้นใน [PubMed Central](https://pmc.ncbi.nlm.nih.gov) หรือ [Unpaywall](https://unpaywall.org)

</div>

</div>


---

## Step 2 — อัปโหลดเปเปอร์ใน NotebookLM


<div class="columns">

<div>


**เปิด [notebooklm.google.com](https://notebooklm.google.com)**

**ขั้นตอน:**

1. สร้าง **Notebook ใหม่** ชื่อหัวข้อวิจัยของท่าน
2. คลิก **Add Source → Upload PDF**
3. อัปโหลด **เปเปอร์ทั้งหมด** ที่ดาวน์โหลดมา
4. รอให้ NotebookLM **วิเคราะห์และสรุป**

> NotebookLM อ้างอิงเฉพาะเนื้อหาใน PDF ที่อัปโหลด — **ไม่สร้าง citation ปลอม**
</div>

<div>

**ถาม NotebookLM ว่า:**

```
- What are the key findings across 
these papers?
- What methods were used to 
[predict/classify/analyze] [topic]?
-What gaps or limitations do the 
authors mention?
-Which paper is most relevant to 
[your research question]?
```

</div>

</div>



---

## Step 2 (ต่อ) — สกัด Gap จาก NotebookLM

<div class="columns">

<div>

**คำถามที่ควรถาม NotebookLM เพื่อหา Research Gap:**

```
Based on all the papers I uploaded:
1. What is the most common research gap mentioned?
2. Which populations or settings are underrepresented?
3. What ML methods have NOT been applied to this topic yet?
4. What outcome variables are rarely studied?

Summarize in 3–5 bullet points.
```

</div>

<div>

**ผลที่ได้:**
- รายการ gap ที่สกัดจากงานจริง ไม่ใช่ความเห็นส่วนตัว
- ข้อมูลพร้อมระบุแหล่งที่มา (ชื่อ paper ที่อัปโหลด)
- พร้อมนำไปเขียน Background และ Research Gap section

</div>
</div>

---

## Step 3 — เขียน Background ด้วย Gemini

**เปิด [gemini.google.com](https://gemini.google.com) เปิดเข้าไป NotebookLM** ใช้ Prompt สำหรับเขียน Background:

```
I am writing a research proposal on [topic]. My research question is: [RQ].
Based on these findings from related literature. Please write a Background/Rationale 
paragraph (150–200 words) that:
1. Introduces the problem and its significance
2. Summarizes what previous studies have found
3. Identifies the research gap
4. Justifies why ML is appropriate for this study
5. Ends with the purpose of this study
Use academic English. Include in-text citations in APA format using the paper titles I 
described. I will verify and update all citations manually.
```

---

## Step 3 (ต่อ) — ตรวจสอบและปรับแก้

**หลังได้ Background draft จาก Gemini:**

<div class="columns">

<div>

**ต้องตรวจสอบทุกครั้ง:**

- ☐ Citation ทุกตัวมีอยู่จริงใน paper ที่อัปโหลด
- ☐ ตัวเลขและสถิติถูกต้อง
- ☐ Gap ที่ระบุสอดคล้องกับ RQ ของท่าน
- ☐ ไม่กล่าวเกินจริงกว่าที่ paper ระบุ
- ☐ ความยาวเหมาะสม (ไม่ยาวหรือสั้นเกินไป)

</div>

<div>

**ปรับ Prompt ถ้าผลยังไม่ดี:**

```
The background is too general.
Please make it more specific to 
[ML task] for [population/setting].
Emphasize the gap related to 
[specific gap from NotebookLM].
```

</div>

</div>

> ✅ เมื่อ Background ผ่านการตรวจแล้ว — นำไปใส่ใน Mini Proposal Canvas

---

## สรุป Literature Lab — 3 เครื่องมือ 3 บทบาท

| เครื่องมือ | บทบาท | Output |
|---|---|---|
| **Google Scholar** | ค้นหาและดาวน์โหลดเปเปอร์จริง | PDF 3–5 บทความ |
| **NotebookLM** | KM — ถามและสกัดความรู้จาก paper | สรุป findings + gap |
| **Gemini** | เขียน Background draft | paragraph พร้อมอ้างอิง |


| HIRF | บทบาทในขั้นตอนนี้ |
|---|---|
| **H** — Human | เลือก keyword, ตรวจ paper, ยืนยัน citation |
| **I** — AI | NotebookLM สรุป, Gemini ร่างเนื้อหา |
| **R** — Research Evidence | PDF จาก Google Scholar เป็นฐาน |
| **F** — Feedback | ตรวจสอบและปรับแก้ก่อนใช้จริง |

---

## ตัวอย่าง Background พร้อม Literature — Dataset 1

**หัวข้อ:** การทำนาย 30-Day Readmission ด้วย Machine Learning

> *Hospital readmission within 30 days is a major quality indicator and cost burden globally. Studies have shown that 15–20% of patients are readmitted within 30 days of discharge (Jencks et al., 2009). Machine learning models have demonstrated promising results in predicting readmission risk, with Logistic Regression and Random Forest achieving AUC > 0.70 in several studies (Frizzell et al., 2017; Mortazavi et al., 2016). However, most existing models rely on EHR data from large academic hospitals in high-income countries, limiting their applicability to community hospital settings. This study aims to address this gap by developing a prediction model using routinely available clinical data from [setting].*

**Gap ที่ระบุ:** งานส่วนใหญ่ทำในโรงพยาบาลใหญ่ในประเทศรายได้สูง — ยังขาดหลักฐานสำหรับบริบทโรงพยาบาลชุมชน

---

## ตัวอย่าง Background พร้อม Literature — Dataset 2

**หัวข้อ:** ปัจจัยทำนายคะแนน Burnout ของพยาบาล

> *Nurse burnout is a persistent challenge affecting healthcare quality and workforce retention. High patient-to-nurse ratios and excessive working hours have been consistently linked to elevated burnout scores (Aiken et al., 2014). Predictive models using regression techniques have begun to explore which workload factors most strongly predict burnout severity (Dall'Ora et al., 2020). Despite this, few studies have examined the combined effect of workload and organizational support on burnout in Southeast Asian hospital settings. This study addresses this gap using regression modeling on survey data from [setting].*

**Gap ที่ระบุ:** ขาดการศึกษาในบริบทเอเชียตะวันออกเฉียงใต้ที่พิจารณาทั้ง workload และ organizational support

---

## ตัวอย่าง Background พร้อม Literature — Dataset 3

**หัวข้อ:** การจำแนกกลุ่มเสี่ยงโรคจากผลตรวจสุขภาพประจำปี

> *Annual health screenings provide an opportunity for early identification of chronic disease risk. Studies have applied machine learning to classify individuals into risk groups using BMI, glucose, and blood pressure (Zou et al., 2018; Islam et al., 2020). However, exercise behavior and family history are rarely integrated as predictors in existing models. This study proposes a multi-class risk classification model incorporating these underexplored variables to improve early identification of at-risk individuals in community health settings.*

**Gap ที่ระบุ:** โมเดลส่วนใหญ่ใช้เพียงตัวแปรทางคลินิก — ยังขาดการรวมพฤติกรรมสุขภาพและประวัติครอบครัว

---

## ตัวอย่าง Background พร้อม Literature — Dataset 4

**หัวข้อ:** การวิเคราะห์ความคิดเห็นผู้รับบริการด้วย NLP

> *Patient satisfaction is increasingly recognized as a key dimension of healthcare quality and a driver of service improvement. Open-ended survey responses contain rich qualitative data, but are often underanalyzed due to the limitations of manual review. NLP approaches such as LDA topic modeling have been used to extract recurring themes from patient feedback (Doing-Harris et al., 2017; Greaves et al., 2013). However, few studies have applied NLP to Thai-language patient feedback in hospital settings. This study applies topic modeling and sentiment analysis to identify key themes and satisfaction patterns from survey data at [setting].*

**Gap ที่ระบุ:** ยังขาดการนำ NLP ไปใช้กับข้อมูลความคิดเห็นภาษาไทยในบริบทโรงพยาบาล

---

## Research Gap — 3 ประเภท

| ประเภท Gap | ความหมาย |
|---|---|
| Knowledge gap | ยังไม่มีองค์ความรู้เพียงพอ |
| Methodological gap | วิธีเดิมยังมีข้อจำกัด |
| Practical gap | ยังไม่มีเครื่องมือหรือแนวทางใช้จริง |

> ระบุให้ชัดว่า proposal นี้แก้ gap ประเภทใด

---

## Research Question

ตัวอย่างโครงประโยคที่ใช้บ่อย:

- What **factors** are associated with …?
- Can machine learning **predict** …?
- How accurately can a model **classify** …?
- What **patterns** can be identified from …?
- What **themes** emerge from …?

---

## Research Objectives

ต้องมี **2 ระดับ** เสมอ:

### Research Objective
เพื่อศึกษาหรือวิเคราะห์ปัญหาวิจัย

### Data Science Objective
เพื่อพัฒนาโมเดลหรือวิเคราะห์ข้อมูลด้วย ML

> To examine factors associated with patient risk.
> To develop a classification model for identifying high-risk patients.

---

<!-- _class: divider -->

## 04
## Methodology & ML Application

Designing a Rigorous ML-based Research Method

---

## Methodology Overview

องค์ประกอบที่ต้องระบุใน proposal:

- Research design
- Population / sample
- Dataset
- Variables
- Data preprocessing
- ML model
- Model evaluation
- Interpretation

---

## Dataset and Variables

| องค์ประกอบ | ตัวอย่าง |
|---|---|
| Unit of analysis | ผู้ป่วย 1 คน |
| Target variable | Risk group |
| Features | age, BMI, glucose, blood pressure |
| Data source | เวชระเบียน / แบบสอบถาม / public dataset |
| Sample size | จำนวนข้อมูลที่คาดว่าจะใช้ |

---

## Data Analysis Plan — ลำดับขั้นตอน

1. Data cleaning
2. Feature selection
3. Train / test split
4. Model training
5. Model evaluation
6. Interpretation
7. Reporting

---

## Candidate ML Models

| ML Task | Possible Models |
|---|---|
| Regression | Linear Regression, Random Forest Regressor |
| Classification | Logistic Regression, Decision Tree, Random Forest |
| Clustering | K-means, Hierarchical Clustering |
| NLP | Text classification, topic modeling, sentiment analysis |

---

## Evaluation Metrics

| ML Task | Metrics |
|---|---|
| Regression | MAE, RMSE, R² |
| Classification | Accuracy, Precision, Recall, F1-score |
| Clustering | Cluster profile, Silhouette score |
| NLP | Accuracy, F1-score, topic coherence, human validation |

---

## Writing ML Methodology Paragraph

**Template:**

> This study will use a machine learning approach to **[predict/classify/analyze]** [target].
> The dataset will include **[data source]** with variables such as **[features]**.
> Candidate models will include **[models]**.
> Model performance will be evaluated using **[metrics]**.
> Potential limitations include **[limitations]**.

---

## ตัวอย่าง Methodology — Dataset 1: Patient Readmission

> *"This study will develop a **binary classification model** to predict 30-day hospital readmission. The dataset includes 500 patient records with features such as age, gender, primary diagnosis, number of comorbidities, and length of previous stay. Candidate models include Logistic Regression and Random Forest. Model performance will be evaluated using **Recall and F1-score**, prioritizing sensitivity for high-risk patients. Potential limitations include class imbalance and limited generalizability to other hospital settings."*

| Component | Value |
|---|---|
| ML Task | Binary Classification |
| Target | Readmission: Yes / No |
| Key Metrics | Recall, F1-score |
| Main Limitation | Class imbalance, generalizability |

---

## ตัวอย่าง Methodology — Dataset 2: Nurse Burnout

> *"This study will apply a **regression model** to predict nurse burnout scores based on workload indicators. The dataset includes 200 nursing staff records with features including weekly working hours, number of patients managed, and organizational support scores. Candidate models include Linear Regression and Random Forest Regressor. Model performance will be evaluated using **MAE and R²**. Potential limitations include self-reported bias and small sample size."*

| Component | Value |
|---|---|
| ML Task | Regression |
| Target | Burnout Score (0–100) |
| Key Metrics | MAE, R² |
| Main Limitation | Self-report bias, n=200 |

---

## ตัวอย่าง Methodology — Dataset 3: Health Screening

> *"This study will develop a **multi-class classification model** to identify disease risk levels (High/Medium/Low) from annual health screening data. The dataset includes 300 records with features such as BMI, fasting glucose, blood pressure, exercise behavior, and family history. Candidate models include Decision Tree and Random Forest. Model performance will be evaluated using **Accuracy and macro F1-score**. Potential limitations include self-reported lifestyle data and cross-sectional design."*

| Component | Value |
|---|---|
| ML Task | Multi-class Classification |
| Target | Risk Group (High/Medium/Low) |
| Key Metrics | Accuracy, macro F1-score |
| Main Limitation | Self-reported lifestyle data |

---

## ตัวอย่าง Methodology — Dataset 4: Patient Satisfaction

> *"This study will apply **NLP and topic modeling** to analyze open-ended patient satisfaction survey responses. The dataset includes 300 survey records with free-text feedback on treatment, service, and suggestions. LDA topic modeling and sentiment analysis will be used to extract themes and sentiment direction. Evaluation will use **topic coherence scores and human validation**. Potential limitations include language variation and subjective interpretation of themes."*

| Component | Value |
|---|---|
| ML Task | NLP / Text Mining |
| Target | Themes & Sentiment |
| Key Metrics | Coherence score, human validation |
| Main Limitation | Language variation, subjectivity |

---

<!-- _class: divider -->

## 05
## Preliminary Findings

Presenting Early Evidence Responsibly

---

## Preliminary Findings คืออะไร?

- ผลการศึกษา**เบื้องต้น** — ยังไม่ใช่ final results
- ใช้เพื่อแสดง**ความเป็นไปได้**ของงานวิจัย
- อาจมาจาก: literature, pilot data, public data, simulated data หรือ ML lab

---

## ประเภทของ Preliminary Findings

| ประเภท | ตัวอย่าง |
|---|---|
| Literature-based | สรุปแนวโน้มจากงานวิจัยเดิม |
| Data-based | ตารางหรือกราฟจากข้อมูลเบื้องต้น |
| ML-based | performance เบื้องต้นของโมเดล |
| Conceptual | กรอบแนวคิดหรือ pattern |
| AI-assisted synthesis | สังเคราะห์จากเอกสาร (ตรวจสอบแหล่งอ้างอิง) |

---

## Preliminary Findings จาก ML Lab

ตัวอย่างผลเบื้องต้น:

- Model achieved **acceptable initial classification** performance
- **Recall** is important for detecting high-risk cases
- Some features may **contribute more strongly** than others
- Results require **further validation**

> ⚠️ ถ้าใช้ข้อมูลจำลอง ต้องระบุว่าเป็น **simulated data**

---

## ตัวอย่าง Preliminary Findings ตาม Dataset

| Dataset | ตัวอย่าง Preliminary Finding |
|---|---|
| **1 — Readmission** | Initial classification model achieved Recall = 0.78 for high-risk patients, suggesting feasibility of early identification |
| **2 — Nurse Burnout** | Regression analysis indicates working hours and patient load are strongly associated with burnout score (R² preliminary = 0.61) |
| **3 — Health Screening** | Multi-class model shows BMI and fasting glucose as top predictors of high-risk group; accuracy = 0.74 in pilot run |
| **4 — Patient Satisfaction** | Topic modeling identified 4 recurring themes: waiting time, staff communication, facility, and follow-up care |

> ⚠️ ผลข้างต้นมาจาก **simulated / preliminary analysis** — ต้องระบุชัดเจนใน proposal

---

## การเขียน Preliminary Findings อย่างปลอดภัย

✅ **ควรใช้:**
- Preliminary results **suggest** that …
- Initial analysis **indicates** that …
- Simulated analysis **demonstrates the feasibility** of …
- Further validation **is required** …

❌ **ไม่ควรใช้:**
- This study **proves** that …
- The model **confirms** that …
- AI **found the true cause** of …

---

<!-- _class: divider -->

## 06
## Workshop

Mini Research Proposal Development

---

## Workshop Task — เลือก Dataset ของท่าน

ใช้ Dataset จากช่วงเช้าเพื่อพัฒนา Mini Proposal

| # | Dataset | ML Task | เหมาะกับ |
|---|---|---|---|
| **1** | Patient Readmission (500 ราย) | Classification | งานวิจัยคลินิก / ระบาดวิทยา |
| **2** | Nurse Burnout (200 คน) | Regression | งานวิจัยด้านบุคลากร / สุขภาพจิต |
| **3** | Health Screening (300 ราย) | Classification | งานส่งเสริมสุขภาพ / ป้องกันโรค |
| **4** | Patient Satisfaction (300 ชุด) | NLP | งานวิจัยเชิงคุณภาพ / บริการสุขภาพ |
| **5** | **ข้อมูลของท่านเอง** | ตามที่ออกแบบ | ทุกสาขา |

> **เลือก 1 แนวทางก่อนเริ่ม Workshop** — ทุก dataset มีผล Lab จากช่วงเช้าแล้ว

---

## Mini Proposal Canvas

**Dataset ที่เลือก:** ☐ 1-Readmission  ☐ 2-Burnout  ☐ 3-Health Screening  ☐ 4-Satisfaction  ☐ ข้อมูลเอง

| Section | Your Draft |
|---|---|
| Title | |
| Background | |
| Research Gap | |
| Research Question | |
| Methodology | |
| AI/ML Application | |
| Preliminary Findings | |
| Ethics / Limitation | |

---

## Prompt สำหรับร่าง Proposal

```
Act as a research methodology advisor. I am developing a mini research proposal using 
[Dataset 1/2/3/4 name]. My research question is [research question]. The data science objective is [objective]. The ML task is 
[classification/regression/NLP]. The target variable is [target]. Key features include[feat].
I already have a verified Background paragraph from my literature review:
[วาง Background draft ที่ได้จาก Literature Lab ที่นี่]
The research gap identified from my literature review is:
[วาง gap ที่สกัดจาก NotebookLM ที่นี่]
Using the Background and gap above as the foundation, please help me draft
the remaining sections of a mini proposal: title, research gap, research question, objectives, 
methodology, AI/ML application, preliminary findings, ethical considerations, and limitations.
Do NOT rewrite the Background — use it as provided.
```

---

## Prompt สำหรับตรวจ Alignment

```
Please review the following mini research proposal.
Check whether the title, research gap, research question,
objectives, methodology, AI/ML application, and
preliminary findings are logically aligned.
Identify inconsistencies and suggest improvements.
```

---

## Proposal Alignment Checklist

| Checkpoint | ✓ |
|---|---|
| Title สอดคล้องกับ RQ | |
| Gap ชัดเจน | |
| RQ ตอบได้ด้วย method ที่เลือก | |
| Objective สอดคล้องกับ RQ | |
| ML task เหมาะกับ target | |
| Dataset มีความเป็นไปได้ | |
| Metrics เหมาะกับโจทย์ | |
| Preliminary findings ไม่กล่าวเกินจริง | |
| Ethics และ limitation ระบุชัดเจน | |

---

<!-- _class: divider -->

## 07
## Process Reflection & Sharing

Reflecting on AI-Assisted Proposal Writing

---

## ทำไมถึงเน้น Process ไม่ใช่ Proposal

> Proposal ที่สร้างวันนี้ยังต้องผ่านการตรวจสอบอีกมาก
> สิ่งที่มีคุณค่ากว่า คือ **กระบวนการทำงานร่วมกับ AI**

- Proposal ต้องการ: เวลา ข้อมูลจริง ผู้เชี่ยวชาญตรวจสอบ
- Process สามารถ**นำกลับไปใช้ใหม่**ได้ทันที
- การสะท้อน process ช่วยพัฒนา**ทักษะ AI-assisted research** ได้จริง

---

## โครงการนำเสนอ — 2 ส่วน

**ส่วนที่ 1 (2 นาที): Mini Proposal**
นำเสนอ proposal ที่สร้างด้วย AI

**ส่วนที่ 2 (2 นาที): Process Reflection**
สะท้อนกระบวนการทำงาน

> เน้น**วิธีการทำงานกับ AI** มากกว่าความสมบูรณ์ของ proposal
> เพราะ proposal ยังต้องผ่านการตรวจสอบอีกพอสมควร

---

## ส่วนที่ 1 — Mini Proposal Pitch (2 นาที)

นำเสนอสั้นๆ ครอบคลุม 5 ประเด็น:

1. **Dataset & Research topic** — ใช้ข้อมูลอะไร เรื่องอะไร
2. **Research gap** — ช่องว่างที่พบจาก Literature Lab
3. **Research question** — คำถามวิจัย
4. **ML approach** — วิธีและโมเดลที่เลือก
5. **Preliminary findings** — ผลเบื้องต้นจาก ML Lab

> ⚠️ ไม่จำเป็นต้องสมบูรณ์ — proposal นี้คือ **draft** ที่ยังต้องตรวจสอบ

---

## ส่วนที่ 2 — Process Reflection (2 นาที)

เล่า **กระบวนการทำงานกับ AI** ที่ผ่านมา:

1. **เครื่องมือที่ใช้** — Google Scholar / NotebookLM / Gemini / อื่นๆ
2. **ขั้นตอนที่ได้ผลดีที่สุด** — อะไรทำให้งานเร็วขึ้นหรือดีขึ้น
3. **ขั้นตอนที่ยังติดขัด** — AI ช่วยได้ไม่พอ หรือต้องปรับมาก
4. **สิ่งที่จะเปลี่ยนถ้าทำใหม่** — จะปรับ prompt หรือ workflow อย่างไร

---

## Reflection Canvas — ประเมินกระบวนการ

| ขั้นตอน | ได้ผลดี ✓ | ยังติดขัด ✗ | จะปรับอย่างไร |
|---|---|---|---|
| ค้นหา paper (Google Scholar) | | | |
| สกัด gap (NotebookLM) | | | |
| เขียน Background (Gemini) | | | |
| ร่าง Proposal sections (AI) | | | |
| ตรวจสอบความถูกต้อง (Human) | | | |

---

## จุดดีของการใช้ AI ในกระบวนการนี้

**สิ่งที่ AI ช่วยได้จริง:**

- ร่างโครงสร้างและภาษาได้รวดเร็ว
- ช่วยให้เห็น **ภาพรวมของ proposal** ก่อนลงรายละเอียด
- สกัด gap จาก paper หลายเล่มพร้อมกัน
- ปรับ tone และ academic language ได้ดี

> ✅ AI ช่วยให้**เริ่มต้นได้เร็วขึ้น** และ**ไม่ติดหน้ากระดาษเปล่า**

---

## จุดที่ต้องระวัง — AI ยังทำได้ไม่พอ

**สิ่งที่ยังต้องตรวจสอบเอง:**

- Citation ที่ AI สร้าง — อาจไม่มีอยู่จริง
- ตัวเลขและสถิติ — ต้องยืนยันจาก paper ต้นฉบับ
- Methodology ที่ดูสมบูรณ์ — อาจทำจริงไม่ได้ในบริบทของท่าน
- Research gap — AI อาจเสนอ gap ที่ไม่ตรงกับความเป็นจริง

> ⚠️ Proposal ที่ได้วันนี้คือ **draft เริ่มต้น** — ยังต้องผ่านการตรวจสอบและปรับปรุง

---

## ข้อเสนอแนะปรับปรุง Workflow

**คำถามสำหรับแลกเปลี่ยน:**

- Prompt ไหนที่ได้ผลดีที่สุดในกลุ่มของท่าน?
- ขั้นตอนไหนที่ใช้เวลานานที่สุด — ทำไม?
- ถ้าจะนำ workflow นี้ไปใช้กับงานวิจัยจริง จะปรับอะไร?
- ต้องการทักษะ / ความรู้อะไรเพิ่มเติม?

---

## Feedback Method: TAG (สำหรับ Process)

| TAG | ใช้กับ Process อย่างไร |
|---|---|
| **T** = Tell | บอก**ขั้นตอนที่ได้ผลดีที่สุด**ในกลุ่มของท่าน |
| **A** = Ask | ถาม**ขั้นตอนที่ยังไม่แน่ใจ**หรือต้องการ clarify |
| **G** = Give | ให้**ข้อเสนอแนะ workflow** ที่จะนำไปปรับใช้

---

<!-- _class: lead -->

# Afternoon Deliverables

สิ่งที่ได้เมื่อจบช่วงบ่าย:

1. **Mini Proposal Draft** — โครงสร้างครบ พร้อมตรวจสอบต่อ
2. **Background พร้อม Literature** — จาก Literature Lab
3. **Reflection Canvas** — ประเมินกระบวนการ AI-assisted
4. **Workflow ที่จะนำไปปรับใช้** — จากการแลกเปลี่ยนกลุ่ม
5. **แผนตรวจสอบ Proposal** — สำหรับนำไปพัฒนาต่อ
