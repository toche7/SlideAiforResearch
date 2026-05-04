---
marp: true
theme: mahidol-green
paginate: true
size: 16:9
footer: "Generative AI for Research | ITM, Mahidol University"
---

<!-- _class: lead -->

<style scoped>
img { position: absolute; top: 36px; right: 64px; width: 150px; height: 150px; object-fit: contain; }
</style>

<img src="fig/logos/mahidol.svg" alt="Mahidol University">

# แนวทางการใช้ AI เพื่อช่วยในการทำวิจัย

<div class="subtitle">Generative AI for Research</div>

**ผศ.ดร.ทวีศักดิ์ สมานชื่น**
กลุ่มสาขาวิชา ITM | มหาวิทยาลัยมหิดล

Credit: ITM 68, MULKC | May 2026



---

## My Research Metrics *(SciVal)*
<div class="center">

![w:1000px](/fig/metrics.png)

</div>

---

## Research Areas
<div class="center">

![w:950px](/fig/researcharea.png)

</div>


---

## Journal Quartiles
<div class="center">

![w:950px](/fig/JournalQuartiles.png)

</div>

---

## ทำไมต้องใช้ AI ในการวิจัย?

<div class="columns">

<div>

**ความท้าทายของนักวิจัย**
- 📚 บทความใหม่ตีพิมพ์ **มากกว่า 2 ล้านฉบับ/ปี**
- ⏱️ Literature Review ใช้เวลา **หลายสัปดาห์ถึงเดือน**
- ✍️ การเขียนและแก้ไขซ้ำ ๆ กินเวลามหาศาล
- 🔍 หา Research Gap ที่แท้จริงทำได้ยาก

</div>

<div>

**AI ช่วยได้อย่างไร**
- 🤖 ค้นหาและสรุปบทความได้ภายในนาที
- 💡 ช่วยระบุ Gap และตั้งคำถามวิจัย
- 📝 ร่างและปรับปรุงงานเขียนเชิงวิชาการ
- 📊 วิเคราะห์และสร้างภาพข้อมูล

> **หลักการ**: AI ไม่ได้มาแทนนักวิจัย — แต่ช่วยให้ทำงานได้ **เร็วขึ้นและลึกขึ้น**

</div>

</div>

---

## เนื้อหาการนำเสนอ

<div class="columns">

<div>

**ส่วนที่ 1 — พื้นฐาน AI**
- 🤖 AI Chatbot & LLM
- ⚡ Fast Model vs Thinking Model

**ส่วนที่ 2 — กรอบการวิจัย**
- 🔬 Research Process & Ethics
- 🧩 HIRF Framework

</div>

<div>

**ส่วนที่ 3 — HIRF 5 Stages**
- 🎯 Stage 1: Problem Framing
- 📚 Stage 2: Literature Review
- 🗂️ Stage 3: Research Design

**ส่วนที่ 4 — การวิเคราะห์และเขียน**
- 📊 Stage 4: Data & Analysis
- ✍️ Stage 5: Scholarly Writing

</div>

</div>

---

<!-- _class: divider -->

## 01
## AI Chatbot & LLM Overview

Large Language Models and their limitations

---
## Modern Chat AI

<div class="center">

![w:1000px](/fig/modernchatai.png)

</div>

---

## Large Language Model (LLM)

**แบบจำลองภาษาขนาดใหญ่** คือโปรแกรม AI ที่ได้รับการฝึกฝนจากข้อมูลจำนวนมหาศาล

- เรียนรู้และสร้างข้อความที่เหมือนมนุษย์
- สร้างบนสถาปัตยกรรม **Deep Learning** (Transformers)
- ทำงานด้าน NLP ได้หลากหลาย:
  - การแปลภาษา
  - การตอบคำถาม
  - การสร้างเนื้อหา

---
## การพัฒนา LLM

<div class="center">

![w:900px](/fig/pretrain.png)

</div>

---
## การพัฒนา LLM

<div class="center">

![w:900px](/fig/finetune.png)

</div>

---
## การทำงานของ LLM

<div class="center">

![w:900px](/fig/predictnextword.png)

</div>

---
## การทำงานของ LLM

<div class="center">

![w:900px](/fig/context.png)

</div>


---
## ข้อจำกัดของ LLM

