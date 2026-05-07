---
marp: true
theme: mahidol-green
paginate: true
size: 16:9
footer: "AI for Research | Day 2 Afternoon — From ML Lab to Research Proposal"
---

<!-- _class: lead -->

<style scoped>
img { position: absolute; top: 36px; right: 64px; width: 150px; height: 150px; object-fit: contain; }
</style>

<img src="fig/logos/mahidol.svg" alt="Mahidol University">

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
7. **Presentation & Feedback** — นำเสนอและรับ feedback

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

## Workshop Task — เลือก 1 แนวทาง

### Option A: ใช้หัวข้อวิจัยของตนเอง
เหมาะกับคนที่มี proposal หรือ dataset แล้ว

### Option B: เลือกโจทย์ตัวอย่าง
เหมาะกับคนที่ยังไม่มีหัวข้อ

### Option C: ใช้ผลจาก Python Lab ช่วงเช้า
เหมาะกับคนที่ต้องการต่อยอดจากกิจกรรม ML

---

## Mini Proposal Canvas

| Section | Your Draft |
|---|---|
| Title | |
| Background | |
| Research Gap | |
| Research Question | |
| Research Objective | |
| Data Science Objective | |
| Methodology | |
| AI/ML Application | |
| Preliminary Findings | |
| Ethics / Limitation | |

---

## Prompt สำหรับร่าง Proposal

```
Act as a research methodology advisor.
I am developing a mini research proposal on [topic].
My research question is [research question].
The data science objective is [objective].
Please help me draft a mini proposal including:
title, background, research gap, research question,
objectives, methodology, AI/ML application,
preliminary findings, ethical considerations,
and limitations.
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
## Presentation & Feedback

3-Minute Pitch and Peer Review

---

## 3-Minute Mini Proposal Pitch

โครงนำเสนอ 3 นาที:

1. **Title** — หัวข้อวิจัย
2. **Research gap** — ช่องว่างที่พบ
3. **Research question** — คำถามวิจัย
4. **Objectives** — เป้าหมาย
5. **Methodology** — วิธีการ
6. **AI/ML application** — การใช้ ML
7. **Preliminary findings** — ผลเบื้องต้น
8. **Expected contribution** — ประโยชน์ที่คาดหวัง

---

## Feedback Method: TAG

| TAG | ความหมาย |
|---|---|
| **T** = Tell | บอก**จุดแข็ง**ที่ชัดเจน |
| **A** = Ask | ถาม**จุดที่ยังไม่ชัด** |
| **G** = Give | ให้**ข้อเสนอแนะ**เพื่อปรับปรุง |

---

## Mini Proposal Rubric

| Criteria | Excellent | Good | Needs Work |
|---|---|---|---|
| Clarity of title | ชัดและตรงประเด็น | พอเข้าใจ | กว้างหรือคลุมเครือ |
| Research gap | มีเหตุผล | มีแต่ยังไม่ชัด | ยังไม่เห็น gap |
| RQ/Objectives | สอดคล้องดี | สอดคล้องบางส่วน | ไม่สัมพันธ์กัน |
| Methodology | เหมาะกับโจทย์ | ต้องปรับบางจุด | ยังไม่เหมาะ |
| AI/ML use | มีเหตุผล | ยังอธิบายไม่พอ | ใช้แบบไม่จำเป็น |
| Preliminary findings | ระบุแหล่งที่มา | มีแต่ยังไม่ชัด | กล่าวเกินจริง |

---

## Final Refinement หลัง Feedback

ปรับปรุง 6 จุด:

1. **Title** — ให้ตรงกับเนื้อหา
2. **RQ / Objectives** — ให้สอดคล้องกัน
3. **Methodology** — ให้เหมาะกับโจทย์
4. **AI/ML application** — ให้มีเหตุผลชัดเจน
5. **Preliminary findings** — ไม่กล่าวเกินจริง
6. **Limitation** — ระบุให้ครบ

---

<!-- _class: lead -->

# Afternoon Deliverables

สิ่งที่ได้เมื่อจบช่วงบ่าย:

1. **Mini Research Proposal** — ฉบับสมบูรณ์
2. **ML-based Methodology section** — พร้อมใช้
3. **Preliminary Findings** — 1 ชิ้น
4. **Feedback** — จากเพื่อนหรือวิทยากร
5. **แผนปรับปรุง** — สำหรับ Day 3
