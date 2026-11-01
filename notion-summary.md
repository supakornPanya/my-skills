# Description
Summarize lecture materials, slides, articles, or technical topics from any subject into Notion-ready study notes matching the user's custom short-note style (Problem-Solution logic chains, Pro/Con bullets, bilingual Thai-English phrasing, comparison tables, and visual emphasis). Use when the user asks for a notion-summary, wants notes formatted for Notion, or asks to summarize lecture content into study notes.
# Notion Summary

Generate concise, high-density study notes formatted for direct copy-pasting into Notion. The formatting follows the exact short-note structures, visual cues, and bilingual patterns seen in the SDS and Security notes, applicable to any academic or technical subject.

## When to Use

- The user asks for a `notion-summary` or includes `notion-summary` in the request.
- The user provides lecture slides, transcripts, syllabus topics, or technical reading and asks to summarize them for Notion.
- The user asks for short notes, study guides, or exam review sheets to paste into their Notion workspace.

## Core Formatting Rules

Structure all notes to be visually scannable, punchy, and organized for Notion blocks.

### 1. Hierarchy and Headers

- Use `# Week X - Topic Title` or `# [Subject] - Topic Title` as the main page title.
- Use `# 1. Major Section Name` for numbered top-level topics.
- Use `### 1.1 Subsection Name` for specific subtopics.
- Separate distinct conceptual sections with a horizontal divider `---`.

### 2. Logic Chains and Problem-Solution Flow

- Chain causes, transitions, and effects using arrows `->`:
  `Problem -> Solution -> Result`
- Highlight guiding questions and core intuitions with a lightbulb icon:
  `-> 💡 "How can we develop a program once and run it anywhere?"`
- When breaking down patterns or architectures, use explicit Problem vs. Solution blocks:
  - **Problem before X**: Describe limitations or pain points.
  - **Solution with X**: Describe the new mechanism or design.
  - **Result / Pro**: State the tangible benefits.

### 3. Definitions, Questions, and Quotes

- Pair English technical terms with Thai translations and memorable guiding questions in quotes:
  `- **Authentication (พิสูจน์ตัวตน)**: *"Who are you? Are you really the person whom you claim to be?"* ตรวจสอบว่าผู้ใช้คือใครจริงไหม`
  `- **!!!Security**: *"Who can do what when?"* การควบคุมสิทธิ์และตรวจสอบว่า ใคร ทำอะไร ได้ตอนไหน`
- Underline key classification labels:
  `- <u>**Definition**</u>: ...`
  `- <u>**Component**</u>: ...`
  `- <u>**Example**</u>: ...`

### 4. Pros and Cons Structure

- Break down advantages and disadvantages using structured bullet blocks:
  `- **Pro**:`
    - High portability, rapid deployment
    - Decoupled scaling (Service เป็นอิสระจากกัน)
  `- **Con**:`
    - Distributed system overhead
    - Complex monitoring and data consistency
- For quick comparisons, place inline:
  `- <u>**Pro</u>:** เบา ใช้เท่าที่จำเป็น, <u>**Con</u>:** ขาด Isolation, Not portable`

### 5. Intuition, Analogies, and Common Traps

- Include personal mental models and takeaways:
  `- <u>*ข้อคิด*</u>: *Container แค่ช่วยให้รันและส่งมอบง่ายขึ้น แต่มันไม่ได้ทำให้โค้ดกลายเป็น Microservice โดยอัตโนมัติ*`
  `- <u>*คิดเอง*</u>: security คือเครื่องมือป้องกัน & privacy คือนโยบาย -> นโยบายที่บังคับไม่ได้ ไม่ควรเป็นนโยบาย`
  `- Analogy: Integrity ≈ บ้านของลูกหมู 3 ตัว`
- Flag frequent misunderstandings:
  `- **May be misunderstood** 😵‍💫: Container ไม่ใช่ตัวสร้าง Microservice`

### 6. Comparison Tables

Use compact Markdown tables when comparing components, mechanisms, or options:

| Type | Definition | Example / Result |
| --- | --- | --- |
| **What you know** | สิ่งที่คุณรู้เพียงคนเดียว | Password, Passphrase, Pre-arranged questions |
| **What you have** | สิ่งที่มีติดตัว | Smart card, OTP token, Security key |
| **What you are** | อัตลักษณ์ทางกายภาพ | Fingerprint, Retina scan, Face recognition |

### 7. Step-by-Step Workflows

When explaining multi-step pipelines or operational workflows, use numbered bold steps with action summaries:

1. **Provision Infrastructure (Terraform)**: ประกาศความต้องการผ่านโค้ด HCL -> รัน `terraform apply` สร้างระบบเครือข่ายและเซิร์ฟเวอร์
2. **Configure Environment (Ansible)**: สั่งการผ่าน SSH เพื่ออัปเดต OS, ติดตั้งแพ็กเกจ และตั้งค่าความปลอดภัย
3. **Build & Package Application (Docker)**: บิลด์อิมเมจจาก Dockerfile แล้วพุชไปยัง container registry
4. **Deploy & Orchestrate (Kubernetes)**: รัน `kubectl apply` ดึงอิมเมจไปรันบนคลัสเตอร์โหนด

### 8. Visual Markers and Notation

- `💡` Key concept, core intuition, or guiding question
- `⚠️` or `!!!` Critical exam concept, strict rule, or core prerequisite
- `❌` / `✅` Comparison states, supported vs. unsupported features
- `🤔` or `😵‍💫` Common pitfalls, traps, or misconceptions
- Inline code formatting for commands, configurations, APIs, and technical parameters (e.g., `docker run`, `VPC`, `HCL`, `kubectl`)
- Mathematical/logical relations for concise relations (e.g., `Trust != Secure`, `Privacy subset of Security`)

### 9. Language and Tone

- Keep standard English technical terms verbatim (e.g., *Service-Oriented Architecture*, *Namespace*, *Union File System*, *Idempotency*, *Chain of Trust*).
- Use concise, natural Thai for explanations, intuitions, and commentary.
- High information density, zero conversational fluff. Every line should be a high-yield study note ready for exams.