| ข้อจำกัด | คำอธิบาย |
|---|---|
| **Outdated Knowledge** | พึ่งพาข้อมูลฝึกฝน ไม่มีข้อมูลล่าสุด |
| **Cannot Take Action** | ไม่สามารถค้นหา คำนวณ หรือดึงข้อมูลเองได้ |
| **Lack of Context** | อาจไม่จดจำรายละเอียดจาก prompt ก่อนหน้า |
| **Hallucination** | อาจสร้างเนื้อหาที่ผิดหรือไร้สาระได้ |

---

<!-- _class: divider -->

## 02
## ประเภทของ LLM

Fast Model vs Thinking Model

---

## ประเภทของ LLM: แนวคิดจาก Daniel Kahneman

<div class="columns">

<div>

**Daniel Kahneman**
- นักจิตวิทยา / นักเศรษฐศาสตร์เชิงพฤติกรรม
- เจ้าของรางวัล **Nobel Prize in Economics (2002)**
- ผู้เขียน *"Thinking, Fast and Slow"* (2011)
- แนวคิด: จิตใจมนุษย์ทำงาน 2 ระบบคู่ขนาน

</div>

<div>

**แนวคิดสู่ LLM**

| ระบบ | ลักษณะมนุษย์ | ลักษณะ LLM |
|---|---|---|
| **System 1** | Fast — สัญชาตญาณ | Fast Model |
| **System 2** | Slow — มีเหตุผล | Thinking Model |

</div>

</div>

---

## 1. Fast Model

- **ความเร็ว**: รวดเร็ว ฉับไว (Immediate)
- **กลไก**: สร้างคำตอบทีละโทเค็นจาก Pattern Recognition
- **การให้เหตุผล**: สัญชาตญาณ ไม่แสดงขั้นตอนการคิด
- **ความแม่นยำ**: ดีสำหรับงานเรียบง่าย อาจ Hallucinate ในงานซับซ้อน
- **เหมาะกับ**: การสนทนาทั่วไป การแปลคำ การสร้างข้อความด่วน

---

## 2. Thinking / Reasoning Model

- **ความเร็ว**: ช้าลง รอบคอบ (Deliberative)
- **กลไก**: ใช้ Chain-of-Thought (CoT) สร้าง Reasoning Traces ก่อนตอบ
- **การให้เหตุผล**: เป็นตรรกะ เป็นขั้นเป็นตอน Step-by-Step
- **ความแม่นยำ**: สูงสำหรับงานซับซ้อน ตรรกะ การคำนวณ
- **เหมาะกับ**: โจทย์คณิตศาสตร์ การวางแผน การสร้างโค้ด

---

<!-- _class: divider -->

## 03
## กระบวนการวิจัย

Research Processes & Ethics

---

## กระบวนการวิจัย (Research Process)

มีหลายรูปแบบตามสาขาวิชา:

- **Generic Research Process** — กระบวนการวิจัยทั่วไป
- **Engineering Research Process** — งานวิศวกรรม
- **Data Science Research Process** — วิทยาศาสตร์ข้อมูล
- **Basic Research Process** — การวิจัยพื้นฐาน


---
## General Research Process

<div class="center">

![h:500px](/fig/researchProcessGeneral.png)

</div>

---
## Engineering Research Process

<div class="center">

![h:500px](/fig/researchProcessEngineering.png)

</div>

---
## Data Science Research Process

<div class="center">

![h:500px](/fig/researchProcessDataScience.png)

</div>

---
## Basic Research Process

<div class="center">

![h:500px](/fig/BasicResearchProcess.png)

</div>

---

## จริยธรรมการวิจัย (Research Ethics)

หลักการสำคัญในการทำวิจัย:

- **ความซื่อสัตย์** — ไม่บิดเบือนข้อมูลหรือผลการวิจัย
- **ความเที่ยงตรง** — รายงานผลตามความเป็นจริง
- **ความถูกต้องรอบคอบ** — ตรวจสอบข้อมูลอย่างละเอียด
- **ความรับผิดชอบ** — รับผิดชอบต่อข้อมูลและผลการวิจัย
- **เคารพทรัพย์สินทางปัญญา** — อ้างอิงแหล่งที่มาอย่างถูกต้อง

---
## Basic Principle of Using AI

