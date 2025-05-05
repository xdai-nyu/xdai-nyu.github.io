# Feedback Buddy

**Enhance learning by providing personalized feedback on reading responses through AI-driven verbal/visual scaffolds**

## Project Members
Jessica Masciovecchio, Lucy Castro, Merry Cui, Yu-ri Chang, Ruolin Zhang

---

## 📄 Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [System Design](#system-design)
- [Prototype](#prototype)
- [Evaluation](#evaluation)
- [Findings](#findings)
- [Ethical Implications](#ethical-implications)
- [Future Work / Next Steps](#future-work--next-steps)
- [References](#references)

---

## 🟨 Abstract

AI-Feedback Buddy is a real-time, AI-powered feedback assistant that helps 3rd to 5th grade students improve their reading response writing by providing scaffolded guidance using the R.A.C.C.E. strategy (Restate, Answer, Cite, Cite Again, Explain). Unlike traditional grading tools, this assistant focuses on metacognitive development through interactive feedback delivered via multimodal channels—visual cues, verbal hints, and emoji-based evaluation. Students are prompted to self-correct, reflect, and revise their writing in real time. Preliminary testing shows improved writing completeness and increased student engagement. Teachers also benefit from reduced feedback time and increased visibility into student progress. The tool offers a scalable solution to enhance feedback equity and writing instruction across diverse classroom environments.


---

## 🟨 Introduction

AI-Feedback Buddy is a multimodal educational assistant designed to help 3rd to 5th grade students improve their reading response writing skills in both classroom and at-home settings. These learners are often expected to complete short written responses to reading passages—an essential but cognitively demanding literacy task that requires clarity, structure, and evidence-based reasoning.

However, our needs analysis and teacher surveys revealed three pressing issues:

1. Delayed or inconsistent feedback due to high student-to-teacher ratios;
2. Cognitive overload resulting from poorly structured or excessive correction;
3. A lack of personalized support aligned with each student’s learning level

Our research question centers on whether AI-generated, scaffolded feedback can support students in producing clearer, more complete written responses while reducing teacher workload. To explore this, we first conducted qualitative surveys with ten elementary school teachers and performed affinity mapping of student pain points. From this, we identified that ideal feedback should be precise, immediate, and motivational, and should support structured strategies like RACCE (Restate, Answer, Cite, Cite Again, Explain)

Building on these findings, we designed a prototype that emulates teacher feedback in real-time, using interactive, multimodal cues (visual, verbal, clickable prompts). The AI does not give direct answers but encourages revision and self-monitoring, aligning with metacognitive feedback principles.

Preliminary teacher and student testing suggests that this approach improves writing completeness and confidence. Teachers expressed enthusiasm for using the tool to track progress and differentiate instruction. Thus, our project aims not just to provide feedback, but to redefine the feedback loop as an interactive learning scaffold, especially in resource-constrained learning environments.


### Key Problems Identified
1. Delayed or inconsistent feedback due to high student-to-teacher ratios
2. Cognitive overload from poorly structured or excessive correction
3. Lack of personalized support aligned with each student’s learning level

### Research Focus
We explored whether AI-generated, scaffolded feedback can support students in producing clearer, more complete written responses while reducing teacher workload. Interviews with teachers helped us define ideal feedback as: precise, immediate, motivational, and strategy-driven (RACCE).

### Early Observations
Teachers and students both reported enthusiasm for the tool’s ability to guide writing progress and differentiate instruction. Our tool is not just about correction but about redefining the feedback loop as a learning scaffold.

---

## 🟦 System Design

The AI-Feedback Buddy system is organized around the R.A.C.C.E. strategy—Restate, Answer, Cite, Cite Again, Explain—which is widely used by educators to scaffold writing responses. Each component of the strategy maps to a distinct module within the interface, providing students with targeted prompts and real-time feedback at each stage of their writing.

### 🔹 System Modules

- **Restate**: Prompts students to rephrase the question using their own words.  
- **Answer**: Guides students to construct a clear response.  
- **Cite / Cite Again**: Encourages evidence-based reasoning with scaffolded sentence starters and text-highlighting support.  
- **Explain**: Promotes deeper thinking through “why/how” follow-up questions.  

### 🔹 User Experience & Visual Themes

Each grade level is associated with a unique theme and visual metaphor to build engagement:

- **3rd Grade**: “Turtle” theme — steady progress and patience  
- **4th Grade**: “Space” theme — exploration and discovery  
- **5th Grade**: “Ocean” theme — depth of reasoning and connection  

These themes are color-coded, child-friendly, and consistent with cognitive load theory to avoid overwhelming users with extraneous details.

### 🔹 Interaction Flow

Students input their responses through a clean writing interface with real-time suggestions and visual cues (e.g., underlines, emojis, and feedback bubbles). The interaction cycle is as follows:

1. Student reads the question and begins drafting.  
2. AI offers scaffolded sentence stems and guiding questions tailored to the RACCE stage they are on.  
3. After submitting a segment, the tool provides tiered feedback—starting with positive reinforcement, then prompting revision or clarification if needed.  
4. Students can choose to revise immediately or proceed to the next segment.  

The system is carefully designed to emulate a dialogic teacher–student exchange, and to minimize cognitive overload through chunked guidance and clear progression steps.

<img width="738" alt="截屏2025-05-04 18 32 31" src="https://github.com/user-attachments/assets/a2d4a095-a331-43e1-8664-2f66d1a90dbf" />

<img width="739" alt="截屏2025-05-04 18 32 47" src="https://github.com/user-attachments/assets/975b34c4-ceb5-4397-80fd-af9868083b5a" />

---

## 🔷 Early Prototype (Low-Fidelity Wireframe)

Our initial prototype focused on testing the core instructional logic of the Feedback Buddy system. This low-fidelity wireframe emphasized structure and functionality over visual aesthetics and was primarily used for early-stage usability testing.

**Key Interface Features**:  
- **Two-Panel Layout**: The left panel displays the reading passage, while the right panel is dedicated to student response input.

**Structured Prompting**:  
Five writing dimensions—**Restate**, **Answer**, **Cite**, **Cite Again**, **Explain**—are represented as gray icons above the text box to guide students in structuring their response.

**Emoji-Based Scoring**:  
Once submitted, the AI provides feedback using colored emoji indicators for each dimension:  
✅ Green = sufficient  
⚠️ Orange = partial  
❌ Red = missing

**Popup Hint System**:  
Students can click the “Questions?” button to receive in-context guidance, such as “What is a good restate?”

**Text Highlighting**:  
Relevant sections of the student’s response are highlighted based on scoring to encourage focused revisions.

<img width="1547" alt="截屏2025-05-04 18 34 53" src="https://github.com/user-attachments/assets/71ee1816-7045-4081-9f9c-f0c8102d6d9a" />

---

## 🟧 Current Prototype (High-Fidelity, Age-Differentiated)

The refined version of Feedback Buddy introduces a visually immersive, gamified interface tailored to students in grades 3–5. Based on teacher feedback and early usability testing, this version emphasizes motivation, autonomy, and alignment with students’ developmental stages.

### Key Enhancements:

#### 🔹 Visual Theme by Grade (Story-Based Races)
- **Grade 3 "The Turtle and the Hare"**: Inspired by Aesop's fable. A forest-themed race with a steady turtle and speedy hare, emphasizing perseverance and pacing.

  
- **Grade 4 "Race to Space"**: Inspired by the first human in space. A rocket-launch-themed race through stars and planets, celebrating courage and exploration.


- **Grade 5 "Inky the Octopus Escape"**: Inspired by the true story of Inky the Octopus. An underwater reef course filled with twists, turns, and clever escapes, highlighting intelligence and adaptability.

  
#### 🔹 Sequential Interaction Zones
- Students progress by clicking through interactive zones (e.g., “1. Restate/Answer”, “2. Cite”)  
- Zones are unlocked as students complete earlier steps  
- Visual path mimics goal-directed learning (from START to FINISH flags)

#### 🔹 Feedback-as-Progress Mechanism
- Instead of showing grades, feedback is embedded as visual unlocks or gentle nudges (“Try again”, “Almost there!”)  
- Encouragement replaces correction to maintain emotional engagement

#### 🔹 Narration & Scaffolding
- Audio prompts support struggling readers  
- Pop-up hints (e.g., “Questions? Ask Here”) guide students with actionable suggestions

#### 🔹 Age-Responsive Language and Icons
- Grade 3 uses larger icons and simpler sentences  
- Grade 5 includes multi-step reasoning support and deeper vocabulary prompts

<img width="1454" alt="截屏2025-05-04 18 37 13" src="https://github.com/user-attachments/assets/731268c0-9dd6-43ee-9105-bf71741914e1" />

---

## 🟦 Evaluation

### Evaluation Questions
From our project planning documents, we identified three primary research goals:

1. **Does the personalized tool improve student writing responses?**  
   → Can structured scaffolds like RACCE enhance clarity and completeness?
2. **Do writing scores improve when comparing pre- and post-tool usage?**  
   → Are students producing higher-quality responses after interacting with the tool?
3. **What do students and users say about their experience using the tool?**  
   → Are students engaged, and do they find the tool helpful or intuitive?

---

### Data Collection Plans

The following data types were gathered through classroom testing sessions:

| Data Type              | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Attention Observation  | Gaze tracking, facial expressions, and structured observational notes       |
| Writing Accuracy       | Rubric-scored student responses (pre/post)                                 |
| Revision Behavior      | Tracked edit types and revision frequency                                   |
| Interaction Patterns   | Clicks, scrolls, submission timing, tool usage flow                         |
| Student Reflection     | Post-task interviews, open-ended comments                                   |

---

### Sample Users

- **User 1**: 
  - Needed support identifying the question prompt.
  - Missed “Explain” initially but used underlining cues to revise.
  - Suggested keeping feedback visible longer and using checkmarks for clarity.
  - Reported that "this feels simpler" and “I like the turtle.”

- **User 2**: 
  - Encountered scroll difficulties; suggested using arrow keys.
  - Requested **real-time feedback** after each part, not at the end.
  - Desired **audio-based input**, and **gamified** elements like “you got a medal!”
  - Commented on punctuation errors not being caught: “It should say ‘uh-oh you forgot it!’”
  - Suggested replacing the static turtle with a more interactive character and a story-based design.

> These feedback sessions offered critical early insights that informed interface adjustments and feature prioritization (e.g., feedback persistence, speech input potential, and improved visual scaffolding).

---

### Methodologies

We used a mix of qualitative and quantitative approaches:

- **Observation & Proxy Testing**  
  → Two guided user sessions with real students, using observational templates

- **Clickstream Log Analysis**  
  → Track which buttons were clicked, when prompts were accepted or ignored

- **Writing Comparison**  
  → Pre/post writing samples scored via NYS-aligned rubric

- **Interviews & Self-Reflections**  
  → Captured both challenges and user-perceived benefits

---

### Variables Table

| Variable                 | Metric                                 | Data Source                           |
|--------------------------|----------------------------------------|----------------------------------------|
| Writing Quality          | Rubric score (NYS standard)            | Pre/Post writing samples               |
| Feedback Interaction     | Clicks accepted/rejected               | System logs                            |
| Time on Task             | Seconds per segment                    | Timestamps + observational notes       |
| Revision Frequency       | # of revisions or edit types           | AI feedback logs, writing diffs        |
| Self-Reflection Quality  | Mention of challenges/improvements     | Post-task interviews                   |
| Citation Accuracy        | Correct quote usage, punctuation       | Student response + AI scoring feedback |
| Engagement               | Use of emoji, turtle, narration, hints | Observations, interface interactions   |

---

### Data Analysis Strategy

- **Qualitative**:  
  Interviews, user quotes, observational notes on confusion/frustration

- **Quantitative**:  
  Rubric scores, time logs, click/edit metrics, writing improvement tracking

---

## 🟦 Findings

Our findings are drawn from user testing sessions with 5 elementary students, including direct observation, video logs, writing samples, and post-task reflections.

---

### 1. Writing Improvements

Based on rubric-graded responses from Day 3 and Day 4 sessions, we observed:

- Students who completed at least 3 RACCE steps produced writing with **noticeably clearer structure**.
- **Restate** and **Cite** steps were the most consistently completed.
- **Explain** was often misunderstood, skipped, or resulted in vague responses.

---

### 2. Observational Insights

#### From User 1 (Mak):
- Attempted all 5 steps but hesitated at "Explain": *"I'm not sure what to do here."*
- Benefited from **visual cues** like underlining and emoji scoring.
- Actively corrected spelling when underlined, showing awareness of feedback.
- Valued the side-by-side layout: *“I like the questions next to it… it helps me know what part I was missing.”*
- Suggested feedback should stay longer or be easier to reference: *“It would help if the feedback stayed longer or had checkmarks to know what to fix.”*

#### From User 2 (Ma):
- Initially confused by navigation, benefited from the numbered stages: *“Oh I think I restate and answer.”*
- Wanted **immediate feedback**: *“This is three words and it didn’t say anything.”*
- Struggled with **error detection**: *“When I type something wrong they never tell me what is wrong… maybe it should tell you how to fix it.”*
- Preferred **audio support** due to slow typing speed: *“By the time you type it out… time’s up!”*
- Desired **gamified experience**: *“You got a medal, yay!”* and suggested the turtle character *“should talk or give missions.”*

These insights suggest a need for anchored instruction, feedback persistence, clearer support for difficult steps (like "Explain"), and age-appropriate multimodal input (e.g., voice).

---

### 3. Student Feedback Highlights

#### 🧩 Simplicity & Layout
- *“This feels simpler to write everything down. The other one you have to go back and forth.”* —Mak

#### 👀 Visual Feedback
- *“I like the turtle.”*
- *“It would help if the feedback stayed longer or had checkmarks to know what to fix.”*

#### 💬 Confidence
- *“I would recommend it to others to help prepare.”* —Mak
- *“Just staring at this is a little boring… you got a medal, yay!”* —Ma

---

### 4. Areas for Improvement

- Keep feedback visible after submission
- Clarify expectations for “Explain” step
- Offer concrete examples when yellow (⚠️) emoji appears
- Support voice input for students with slower typing speed
- Introduce gamified elements (e.g., medals, missions) to sustain engagement

---

### 5. Ethical Compliance

All student participants completed assent forms and received parental consent. No names or identifying information were stored.

---

## 🟦 Ethical Implications

The development and deployment of AI-Feedback Buddy raised several ethical considerations, especially given its application in K–5 educational settings. Below we outline key categories of concern and our corresponding mitigation strategies.

### 1. Bias and Fairness
AI feedback may misinterpret linguistic variations or reflect bias in training data. Students from diverse socioeconomic and cultural backgrounds may be unfairly evaluated.

**Mitigations:**
- Train models on demographically diverse student writing samples  
- Include culturally varied prompts and passages  
- Allow teacher flagging of culturally mismatched responses for review  

---

### 2. Privacy and Data Security
AI systems may collect sensitive student writing and behavior logs. Protecting that data and ensuring informed participation is essential.

**Mitigations:**
- Anonymize all student data and avoid storing names  
- Collect guardian consent (see Consent Form)  
- Follow FERPA compliance for educational data storage  

---

### 3. Transparency and Explainability
Students and teachers should understand why specific feedback is being given and how the model interprets writing.

**Mitigations:**
- Link all AI feedback to the NYS writing rubric  
- Include a “Why this feedback?” clickable option  
- Explain the choice of the RACCE framework in onboarding  

---

### 4. Equity and Accessibility
Students with limited tech access or learning differences must not be disadvantaged.

**Mitigations:**
- Tool is browser-based, compatible with low-spec devices  
- Features text-to-speech, adjustable reading levels  
- Add offline-friendly mode and low-bandwidth options  

---

### 5. Teacher and Student Autonomy
AI should support—not replace—teachers. Students should still think critically without relying too heavily on AI.

**Mitigations:**
- Teachers can override or hide AI suggestions  
- Students can toggle levels of feedback scaffolding  
- Manual writing still encouraged in prompts  

---

### 6. Intellectual Property and Plagiarism
AI tools may inadvertently encourage copying or raise concerns about authorship.

**Mitigations:**
- Disable copy-paste in writing tool  
- Clearly tag AI-generated sentence starters  
- Track writing/editing timestamps  

---

### 7. Emotional Well-being
Repetitive negative feedback or confusing prompts may frustrate students.

**Mitigations:**
- Use affirming language in all feedback  
- Provide “encouragement mode” after multiple failed attempts  
- Include “I need help” button linking to teacher support  

---

### 8. Accountability and Responsibility
When feedback is incorrect, it's vital to trace model outputs and ensure educator oversight.

**Mitigations:**
- Include model version and rubric reference with each feedback  
- Store editable history and timestamp logs  
- Keep teacher in the loop through review dashboards  

---

### 9. Overselling and Hype
AI-Feedback Buddy should not be seen as a magical solution.

**Mitigations:**
- Frame AI as a teacher assistant, not a replacement  
- Avoid guarantees like “better scores” in promotion  
- Emphasize critical thinking, not automation  

---

### 10. Ethical AI Education
Educators and students alike need support in understanding how AI works and where its boundaries lie.

**Mitigations:**
- Provide onboarding materials about AI capabilities  
- Offer “AI Ethics 101” as part of initial teacher training  
- Encourage ongoing feedback about fairness and accuracy  

<img width="1426" alt="截屏2025-05-04 18 58 07" src="https://github.com/user-attachments/assets/7b92032f-78e3-481c-8e31-f93248140943" />

---

## 🟦 Future Work / Next Steps

Future iterations of AI-Feedback Buddy will build on early insights by expanding both functional capabilities and engagement strategies:

### 🧠 Enhanced Feedback Logic
- Incorporate **specific feedback by RACCE step** (e.g., targeted hints for "Explain"), moving beyond overall summative feedback.
- Enable **formative feedback** with real-time guidance as students write, not just after submission.
- Ensure **feedback and emoji scores remain visible** while students revise their responses.
- Anchor feedback bubbles to the relevant response sections during editing.

### 📍 Prompt Placement & Visual Flow
- Improve **question visibility** by repositioning guiding prompts within closer proximity to the active writing box.
- Add **checkpoint narration** such as “Great work!”, “Level 1 complete”, or “Start here” to motivate progress.

### 🗣️ Voice & Accessibility Support
- Implement **voice input** options for students with limited typing fluency.
- Add a **conversational chat assistant** that supports real-time audio and text-based scaffolding.
- Include **audio-based encouragement** during transitions, checkpoints, and upon completion.

### 🎮 Gamification & Storytelling
- Expand the **race track narrative** into a full game-like journey:
  - Character movement across progress checkpoints.
  - A **second character "chasing"** the student to build pacing and motivation.
  - Unlockable **stars**, **badges**, and **points** for milestone completion.
- Design an **animated intro** to explain the storyline, goals, and motivation mechanics.

### 🧭 UX Improvements
- Introduce **scrolling navigation** to better handle long responses and feedback history.
- Allow students to **view feedback side-by-side** with their writing while making edits.

### 📊 Rigorous Evaluation
- Conduct a **larger-scale classroom pilot** with broader user diversity.
- Collect **pre- and post-assessment data** based on NYS-aligned writing rubrics.
- Use **observational indicators** (e.g., body language, engagement behaviors) to assess emotional and cognitive responses.

These improvements will transform the prototype into a robust, classroom-ready tool that enhances both learning outcomes and student motivation.


