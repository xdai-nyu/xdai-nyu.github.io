# KnowCheck
**KnowCheck: An AI-Powered Knowledge Mastery Tool for Adult Learners**

---

## Problem Statement
Many adult learners studying AI concepts rely on scattered resources (online courses, podcasts, articles, and workplace training). While they may feel confident, research shows that self-assessment often fails to match actual ability—especially when it comes to applying or transferring knowledge.  

Most current assessments focus on memorization, not on mastery. Learners need a reliable way to measure true understanding and practical transfer of knowledge, not just recall.

---

## Target Learning Audience
KnowCheck is designed for young and mid-career adult learners, typically between **18–45 years old**, who are adapting to the rapid changes brought by AI.  

This group includes professionals and lifelong learners who are often self-studying AI topics while balancing work, study, and personal responsibilities.  

Unlike traditional students, they rarely have access to structured programs or consistent mentorship. They self-study topics such as **LLM principles**, **prompt engineering**, and **applied AI use in business settings**, pulling resources from fragmented sources like online courses, podcasts, and in-house trainings.  

Their learning is often fragmented and pragmatic—focused on “making it work” rather than deeply verifying understanding.  

**KnowCheck** provides a clear, context-independent way to check mastery and build confidence in applying knowledge in real-world scenarios.

---

## Identified Learning Need
For adults trying to learn AI on their own, it can be surprisingly difficult to know whether they’ve really mastered the material.  

Research shows that learners often **misjudge their own abilities**; in particular, low performers tend to overestimate their competence—a pattern described by the **Dunning–Kruger effect** (Kruger & Dunning, 1999).  

This issue is amplified in **fragmented, informal learning environments**, where adults rely on scattered resources such as online tutorials, podcasts, or in-house training.  

In these settings, learners may feel confident, but their performance often falls short when tested in real-world scenarios (Mahmood, 2016).  

Most current assessments are limited to **recall**, while professional contexts demand **application** and **transfer**. Without clear benchmarks or feedback, learners often mistake **recognition for mastery**.  

An **objective tool** with **targeted feedback** can help adults better calibrate their self-assessment and guide future learning (Lu et al., 2021).

---

## Literature Review

### Account 1: Generative AI Tutors and Student Learning Outcomes

A large-scale study conducted in high school math classrooms compared two AI-supported learning conditions: an unrestricted version of GPT-4 (“GPT Base”) and a structured, teacher-designed version (“GPT Tutor”) with built-in guardrails. The results showed that unrestricted access to GPT-4 harmed learning outcomes, with students scoring 17% lower on unaided post-tests, even though they believed they had learned more. In contrast, the guardrailed version, which provided hints instead of full answers, mitigated these negative effects.

**GPT Base (no guardrails)** = gives full answers → can create an illusion of learning.

**GPT Tutor (with guardrails)** = gives guided hints → supports deeper understanding and engagement.

This research highlights a key issue: the illusion of mastery. Learners exposed to generative AI often feel they have learned more than they actually have. When answers are easily accessible, the brain mistakes recognition for understanding. However, guided feedback—such as prompting reflection or offering partial hints—encourages deeper cognitive processing.

**Limitations:**
Focused on high school learners, not adults or professionals.
Conducted in controlled classrooms rather than self-directed learning environments.
Short-term results; no long-term or transferability assessment.

**Alignment with KnowCheck:**
KnowCheck addresses the same gap from a self-directed learning perspective. Adult learners using AI tools often face similar calibration problems, misjudging what they truly know. This evidence supports KnowCheck’s emphasis on diagnostic feedback and active engagement rather than passive correctness.

---

### Account 2: Google Cloud — Generative AI Leader Certification and Vertex AI Skill Badges

Google Cloud has developed two prominent learning and assessment systems designed to validate AI-related competencies across different levels of expertise:

**Generative AI Leader Certification** — a timed and proctored assessment for non-technical professionals that focuses on conceptual understanding of AI principles, ethical considerations, and strategic implementation.

**Vertex AI Skill Badges** — a series of hands-on labs where learners complete practical AI tasks within a live cloud environment, demonstrating technical application and workflow mastery.

**Limitations:**
Despite their strengths, these systems remain primarily summative. Learners receive a completion badge or pass/fail result but rarely gain insight into why they performed well or poorly. The fixed task structures also limit opportunities to assess adaptability or creative problem-solving in unfamiliar contexts.

**Alignment with KnowCheck:**

To move beyond this limitation, KnowCheck aims to offer formative, reflective feedback—helping learners understand not only their level of mastery, but also their reasoning patterns, misconceptions, and potential areas for transfer and growth. These certification systems share common ground with KnowCheck’s goals by combining conceptual testing and practical application. Learners are evaluated on real-world tasks, not just factual recall, and performance is automatically assessed through their task submissions and activity logs. This model emphasizes authentic, skills-based learning rather than rote memorization.

---

### Account 3: AWS’s Simulation-Based Learning Models — AI Practitioner Certification, SimuLearn, and Cloud Quest

Amazon Web Services (AWS) has developed a multi-tiered ecosystem of AI learning and assessment programs aimed at different learner needs and levels of expertise:

