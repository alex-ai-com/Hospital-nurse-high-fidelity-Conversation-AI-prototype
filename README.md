# 🏥 NurseVoice
### Frontline Nurse Intelligence Platform — Conversational AI Prototype

> A high-fidelity mobile prototype that captures frontline nurse voices during their shifts through guided conversational micro-prompts — anonymously, securely, and without disrupting patient care.

---

## 📌 Overview

NurseVoice is a smartphone-first conversational AI tool built to surface the operational insights of frontline nurses — the equipment failures, unsafe staffing ratios, handoff breakdowns, and coordination gaps that never make it into formal incident reports. Instead of open-ended dictation or institutional feedback forms, NurseVoice uses a structured micro-prompt framework designed around real clinical work realities: high cognitive load, strict time windows, peer surveillance anxiety, and the ever-present possibility of a mid-session emergency.

This prototype was built as the capstone deliverable of a **40-hour Health-Tech UX Micro-Internship**, progressing from scenario research through conversation flow architecture to a fully interactive, single-file mobile UI.

---

## 🎯 Problem Statement

Frontline nurses hold the most operationally accurate picture of hospital system failures. That picture is routinely lost because:

- Formal incident reporting channels are perceived as punitive
- Shared hospital workstations are contested, visible, and shift-bound
- Open-ended feedback tools ignore the cognitive load of post-incident states
- No existing tool accounts for the reality that any interaction can be interrupted by a patient emergency at any moment

NurseVoice is designed to close this gap.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🔐 **Secure Mode** | Persistent AES-256 encryption badge with animated live status indicator |
| 🎙️ **Voice Capture** | Mic recording simulation with animated waveform and typewriter transcription |
| ⚠️ **Noise Error Handling** | Auto-detects simulated low-confidence STT and offers tap/type fallback |
| 📋 **Guided Micro-Prompts** | 3-question progressive wizard: Trigger → Pattern → Workaround & Fix |
| 🚨 **Panic Pause Button** | Single-tap emergency exit that freezes, blurs, and locally caches the session |
| 🛡️ **Anonymisation Engine** | Strips name, unit ID, and shift code before any data transmission |
| 📊 **Reports Dashboard** | Live status tracker with escalation timeline logs per submitted issue |
| ✨ **Impact View** | Shows systemic changes driven by anonymised nurse report patterns |
| 🧠 **Scenario Adaptive** | Prompts dynamically adjust based on selected nurse persona (Med-Surg, ED, ICU, Peds) |

---

## 🗂️ Project Deliverables

This project was completed across four structured phases:

### Phase 1 — Scenario Research
Four detailed nurse engagement scenarios built from real hospital work realities, each containing a nurse persona, workflow trigger, trust & privacy constraints, and the core operational insight to be captured.

**Personas designed:**
- Grace · Night Shift Med-Surg · Post near-miss incident
- Tobias · Emergency Department · Mid-shift 90-second window
- Amara · Cardiac ICU · End-of-shift locker room
- Seren · Pediatric Ward · Between-task moral distress window

### Phase 2 — Conversation Flow Architecture
A complete Mermaid.js flowchart mapping the app's full logic including biometric login, guided Q&A paths, emergency interruption branch, STT noise error loops, and dashboard routing.

### Phase 3 — High-Fidelity UI Prototype
A single-file interactive mobile prototype (HTML + Tailwind CSS + Vanilla JS) rendered inside a 390×844px smartphone chassis. All buttons are functional and alter UI state dynamically.

### Phase 4 — Design Summary Document
A 2-page professional design rationale linking every UX and technical decision to clinical workflow research, psychological safety literature, and human factors principles.

---

## 🏗️ Technical Architecture

```
NurseVoice/
├── prototype/
│   └── index.html          # Full app — single file, zero dependencies
├── flows/
│   └── conversation_flow.mmd   # Mermaid.js architecture diagram
├── docs/
│   └── design_summary.md   # UX rationale & stakeholder document
└── README.md
```

