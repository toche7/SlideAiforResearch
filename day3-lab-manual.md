# Day 3 Lab Manual — LaTeX for Research Papers
## AI for Research Workshop | Mahidol University × BDI

> **วิธีใช้คู่มือนี้**  
> คู่มือนี้ออกแบบให้ใช้คู่กับ slides ของวันที่ 3  
> แต่ละ exercise มีเนื้อหาละเอียดกว่าที่แสดงใน slide  
> รวมถึง template LaTeX code ที่ copy ไปใช้ได้ทันที

---

## สารบัญ

| # | กิจกรรม | เวลา | หน้า |
|---|---|---|---|
| Lab 1 | First Compile — สร้าง Elsevier document แรก | 10 นาที | §1 |
| Lab 2 | Abstract — เขียน structured abstract ของตัวเอง | 10 นาที | §2 |
| Lab 3 | Table — สร้าง LaTeX table ด้วย AI | 10 นาที | §3 |
| Lab 4 | Elsevier Template Setup — กรอก frontmatter ครบ | 20 นาที | §4 |
| **Workshop** | Mini Proposal → Elsevier Paper Draft | 90 นาที | §5 |

---

## §1 Lab 1 — First Compile (10 นาที)

### เป้าหมาย
สร้าง Overleaf project แรกด้วย Elsevier template และ compile ให้ได้ PDF สำเร็จ

### ขั้นตอน

**Step 1 — เปิด Overleaf**

