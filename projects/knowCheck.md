# KnowCheck
**KnowCheck: An AI-Powered Mastery Assessment Tool for Adult Learners in AI**

## Abstract

KnowCheck is an AI-powered assessment tool designed to help young and adult learners accurately measure their understanding of artificial intelligence concepts beyond memorization. Many learners rely on fragmented resources and AI tools that often create an illusion of knowledge mastery. KnowCheck addresses this by offering systematic, diagnostic and scenario-based assessments that emphasize conceptual understanding, application, and transfer of knowledge towards the users. Instead of serving as another learning content platform, KnowCheck positions itself as an independent mastery-check layer that evaluates whether learners can reason, apply, and adapt knowledge in real-world contexts. Through personalized difficulty levels, diagnostic feedback, and calibration of user confidence against performance, KnowCheck aims to improve learners’ self-awareness, learning efficiency, and confidence accuracy.


## 1. Introduction

### 1.1 Target Audience

KnowCheck target both young and adult learners age 18 to 45 years learning the AI concepts outsidde formal academic programs. This will cover professionals, students, and career switchers who depend on fragmented sources of learning like online courses, podcasts, articles, and job-based resources to develop AI literacy. These students tend to be self-directed, time-pressed, and practice-oriented as opposed to meticulously testing mastery of concepts. Without structured programs or consistent feedback, many struggle to determine whether they truly understand what they are learning.

KnowCheck provides a structured way to help them verify mastery and build confidence through real-world, scenario-based assessment.

### 1.2 Identified Learning Need

Research consistently demonstrates that individuals tend to overestimate their own competence, especially in unstructured learning environments. This is what is referred to as the Dunning-Kruger effect. This miscalibration is also intensified in the context of AI-assisted learning since the chat-based AI systems suggest instant responses, and they may give an illusion of comprehension without meaningful engagement.

The majority of conventional evaluation systems:

- Focus on memorization as opposed to applied reasoning.

- Lack feedback about how answers are produced

- Offer little to no information on the confidence of learners.

As a result, learners mat progress with misplacedd confidence before they are faced with a challenging or real-world problems that they are unable to solve indpendently.

### 1.3 Problem Statement

How can AI be used to provide systematic, diagnostic assessment that helps learners accurately measure and reflect on their understanding rather than merely test recall?

### 1.4 Research Motivation

KnowCheck is motivated by three educational challenges:

1. Widespread overconfidence in self-directed learning

2. Limited access to diagnostic feedback

3. Overreliance on recall-based assessments

The system is designed to shift learning evaluation from content coverage to mastery detection.

### 1.5 Design Approach andd System Philosophy

KnowCheck addresses this challenge by changing the assessment pattern from content mastery to reasoning mastery. KnowCheck does not act as an additional learning platform or tutor but rather positioins itself as an independent evaluation layer in the process of learning. The system assesses the understanding of learners by using dynamic, scenario based questions that are used to test comprehension, application, and transfer. Onboarding occurs briefly before the user is presented with questions to diffuse in line with their context (age, role and self-assessed level of knowledge). During the evaluation process, the users get real time feedback and a diagnostic report which provides their performance summaries, calibration analysis and learning recommendations.

### 1.6 Preliminary Findings and Observations

Preliminary classroom testing and peer feedback surfaced several early findings. The first impression of the users was often overestimated and and were surprised by gaps revealed through scenario-based questions. Feedback explaining reasoning errors was valued more than correctness alone. The calibration report also helped them to understand the strengths and weaknesses of the users, which is why the users noted that the calibration report made them more aware of themselves in the sense that they needed to conduct reflective self-assessment and not passive testing.

**KnowCheck** provides a clear, context-independent way to check mastery and build confidence in applying knowledge in real-world scenarios.

## 2. System Design

This section describes KnowCheck’s core features, early prototypes, and the design process that led to the final system.

### 2.1 Design Features

KnowCheck is designed as a **diagnostic assessment system** rather than a tutoring or content platform. Its features are organized into three functional layers:

**1. Personalization & Calibration**
Used to tailor the assessment experience and establish confidence baseline.
- Age input
- Identity role selection (student, professional, educator, etc.)
- Self-rated knowledge level (1–5)
- Initial difficulty setting based on user profile