**Stack:**
- **UI:** Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Styling:** Tailwind CSS utility classes + custom CSS variables
- **Fonts:** Inter (Google Fonts)
- **Diagrams:** Mermaid.js
- **Dependencies:** Zero runtime dependencies — fully self-contained

---

## 📱 Prototype Screens

| Screen | Description |
|---|---|
| **Scenario Selector** | Choose nurse persona; unlocks the guided interview |
| **Q1 — Operational Trigger** | What broke down? Voice or chip selection |
| **Q2 — Pattern & Frequency** | How often has this occurred? |
| **Q3 — Workaround & Fix** | What are you doing to compensate, and what would fix it? |
| **Panic Overlay** | Full-screen blur lock with cache confirmation and resume/discard options |
| **Submission Confirmation** | Anonymisation checklist and escalation pathway explanation |
| **Reports Dashboard** | Status-tracked issue cards with timeline logs |
| **Impact View** | Real systemic changes attributed to nurse report patterns |

---

## 🔐 Privacy & Security Design Principles

NurseVoice is built on the principle that trust must be **warranted by architecture, not requested through promises.**

1. **Local-cache-first** — data is stored on-device before any network sync
2. **Structural anonymisation** — name, unit, and shift code are stripped before storage; no reverse linkage is possible
3. **Audio deletion** — voice recordings are discarded after transcription; only text is retained
4. **Zero confirmation overhead** — the panic pause requires a single tap and produces no sound, alert, or visible state change to bystanders
5. **Pattern-based escalation** — no single report is attributable; issues auto-escalate only when 3+ nurses report the same pattern

---

## 🧪 Design Research Foundations

| Principle | Application in NurseVoice |
|---|---|
| **Cognitive Load Theory** | Micro-prompts offload narrative structure from nurse to interface |
| **Motivational Interviewing** | Q1→Q2→Q3 arc: immediate reality → pattern recognition → generative fix |
| **Psychological Safety (Edmondson)** | Operational framing removes welfare stigma from disclosure |
| **Context-Dependent Behaviour** | Personal device activates different self-disclosure register than institutional terminals |
| **Human Factors / Clinical Workflow** | Session lengths calibrated to real nurse micro-break windows (90s–8min) |

---

## 🚀 Getting Started

No installation required. The prototype runs entirely in the browser.

```bash
# Clone the repository
git clone https://github.com/your-org/nursevoice.git

# Open the prototype
open prototype/index.html
```

Or simply open `index.html` in any modern browser. No server, build step, or package manager needed.

---

## 📄 Documentation

- [`docs/design_summary.md`](docs/design_summary.md) — Full UX & technical design rationale (stakeholder-ready)
- [`flows/conversation_flow.mmd`](flows/conversation_flow.mmd) — Mermaid.js conversation architecture diagram

---

## 🛣️ Potential Next Steps

- [ ] Integrate real Web Speech API for live voice transcription
- [ ] Connect to a de-identified research backend (e.g. Supabase with RLS policies)
- [ ] Build native iOS/Android shell via React Native or Capacitor
- [ ] Add pattern-detection logic for auto-escalation threshold triggers
- [ ] Conduct usability testing with 5–8 frontline nurses across shift types
- [ ] Explore integration with existing hospital incident reporting systems via HL7 FHIR

---

## 👤 Author

Built as a **Health-Tech UX Micro-Internship** capstone project.
Designed from the perspective of a Principal Healthcare UX Designer & Health-Tech Product Manager.

---

## ⚖️ Disclaimer

NurseVoice is a research prototype. It is not a certified medical device and is not intended for clinical deployment without appropriate regulatory review, IRB approval for data collection, and full security audit. All nurse personas and report data shown in the prototype are fictional and created for design demonstration purposes only.

---

