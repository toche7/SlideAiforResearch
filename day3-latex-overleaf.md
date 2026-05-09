---
marp: true
theme: mahidol-green
paginate: true
size: 16:9
footer: "LaTeX for Research & Proposal Workshop | AI for Research Day 3"
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

# LaTeX for Research Papers

<div class="subtitle">Day 3 — Morning & Afternoon Session</div>

**จาก Mini Proposal สู่ Academic Paper ด้วย LaTeX & Overleaf**

---

## ภาพรวม Day 3

<div class="columns">

<div>

**ช่วงเช้า — LaTeX & Overleaf**

1. **Why LaTeX** — ทำไมนักวิจัยต้องรู้จัก LaTeX
2. **Overleaf** — แพลตฟอร์มเขียน LaTeX บน Cloud
3. **Document Structure** — โครงสร้างของ LaTeX 
4. **Writing Sections** — Abstract, Introduction, Methods, Results
5. **Tables & Figures** — การใช้ตารางและรูปภาพ
6. **Bibliography** — การจัดการ reference ด้วย BibTeX

</div>
<div>

**ช่วงบ่าย — Workshop: Mini Proposal → Elsevier Paper**

7. **Elsevier Template** — ใช้ template จริงของวารสาร
8. **Mapping** — แปลง proposal เป็น paper sections
9. **Workshop** — ลงมือเขียนด้วย AI + LaTeX
</div>
</div>


---

<!-- _class: divider -->

## 01
## Why LaTeX?

The Standard for Academic Publishing

---

## LaTeX คืออะไร?

- **LaTeX** คือ typesetting system สำหรับสร้างเอกสารคุณภาพสูง
- ใช้กันอย่างแพร่หลายใน: คณิตศาสตร์, ฟิสิกส์, วิศวกรรม, **งานวิจัยทางการแพทย์**
- วารสารชั้นนำส่วนใหญ่รับ submission เป็น LaTeX

> **ต่างจาก Word ตรงไหน?**
> Word = WYSIWYG (เห็นอะไรได้อย่างนั้น)
> LaTeX = เขียนคำสั่ง → system จัดหน้าให้อัตโนมัติ

---

## ทำไมนักวิจัยต้องรู้จัก LaTeX

| เรื่อง | Microsoft Word | LaTeX |
|---|---|---|
| สมการคณิตศาสตร์ | ยุ่งยาก | สวยงาม ง่ายมาก |
| Reference management | Manual / Mendeley Plugin | BibTeX — อัตโนมัติ |
| Journal template | ต้องปรับเอง | ใช้ `.cls` ของวารสาร |
| Version control | ยาก | Git-friendly (plain text) |
| ความสม่ำเสมอ | ต้องระวัง | System จัดการเอง |
| ขนาดไฟล์ | ใหญ่ | เล็กมาก |

---

## วารสารที่ใช้ LaTeX Template

| วารสาร / Publisher | Template |
|---|---|
| **Elsevier** (Lancet, JAMDA, etc.) | `elsarticle.cls` |
| **Springer** (Nature journals) | `svjour3.cls` |
| **IEEE** (engineering/AI) | `IEEEtran.cls` |
| **PLOS ONE** | Custom Overleaf template |
| **BMJ, JAMA** | Custom submission format |

> ✅ วันนี้เราจะใช้ **Elsevier template** — ครอบคลุมวารสารด้านสุขภาพ/คลินิก

---

## LaTeX กับ AI — ทำงานร่วมกันได้ดี

- AI (Gemini / ChatGPT) สามารถ**เขียน LaTeX code** ได้
- สามารถขอ AI **แปลง text เป็น LaTeX** ทันที
- AI ช่วย **debug LaTeX errors** ได้
- ผลลัพธ์ที่ได้: PDF คุณภาพระดับ journal-ready

> **Workflow ใหม่:**
> AI ช่วยเขียนเนื้อหา → LaTeX จัดรูปแบบ → Overleaf compile → Submit

---

<!-- _class: divider -->

## 02
## Overleaf

LaTeX บน Cloud — ไม่ต้องติดตั้ง

---

## Overleaf คืออะไร?