<div class="center">

![w:1100px](/fig/BasicPrincipleofUsingAI.png)

</div>

---

## นโยบาย AI สำหรับผู้แต่งบทความ (Elsevier)

- ✅ ใช้ AI ช่วยปรับปรุงภาษาได้
- ❌ ห้ามใช้ AI แทนการคิดวิเคราะห์ของมนุษย์
- ✅ ผู้แต่งรับผิดชอบเนื้อหาทั้งหมด 100%
- ✅ ต้องเปิดเผย (Disclose) การใช้ AI ในบทความ
- ❌ ห้ามใส่ชื่อ AI เป็นผู้แต่งร่วม
- ❌ ห้ามใช้ AI สร้าง/ดัดแปลงรูปภาพในบทความ

[Link อ้างอิง](https://www.elsevier.com/about/policies-and-standards/generative-ai-policies-for-journals)

---

## นโยบาย AI สำหรับผู้ประเมินและบรรณาธิการ

**ผู้ประเมินบทความ (Reviewer)**
- ❌ ห้ามอัปโหลดบทความลงใน AI เด็ดขาด
- ❌ ห้ามใช้ AI ช่วยเขียนรายงานการประเมิน

**บรรณาธิการ (Editor)**
- ❌ ห้ามอัปโหลดบทความหรือจดหมายโต้ตอบลงใน AI
- ❌ ห้ามใช้ AI ช่วยตัดสินรับ/ปฏิเสธบทความ
  
[Link อ้างอิง](https://www.elsevier.com/about/policies-and-standards/generative-ai-policies-for-journals)

---

<!-- _class: divider -->

## 04
## HIRF

Hybrid Intelligence Research Framework

---

## HIRF คืออะไร?

**Hybrid Intelligence Research Framework (HIRF)**

> กรอบแนวทางที่ผสาน **การคิดเชิงวิชาการของมนุษย์** เข้ากับ **ความสามารถของ Generative AI** แบบวนซ้ำ มีหลักจริยธรรมกำกับ

**หลักการหลัก**:
> *Human intelligence leads. AI assists.*

นักวิจัยเป็นผู้ตัดสินใจหลัก — AI ช่วยเสริม ขยาย และเร่งกระบวนการ

---
## HIRF Concept

<div class="center">

![h:500px](/fig/HIRF.png)

</div>

---

## 5 ขั้นตอนของ HIRF

| # | ขั้นตอน | บทบาทมนุษย์ | บทบาท AI |
|---|---|---|---|
| 1 | **Problem Framing** | ระบุปัญหา ตั้งคำถาม | สรุปภาพรวม เสนอรูปแบบ |
| 2 | **Literature Review** | วิพากษ์ สร้างกรอบทฤษฎี | รวบรวม สรุป จัดกลุ่ม |
| 3 | **Research Design** | เลือกวิธีวิจัย ตัวแปร | เสนอรูปแบบ สร้างเทมเพลต |
| 4 | **Data & Analysis** | เก็บข้อมูล ตีความ ตรวจสอบ | ทำความสะอาดข้อมูล วิเคราะห์ |
| 5 | **Scholarly Writing** | เรียบเรียง ตรวจคุณภาพ | ช่วยร่าง ปรับภาษา สร้างกราฟ |

---
## HIRF Cycle

<div class="center">

![h:500px](/fig/HIRFProcess.png)

</div>

---
## HIRF Process

<div class="center">

![h:500px](/fig/hirfProcessBlock.png)

</div>

---
## Writing Process

<div class="center">

![h:500px](/fig/hirfWriting.png)

</div>

---

<!-- _class: divider -->

## 05
## Stage 1: Problem Framing

Define Research Topic & Research Focus


---
## Topic Development Process

<div class="center">

![w:1000px](/fig/topicDev.png)

</div>

---
## Alternative Topic Development Process

<div class="center">

![w:700px](/fig/topicDevActual.png)

</div>

---

## การกำหนดหัวข้อวิจัย

**3 วิธีหาไอเดียหัวข้อวิจัยด้วย AI**

1. **กำหนด Scope และความสนใจ**
   - สาขา, Sub-field, ประเภทการวิจัย

2. **ค้นหา Emerging Trends / Research Gaps**
   - ขอ AI ระบุช่องว่างในสาขาที่สนใจ

3. **ขอ Topic Suggestions เฉพาะเจาะจง**
   - ระบุกลุ่มเป้าหมาย บริบท หรือ Use case

---

## ตัวอย่าง Prompt สำหรับ Stage 1

<div class="columns">

<div>

**ค้นหา Trend:**
> *"Suggest emerging research topics in the use of AI in higher education, with a focus on ethical implications and policy."*

**ค้นหา Gap:**
> *"What are the research gaps in applying Generative AI in public sector data analysis?"*

</div>

<div>

**ขอ Topics เฉพาะ:**
> *"Give me 5 research topics combining GenAI and statistical literacy for government employees."*

</div>

</div>

---

<!-- _class: divider -->

## 06
## Stage 2: Literature Review

Knowledge Expansion with AI Tools

---

## กระบวนการ Literature Review ด้วย AI

1. **กำหนดขอบเขต (Scope)** — หัวข้อ, คำค้น, ช่วงเวลา, ฐานข้อมูล
2. **ค้นหาและสรุปบทความ** ด้วย AI Tools
3. **ร่างสังเคราะห์เนื้อหา** (Thematic Synthesis)
4. **เรียบเรียง Literature Review**
5. **ตรวจสอบความถูกต้อง** และอ้างอิงด้วยตนเอง

---

## เครื่องมือ AI สำหรับสืบค้นงานวิจัย

| เครื่องมือ | จุดเด่น |
|---|---|
| [**SciSpace**](https://scispace.com/) | จัดระเบียบข้อมูล, AI Writer, Citation Generator |
| [**Paper Finder**](https://paperfinder.allen.ai/chat) | Semantic Search, บอกเหตุผลการแนะนำ, Export Bib ฟรี |
| [**Elicit**](https://elicit.com/) | PICO framework, สกัดข้อมูลเชิงโครงสร้าง, 125M papers |
| [**Consensus AI**](https://consensus.app/) | Consensus Meter, เน้นสายสุขภาพ-การแพทย์ |
| [**Scopus AI**](https://www.scopus.com/) | ฐานข้อมูลใหญ่น่าเชื่อถือ, Concept Maps, Deep Research |
| [**NotebookLM**](https://notebooklm.google.com/) | อ่านเอกสารที่ upload, ลด hallucination, สร้าง Mind Map |

---

## SciSpace

🔗 https://scispace.com/

**จุดเด่น**
- จัดระเบียบข้อมูล Export ได้ง่าย
- มี AI Writer, Literature Review, Citation Generator
- เหมาะทั้งผู้เริ่มต้นและผู้เชี่ยวชาญ

**ข้อจำกัด**
- ไม่สามารถเข้าถึงบทความแบบเสียเงินโดยไม่มี subscription
- ไม่สามารถ Export Bibliography ใน Free Version

---

## Elicit

🔗 https://elicit.com/

**จุดเด่น**
- ฐานข้อมูล **125 ล้านฉบับ**
- รองรับ **PICO framework** (Population, Intervention, Comparison, Outcome)
- ลดเวลา Systematic Review ได้ **มากถึง 80%**
- ทุกคำตอบมีแหล่งอ้างอิงตรวจสอบได้ — ลด Hallucination

**ข้อจำกัด**
- พึ่ง Semantic Scholar — อาจไม่ครอบคลุมทุกงาน
- ภาษาไทยยังไม่สมบูรณ์

---

## Consensus AI

🔗 https://consensus.app/

**จุดเด่น**
- **Consensus Meter** — แสดงระดับความเห็นพ้องของงานวิจัย
- เชื่อมต่อ PubMed, Semantic Scholar, OpenAlex
- เด่นด้าน **สุขภาพ-การแพทย์**

**ข้อจำกัด**
- AI credits จำกัด (Free: 20 ครั้ง/เดือน)
- ภาษาไทยมีข้อจำกัดด้าน NLP
- ไม่เชื่อมต่อฐานข้อมูลภาษาไทย (ThaiJo, TDC)

---

## Scopus AI

🔗 https://www.scopus.com/

**จุดเด่น**
- ฐานข้อมูลใหญ่และน่าเชื่อถือที่สุด (peer-reviewed)
- **Concept Maps** — แสดงความสัมพันธ์หัวข้อ/นักวิจัย
- **Deep Research** — สร้าง Research Synthesis Report
- ระบุแหล่งอ้างอิงทุกข้อสรุป

**ข้อจำกัด**
- ต้องมี subscription เพื่อเข้าถึง full-text
- ผลการค้นหาเป็นภาษาอังกฤษเกือบทั้งหมด

---

## เทคนิค Literature Review ด้วย NotebookLM

🔗 https://notebooklm.google.com/

1. Upload บทความที่เกี่ยวข้องลงใน NotebookLM
2. สร้าง **Mind Map** เพื่อดูความสัมพันธ์ของงานวิจัย
3. ใช้ Mind Map เป็นโครงร่าง Literature Review
4. นำ Draft ไปขยายต่อใน ChatGPT
5. ตรวจสอบความถูกต้องและใส่ Reference

---

## ChatGPT / Gemini ใช้ค้นหาบทความได้ไหม?

<div class="columns">

<div>

**✅ ทำได้**
- สร้าง **keywords** สำหรับค้นหา
- สรุปบทความที่ **paste ข้อความให้**
- ร่างโครงสร้าง Literature Review
- อธิบายแนวคิดและทฤษฎีต่าง ๆ

</div>

<div>

**❌ ไม่ควรทำ**
- ให้หาบทความตรง ๆ — เสี่ยง **Hallucination สูง**
- สร้างชื่อบทความ / DOI ที่ **ไม่มีอยู่จริง**
- นำ reference จาก ChatGPT ไปใช้โดยไม่ตรวจสอบ

</div>

</div>

---

## เปรียบเทียบ: ChatGPT/Gemini vs เครื่องมือเฉพาะทาง

| ความสามารถ | ChatGPT / Gemini | Elicit / SciSpace / Scopus AI |
|---|---|---|
| ค้นหาบทความจริง | ❌ ไม่เชื่อมฐานข้อมูล | ✅ เชื่อมโดยตรง |
| Hallucinate citations | ⚠️ เสี่ยงสูง | ✅ มี citation จริง |
| สรุปบทความที่ upload | ✅ ทำได้ดี | ✅ ทำได้ดี |
| ช่วยวางโครงสร้าง | ✅ ทำได้ดี | ⚠️ จำกัด |

> **แนวทางแนะนำ**: ใช้ Elicit/ScopusAI **หาบทความ** → นำมาใส่ใน **NotebookLM หรือ ChatGPT** เพื่อสรุปและร่าง Literature Review ต่อ

---

<!-- _class: divider -->

## 07
## Stage 3: Research Design

Method Planning with AI

---

## การออกแบบวิธีวิจัยด้วย AI

**ขั้นตอน:**
1. ส่ง Literature Review + หัวข้อที่เลือกให้ AI
2. ให้ AI แนะนำวิธีวิจัยที่เหมาะสม
3. เลือกวิธีวิจัยที่ต้องการ
4. ให้ AI ช่วยออกแบบ **เครื่องมือวิจัย** (แบบสอบถาม, แบบประเมิน)
5. เขียน Methodology เป็นภาษาอังกฤษ

---

## ตัวอย่าง Prompt สำหรับ Stage 3

<div class="columns">

<div>

**Prompt 1:**
> *"ฉันเลือกหัวข้อ 'กรอบนโยบายสำหรับการบูรณาการ Generative AI อย่างมีจริยธรรมในมหาวิทยาลัย' ช่วยแนะนำวิธีวิจัยที่เหมาะสม"*

**Prompt 2:**
> *"เขียนวัตถุประสงค์การวิจัยและ Scope of Work เป็นภาษาอังกฤษ"*
</div>
<div>

**Prompt 3:**
> *"Create the form for expert evaluation"*

</div>
</div>

---

<!-- _class: divider -->

## 08
## Stage 4: Data Work

Analytical Reasoning with AI

---

## การวิเคราะห์ข้อมูลด้วย AI

**ขั้นตอน:**
1. **จำลองข้อมูล** (Dummy Data) เพื่อทดสอบการวิเคราะห์
2. ให้ AI ระบุ **สถิติที่เหมาะสม** กับข้อมูล
3. ให้ AI คำนวณ **Descriptive Statistics**
4. ให้ AI สร้าง **ตาราง/กราฟ** สรุปผล
5. ร่าง **Discussion** จากผลที่ได้

---

## ตัวอย่าง Prompt สำหรับ Stage 4

<div class="columns">

<div>

**หาสถิติที่เหมาะสม:**
> *"From data Part 2: Evaluation (Likert Scale 1–5). What stat that we can produce?"*

**คำนวณ:**
> *"Compute Descriptive Statistics"*

</div>
<div>

**สร้างกราฟ:**
> *"จากตารางสร้าง เราควรสร้างเป็นกราฟหรือตารางดี"*

**เขียน Discussion:**
> *"Write the discussion from these results"*
</div>
</div>

---

<!-- _class: divider -->

## 09
## Stage 5: Scholarly Writing

Academic Paper with AI

---

## ลำดับการเขียนบทความวิชาการ

```
ข้อมูล → บทที่ 4 (Result) → บทที่ 5 (Conclusion)
      → บทที่ 1 (Introduction) → Abstract → Polishing
```

| ลำดับ | บท | เนื้อหา |
|---|---|---|
| 1 | Chapter 4 | Result and Discussion |
| 2 | Chapter 5 | Conclusion |
| 3 | Chapter 3 | Methodology |
| 4 | Chapter 2 | Literature Review |
| 5 | Chapter 1 | Introduction |
| 6 | — | Abstract & Polishing |

---

## ตัวอย่าง Prompt สำหรับ Stage 5

<div class="columns">
<div>

**เขียน Conclusion:**
> *"Rewrite the conclusion"*

**เขียน Introduction:**
> *"Rewrite the introduction section"*

</div>
<div>

**เขียน Abstract:**
> *"Rewrite the abstract"*

**เครื่องมือเขียนบทความ:**
- Microsoft Word
- LaTeX / Overleaf (overleaf.com)

</div>
</div>

---

## Declaration of Using Generative AI

ต้องระบุในบทความ:

- **ชื่อ AI** ที่ใช้ (เช่น ChatGPT, Claude, Gemini)
- **จุดประสงค์** การใช้งาน (เช่น ปรับปรุงภาษา, สรุปเนื้อหา)
- ใส่ไว้ **ท้ายบทความ ก่อนรายการอ้างอิง**

> ตัวอย่าง: *"The authors used ChatGPT (OpenAI) to improve the readability of the manuscript. The authors reviewed and edited all AI-generated content."*

---

<!-- _class: divider -->

## สรุป
## HIRF Workflow

Human Intelligence Leads, AI Assists

---

## สรุป HIRF Framework

| Stage | กระบวนการ | ผลลัพธ์ |
|---|---|---|
| 1 | Problem Framing | ประเด็นวิจัย, คำถามวิจัย |
| 2 | Literature Review | สังเคราะห์วรรณกรรม, กรอบแนวคิด |
| 3 | Research Design | แผนวิจัย, เครื่องมือ |
| 4 | Data & Analysis | ผลการวิเคราะห์, ตาราง/กราฟ |
| 5 | Scholarly Writing | บทความ, วิทยานิพนธ์, สไลด์ |

> **หลักการ**: มนุษย์ตัดสินใจ — AI ช่วยเสริมและเร่งกระบวนการ


---

## วิทยากร

<div class="columns">

<div>

**ผศ.ดร.ทวีศักดิ์ สมานชื่น**
*Asst. Prof. Taweesak Samanchuen, Ph.D.*

- รองผู้อำนวยการฝ่ายดิจิทัลเทคโนโลยี **MULKC**
- อาจารย์ประจำสาขา **ITM** คณะวิศวกรรมศาสตร์ มหาวิทยาลัยมหิดล
- หัวหน้าโครงการ **CBTU**

📧 t.samanchuen@gmail.com
☎ 081-441-4906
🔗 [itm.eg.mahidol.ac.th](https://itm.eg.mahidol.ac.th/personnel/taweesak-samanchuen/)

</div>

<div>

![w:400px](/fig/googleScholar.png)

</div>

</div>

---

<!-- _class: lead -->

# ขอบคุณ

**ผศ.ดร.ทวีศักดิ์ สมานชื่น**

📧 t.samanchuen@gmail.com | ☎ 081-441-4906