*"The most important clinical data in any hospital is the knowledge inside the heads of nurses at the end of a 12-hour shift. NurseVoice is built to catch it before it disappears."*
Healthcare institutions have, over decades, constructed formal feedback infrastructure — incident reporting portals, patient safety surveys, near-miss logs — that are structurally distrusted by the very workforce they are designed to serve. The mechanism of this distrust is well-documented in organisational psychology literature: when feedback channels are administered by the same institutional hierarchy that holds disciplinary authority, the rational calculus for frontline workers shifts from disclosure to self-protection. Nurses do not withhold information because they are disengaged; they withhold it because the risk-reward structure of formal reporting is, in many institutional cultures, genuinely adverse.

NurseVoice addresses this paradox not through reassurance, but through architecture. The distinction is critical. A system that tells nurses their data is safe is asking for trust. A system that makes it structurally impossible to violate that safety is warranting trust. Every element of the NurseVoice security model is designed to warrant rather than request.

### Dissecting the 'Secure Mode' Interface Decision

The persistent "Data Encrypted & Anonymized" header badge — visible on every screen, animated with a live pulsing indicator — serves a function that goes beyond visual reassurance. It is a continuous, ambient signal that the system's privacy posture has not changed since the nurse last looked. This matters because nurses interacting with the tool during a high-stress window (immediately post-incident, during a break taken under social observation) cannot afford the cognitive overhead of re-evaluating the system's trustworthiness at each interaction point. The badge externalises that evaluation, offloading it from working memory.

Local caching — the decision to store in-progress and completed session data on-device in AES-256 encrypted local storage before any network sync — addresses a more specific and acute fear: the fear that submission means immediate institutional visibility. Under a server-first architecture, hitting "submit" is an irreversible act with unclear downstream consequences. Under a local-cache-first architecture, the nurse retains a mental model of control: the data has not left my device until network conditions and my own confirmation allow it. This asymmetry of perceived control is not cosmetic — it directly lowers the activation threshold for disclosure.

The anonymisation engine's structural design — stripping name, unit identifier, and shift code before any transmission occurs — further addresses the specific vulnerability pattern identified across all four nurse personas: the fear of being identified not by management, but by peers. Grace (Med-Surg) fears disciplinary review; Seren (Peds) fears being perceived as unable to cope; Tobias (ED) fears the social cost of being seen using what might register as a "feelings app." Structural anonymisation removes the identity layer before the data ever becomes shareable, making the question of who-said-what unanswerable by design.

### Framing Language as a Psychological Safety Mechanism

The choice to frame all prompts in operational and clinical language — "what broke down structurally" rather than "how did that make you feel" — is not merely a tone decision. It is a psychological safety intervention. Welfare and mental health framing, applied to nurses during a shift, activates professional vulnerability schemas associated with performance evaluation and fitness-to-practice concerns. Operational framing activates a different schema entirely: problem-identification, clinical reasoning, systemic analysis. Nurses are highly trained in the latter mode. By keeping the conversational register firmly in the operational domain, NurseVoice reduces the perceived stakes of disclosure without diminishing the emotional and professional honesty of the content captured.

---

## Section 3: Workflow & Time Constraint Principles

### Why Unstructured Dictation Fails in Clinical Environments

Open-ended voice dictation, as a primary input modality for frontline clinical insight capture, fails against three simultaneous and non-negotiable constraints: cognitive load, time availability, and environmental noise. Each of these constraints is individually sufficient to compromise dictation quality; their co-occurrence in a clinical shift environment makes unstructured dictation a fundamentally inappropriate mechanism for the use cases NurseVoice serves.