- **[overleaf.com](https://www.overleaf.com)** — LaTeX editor บน web browser
- ไม่ต้องติดตั้งโปรแกรมบนเครื่อง
- Compile อัตโนมัติ — เห็นผล PDF ทันที
- มี **template library** จากวารสารชั้นนำ
- รองรับ **collaboration** — เขียนร่วมกันได้เหมือน Google Docs

> ✅ เหมาะสำหรับผู้เริ่มต้น LaTeX — ไม่ต้องกังวลเรื่อง configuration

---

## เริ่มต้นกับ Overleaf

**ขั้นตอนการสมัครและเริ่มต้น:**

1. ไปที่ **[overleaf.com](https://www.overleaf.com)**
2. คลิก **Register** — ใช้ email มหาวิทยาลัย (มี plan พิเศษ)
3. คลิก **New Project** → **Blank Project** หรือ **From Template**
4. ตั้งชื่อ project ตามหัวข้อวิจัย
5. เริ่มเขียนใน editor ด้านซ้าย — PDF แสดงด้านขวา

---

## Overleaf Interface

<div class="columns">

<div>

**Panel ซ้าย: Editor**
- เขียน LaTeX code
- จัดการไฟล์ใน project
- อัปโหลดรูปและ bib file

**Panel ขวา: PDF Preview**
- เห็นผลลัพธ์ทันทีหลัง compile
- Download PDF ได้ตลอด

</div>

<div>

**Menu สำคัญ:**

- **Recompile** — อัปเดต PDF
- **Share** — เชิญผู้ร่วมงาน
- **History** — ดู version เก่า
- **Menu → Compiler** — เลือก pdfLaTeX / XeLaTeX

> ✅ ใช้ **XeLaTeX** ถ้าต้องการรองรับภาษาไทยหรือ Unicode

</div>

</div>

---

## เปิด Elsevier Template ใน Overleaf

**วิธีที่ 1 — จาก Overleaf Template Gallery:**

1. ไปที่ **overleaf.com/gallery**
2. ค้นหา **"Elsevier"**
3. คลิก **"Elsevier - LaTeX Template for Journal Articles"**
4. คลิก **"Open as Template"**

**วิธีที่ 2 — จาก Elsevier โดยตรง:**

1. ไปที่ **[elsevier.com/authors/tools-and-resources/latex](https://www.elsevier.com/authors/tools-and-resources/latex)**
2. Download **elsarticle package**
3. Upload ไปยัง Overleaf project

---

<!-- _class: divider -->

## 03
## LaTeX Document Structure

ทำความเข้าใจโครงสร้างเอกสาร

---

## โครงสร้าง LaTeX Document

<!-- _class: dense -->
```latex
\documentclass[...]{elsarticle}   % ประกาศประเภทเอกสาร
\usepackage{...}                   % โหลด packages

\begin{document}                   % เริ่มเนื้อหา

  \begin{frontmatter}              % ส่วนหน้า
    \title{...}
    \author{...}
    \begin{abstract}...\end{abstract}
    \begin{keyword}...\end{keyword}
  \end{frontmatter}

  \section{Introduction}           % บทนำ
  \section{Methods}                % วิธีการ
  \section{Results}                % ผลลัพธ์
  \section{Discussion}             % อภิปราย
  \bibliography{references}        % บรรณานุกรม
\end{document}
```

---

## Elsevier Template — Frontmatter
<!-- _class: dense -->
```latex
\begin{frontmatter}
\title{Predicting 30-Day Hospital Readmission Using Machine Learning: A Retrospective Study}
\author[1]{First Author}
\author[2]{Second Author}
\address[1]{Faculty of Medicine, Mahidol University, Bangkok, Thailand}
\address[2]{Department of Biomedical Informatics, ...}
\begin{abstract}
  Background: ...
  Objective: ...
  Methods: ...
  Results: ...
  Conclusion: ...
\end{abstract}
\begin{keyword}
  machine learning \sep hospital readmission \sep 
  classification \sep healthcare informatics
\end{keyword}
\end{frontmatter}
```

---

## คำสั่ง LaTeX พื้นฐานที่ใช้บ่อย

| คำสั่ง | ผลลัพธ์ |
|---|---|
| `\textbf{text}` | **ตัวหนา** |
| `\textit{text}` | *ตัวเอียง* |
| `\section{Title}` | หัวข้อหลัก |
| `\subsection{Title}` | หัวข้อรอง |
| `\cite{key}` | อ้างอิง [1] |
| `\ref{label}` | อ้างถึง Table 1 |
| `\% comment` | comment (ไม่แสดงผล) |
| `\\` | ขึ้นบรรทัดใหม่ |
| `~` | non-breaking space |

---

<!-- _class: divider -->

## 04
## Writing Paper Sections

Abstract · Introduction · Methods · Results · Discussion

---

## Abstract — โครงสร้างสำหรับงาน ML

Abstract ที่ดีสำหรับงาน ML มี 5 ส่วน:

1. **Background** — ปัญหาและความสำคัญ
2. **Objective** — เป้าหมายของการศึกษา
3. **Methods** — ข้อมูล + ML model ที่ใช้
4. **Results** — ตัวเลขสำคัญจากโมเดล
5. **Conclusion** — ข้อสรุปและนัยสำคัญ

> ✅ Abstract ต้อง **ยืนหยัดได้ด้วยตัวเอง** — อ่านแล้วเข้าใจงานทั้งหมด
> ❌ ไม่ควรมี citation ใน abstract

---

## Abstract ใน LaTeX
<!-- _class: dense -->
```latex
\begin{abstract}
\textbf{Background:} Hospital readmission within 30 days 
represents a significant quality and cost burden in healthcare.
Existing prediction tools often rely on complex clinical data 
unavailable in community hospital settings.
\textbf{Objective:} To develop a machine learning model for 
predicting 30-day readmission using routinely available 
clinical variables.
\textbf{Methods:} A retrospective dataset of 500 patient 
records was analyzed. Logistic Regression and Random Forest 
classifiers were compared using Recall and F1-score.
\textbf{Results:} The Random Forest model achieved Recall 
of 0.78 and F1-score of 0.74 on the test set.
\textbf{Conclusion:} Machine learning models using basic 
clinical variables can feasibly identify high-risk patients 
for early intervention.
\end{abstract}
```

---

## Introduction — CARS Model

**C**reate a **R**esearch **S**pace (Swales, 1990)

| Move | เนื้อหา | ตัวอย่าง |
|---|---|---|
| **Move 1** | Establish territory | "Hospital readmission is a major challenge..." |
| **Move 2** | Establish niche (Gap) | "However, most models require EHR data..." |
| **Move 3** | Occupy the niche | "This study aims to develop a model using..." |

> ✅ Introduction ที่ดีต้อง **อ้างอิงวรรณกรรม** อย่างน้อย 10–15 บทความ
> ✅ ลงท้ายด้วย **aim of the study** ที่ชัดเจน

---

## Introduction ใน LaTeX
<!-- _class: dense -->
```latex
\section{Introduction}
Hospital readmission within 30 days of discharge is a key quality indicator and represents 
a significant economic burden \cite{jencks2009rehospitalizations}. Approximately 15--20\% of 
patients are readmitted within this period, costing the healthcare system billions annually 
\cite{krumholz2013post}.

Machine learning approaches have demonstrated promising results in predicting readmission 
risk, with several models achieving area under the curve (AUC) values above 0.70 
\cite{frizzell2017prediction}. However, most existing models rely on 
comprehensive electronic health record (EHR) data available only in 
large academic medical centers \cite{zheng2015predictors}.

This study aims to develop and evaluate a machine learning model for predicting 30-day 
readmission using routinely collected clinical variables available in community 
hospital settings.

```



---

## Methods Section — ส่วนประกอบ

Methods section สำหรับงาน ML ควรมี:

1. **Study design** — retrospective / prospective / cross-sectional
2. **Setting & population** — where, who, when
3. **Dataset** — source, size, inclusion/exclusion criteria
4. **Variables** — outcome, predictors, definitions
5. **Data preprocessing** — missing data, encoding, scaling
6. **Model development** — train/test split, models used
7. **Model evaluation** — metrics, validation strategy
8. **Ethical approval** — IRB / Ethics committee


---

## Methods ใน LaTeX
<!-- _class: dense -->
```latex
\section{Methods}
\subsection{Study Design and Setting}
This retrospective cohort study analyzed patient discharge records from [Hospital Name] 
between January 2022 and December 2023.

\subsection{Dataset and Variables}
The dataset comprised 500 patient records. The outcome 
variable was 30-day readmission (binary: yes/no). 
Predictor variables included age, sex, primary diagnosis 
(ICD-10 category), number of comorbidities, length of 
stay, and number of prior admissions within 12 months.

\subsection{Data Preprocessing}
Missing values were imputed using median imputation for 
continuous variables and mode imputation for categorical 
variables. Categorical variables were encoded using 
one-hot encoding.
```

---

<!-- _class: divider -->

## 05
## Tables & Figures in LaTeX

การนำเสนอข้อมูลในรูปแบบ Journal

---

## Tables ใน LaTeX
<!-- _class: dense -->
```latex
\begin{table}[h]
  \caption{Baseline characteristics of the study population}
  \label{tab:baseline}
  \begin{tabular}{lcc}
    \hline
    \textbf{Variable} & \textbf{Readmitted} & 
                        \textbf{Not Readmitted} \\
    \hline
    Age, mean (SD)       & 65.2 (12.4) & 58.7 (14.1) \\
    Female, n (\%)       & 48 (42.5\%) & 183 (47.2\%) \\
    Comorbidities $\geq 2$ & 83 (73.5\%) & 201 (51.8\%) \\
    Length of stay, days & 7.3 (3.8)   & 4.9 (2.6)   \\
    \hline
  \end{tabular}
\end{table}
```


---

## Figures ใน LaTeX
<!-- _class: dense -->
```latex
\usepackage{graphicx}   % ใส่ใน preamble

% ในเนื้อหา:
\begin{figure}[h]
  \centering
  \includegraphics[width=0.8\textwidth]{fig/roc_curve.png}
  \caption{ROC curves for Logistic Regression and 
           Random Forest models. AUC values are shown 
           in parentheses.}
  \label{fig:roc}
\end{figure}

% อ้างถึงรูปในเนื้อหา:
As shown in Figure~\ref{fig:roc}, the Random Forest 
model achieved superior AUC compared to Logistic Regression.
```

---

## สมการ / Math ใน LaTeX
<!-- _class: dense -->
**Inline math** — ใช้ `$...$`

```latex
The model performance was assessed using F1-score, defined 
as $F_1 = 2 \cdot \frac{precision \cdot recall}
{precision + recall}$.
```

**Display math** — ใช้ `\begin{equation}...\end{equation}`

```latex
\begin{equation}
  \text{AUC} = \int_0^1 \text{TPR}(t) \, d[\text{FPR}(t)]
  \label{eq:auc}
\end{equation}
```

> ✅ LaTeX เป็น gold standard สำหรับสมการ — Word ทำได้ไม่สวยเท่า

---

<!-- _class: divider -->

## 06
## Bibliography with BibTeX

การจัดการอ้างอิงอัตโนมัติ

---

## BibTeX คืออะไร?
<!-- _class: dense -->
- ไฟล์ `.bib` เก็บข้อมูล reference ทุกอัน
- LaTeX ดึงมาจัดรูปแบบ **อัตโนมัติ** ตาม journal style
- ไม่ต้องจัดรูปแบบเอง — เพียงระบุ style

```bibtex
% ไฟล์ references.bib
@article{jencks2009rehospitalizations,
  author  = {Jencks, Stephen F. and Williams, Mark V. 
             and Coleman, Eric A.},
  title   = {Rehospitalizations among patients in the 
             {Medicare} fee-for-service program},
  journal = {New England Journal of Medicine},
  year    = {2009},
  volume  = {360},
  number  = {14},
  pages   = {1418--1428},
  doi     = {10.1056/NEJMsa0803563}
}
```

---
<!-- _class: dense -->
## ดึง BibTeX จาก Google Scholar

**วิธีง่ายที่สุด:**

1. ค้นหา paper ใน **[scholar.google.com](https://scholar.google.com)**
2. คลิกเครื่องหมาย **"** (Cite) ใต้บทความ
3. คลิก **BibTeX**
4. Copy text ที่ได้ทั้งหมด
5. วางใน **`references.bib`** ใน Overleaf

**Alternative — ดึงจาก PubMed:**
1. เปิดหน้า paper ใน PubMed
2. คลิก **Cite** → **Download .nbib**
3. แปลงเป็น BibTeX ด้วย **[converter.bibtex.online](https://converter.bibtex.online)**

---
<!-- _class: dense -->
## ใช้ Bibliography ใน LaTeX

**ใน document body — อ้างอิง:**

```latex
Previous studies have demonstrated AUC values above 0.70 
\cite{frizzell2017prediction, mortazavi2016analysis}.
```

**ท้าย document — แสดงบรรณานุกรม:**

```latex
\bibliographystyle{elsarticle-num}   % Elsevier numbered style
\bibliography{references}            % ชื่อไฟล์ .bib (ไม่มีนามสกุล)
```

**Style ที่ใช้บ่อยกับ Elsevier:**

| Style | รูปแบบ |
|---|---|
| `elsarticle-num` | [1], [2], [3] |
| `elsarticle-harv` | (Author, Year) |
| `elsarticle-num-names` | [Author1 et al., 2020] |

---
<!-- _class: dense -->
## AI ช่วย Generate BibTeX

**Prompt สำหรับขอ BibTeX:**

```
I need a BibTeX entry for the following paper:
Title: "Prediction of hospital readmission for heart failure 
        using simple administrative variables"
Authors: Frizzell et al.
Journal: PLOS ONE, 2017

Please generate a complete BibTeX entry. I will verify 
the details against the actual publication.
```

> ⚠️ **สำคัญ:** ตรวจสอบทุก field ก่อนใช้ — AI อาจสร้างข้อมูลผิด
> ✅ ใช้ DOI ยืนยัน: **[doi.org/[doi-number]](https://doi.org)**

---
<!-- _class: dense -->
## สรุปช่วงเช้า — LaTeX Workflow

```
ค้นหา paper                    เขียนเนื้อหา
Google Scholar / PubMed  →  AI (Gemini) ช่วยร่าง
        ↓                            ↓
  Export BibTeX           วาง LaTeX code ใน Overleaf
        ↓                            ↓
 references.bib          Compile → PDF พร้อม reference
        ↓                            ↓
  ตรวจสอบ DOI            ตรวจสอบความถูกต้องของเนื้อหา
```

**3 ไฟล์หลักใน Overleaf Project:**
- `main.tex` — เนื้อหาทั้งหมด
- `references.bib` — บรรณานุกรม
- `fig/` — รูปภาพ / กราฟ

---
<!-- _class: dense -->
## Morning Lab — ฝึกปฏิบัติ

**เป้าหมาย:** เปิด Elsevier template และกรอกข้อมูลเบื้องต้น

**ขั้นตอน (20 นาที):**

1. ไปที่ **overleaf.com** → New Project → From Template
2. ค้นหา **"Elsevier"** → Open as Template
3. กรอก `\title{}` ด้วย research title ของท่าน
4. กรอก `\author{}` และ `\address{}`
5. เขียน abstract draft ใน `\begin{abstract}...\end{abstract}`
6. เพิ่ม keywords ใน `\begin{keyword}...\end{keyword}`
7. Compile และดูผล PDF

> ✅ เมื่อเสร็จแล้ว Share link Overleaf กับ facilitator

---

<!-- _class: divider -->

## 07
## Afternoon Session

Workshop: Mini Proposal → Elsevier Research Paper

---

<!-- _class: lead -->

# ช่วงบ่าย — Workshop

**จาก Mini Proposal (Day 2) สู่ Elsevier Research Paper**

ใช้ proposal ที่สร้างเมื่อวาน + AI + LaTeX
เพื่อร่าง paper structure ที่ journal-ready

---

## ภาพรวมช่วงบ่าย

1. **Mapping** — แปลง proposal sections เป็น paper sections
2. **Elsevier Template Setup** — ตั้งค่า template สำหรับหัวข้อของท่าน
3. **AI-Assisted Writing** — ใช้ AI ร่างแต่ละ section
4. **Workshop** — ลงมือเขียนจริง
5. **Peer Review** — ตรวจสอบงานกันเอง
6. **Reflection** — สะท้อนกระบวนการทำงาน

---

<!-- _class: divider -->

## 08
## Mapping Proposal to Paper

จาก Mini Proposal สู่ Journal Article Structure

---

## Proposal → Paper: Mapping ทั่วไป

| Mini Proposal Section | Journal Paper Section |
|---|---|
| Title | Title |
| Background + Literature Review | Introduction (CARS) |
| Research Gap | Introduction — Move 2 |
| Research Question | Introduction — Move 3 / Objective |
| Objectives | Objectives / End of Introduction |
| Methodology | Methods |
| AI/ML Application | Methods — Data Analysis subsection |
| Preliminary Findings | Results (preliminary) |
| Ethical Considerations | Methods — Ethics / Study Design |
| Limitations | Discussion — Limitations subsection |

---

## สิ่งที่ต้องเพิ่มจาก Proposal → Paper

**Proposal มีแล้ว:**
- หัวข้อ, gap, RQ, methodology, preliminary findings

**ต้องเพิ่มใน Paper:**

| เพิ่ม | รายละเอียด |
|---|---|
| Full Introduction | CARS model พร้อม citation ครบ |
| Detailed Methods | ระบุทุก decision ให้ reproducible |
| Results section | ตาราง / กราฟ / ตัวเลขจริง |
| Discussion | ตีความผล + เปรียบเทียบกับ literature |
| Conclusion | ข้อสรุปและ implication |
| Full reference list | BibTeX entries ที่ตรวจสอบแล้ว |

---

## Elsevier Paper Structure — ภาพรวม

```
\begin{frontmatter}
  Title / Authors / Abstract / Keywords
\end{frontmatter}

\section{1. Introduction}
  - Background (literature review)
  - Research gap
  - Objective / Aim

\section{2. Methods}
  - Study design & setting
  - Dataset & variables
  - Preprocessing & model development
  - Evaluation metrics
  - Ethical approval

\section{3. Results}
  - Descriptive statistics (Table 1)
  - Model performance (Table 2 / Figure 1)
  - Feature importance (if applicable)

\section{4. Discussion}
  - Key findings & interpretation
  - Comparison with literature
  - Strengths & limitations

\section{5. Conclusion}
```

---

<!-- _class: divider -->

## 09
## Workshop Setup

ตั้งค่า Elsevier Template สำหรับหัวข้อของท่าน

---

## Workshop Task 1 — ตั้งค่า Template

**เปิด Overleaf project จากช่วงเช้า**

ตรวจสอบว่า `main.tex` มีบรรทัดเหล่านี้:

```latex
\documentclass[preprint,12pt]{elsarticle}

\usepackage{graphicx}
\usepackage{booktabs}
\usepackage{hyperref}
\usepackage{amsmath}

\journal{Journal Name TBD}

\begin{document}
```

**เลือก journal (ใส่ใน `\journal{}`):**

| Dataset | แนะนำ Journal |
|---|---|
| 1 Readmission | Journal of Hospital Medicine / JAMDA |
| 2 Burnout | International Journal of Nursing Studies |
| 3 Health Screening | BMC Public Health |
| 4 Satisfaction | Patient Education and Counseling |

---

## Workshop Task 2 — กรอก Frontmatter

**ใช้ Prompt ต่อไปนี้กับ Gemini:**

```
I am writing a research paper for submission to an Elsevier journal.
My research topic is: [topic from Day 2 proposal]
Research question: [RQ from Day 2]
Dataset: [dataset used]

Please help me write:
1. A structured abstract (Background / Objective / Methods / 
   Results / Conclusion) in 200–250 words
2. A list of 5–8 MeSH-style keywords

Use the following preliminary findings:
[วาง preliminary findings จาก Day 2 ที่นี่]

I will verify all claims against actual analysis results.
```

---

## Workshop Task 3 — เขียน Introduction

**AI Prompt สำหรับ Introduction:**

```
Write an Introduction section for a research paper using the 
CARS model (Swales, 1990):
- Move 1: Establish the importance of [topic]
- Move 2: Identify the research gap related to [specific gap 
  from Day 2 Literature Lab]
- Move 3: State the aim: to develop a [ML model] for [objective]

Use academic English appropriate for an Elsevier health 
informatics journal. Include placeholder citations in the 
format \cite{author_year} — I will replace them with verified 
BibTeX entries.

Base the gap statement on: [วาง gap จาก NotebookLM ที่นี่]
```

---

## Workshop Task 4 — เขียน Methods

**AI Prompt สำหรับ Methods:**

```
Write a Methods section for an Elsevier journal paper.
Use the following information:

Study design: retrospective / cross-sectional / survey
Dataset: [dataset name, n=XXX records/participants]
Setting: [hospital / community / online survey]
Outcome variable: [target variable]
Predictor variables: [list of features]
ML models used: [model 1, model 2]
Train/test split: 80/20 stratified
Evaluation metrics: [metrics]
Ethics: [IRB approval or state "simulated data for demonstration"]

Write in past tense, passive voice where appropriate.
Use subsections: Study Design, Data Sources, Variables, 
Data Preprocessing, Model Development, Model Evaluation.
```

---

## Workshop Task 5 — Results Section

**สร้าง Table 1 (Baseline Characteristics):**

```
Create a LaTeX table for an Elsevier paper showing baseline 
characteristics of the study population. 

Use these variables and values:
[วาง descriptive statistics จาก dataset ที่นี่]

Format as a 3-column table with variable name, overall 
statistics, and subgroup comparison (if applicable).
Use booktabs style with \toprule, \midrule, \bottomrule.
```

**สร้าง Table 2 (Model Performance):**

```
Create a LaTeX table comparing model performance metrics.
Models: [model 1] vs [model 2]
Metrics: [Accuracy / Recall / F1-score / AUC / etc.]
Values: [preliminary values from ML Lab]

Add a note below: "Results based on preliminary analysis 
using simulated data. Final values pending complete analysis."
```

---

## ตัวอย่าง Results Section

```latex
\section{Results}

\subsection{Baseline Characteristics}
The study included 500 patient records. Patient 
characteristics are summarized in Table~\ref{tab:baseline}. 
The readmission rate was 22.6\% (n=113). Readmitted 
patients were older (mean age 65.2 vs. 58.7 years) and 
had more comorbidities.

\subsection{Model Performance}
Both models demonstrated acceptable discrimination 
(Table~\ref{tab:performance}). The Random Forest model 
outperformed Logistic Regression on Recall (0.78 vs. 0.61), 
which is the primary metric given the clinical importance 
of identifying high-risk patients.

\subsection{Feature Importance}
Number of prior admissions, number of comorbidities, and 
length of stay were identified as the three most important 
predictors in the Random Forest model 
(Figure~\ref{fig:importance}).
```

---

## Workshop Task 6 — Discussion

**AI Prompt สำหรับ Discussion:**

```
Write a Discussion section for an Elsevier journal paper.
Key findings:
- [Main finding 1 — e.g., Random Forest Recall = 0.78]
- [Main finding 2 — e.g., top predictors]
Please structure the Discussion as:
1. Summary of key findings (2–3 sentences)
2. Comparison with previous literature (use placeholders 
   \cite{key} — I will verify)
3. Clinical/practical implications
4. Strengths of this study
5. Limitations (mention: sample size, single-site, 
   simulated/preliminary data)
6. Future directions

Length: approximately 400–500 words.
Academic English for health informatics journal.
```

---

## Limitations — สำคัญที่สุดใน ML Research

**Limitations ที่ต้องระบุเสมอ:**

| Limitation | วิธีเขียนใน Paper |
|---|---|
| ข้อมูลจำลอง / เบื้องต้น | "This study used simulated/preliminary data; results require validation with real clinical data" |
| Sample size เล็ก | "The relatively small sample (n=XXX) may limit statistical power and generalizability" |
| Single-site data | "Data from a single institution may not generalize to other settings" |
| Self-report bias | "Self-reported variables are subject to recall and social desirability bias" |
| Cross-sectional design | "Causal inference cannot be drawn from cross-sectional data" |

> ✅ การระบุ limitation อย่างครบถ้วน = ความน่าเชื่อถือ ไม่ใช่จุดอ่อน

---

## Workshop Checklist — Elsevier Paper Draft

| Section | เสร็จ | AI ช่วย | ตรวจสอบแล้ว |
|---|---|---|---|
| Title | ☐ | ☐ | ☐ |
| Abstract (structured) | ☐ | ☐ | ☐ |
| Keywords (5–8) | ☐ | ☐ | ☐ |
| Introduction (CARS) | ☐ | ☐ | ☐ |
| Methods — Study design | ☐ | ☐ | ☐ |
| Methods — Dataset & variables | ☐ | ☐ | ☐ |
| Methods — Model development | ☐ | ☐ | ☐ |
| Results — Table 1 (baseline) | ☐ | ☐ | ☐ |
| Results — Table 2 (performance) | ☐ | ☐ | ☐ |
| Discussion | ☐ | ☐ | ☐ |
| Limitations | ☐ | ☐ | ☐ |
| Conclusion | ☐ | ☐ | ☐ |
| References (.bib) | ☐ | ☐ | ☐ |

---

<!-- _class: divider -->

## 10
## Peer Review Workshop

ตรวจสอบงานกันเอง

---

## Peer Review — วิธีตรวจสอบ

**แลกเปลี่ยน Overleaf link กับผู้เข้าอบรมในกลุ่ม**

ตรวจสอบ 5 ประเด็น:

1. **Alignment** — Title / RQ / Methods / Results สอดคล้องกันหรือไม่
2. **Methods completeness** — ผู้อื่น reproduce ได้หรือไม่
3. **Citation accuracy** — มี citation ที่ตรวจสอบได้หรือไม่
4. **Claims** — มีการกล่าวเกินหลักฐานหรือไม่
5. **Limitations** — ระบุข้อจำกัดสำคัญครบหรือไม่

---

## TAG Feedback — สำหรับ Peer Review

| TAG | สำหรับงานวันนี้ |
|---|---|
| **T** = Tell | บอก **1 จุดแข็ง** ที่เห็นในงานของเพื่อน |
| **A** = Ask | ถาม **1 คำถาม** เกี่ยวกับ methodology หรือ finding |
| **G** = Give | ให้ **1 ข้อเสนอแนะ** ที่ specific และทำได้จริง |

> เป้าหมาย: ให้ feedback ที่ **ช่วยพัฒนางาน** ไม่ใช่เพียงชมหรือวิจารณ์

---

<!-- _class: divider -->

## 11
## Process Reflection

AI + LaTeX + Research Writing

---

## สะท้อนกระบวนการทำงาน Day 3

<div class="columns">

<div>

**สิ่งที่ AI ช่วยได้ดีวันนี้:**

- ร่าง LaTeX code ได้รวดเร็ว
- แปลง proposal → paper structure
- สร้าง table skeleton ใน LaTeX
- ปรับภาษาให้ academic

</div>

<div>

**สิ่งที่ต้องตรวจสอบเอง:**

- Citation และ DOI ทุกอัน
- ตัวเลขในผลลัพธ์ (results)
- Methodology — feasibility จริง
- Claim ที่อาจกล่าวเกินจริง
- LaTeX compilation errors

</div>

</div>

---

## Reflection Canvas — Day 3

| ขั้นตอน | ได้ผลดี ✓ | ยังติดขัด ✗ | จะปรับอย่างไร |
|---|---|---|---|
| Setup Overleaf template | | | |
| AI ร่าง Introduction | | | |
| AI ร่าง Methods | | | |
| สร้าง LaTeX tables | | | |
| จัดการ BibTeX references | | | |
| Compile ได้สำเร็จ | | | |
| Peer review ช่วยพัฒนางาน | | | |

---

## AI + LaTeX Workflow — สรุป Day 3

```
Mini Proposal (Day 2)
        ↓
Mapping: Proposal → Paper sections
        ↓
Overleaf: เปิด Elsevier Template
        ↓
AI (Gemini): ร่าง Introduction / Methods / Discussion
        ↓
Copy LaTeX code → วางใน Overleaf
        ↓
ตรวจสอบ: citation / claim / numbers
        ↓
Compile → PDF Draft
        ↓
Peer Review → ปรับแก้
```

---

## ข้อควรจำ — Research Integrity กับ AI

⚠️ **AI-Generated Content ต้องผ่านการตรวจสอบก่อนส่งตีพิมพ์:**

- ตรวจสอบ citation ทุกอัน — อย่าเชื่อ AI 100%
- ข้อมูลตัวเลขในผลลัพธ์ต้องมาจากการวิเคราะห์จริง
- ไม่ส่ง paper ที่มีข้อมูลจำลองเป็นผลลัพธ์จริง
- เปิดเผยการใช้ AI tools ตามนโยบายวารสาร

> ✅ หลายวารสาร Elsevier กำหนดให้ **ประกาศการใช้ AI** ใน Author Statement

---

## AI Declaration ใน Elsevier Paper

**ตัวอย่าง Author Statement สำหรับ AI use:**

```latex
\section*{Declaration of Generative AI and AI-assisted 
          technologies in the writing process}

During the preparation of this work the authors used 
[AI tool name] in order to [reason: improve readability 
/ draft initial text structure / generate LaTeX code]. 
After using this tool, the authors reviewed and edited 
the content as needed and take full responsibility for 
the content of the publication.
```

> ✅ Elsevier นโยบายปี 2024: AI ไม่สามารถเป็น "author" ได้ — แต่ต้องประกาศการใช้

---

<!-- _class: lead -->

# Day 3 Deliverables

สิ่งที่ได้เมื่อจบ Day 3:

1. **Overleaf Project** — Elsevier paper draft พร้อม LaTeX structure
2. **Structured Abstract** — ตรงตาม journal format
3. **Introduction** — CARS model พร้อม citation placeholder
4. **Methods** — ละเอียดพอสำหรับ reproducibility
5. **Results Tables** — LaTeX format พร้อม compile
6. **Discussion & Limitations** — ครบถ้วนและซื่อสัตย์
7. **BibTeX file** — reference ที่ตรวจสอบแล้วอย่างน้อย 5 รายการ
8. **Reflection** — กระบวนการ AI + LaTeX สำหรับนำไปใช้ต่อ

---

## แหล่งเรียนรู้เพิ่มเติม

| แหล่ง | เนื้อหา | URL |
|---|---|---|
| **Overleaf Learn** | LaTeX tutorial ครบถ้วน | overleaf.com/learn |
| **Elsevier Author Services** | Guide for authors | elsevier.com/authors |
| **BibTeX.online** | แปลงและตรวจสอบ BibTeX | bibtex.online |
| **Detexify** | ค้นหา LaTeX symbol | detexify.kirelabs.org |
| **Tables Generator** | สร้าง LaTeX table แบบ GUI | tablesgenerator.com |
| **Writefull for Overleaf** | AI ตรวจภาษา English | writefull.com |

---

## สิ่งที่ต้องทำต่อ — หลัง Workshop

**Before submitting any paper:**

1. ☐ วิเคราะห์ข้อมูล**จริง** และแทนที่ค่า preliminary
2. ☐ ตรวจสอบ citation ทุกอัน — อ่าน abstract ต้นฉบับ
3. ☐ ให้ **ผู้เชี่ยวชาญในสาขา** ตรวจสอบ methodology
4. ☐ ส่ง ethics application ถ้าใช้ข้อมูลจริง
5. ☐ ตรวจสอบ **author guidelines** ของวารสารที่จะ submit
6. ☐ Proofread ภาษาอังกฤษทั้งหมด
7. ☐ ตรวจสอบ AI declaration policy ของวารสาร

> ✅ Paper ที่สร้างใน workshop นี้คือ **draft ที่มีคุณภาพเป็นจุดเริ่มต้น**
> ยังต้องผ่านกระบวนการวิจัยและตรวจสอบอีกพอสมควร

---

<!-- _class: lead -->

# ขอบคุณ

**AI for Research — Day 3**

*LaTeX for Research Papers & Proposal Workshop*

---

จาก Workshop สู่การตีพิมพ์จริง:
**Human judgment + AI assistance + LaTeX quality**