1. ไปที่ [https://www.overleaf.com](https://www.overleaf.com)
2. Log in ด้วย account ของท่าน (ถ้ายังไม่มี → Register ด้วย email มหาวิทยาลัย)
3. คลิก **New Project** → เลือก **Blank Project**
4. ตั้งชื่อ project เช่น `MyResearchPaper_Day3`

**Step 2 — วาง template code**

ลบ code ทั้งหมดใน `main.tex` แล้วแทนที่ด้วย template ด้านล่างนี้:

```latex
\documentclass[preprint,12pt]{elsarticle}

% --- Packages ---
\usepackage{graphicx}    % รูปภาพ
\usepackage{booktabs}    % ตารางสวยงาม
\usepackage{hyperref}    % hyperlink
\usepackage{amsmath}     % สมการ

% --- Journal name ---
\journal{Journal Name TBD}

\begin{document}

\begin{frontmatter}

%% ใส่ชื่อเรื่อง
\title{[ใส่ research title ของท่านที่นี่]}

%% ใส่ชื่อผู้แต่ง
\author[1]{[ชื่อ-นามสกุล ภาษาอังกฤษ]}

%% ใส่ที่อยู่
\address[1]{[Faculty / Department], [University], [City], [Country]}

%% Abstract เบื้องต้น
\begin{abstract}
\textbf{Background:} [ระบุปัญหาและความสำคัญสั้นๆ]

\textbf{Objective:} [เป้าหมายของการศึกษา]

\textbf{Methods:} [ข้อมูล n=XXX + model ที่ใช้]

\textbf{Results:} [ผลลัพธ์เบื้องต้น]

\textbf{Conclusion:} [ข้อสรุป]
\end{abstract}

%% Keywords
\begin{keyword}
  [keyword 1] \sep [keyword 2] \sep [keyword 3] \sep [keyword 4]
\end{keyword}

\end{frontmatter}

%%---------- Introduction ----------
\section{Introduction}

[เนื้อหา introduction เบื้องต้น — จะเขียนให้สมบูรณ์ในช่วงบ่าย]

\end{document}
```

**Step 3 — Compile**

1. คลิกปุ่ม **Recompile** (หรือกด `Ctrl+Enter` / `Cmd+Enter`)
2. รอสักครู่ — PDF จะแสดงด้านขวา
3. ถ้า compile สำเร็จ จะเห็น PDF หน้าแรกที่มี title และ author

**Step 4 — ทดลองแก้ไข**

ลองแก้ค่าต่อไปนี้แล้ว Recompile ดูผล:
- เปลี่ยน `\title{}` เป็นชื่อวิจัยของท่าน
- เปลี่ยน `\author{}` เป็นชื่อของท่าน
- เปลี่ยน `\journal{}` ตามตารางด้านล่าง

### เลือก Journal Name

| Dataset ที่ใช้ | ใส่ใน `\journal{}` |
|---|---|
| Hospital Readmission | `Journal of Hospital Medicine` |
| Nurse Burnout | `International Journal of Nursing Studies` |
| Health Screening | `BMC Public Health` |
| Patient Satisfaction | `Patient Education and Counseling` |

### Checklist ✅

- [ ] Overleaf project สร้างแล้ว
- [ ] Template code วางแล้ว
- [ ] Compile สำเร็จ — เห็น PDF
- [ ] ใส่ชื่อวิจัย ชื่อผู้แต่ง และ journal แล้ว

---

## §2 Lab 2 — เขียน Abstract ของตัวเอง (10 นาที)

### เป้าหมาย
เขียน structured abstract 5 ส่วนของหัวข้อวิจัยจริงของท่านใส่ใน Overleaf

### โครงสร้าง Abstract ที่ดี

| ส่วน | เนื้อหา | ความยาวแนะนำ |
|---|---|---|
| **Background** | ปัญหาและความสำคัญ | 2–3 ประโยค |
| **Objective** | เป้าหมายของการศึกษา | 1 ประโยค |
| **Methods** | ข้อมูล + model ที่ใช้ + metrics | 2–3 ประโยค |
| **Results** | ตัวเลขผลลัพธ์สำคัญ | 1–2 ประโยค |
| **Conclusion** | ข้อสรุปและ implication | 1–2 ประโยค |

รวมทั้งหมด: **200–250 คำ**

### Template Abstract LaTeX

แทนที่ `\begin{abstract}...\end{abstract}` ใน Overleaf ด้วย:

```latex
\begin{abstract}
\textbf{Background:} [REPLACE: ระบุปัญหาทางคลินิก/สาธารณสุขที่ศึกษา
และความสำคัญของปัญหานี้ 2-3 ประโยค]

\textbf{Objective:} To [REPLACE: กริยา เช่น develop / evaluate / examine]
a [REPLACE: ประเภท model] for [REPLACE: วัตถุประสงค์]
using [REPLACE: ข้อมูลที่ใช้].

\textbf{Methods:} A [REPLACE: retrospective / cross-sectional / survey]
study analyzed [REPLACE: n=XXX] [REPLACE: patient records / participants].
[REPLACE: ชื่อ model 1] and [REPLACE: ชื่อ model 2] were compared
using [REPLACE: Recall / F1-score / AUC / etc.].

\textbf{Results:} The [REPLACE: ชื่อ model ที่ดีที่สุด] achieved
[REPLACE: metric] of [REPLACE: ค่า] on the test set
(n=[REPLACE: จำนวน test set]).
[REPLACE: ผลลัพธ์ที่ 2 ถ้ามี]

\textbf{Conclusion:} [REPLACE: ข้อสรุปว่า model ทำงานได้อย่างไร
และจะนำไปใช้ประโยชน์อะไรได้]
\end{abstract}
```

### Template Keywords

```latex
\begin{keyword}
  machine learning \sep
  [REPLACE: clinical topic keyword] \sep
  [REPLACE: method keyword เช่น random forest / logistic regression] \sep
  [REPLACE: setting keyword เช่น hospital / community health] \sep
  [REPLACE: outcome keyword เช่น prediction / classification]
\end{keyword}
```

### ตัวอย่าง Abstract ที่สมบูรณ์ (สำหรับอ้างอิง)

```latex
\begin{abstract}
\textbf{Background:} Hospital readmission within 30 days of discharge
is a key quality indicator representing significant clinical and economic
burden. Existing prediction tools often require comprehensive electronic
health record data unavailable in community hospital settings.

\textbf{Objective:} To develop a machine learning model for predicting
30-day hospital readmission using routinely available clinical variables.

\textbf{Methods:} A retrospective study analyzed 500 patient discharge
records from a community hospital. Logistic Regression and Random Forest
classifiers were developed and evaluated using Recall and F1-score as
primary metrics, with stratified 80/20 train-test splitting.

\textbf{Results:} The Random Forest model achieved Recall of 0.78 and
F1-score of 0.74 on the test set (n=100). This outperformed Logistic
Regression (Recall=0.61, F1=0.66). The top predictors were number of
prior admissions, comorbidity count, and length of stay.

\textbf{Conclusion:} Machine learning models using basic clinical
variables can feasibly identify high-risk patients for early intervention
in community hospital settings.
\end{abstract}
```

### AI Prompt สำหรับช่วย Draft Abstract

ถ้าต้องการให้ AI ช่วย copy prompt นี้ไปใส่ใน Gemini:

```
I am writing a structured abstract for an Elsevier journal paper.
Please write a 200-250 word abstract with 5 labeled sections:
Background, Objective, Methods, Results, Conclusion.

My research:
- Topic: [ระบุหัวข้อ]
- Dataset: [ระบุข้อมูลที่ใช้ n=XXX]
- Models compared: [ระบุ model]
- Key findings: [ระบุผลลัพธ์เบื้องต้น]
- Setting: [ระบุ hospital / community / etc.]

Format each section with \textbf{Section:} at the start,
suitable for LaTeX input.
I will verify all numerical results against my actual analysis.
```

### Checklist ✅

- [ ] Abstract มีครบ 5 ส่วน (Background / Objective / Methods / Results / Conclusion)
- [ ] ใส่ตัวเลข/ข้อมูลเบื้องต้นแล้ว (แม้ยังไม่ใช่ค่าสุดท้าย)
- [ ] Keywords 4–6 คำ ที่ครอบคลุมหัวข้อ
- [ ] Compile สำเร็จ — เห็น abstract ใน PDF

---

## §3 Lab 3 — สร้าง Table ด้วย AI (10 นาที)

### เป้าหมาย
ใช้ AI สร้าง LaTeX performance comparison table แล้ว paste ลง Overleaf

### Step 1 — Prompt สำหรับ Model Performance Table

Copy prompt นี้ไปใส่ใน **Gemini / ChatGPT**:

```
Create a LaTeX table for an Elsevier journal paper using booktabs style.
Show a model performance comparison table:

Metric       | Logistic Regression | Random Forest
Accuracy     | 0.74                | 0.79
Recall       | 0.61                | 0.78
F1-score     | 0.66                | 0.74
AUC          | 0.71                | 0.82

Requirements:
- Use \toprule, \midrule, \bottomrule (no \hline)
- Add \caption{Comparison of model performance on the test set}
- Add \label{tab:performance}
- Center-align numeric columns
- Use \usepackage{booktabs} in preamble
- Add a table note: "Results based on preliminary analysis."
```

### Step 2 — Template Table (ถ้าไม่มี AI ตอนนี้)

Copy code นี้ใส่ใน Overleaf ก่อน `\end{document}`:

```latex
%% ใส่ใน preamble (ก่อน \begin{document}):
%% \usepackage{booktabs}

\begin{table}[h]
  \centering
  \caption{Comparison of model performance on the test set}
  \label{tab:performance}
  \begin{tabular}{lccc}
    \toprule
    \textbf{Metric} & \textbf{Logistic Regression} & \textbf{Random Forest} \\
    \midrule
    Accuracy  & 0.74 & 0.79 \\
    Recall    & 0.61 & \textbf{0.78} \\
    F1-score  & 0.66 & \textbf{0.74} \\
    AUC       & 0.71 & \textbf{0.82} \\
    \bottomrule
  \end{tabular}
  \begin{tablenotes}
    \small
    \item \textit{Note:} Results based on preliminary analysis
    using simulated data. Final values pending complete analysis.
  \end{tablenotes}
\end{table}
```

### Step 3 — อ้างถึง Table ในเนื้อหา

เพิ่มข้อความนี้ใน `\section{Introduction}` หรือสร้าง `\section{Results}`:

```latex
\section{Results}

Model performance is summarized in Table~\ref{tab:performance}.
The Random Forest model outperformed Logistic Regression across
all metrics, particularly on Recall (0.78 vs. 0.61), which is
the primary metric for identifying high-risk patients.
```

### Step 4 — Baseline Characteristics Table (Bonus)

ถ้ามีเวลาเพิ่ม ลองสร้าง Table 1:

```latex
\begin{table}[h]
  \centering
  \caption{Baseline characteristics of the study population}
  \label{tab:baseline}
  \begin{tabular}{lccc}
    \toprule
    \textbf{Variable} & \textbf{Overall} &
                        \textbf{Readmitted} &
                        \textbf{Not Readmitted} \\
    \midrule
    N (\%)            & 500 (100\%) & 113 (22.6\%) & 387 (77.4\%) \\
    Age, mean (SD)    & 60.4 (13.8) & 65.2 (12.4)  & 58.7 (14.1)  \\
    Female, n (\%)    & 231 (46.2\%) & 48 (42.5\%) & 183 (47.2\%) \\
    Comorbidities $\geq$2 & 284 (56.8\%) & 83 (73.5\%) & 201 (51.8\%) \\
    LOS, days mean (SD) & 5.5 (3.1)  & 7.3 (3.8)   & 4.9 (2.6)    \\
    \bottomrule
  \end{tabular}
\end{table}
```

### Checklist ✅

- [ ] ได้ LaTeX table code จาก AI หรือ template
- [ ] วาง code ใน Overleaf แล้ว compile สำเร็จ
- [ ] ตารางแสดงใน PDF ถูกต้อง
- [ ] เพิ่ม `\usepackage{booktabs}` ใน preamble แล้ว
- [ ] (Bonus) อ้างถึง table ด้วย `Table~\ref{tab:performance}` ในเนื้อหา

---

## §4 Lab 4 — Elsevier Template Setup (20 นาที)

### เป้าหมาย
เปิด Elsevier template จริงใน Overleaf และกรอก frontmatter ครบถ้วน

### Step 1 — เปิด Elsevier Template

**วิธีที่ 1 — จาก Overleaf Gallery (แนะนำ):**

1. ไปที่ [overleaf.com/gallery](https://www.overleaf.com/gallery)
2. ค้นหา **"Elsevier"**
3. เลือก **"Elsevier - LaTeX Template for Journal Articles"**
4. คลิก **"Open as Template"**
5. ตั้งชื่อ project ของท่าน

**วิธีที่ 2 — ใช้ project จาก Lab 1:**

ใช้ project เดิมได้เลย แต่ตรวจสอบว่า preamble มี packages ครบ:

```latex
\documentclass[preprint,12pt]{elsarticle}

\usepackage{graphicx}
\usepackage{booktabs}
\usepackage{hyperref}
\usepackage{amsmath}
\usepackage{threeparttable}  % สำหรับ table notes

\journal{[ชื่อ Journal]}
```

### Step 2 — กรอก Frontmatter ให้ครบ

แทนที่ placeholder ทั้งหมดใน frontmatter:

```latex
\begin{frontmatter}

%% ชื่อเรื่อง — ควรมี: topic + method + setting/population
\title{[Method] for [Outcome] Prediction Using [ML Approach]:
       A [Study Design] Study}

%% ตัวอย่าง:
%% \title{Machine Learning-Based Prediction of 30-Day Hospital
%%        Readmission Using Routinely Collected Clinical Data:
%%        A Retrospective Cohort Study}

%% ผู้แต่ง (เพิ่มได้หลายคน)
\author[1]{[First Author Full Name]}
\author[2]{[Second Author Full Name]}     % ถ้ามี
\corref{cor1}                             % corresponding author

%% ที่อยู่
\address[1]{[Department], [Faculty],
            [University], [City], [Country]}
\address[2]{[Department], [Institution],  % ถ้ามี
            [City], [Country]}

%% Corresponding author email
\ead{email@university.ac.th}

%% Abstract
\begin{abstract}
\textbf{Background:} [2-3 ประโยค]

\textbf{Objective:} [1 ประโยค]

\textbf{Methods:} [2-3 ประโยค — ใส่ n= และ model]

\textbf{Results:} [1-2 ประโยค — ใส่ตัวเลข]

\textbf{Conclusion:} [1-2 ประโยค]
\end{abstract}

%% Keywords (5-8 คำ, ใช้ \sep คั่น)
\begin{keyword}
  machine learning \sep
  [clinical topic] \sep
  [ML method] \sep
  [setting] \sep
  [outcome/application]
\end{keyword}

\end{frontmatter}
```

### Step 3 — เพิ่ม Section Headings

เพิ่ม section structure หลัง `\end{frontmatter}`:

```latex
%%---------- 1. Introduction ----------
\section{Introduction}
% [เขียนในช่วงบ่าย ด้วย AI]

%%---------- 2. Methods ----------
\section{Methods}

\subsection{Study Design and Setting}
% [เขียนในช่วงบ่าย]

\subsection{Dataset and Variables}
% [เขียนในช่วงบ่าย]

\subsection{Data Preprocessing}
% [เขียนในช่วงบ่าย]

\subsection{Model Development}
% [เขียนในช่วงบ่าย]

\subsection{Model Evaluation}
% [เขียนในช่วงบ่าย]

\subsection{Ethical Considerations}
This study used [simulated data for demonstration purposes /
de-identified retrospective data approved by the Institutional
Review Board (IRB No. XXXX)].

%%---------- 3. Results ----------
\section{Results}
% [เขียนในช่วงบ่าย]

%%---------- 4. Discussion ----------
\section{Discussion}
% [เขียนในช่วงบ่าย]

%%---------- 5. Conclusion ----------
\section{Conclusion}
% [เขียนในช่วงบ่าย]

%%---------- Declarations ----------
\section*{Declaration of Competing Interest}
The authors declare that they have no known competing financial
interests or personal relationships that could have appeared to
influence the work reported in this paper.

\section*{Declaration of Generative AI and AI-assisted
          technologies in the writing process}
During the preparation of this work the authors used
[Gemini / ChatGPT] in order to [draft initial text structure /
improve readability / generate LaTeX code]. After using this
tool, the authors reviewed and edited the content as needed
and take full responsibility for the content of the publication.

%%---------- References ----------
\bibliographystyle{elsarticle-num}
\bibliography{references}

\end{document}
```

### Step 4 — สร้างไฟล์ references.bib

1. คลิกไอคอน **"New File"** ใน Overleaf (มุมบนซ้าย)
2. ตั้งชื่อว่า `references.bib`
3. วาง BibTeX entries ตัวอย่าง:

```bibtex
@article{example2024,
  author  = {[Last, First] and [Last, First]},
  title   = {[Paper title]},
  journal = {[Journal name]},
  year    = {2024},
  volume  = {XX},
  number  = {X},
  pages   = {XXX--XXX},
  doi     = {10.XXXX/XXXXXX}
}
```

4. ดึง BibTeX จริงจาก **Google Scholar**:
   - ค้นหา paper → คลิก **"** → คลิก **BibTeX** → Copy → วางใน `references.bib`

### Lab 4 Checklist ✅

- [ ] Overleaf project เปิดแล้ว (จาก template หรือ project เดิม)
- [ ] `\title{}` — ใส่ชื่อวิจัยจริงของท่าน
- [ ] `\author{}` และ `\address{}` — ใส่ข้อมูลครบ
- [ ] `\journal{}` — เลือก journal ที่เหมาะสม
- [ ] Abstract มีครบ 5 ส่วน
- [ ] Keywords 5–8 คำ
- [ ] Section headings ทั้ง 5 sections ครบ
- [ ] `references.bib` สร้างแล้ว
- [ ] Compile สำเร็จ — PDF แสดงผลถูกต้อง
- [ ] Share Overleaf link กับ facilitator

---

## §5 Workshop — Mini Proposal → Elsevier Paper Draft (90 นาที)

### เป้าหมาย
นำ Mini Proposal จาก Day 2 มาพัฒนาเป็น Elsevier paper draft ที่มีโครงสร้างสมบูรณ์ โดยใช้ AI ช่วยร่างแต่ละ section

---

### Workshop Task 1 — ตั้งค่า Template

**เปิด Overleaf project จาก Lab 4**

ตรวจสอบว่า `main.tex` มี packages ครบ:

```latex
\documentclass[preprint,12pt]{elsarticle}
\usepackage{graphicx}
\usepackage{booktabs}
\usepackage{hyperref}
\usepackage{amsmath}
\usepackage{threeparttable}
\journal{[ชื่อ Journal]}
```

**เลือก Journal ตาม Dataset:**

| Dataset | แนะนำ Journal |
|---|---|
| 1 Readmission | Journal of Hospital Medicine / JAMDA |
| 2 Burnout | International Journal of Nursing Studies |
| 3 Health Screening | BMC Public Health |
| 4 Satisfaction | Patient Education and Counseling |

---

### Workshop Task 2 — กรอก Frontmatter ด้วย AI

Copy prompt นี้ไปใส่ใน **Gemini**:

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

> ⚠️ ตรวจสอบตัวเลขและ claim ทุกอันก่อนวางใน Overleaf

---

### Workshop Task 3 — เขียน Introduction (CARS Model)

Copy prompt นี้ไปใส่ใน **Gemini**:

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

**วางผลลัพธ์ใน Overleaf:**
```latex
\section{Introduction}
% วาง AI-generated text ที่นี่
% แล้วแทนที่ \cite{} placeholders ด้วย BibTeX keys จริง
```

---

### Workshop Task 4 — เขียน Methods

Copy prompt นี้ไปใส่ใน **Gemini**:

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
Ethics: [IRB approval or "simulated data for demonstration"]

Write in past tense, passive voice where appropriate.
Use subsections: Study Design, Data Sources, Variables,
Data Preprocessing, Model Development, Model Evaluation.
```

---

### Workshop Task 5 — Results: สร้าง Tables ด้วย AI

**Prompt สำหรับ Table 1 — Baseline Characteristics:**

```
Create a LaTeX table for an Elsevier paper showing baseline
characteristics of the study population.

Use these variables and values:
[วาง descriptive statistics จาก dataset ที่นี่]

Format as a 3-column table: variable name, overall statistics,
and subgroup comparison (if applicable).
Use booktabs style with \toprule, \midrule, \bottomrule.
Add \caption and \label{tab:baseline}.
```

**Prompt สำหรับ Table 2 — Model Performance:**

```
Create a LaTeX table comparing model performance metrics.
Models: [model 1] vs [model 2]
Metrics: [Accuracy / Recall / F1-score / AUC / etc.]
Values: [preliminary values from ML Lab]

Add a note below the table:
"Results based on preliminary analysis using simulated data.
Final values pending complete analysis."
Add \caption and \label{tab:performance}.
```

**Template Results Section:**

```latex
\section{Results}

\subsection{Baseline Characteristics}
The study included [n] [patient records / participants].
Baseline characteristics are summarized in
Table~\ref{tab:baseline}.

% [วาง Table 1 ที่นี่]

\subsection{Model Performance}
Model performance is summarized in
Table~\ref{tab:performance}.
The [best model] outperformed [other model] on [key metric]
([value] vs. [value]).

% [วาง Table 2 ที่นี่]

\subsection{Feature Importance}
[Top predictor 1], [top predictor 2], and [top predictor 3]
were identified as the most important predictors.
```

---

### Workshop Task 6 — เขียน Discussion

Copy prompt นี้ไปใส่ใน **Gemini**:

```
Write a Discussion section for an Elsevier journal paper.
Key findings:
- [Main finding 1 — e.g., Random Forest Recall = 0.78]
- [Main finding 2 — e.g., top predictors]

Structure the Discussion as:
1. Summary of key findings (2–3 sentences)
2. Comparison with previous literature
   (use \cite{key} placeholders — I will verify)
3. Clinical/practical implications
4. Strengths of this study
5. Limitations (mention: sample size, single-site,
   simulated/preliminary data)
6. Future directions

Length: approximately 400–500 words.
Academic English for health informatics journal.
```

**Common Limitations to include:**

| Limitation | วิธีเขียนใน Paper |
|---|---|
| ข้อมูลจำลอง | "This study used simulated data; results require validation with real clinical data" |
| Sample size เล็ก | "The relatively small sample (n=XXX) may limit statistical power and generalizability" |
| Single-site | "Data from a single institution may not generalize to other settings" |
| Self-report bias | "Self-reported variables are subject to recall and social desirability bias" |
| Cross-sectional | "Causal inference cannot be drawn from cross-sectional data" |

---

### Workshop Checklist ✅

| Section | เสร็จ | AI ช่วย | ตรวจสอบแล้ว |
|---|---|---|---|
| Title | ☐ | ☐ | ☐ |
| Abstract (structured 5 ส่วน) | ☐ | ☐ | ☐ |
| Keywords (5–8 คำ) | ☐ | ☐ | ☐ |
| Introduction (CARS model) | ☐ | ☐ | ☐ |
| Methods — Study design | ☐ | ☐ | ☐ |
| Methods — Dataset & variables | ☐ | ☐ | ☐ |
| Methods — Model development | ☐ | ☐ | ☐ |
| Results — Table 1 (baseline) | ☐ | ☐ | ☐ |
| Results — Table 2 (performance) | ☐ | ☐ | ☐ |
| Discussion | ☐ | ☐ | ☐ |
| Limitations | ☐ | ☐ | ☐ |
| Conclusion | ☐ | ☐ | ☐ |
| References (.bib ≥ 5 entries) | ☐ | ☐ | ☐ |
| AI Declaration | ☐ | — | ☐ |
| Compile สำเร็จ — PDF ครบทุก section | ☐ | — | — |
| Share Overleaf link กับ facilitator | ☐ | — | — |

---

## ภาคผนวก — Template Files สรุป

### A. Full Elsevier Template (copy-ready)

```latex
\documentclass[preprint,12pt]{elsarticle}

%% --- Packages ---
\usepackage{graphicx}
\usepackage{booktabs}
\usepackage{hyperref}
\usepackage{amsmath}
\usepackage{threeparttable}

%% --- Journal ---
\journal{[Journal Name]}

\begin{document}

\begin{frontmatter}
\title{[Full Paper Title]}
\author[1]{[Author Name]}
\address[1]{[Department, University, Country]}
\ead{[email]}

\begin{abstract}
\textbf{Background:} [...]
\textbf{Objective:} [...]
\textbf{Methods:} [...]
\textbf{Results:} [...]
\textbf{Conclusion:} [...]
\end{abstract}

\begin{keyword}
[kw1] \sep [kw2] \sep [kw3] \sep [kw4] \sep [kw5]
\end{keyword}
\end{frontmatter}

\section{Introduction}

\section{Methods}
\subsection{Study Design and Setting}
\subsection{Dataset and Variables}
\subsection{Data Preprocessing}
\subsection{Model Development}
\subsection{Model Evaluation}
\subsection{Ethical Considerations}

\section{Results}
\subsection{Baseline Characteristics}
\subsection{Model Performance}

\section{Discussion}

\section{Conclusion}

\section*{Declaration of Competing Interest}
The authors declare no competing interests.

\section*{Declaration of Generative AI}
During preparation, [AI tool] was used for [purpose].
Authors reviewed and take full responsibility for all content.

\bibliographystyle{elsarticle-num}
\bibliography{references}

\end{document}
```

### B. AI Prompts สรุป

**Abstract:**
```
Write a 200-250 word structured abstract with sections:
Background / Objective / Methods / Results / Conclusion.
Topic: [topic], Dataset: n=[n], Models: [models],
Key result: [result]. Format with \textbf{Section:} in LaTeX.
```

**Introduction (CARS model):**
```
Write an Introduction using CARS model:
Move 1: Importance of [topic]
Move 2: Gap — [specific gap]
Move 3: Aim — to develop [model] for [objective]
Use \cite{author_year} placeholders. ~400 words.
```

**Methods:**
```
Write a Methods section for an Elsevier paper:
Design: [design], Dataset: n=[n], Setting: [setting],
Outcome: [outcome], Predictors: [list],
Models: [models], Split: 80/20 stratified,
Metrics: [metrics], Ethics: [IRB/simulated].
Past tense, passive voice. Include subsections.
```

**Table:**
```
Create a booktabs LaTeX table for Elsevier.
[Data here]
Use \toprule \midrule \bottomrule. Add \caption and \label.
```

**BibTeX:**
```
Generate a BibTeX entry for:
Title: [title], Authors: [authors],
Journal: [journal], Year: [year].
I will verify against the actual publication.
```

---

## หมายเหตุสำคัญ

> ⚠️ **Research Integrity**  
> - ตัวเลขในผลลัพธ์ต้องมาจากการวิเคราะห์จริง ไม่ใช่ค่า placeholder  
> - Citation ทุกอันต้องตรวจสอบจากแหล่งต้นฉบับ  
> - AI-generated content ต้องผ่านการตรวจสอบก่อนส่งตีพิมพ์  
> - ประกาศการใช้ AI ใน Author Statement ตามนโยบายวารสาร

---

*Day 3 Lab Manual | AI for Research Workshop | Version 1.0 | May 2026*
