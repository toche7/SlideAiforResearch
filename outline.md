

# โครงสไลด์ช่วงเช้า วันที่ 2

**Theme: From Research Questions to Machine Learning-based Research Design**

---

## Section 1: Opening & Learning Goals

**ประมาณ 3–4 สไลด์**

### Slide 1: Title Slide

**From Research Questions to Machine Learning-based Research Design**

เนื้อหา:

- เป้าหมายของช่วงเช้า
    
- เชื่อมโยงจากวันที่ 1: AI for Research / HIRF
    
- สิ่งที่จะนำไปใช้ต่อช่วงบ่าย: Mini Proposal
    

---

### Slide 2: What We Will Do This Morning

หัวข้อ:

- แปลงคำถามวิจัยเป็นโจทย์ ML
    
- เข้าใจประเภทของ ML
    
- รู้จัก target, features, dataset, metrics
    
- ออกแบบ ML-based analysis plan
    

---

### Slide 3: Morning Output

สิ่งที่ผู้เข้าอบรมต้องได้ก่อนพักเที่ยง:

1. Research Question Mapping
    
2. Data Science Objective
    
3. ML Task
    
4. Target Variable / Features
    
5. Draft ML-based Analysis Plan
    

---

### Slide 4: Why ML Matters in Research

ประเด็น:

- ML ช่วยค้นหารูปแบบจากข้อมูล
    
- ML ช่วยทำนายหรือจำแนกกลุ่ม
    
- ML เหมาะกับข้อมูลซับซ้อนหรือหลายตัวแปร
    
- แต่ ML ไม่ได้แทนที่ research design และ researcher judgment
    

---

# Section 2: From Research Questions to ML Problems

**ประมาณ 7–8 สไลด์**

### Slide 5: Research Question คืออะไร

เนื้อหา:

- คำถามหลักที่งานวิจัยต้องการตอบ
    
- ต้องชัดเจน วัดได้ และสอดคล้องกับ methodology
    
- ตัวอย่าง:
    
    - ปัจจัยใดสัมพันธ์กับความเสี่ยงของผู้ป่วย?
        
    - สามารถทำนายผลลัพธ์การรักษาได้หรือไม่?
        

---

### Slide 6: Research Question vs Data Science Question

ทำเป็นตาราง:

|Research Question|Data Science Question|
|---|---|
|ปัจจัยใดสัมพันธ์กับผลลัพธ์|ตัวแปรใดช่วยทำนายผลลัพธ์ได้ดี|
|กลุ่มตัวอย่างมีลักษณะอย่างไร|สามารถแบ่งกลุ่มจาก pattern ได้หรือไม่|
|ความคิดเห็นสะท้อนประเด็นใด|สามารถจำแนก/สกัด theme จากข้อความได้หรือไม่|

---

### Slide 7: Research Objective vs Data Science Objective

ตัวอย่าง:

**Research Objective:**  
เพื่อศึกษาปัจจัยที่เกี่ยวข้องกับการกลับมารักษาซ้ำของผู้ป่วย

**Data Science Objective:**  
เพื่อพัฒนาโมเดลจำแนกผู้ป่วยที่มีความเสี่ยงสูงต่อการกลับมารักษาซ้ำภายใน 30 วัน

---

### Slide 8: Formula การแปลงหัวข้อวิจัยเป็น ML Project

ใช้โครงนี้:

> Research Topic → Research Question → Data Science Objective → ML Task → Target Variable → Features → Metrics

สไลด์นี้สำคัญมาก ควรทำเป็น diagram

---

### Slide 9: เมื่อใดควรใช้ ML ในงานวิจัย

ใช้ ML เมื่อ:

- ต้องการทำนายผลลัพธ์
    
- ต้องการจำแนกกลุ่ม
    
- ต้องการหากลุ่มแฝง
    
- มีข้อมูลหลายตัวแปร
    
- มีข้อมูลข้อความจำนวนมาก
    
- ต้องการ pattern ที่อาจมองไม่เห็นด้วยวิธีพื้นฐาน
    

ไม่ควรใช้ ML เมื่อ:

- ข้อมูลน้อยมาก
    
- คำถามต้องการแค่สถิติเชิงพรรณนา
    
- ไม่มี target หรือข้อมูลที่ชัดเจน
    