**2. Assessment Engine**
Delivers adaptive, scenario-based questions to test understanding.
- Question types: MCQ, True/False, Matching, Bucket (drag-and-drop), Short Answer
- Dynamic question generation via AI
- Real-time feedback (correct / partial / incorrect)
- Progress indicator (e.g., “3/6”)
- Background preloading to reduce wait time

**3. Diagnostic Reporting**
Generates a personalized mastery report at the end of the session.
- Calibration analysis (confidence vs. performance)
- Skill breakdown by topic (0–100 scale)
- Visual indicators (low / medium / high proficiency)
- Strengths and improvement areas
- Recommended learning resources (video, article, course, blog)
- Retake option for reflection and iteration

---

### 2.2 Early Prototypes

Initial prototypes focused on basic quiz-style interactions.  
These were quickly rejected after it became clear they encouraged recall rather than reasoning.

Early wireframes explored:
- Onboarding flow
- Knowledge-level selection
- Question navigation
- Result summary

After feedback, prototypes evolved to emphasize:
- Scenario-based questioning
- Diagnostic feedback
- Confidence calibration
- Visual reporting

Final interfaces were built in Figma with interactive flows, simulated AI output, and report visualizations.

---

### 2.3 Design Process

**1. Problem Discovery**
Research highlighted:
- Overconfidence in self-directed learning
- The Dunning–Kruger effect
- AI’s tendency to create illusion of mastery

This shifted the project away from content delivery and toward diagnosis.

**2. Design Pivot**
The original direction (tool recommendations and learning content) was replaced with:
- Assessment-first design
- Calibration-based reporting
- Reflection-driven feedback

**3. Refinement**
The final system prioritizes:
- Short assessment sessions (5–7 minutes)
- Minimal onboarding friction
- Scenario-driven questions
- Visual insight over raw scoring
- Learning resources as support, not instructio

KnowCheck demonstrates how AI can function as a **diagnostic evaluator** rather than a tutor by helping learners understand what they truly know.

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

## Needfinding Report: Understanding Learner Pain Points and Motivation

### 1. Objective

The goal of this needfinding study was to understand how adult learners—particularly those self-studying AI concepts—evaluate their own learning progress, what challenges they face in accurately gauging understanding, and how AI tools might help them receive more meaningful feedback.

### 2. Methods

Online survey: Distributed to students in the ECT program to capture broader perspectives on using AI for learning, self-assessment, and feedback.

### 3. Key insights

Learners consistently expressed uncertainty about what it means to truly “master” a concept, often asking when they could confidently claim understanding. Many felt that despite extensive study, their confidence decreased over time, revealing a lack of clear benchmarks for measuring progress. Rather than struggling to find learning materials, they struggled to verify whether they had genuinely understood or could apply what they learned. Traditional quizzes and recall-based tests were viewed as inadequate, since high scores could be achieved through guessing or pattern recognition. This led to frustration and self-doubt, as learners realized their perceived competence often didn’t match their actual ability. Together, these insights highlight a need for tools that provide measurable, evidence-based, and reflective ways to assess learning—focusing on conceptual understanding, real-world application, and the alignment between confidence and performance.

###  4. Design Implications for KnowCheck

Based on these insights, KnowCheck is designed around four guiding principles:

**Layered understanding:**

Break down mastery into stages — comprehension, application, and transfer — each with clear and measurable benchmarks.

**Evidence-based feedback:**

Go beyond single test scores by showing learners their reasoning patterns, examples, and counterexamples, helping them understand why they got something right or wrong.

**Confidence calibration:**

Collect learners’ self-rated confidence before tasks and visualize how it aligns with their actual performance.

**Contextual challenges:**

Use realistic, adaptive scenarios that test flexible thinking, rather than memorization or pattern recognition.

### 5. Data Sources

Reddit and StackExchange discussions about what it means to “truly know” machine learning.

Kaggle and Hacker News threads about skill evaluation and self-assessment in data science.

PNAS (2024) research on the gap between perceived and actual learning outcomes in AI-assisted environments.

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