Cognitive load in post-incident or mid-shift states is demonstrably elevated. The nurse is not in a reflective, composing mindset — she is in a physiologically aroused, task-switching state. Open-ended prompts ("Tell us what happened") place the burden of structure, prioritisation, and narrative framing entirely on the user at the moment when her cognitive resources are most depleted. Research in human factors and clinical decision-making consistently shows that decision quality and information recall degrade significantly under high workload conditions. Structured micro-prompts — where the system provides the narrative scaffold and the nurse fills specific, bounded slots — offload the structural burden from the user to the interface. This is not a simplification of the insight being captured; it is a recognition that the quality of insight is determined not by the openness of the prompt but by the precision of the framework within which the nurse's expertise is expressed.

### The Micro-Prompt Architecture as a Time Contract

Each of the four nurse scenarios in NurseVoice is assigned an explicit session duration — 90 seconds (ED), 4 minutes (Med-Surg), 6 minutes (Peds), 8 minutes (ICU) — calibrated against the realistic time windows identified during scenario research. This session-length specification is not a soft guideline; it functions as a time contract between the system and the nurse. The nurse enters the interaction knowing precisely how much of her time it will consume, eliminating the principal deterrent to engagement with open-ended feedback systems: temporal unpredictability.

The three-question progressive disclosure structure — Operational Trigger → Pattern & Frequency → Workaround & Fix — is ordered deliberately against the cognitive and emotional arc of a post-event state. The first question meets the nurse where she is: describing what she just experienced, in concrete operational terms. The second question invites pattern recognition, a higher-order cognitive task that the first question has now primed her for. The third question asks for generative thinking — workarounds and fixes — which requires the highest cognitive investment and is therefore placed last, when engagement and disclosure momentum are highest. This sequencing is consistent with motivational interviewing principles adapted for operational contexts: establish the immediate reality before requesting abstract analysis.

### Emergency Pause Logic as Friction Elimination

The "Pause Session — Run to Patient" button represents the single most clinically-informed interaction design decision in the NurseVoice prototype. Its logic is grounded in a fundamental and non-negotiable reality of nursing work: any tool that imposes a cost for interruption will be abandoned at the moment of interruption and will not be resumed. The nurse who is mid-response when a call bell fires, a code is announced, or a colleague requests urgent assistance has two competing obligations — both of which are legitimate, neither of which can be subordinated to the other.

Conventional form-based data entry creates a punitive interruption dynamic: abandon the form, lose the data, experience the sunk cost, and reduce the probability of re-engagement. NurseVoice's single-tap panic pause eliminates this dynamic entirely. The gesture is instantaneous — requiring no confirmation dialog, no save prompt, no decision overhead — and the outcome is unambiguous: the screen blanks to a neutral locked state indistinguishable from a standard lock screen, data is preserved in encrypted local cache, and the session resumes exactly where it was paused upon biometric re-authentication.

This design choice reflects a principle that has broad applicability in clinical tool design: the system must be demonstrably more respectful of the nurse's primary obligations than it is demanding of its own completion. A tool that interrupts patient care for data entry is not a clinical tool — it is an administrative burden with a clinical veneer. By making the cost of interruption zero, NurseVoice earns the right to exist in the clinical workflow without competing with it.

---

## Conclusion

The design decisions documented in this summary collectively constitute a coherent position: that capturing frontline clinical insight at sufficient quality and volume to drive systemic change requires, above all, a design practice that begins with the nurse's actual situation rather than the institution's preferred infrastructure. Personal device deployment, structural anonymisation, operational framing, constrained micro-prompt architecture, and zero-friction interruption handling are not independent feature choices — they are a unified response to the specific human realities of nursing work. Each decision can be traced directly to a constraint surfaced in scenario research and defended against both UX principles and clinical workflow evidence. That traceability — from research reality to design decision to implemented behaviour — is what distinguishes a prototype that nurses might actually use from one that merely demonstrates that someone cared about trying.

---

*Document prepared as part of a 40-hour Health-Tech UX Micro-Internship. Prototype built using HTML, Tailwind CSS, and Vanilla JavaScript. Conversational flow architecture designed in Mermaid.js. Scenarios grounded in published nursing workflow research and clinical human factors literature.*

