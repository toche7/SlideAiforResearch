---
marp: true
theme: mahidol-green
paginate: true
size: 16:9
footer: "Feynman AI — Open Source Research Agent | ITM, Mahidol University"
---

<!-- _class: lead -->

<style scoped>
img { position: absolute; top: 36px; right: 64px; width: 150px; height: 150px; object-fit: contain; }
</style>

<img src="fig/logos/mahidol.svg" alt="Mahidol University">

# Feynman AI
# Open Source AI Research Agent

<div class="subtitle">feynman.is — อ่านบทความ · ค้นหาข้อมูล · รันการทดลอง · อ้างอิงทุก Claim</div>

**ผศ.ดร.ทวีศักดิ์ สมานชื่น**
กลุ่มสาขาวิชา ITM | มหาวิทยาลัยมหิดล

May 2026

---

## Feynman AI คืออะไร?

<div class="columns">

<div>

**AI Research Agent แบบ Open Source**
- 🧠 ทำงานบนเครื่องของคุณเองแบบ **Local**
- 🔍 อ่านบทความ ค้นหาเว็บ เขียนร่าง รันทดลอง
- 📎 **อ้างอิงทุก Claim** — ไม่มี Hallucination แบบไม่มีที่มา
- 🔓 Open Source — ใช้ได้ฟรี แก้ไขได้

</div>

<div>

**ทำไม Feynman?**
- ตั้งชื่อตาม **Richard Feynman** นักฟิสิกส์ผู้โด่งดัง
- แนวคิด: *"ถ้าอธิบายไม่ได้ แสดงว่ายังไม่เข้าใจจริง"*
- เน้นความ **โปร่งใส** และ **ตรวจสอบได้**
- Built on **Pi** and **alphaXiv** platforms

</div>
</div>

> 🚀 **ติดตั้งง่าย**: `curl -fsSL https://feynman.is/install | bash`

---

## Chatbot vs. Agent CLI — ต่างกันอย่างไร?

<div class="columns">

<div>

**💬 Chatbot (ChatGPT / Gemini)**
- โต้ตอบผ่าน **Web UI** หรือ App
- ตอบคำถามแบบ **ครั้งต่อครั้ง** (Conversational)
- ทำงานบน **Cloud** ของผู้ให้บริการ
- ไม่มี Memory ข้ามเซสชันโดย default
- **ไม่สามารถรัน Code หรือ Experiment** ได้เอง
- ผลลัพธ์อาจ Hallucinate — อ้างอิงไม่แน่นอน
- ควบคุม Privacy ของข้อมูลได้น้อย

</div>

<div>

**🤖 Agent CLI (Feynman)**
- ทำงานผ่าน **Terminal** บนเครื่องของคุณ
- ดำเนินงานแบบ **Task-oriented** — วางแผนและรัน
- ทำงาน **Local** — ข้อมูลไม่ออกนอกเครื่อง
- จำ Context ข้าม **หลาย Session**
- **รัน Code จริงใน Docker** และวัดผลได้
- ทุก output **มีแหล่งอ้างอิง** ตรวจสอบได้
- ส่งงานต่อระหว่าง **Multi-agent** อัตโนมัติ

</div>
</div>

> **กล่าวง่าย ๆ**: Chatbot = ผู้ช่วยตอบคำถาม | Agent CLI = ผู้ช่วยที่ **ลงมือทำงานแทน** คุณได้

---

## เริ่มใช้งาน — Command พื้นฐาน

| คำสั่ง | ผลลัพธ์ |
|--------|---------|
| `feynman "what do we know about scaling laws"` | สรุปงานวิจัยพร้อมอ้างอิง |
| `feynman deepresearch "mechanistic interpretability"` | Multi-agent deep dive + synthesis |
| `feynman lit "RLHF alternatives"` | Literature review + consensus |
| `feynman audit 2401.12345` | ตรวจสอบ Paper vs. Code จริง |
| `feynman replicate "chain-of-thought improves math"` | วางแผนและรัน Replication |

> **ทุก output มีการอ้างอิงแหล่งที่มา** — ใช้ในงานวิชาการได้อย่างมั่นใจ

---

## Workflows — Slash Commands

<div class="columns">

<div>

**การวิจัย**
- `/deepresearch` — สืบค้นลึกจาก Papers + Web + Code
- `/lit` — Literature Review จากแหล่งปฐมภูมิ
- `/audit` — ตรวจสอบความสอดคล้อง Paper-to-Code
- `/replicate` — วางแผนและรัน Replication

</div>

<div>

**การเขียนและติดตาม**
- `/review` — Peer Review จำลอง พร้อม Severity Score
- `/compare` — เปรียบเทียบแหล่งข้อมูลแบบ Side-by-side
- `/draft` — ร่างบทความพร้อม Inline Citations
- `/autoresearch` — วนซ้ำอัตโนมัติ: สมมติฐาน → ทดลอง → วัดผล
- `/watch` — ติดตาม Papers/Code ใหม่แบบอัตโนมัติ

</div>
</div>

---