**AI Practitioner Certification** — a standardized knowledge exam designed to evaluate conceptual understanding of AI principles within the AWS environment.

**SimuLearn** — an AI-driven simulation platform where learners engage with virtual clients, design tailored AI solutions, and receive real-time, context-specific feedback.

**Cloud Quest** — a gamified, role-based platform that allows learners to practice AI and cloud problem-solving through interactive missions.

**Limitations:**

Despite these innovations, AWS’s systems remain largely platform-dependent and procedurally focused. The simulations and exams test learners’ ability to execute known workflows within the AWS ecosystem, rather than their capacity to generalize and apply concepts to unfamiliar or cross-platform contexts.

**Alignment with KnowCheck:**

KnowCheck builds on this gap by emphasizing conceptual transfer and diagnostic feedback. Instead of validating step-by-step execution, KnowCheck seeks to assess how learners reason, adapt, and explain their choices—skills that reflect genuine understanding beyond procedural repetition. AWS’s learning tools share several parallels with KnowCheck’s goals. Both emphasize applied learning and reflective engagement. For example, SimuLearn provides personalized, targeted feedback on both technical performance and communication—helping learners recognize skill gaps and calibrate their self-assessment. Meanwhile, Cloud Quest introduces scenario-based challenges that mirror real workplace tasks, promoting practical reasoning and transfer of knowledge.

---

## Rationale for AI Assistance
Traditional knowledge assessments, such as standardized tests or course-embedded exercises, often focus on evaluating a learner's ability to *recall* and *restate* information.  

However, for the adult self-learners we are targeting, the real challenge lies in their ability to *apply* knowledge in typical scenarios and, more importantly, *transfer* it to atypical, complex work situations.  

This higher-order competence is difficult to measure effectively with static, predefined question banks, which is precisely where **AI** can play a pivotal role.

---

### Personalization and Adaptive Feedback
AI/intelligent tutoring systems can generate scaffolded tasks and provide adaptive feedback based on the learner's proficiency and goals, with long-term evidence supporting their learning gains (vanLehn, 2011).  

In our design, this adaptability is specifically embodied by AI's capability to dynamically generate high-fidelity work scenarios to accurately assess a learner's true ability to *apply* and *transfer* knowledge.  

The feedback provided is not merely a judgment of correctness but also acts like a mentor, offering “why” explanations that pinpoint potential risks or logical fallacies in the user's proposed solutions.  

This constitutes the core of **explainable diagnostic feedback**.

---

### Usability of LLMs in Education
A recent survey by Wang et al. (2024) summarizes the applications of **LLMs in education**, including conceptual understanding detection, personalized guidance, and automated assessment, offering a direct reference for our design.  

AI can not only be used to evaluate performance but also to explain a user's cognitive blind spots and recommend the next steps in their learning path accordingly.  

This approach focuses on helping learners **calibrate their self-perception of competence**.  

By leveraging AI to create a highly realistic, interactive, and feedback-rich assessment environment, our tool aims to facilitate **cognitive self-calibration** for adult learners.  

This effectively helps them recognize their own capability boundaries and supports them in making the developmental leap from “knowing” to “doing.”

---

## Approach and Deliverables

We have chosen AI/LLM as the initial subject matter for our tool, focusing on the following assessment dimensions:

- **Restate:** The ability to explain a concept and its boundaries in one's own words.  
- **Apply:** The ability to use a concept correctly in typical scenarios.  
- **Transfer:** The ability to propose viable strategies in atypical or constrained scenarios.  
- **Evaluation:** The system will output a multi-layered score (covering recall, application, and transfer), a calibration map, an evidence package, and a supplementary learning path.  
- **Scope:** This tool does not provide courses or question banks; it is positioned as an independent mastery assessment layer to be used after learning has taken place.

---

## Team Contribution
- **Chenyu** drafted the initial version.  
- **Nanxi** revised the draft and incorporated changes.  
- **Sixin** finalized the writing and editing.


---

## References
- Lu, F.-I., Takahashi, S. G., & Kerr, C. (2021). *Myth or reality: Self-assessment is central to effective curriculum in graduate medical education.* **Academic Pathology, 8, 23742895211013528.**  
- Mahmood, K. (2016). *Do people overestimate their information literacy skills? A systematic review of empirical evidence on the Dunning–Kruger effect.* **Communications in Information Literacy, 10(2), 198–213.**  
- Wang, S., Xu, T., Li, H., Zhang, C., Liang, J., Tang, J., Yu, P. S., & Wen, Q. (2024). *Large Language Models for Education: A Survey and Outlook.* **arXiv:2403.18105.**  
- Kruger, J., & Dunning, D. (1999). *Unskilled and unaware of it: How difficulties in recognizing one’s own incompetence lead to inflated self-assessments.* **Journal of Personality and Social Psychology, 77(6), 1121–1134.**  
- vanLehn, K. (2011). *The relative effectiveness of human tutoring, intelligent tutoring systems, and other tutoring systems.* **Educational Psychologist, 46(4), 197–221.**