- ไม่สามารถอธิบายผลลัพธ์ได้อย่างน่าเชื่อถือ
    

---

### Slide 10: Example 1 — Classification

หัวข้อ:  
**ทำนายความเสี่ยงการกลับมารักษาซ้ำภายใน 30 วัน**

เนื้อหา:

- ML Task: Classification
    
- Target: Readmission Yes/No
    
- Features: อายุ เพศ โรคร่วม จำนวนวันนอน รพ. ผลตรวจ
    
- Metrics: Precision, Recall, F1-score
    

---

### Slide 11: Example 2 — Regression

หัวข้อ:  
**ทำนายระยะเวลานอนโรงพยาบาล**

เนื้อหา:

- ML Task: Regression
    
- Target: Length of Stay
    
- Features: อายุ โรคหลัก ความรุนแรง ผลแล็บ
    
- Metrics: MAE, RMSE, R²
    

---

### Slide 12: Example 3 — Clustering / NLP

แบ่งครึ่งสไลด์:

**Clustering:**  
แบ่งกลุ่มผู้ป่วยตามพฤติกรรมสุขภาพ

**NLP:**  
วิเคราะห์ความคิดเห็นจากแบบสอบถามปลายเปิด

---

# Section 3: Introduction to Machine Learning for Research

**ประมาณ 12–14 สไลด์**

### Slide 13: Machine Learning คืออะไร

นิยามแบบง่าย:

> Machine Learning คือการให้คอมพิวเตอร์เรียนรู้รูปแบบจากข้อมูล เพื่อทำนาย จำแนก หรือค้นหารูปแบบใหม่

เน้นว่าในงานวิจัย ML คือ “เครื่องมือวิเคราะห์ข้อมูล” ไม่ใช่แค่เทคโนโลยีล้ำสมัย

---

### Slide 14: AI vs ML vs Deep Learning

ทำเป็นแผนภาพวงซ้อน:

- AI = แนวคิดใหญ่
    
- ML = วิธีให้ระบบเรียนรู้จากข้อมูล
    
- Deep Learning = ML ที่ใช้ neural networks หลายชั้น
    
- Generative AI = AI ที่สร้างข้อความ ภาพ โค้ด หรือเนื้อหา
    

---

### Slide 15: Traditional Statistics vs Machine Learning

ตารางเปรียบเทียบ:

|ประเด็น|Statistics|Machine Learning|
|---|---|---|
|เป้าหมาย|อธิบาย/ทดสอบสมมติฐาน|ทำนาย/จำแนกรูปแบบ|
|คำถาม|ปัจจัยใดมีนัยสำคัญ|โมเดลทำนายได้ดีแค่ไหน|
|ผลลัพธ์|p-value, CI, effect size|accuracy, F1, RMSE|
|จุดแข็ง|ตีความง่าย|จัดการ pattern ซับซ้อน|
|จุดเสี่ยง|assumption|overfitting / black box|

---

### Slide 16: Types of Machine Learning

หัวข้อ:

- Supervised Learning
    
- Unsupervised Learning
    
- Semi-supervised Learning
    
- Reinforcement Learning แบบกล่าวถึงสั้น ๆ
    

เน้นแค่ 2 กลุ่มหลักที่ใช้ใน workshop:

- Supervised
    
- Unsupervised
    

---

### Slide 17: Supervised Learning

เนื้อหา:

- มีข้อมูล input และคำตอบที่ถูกต้อง
    
- ใช้สำหรับ prediction/classification
    
- ตัวอย่าง:
    
    - ทำนายระยะเวลานอนโรงพยาบาล
        
    - จำแนกกลุ่มเสี่ยง
        
    - ทำนายผลการรักษา
        

---

### Slide 18: Regression

เนื้อหา:

- ใช้เมื่อ target เป็นค่าตัวเลขต่อเนื่อง
    
- ตัวอย่าง target:
    
    - Length of stay
        
    - Cost
        
    - Quality of life score
        
    - Satisfaction score
        
- Metrics:
    
    - MAE
        
    - RMSE
        
    - R²
        

---

### Slide 19: Classification

เนื้อหา:

- ใช้เมื่อ target เป็นกลุ่มหรือ class
    
- ตัวอย่าง target:
    
    - High risk / Low risk
        
    - Readmission: Yes / No
        
    - Improved / Not improved
        
    - Positive / Negative sentiment
        