## ทีม AI Agents

<div class="columns">

<div>

**🔬 Researcher**
ค้นหาหลักฐานจาก Papers, เว็บ, Repos และ Docs

**📝 Writer**
จัดโครงสร้าง Notes เป็น Briefs, Drafts และ Paper-style output

</div>

<div>

**🔎 Reviewer**
ให้คะแนน Claim ตาม Severity, ระบุช่องว่าง, แนะนำการปรับปรุง

**✅ Verifier**
ตรวจสอบทุก Citation, ยืนยัน URL, ลบ Dead Links

</div>
</div>

> Feynman จัดทีม Agent ที่เหมาะสมให้อัตโนมัติตามคำถามของคุณ

---

## Skills & Tools

<div class="columns">

<div>

**ค้นหาและอ่านข้อมูล**
- 📄 **AlphaXiv** — ค้นหา Paper, Q&A, อ่าน Code และ Annotations
- 🌐 **Web Search** — ผ่าน Gemini หรือ Perplexity
- 🗂️ **Session Search** — จำ Context ข้ามหลาย Research Sessions

</div>

<div>

**Export และ Preview**
- 🌍 **Browser Preview** — ดูผลลัพธ์ก่อน Export
- 📄 **PDF Export** — บันทึก Artifact ที่สร้างขึ้น

**ระบบ**
- ทุก Capability เป็น **Pi Skills**
- ทุก Output ผูกกับ **Source** เสมอ

</div>
</div>

---

## Compute — รันการทดลองได้จริง

<div class="columns">

<div>

**Local Environment**
- 🐳 **Docker** — Container แยกสำหรับการทดลองที่ปลอดภัย
- รัน Experiment โดยไม่กระทบสิ่งแวดล้อมหลัก

</div>

<div>

**Cloud GPU (Burst)**
- ⚡ **Modal** — Serverless GPU สำหรับ Training และ Inference
- 🖥️ **RunPod** — GPU Pod แบบ Persistent พร้อม SSH Access

</div>
</div>

> Feynman ไม่ได้แค่ "ค้นหา" — สามารถ **รันการทดลองจริง** และวัดผลได้

---

## Feynman vs. เครื่องมือวิจัย AI อื่น

| ฟีเจอร์ | Feynman | ChatGPT/Gemini | Elicit | Connected Papers |
|--------|:-------:|:--------------:|:------:|:----------------:|
| Open Source | ✅ | ❌ | ❌ | ❌ |
| Local / Private | ✅ | ❌ | ❌ | ❌ |
| อ้างอิงทุก Claim | ✅ | ⚠️ | ✅ | N/A |
| รัน Experiment ได้ | ✅ | ❌ | ❌ | ❌ |
| Multi-agent | ✅ | ❌ | ❌ | ❌ |
| Paper-to-Code Audit | ✅ | ❌ | ❌ | ❌ |

---

## Use Cases สำหรับนักวิจัย

<div class="columns">

<div>

**เตรียม Literature Review**
```
feynman lit "explainable AI in healthcare"
```
→ ได้ Consensus, Open Questions, Citations

**ตรวจสอบงานวิจัยก่อน Cite**
```
feynman audit 2312.12345
```
→ เช็ก Paper vs. Code จริงว่าตรงกันไหม

</div>

<div>

**ติดตาม Field อัตโนมัติ**
```
feynman /watch "LLM reasoning benchmarks"
```
→ แจ้งเตือนเมื่อมี Paper ใหม่

**วางแผน Replication Study**
```
feynman replicate "GPT-4 outperforms doctors"
```
→ ได้ Replication Plan + Compute Estimate

</div>
</div>

---

## เริ่มต้นใช้ Feynman AI

<div class="columns">

<div>

**ติดตั้ง (ใช้ curl)**
```bash
curl -fsSL https://feynman.is/install | bash
```

**หรือผ่าน npm**
```bash
npm install -g feynman
```

**ถ้าต้องการแค่ Skills**
ดูที่ [feynman.is/docs](https://www.feynman.is/docs/getting-started/installation)
สำหรับ Skills-only bundle

</div>

<div>

**แหล่งข้อมูลเพิ่มเติม**
- 🌐 Website: [feynman.is](https://www.feynman.is)
- 📚 Docs: [feynman.is/docs](https://www.feynman.is/docs/getting-started/installation)
- 💻 GitHub: [github.com/getcompanion-ai/feynman](https://github.com/getcompanion-ai/feynman)

**Built on**
- [Pi](https://github.com/badlogic/pi-mono) — Pi Skill System
- [alphaXiv](https://www.alphaxiv.org/) — Paper Discovery

</div>
</div>

---

<!-- _class: lead -->

# สรุป

**Feynman AI** คือ Open Source AI Research Agent
ที่รันบนเครื่องของคุณ — อ่านบทความ ค้นหา เขียน และรัน Experiment

> *"อธิบายให้ได้ จึงจะเข้าใจจริง"* — Richard Feynman

🔗 **feynman.is** | GitHub: `getcompanion-ai/feynman`