- Metrics:
    
    - Accuracy
        
    - Precision
        
    - Recall
        
    - F1-score
        

---

### Slide 20: Unsupervised Learning

เนื้อหา:

- ไม่มี target variable
    
- ใช้ค้นหาโครงสร้างหรือ pattern ในข้อมูล
    
- เหมาะกับ exploratory research
    

---

### Slide 21: Clustering

เนื้อหา:

- ใช้แบ่งกลุ่มจากความคล้ายกันของข้อมูล
    
- ตัวอย่าง:
    
    - กลุ่มผู้ป่วยตามพฤติกรรมสุขภาพ
        
    - กลุ่มผู้รับบริการตามรูปแบบการใช้บริการ
        
    - กลุ่มงานวิจัยตามหัวข้อ
        
- Output:
    
    - Cluster profiles
        
    - Pattern interpretation
        

---

### Slide 22: Text Mining / NLP for Research

เนื้อหา:

- ใช้กับข้อมูลข้อความ
    
- ตัวอย่าง:
    
    - abstract
        
    - interview transcript
        
    - open-ended survey
        
    - patient feedback
        
    - policy documents
        
- งานที่ทำได้:
    
    - topic extraction
        
    - sentiment analysis
        
    - text classification
        
    - summarization
        

---

### Slide 23: ML Pipeline for Research

ควรทำเป็น diagram:

> Data → Cleaning → Feature Engineering → Model Training → Evaluation → Interpretation → Research Conclusion

---

### Slide 24: Dataset Structure for ML

อธิบายง่าย ๆ:

|Row|หน่วยข้อมูล|
|---|---|
|ผู้ป่วย 1 คน|1 observation|
|โครงการวิจัย 1 โครงการ|1 observation|
|แบบสอบถาม 1 ชุด|1 observation|
|abstract 1 บทความ|1 observation|

Column:

- features
    
- target variable
    
- metadata
    

---

### Slide 25: Target Variable and Features

ตัวอย่าง:

|ส่วน|ความหมาย|ตัวอย่าง|
|---|---|---|
|Target|สิ่งที่ต้องการทำนาย|Readmission Yes/No|
|Features|ตัวแปรที่ใช้ทำนาย|อายุ เพศ โรคร่วม ผลแล็บ|
|Model|วิธีเรียนรู้จากข้อมูล|Logistic Regression / Random Forest|
|Metrics|วิธีวัดผล|Recall / F1|

---

### Slide 26: Model Evaluation แบบเข้าใจง่าย

หัวข้อ:

- โมเดลต้องวัดผล ไม่ใช่แค่สร้างได้
    
- ต้องแยก train/test
    
- ต้องระวัง overfitting
    
- เลือก metric ให้ตรงโจทย์
    

---

# Section 4: Designing ML-based Analysis Plan

**ประมาณ 8–10 สไลด์**

### Slide 27: What is an ML-based Analysis Plan?

เนื้อหา:  
แผนที่บอกว่าเราจะใช้ข้อมูลอะไร ใช้โมเดลอะไร วัดผลอย่างไร และตีความอย่างไร

---

### Slide 28: Components of ML-based Analysis Plan

หัวข้อ:

1. Research Objective
    
2. Data Science Objective
    
3. Dataset
    
4. Target Variable
    
5. Features
    
6. Preprocessing
    
7. Candidate Models
    
8. Evaluation Metrics
    
9. Interpretation
    
10. Bias and Limitation
    

---

### Slide 29: Step 1 — Define the Data Science Objective

ตัวอย่างประโยค:

> To develop a machine learning model to predict/classify/cluster/analyze [target or pattern] using [data source].

---

### Slide 30: Step 2 — Identify Target Variable

คำถามนำ:

- เราต้องการทำนายอะไร?
    
- คำตอบเป็นตัวเลขหรือกลุ่ม?
    
- วัดได้จริงไหม?
    
- มีข้อมูล target นี้หรือไม่?
    

---

### Slide 31: Step 3 — Identify Features

คำถามนำ:

- ตัวแปรใดอาจช่วยทำนาย target?
    
- เก็บข้อมูลได้จริงหรือไม่?
    
- มีประเด็น privacy หรือไม่?
    
- มีตัวแปรที่อาจก่อให้เกิด bias หรือไม่?
    

---

### Slide 32: Step 4 — Choose ML Task

ทำเป็น decision rule:

|คำถาม|ML Task|
|---|---|
|ต้องการทำนายตัวเลข|Regression|
|ต้องการจำแนกกลุ่ม|Classification|
|ต้องการแบ่งกลุ่มโดยไม่มีคำตอบล่วงหน้า|Clustering|
|ต้องการวิเคราะห์ข้อความ|NLP/Text Mining|

---

### Slide 33: Step 5 — Choose Evaluation Metrics

ตาราง:

|ML Task|Metrics|
|---|---|
|Regression|MAE, RMSE, R²|
|Classification|Accuracy, Precision, Recall, F1|
|Clustering|Silhouette, cluster profile|
|NLP|Accuracy, F1, topic coherence, human validation|

---

### Slide 34: Bias and Limitation in ML Research

หัวข้อ:

- sample bias
    
- missing data
    
- class imbalance
    
- overfitting
    
- limited generalizability
    
- lack of interpretability
    
- ethical and privacy concerns
    

---

### Slide 35: How to Write ML Methodology in Proposal

ให้โครง paragraph:

> This study will use a machine learning approach to [predict/classify/analyze] [target]. The dataset will include [data source] with variables such as [features]. Candidate models may include [models]. Model performance will be evaluated using [metrics]. Potential limitations include [bias/limitation].

---

### Slide 36: Example Methodology Paragraph

ยกตัวอย่างหนึ่งโจทย์ เช่น readmission หรือ length of stay

---

# Section 5: Morning Workshop

**ประมาณ 5–6 สไลด์**

### Slide 37: Activity — Research Question to ML Project

ให้ผู้เข้าอบรมกรอก:

1. Research Topic
    
2. Research Question
    
3. Research Objective
    
4. Data Science Objective
    
5. ML Task
    

---

### Slide 38: Activity — Target and Features Mapping

ให้เติมตาราง:

|Target Variable|Feature 1|Feature 2|Feature 3|Feature 4|Feature 5|
|---|---|---|---|---|---|

---

### Slide 39: Activity — ML Task Selection

ให้เลือก:

- Regression
    
- Classification
    
- Clustering
    
- NLP/Text Mining
    

พร้อมให้เหตุผลว่าเพราะอะไร

---

### Slide 40: Activity — Evaluation Metrics

ให้ระบุ:

- จะใช้ metric อะไร
    
- metric นี้ตอบโจทย์วิจัยอย่างไร
    
- หาก metric ดี แปลว่าอะไรในบริบทงานวิจัย
    

---

### Slide 41: ML-based Analysis Plan Canvas

สไลด์นี้เป็นใบงานหลัก:

|Component|Your Project|
|---|---|
|Research Topic||
|Research Objective||
|Data Science Objective||
|Dataset||
|Target Variable||
|Features||
|ML Task||
|Candidate Models||
|Evaluation Metrics||
|Bias / Limitation||

---

### Slide 42: Prompt Template for AI Assistance

```text
I am designing a research project on [topic].
My research question is [research question].
Please help me convert it into a machine learning-based analysis plan.
Include data science objective, ML task, target variable, input features, possible dataset, candidate models, evaluation metrics, and limitations.
```

---

# Section 6: Transition to Afternoon Proposal Workshop

**ประมาณ 2–3 สไลด์**

### Slide 43: From ML Analysis Plan to Mini Proposal

เชื่อมว่าแผน ML ช่วงเช้าจะกลายเป็นส่วนหนึ่งของ proposal ช่วงบ่าย

|Morning Output|Afternoon Proposal Section|
|---|---|
|Research Topic|Title|
|Research Question|RQ|
|Data Science Objective|Objective / Method|
|Target & Features|Data / Variables|
|ML Task|Methodology|
|Metrics|Analysis Plan|
|Bias / Limitation|Limitation / Ethics|

---

### Slide 44: Afternoon Task Preview

ช่วงบ่ายจะทำ:

- Mini Proposal
    
- Preliminary Findings
    
- Presentation
    
- Feedback
    

---

### Slide 45: Checklist Before Lunch

ผู้เข้าอบรมควรมี:

- Research Topic
    
- Research Question
    
- Data Science Objective
    
- ML Task
    
- Target Variable
    
- Features
    
- Evaluation Metrics
    
- Draft ML-based Analysis Plan
    

---

