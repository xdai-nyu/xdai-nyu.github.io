---
layout: page
title: [S25] Cognizance
nav_exclude: true
---

## Cognizance: Your Deep Learning Pal
![COGNIZANCE LOGO](https://github.com/user-attachments/assets/337d1457-b9c3-4417-a2d1-a1ea189a0be3)

## Project Members: 
Danira (Dira) Khatwani, Huishan (Rae) Ruan, Zulsyika (Syika) Nurfaizah

## Target Learning Audience:
The target audience for this project is adult learners (college students, graduates, working professionals) who engage with reading assignments in humanities, social sciences, and STEM courses. These students often encounter dense, complex academic texts that require critical thinking, interpretation, and synthesis of ideas. Many struggle to extract key insights, connect concepts across readings, and engage deeply with course materials. Additionally, challenges arise in large courses where individualized guidance is difficult.

## Project Brief (Updated):  
Reading assignments are a fundamental part of college education, yet many students find them overwhelming and struggle with comprehension. Research suggests that academic texts often use discipline-specific language, complex structures, and abstract arguments that can hinder understanding, particularly for students new to the subject (Snow, 2002). Many students engage with readings passively, skimming the text without developing a deep understanding or making connections to broader course themes (Chi, 2009). Instructors often encourage students to take an active approach to reading—annotating, questioning, summarizing, and synthesizing—but providing individualized scaffolding for these strategies is difficult in large classroom settings.

Scaffolding effectively supports students' reading comprehension, particularly when students are guided through progressive levels of engagement with the text (Wood, Bruner, & Ross, 1976). However, traditional methods of scaffolding, such as instructor-led discussions and guided reading exercises, are difficult to scale. Many students are left to navigate complex texts on their own, often struggling to engage with the material at the deeper level expected in college courses.

## Rationale for AI Assistant
AI can provide a personalized scaffolding experience that helps college students engage in active, deeper reading of course materials. The AI assistant can work alongside students as they complete reading assignments, offering structured guidance to help them process, analyze, and critically engage with texts. Prior research shows that AI-enhanced reading interventions can improve comprehension, promote metacognition, and foster deeper engagement with academic texts (Graesser et al., 2005; McNamara et al., 2012).  

The AI will provide scaffolded reading support through:
1. Scaffolding Learning – AI guides students through structured questioning, interactive explanations, and learning progress visualization.
2. Encouraging Constructive Negotiation – AI challenges students with counterarguments, debate prompts, and opposing viewpoints.

We translated those into several features:  
### Must Have: 
1. ✅ Personalized Scaffolding: Provide a scaffolding based on students’ personal ZPD and needs using the Socratic method and structured breakdown.
2. ✅ Context-Aware Responses: AI grounds responses in course materials (RAG approach).
Provides citations & links to relevant resources to reduce misinformation.

### Nice to Have
1. Notes: A dedicated section for note-taking, to sum up the main points of conversations with AI.
2. Analytics: Tracking data analytics to improve students' learning performance.
3. Summary: Informational menu to summarize the conversation, key terms, and additional resources to delve deeper into the concept.

## Need-Finding Insights
Our initial project focus is on developing AI add-ons/plugins for LMS, here is our survey form: [Needs Analysis for Cognizance: Your Personalized Learning Pal](https://forms.gle/ueL9fDrshxe9L3Wx6)  

Based on our initial survey questions, we discovered several interesting insights:  

### 1. LMS is not used as a study platform
![image](https://github.com/user-attachments/assets/8020d960-ceb6-4224-8688-62d6cd1dd56c)
> Most respondents view LMS as a tool for receiving instructor feedback, submitting assignments, and accessing learning materials instead of an active study platform. **Respondents prefer offline tools** (document readers) to read and annotate the learning contents. LMS discussion features are perceived as less effective, and often used for participation points rather than meaningful discussion, they prefer third-party communication tools like Slack.  

### 2. Clear information and intuitive navigation support comprehension
![image](https://github.com/user-attachments/assets/4c43f671-e5e4-4b6f-a71d-6166f2f99a2f)
> Respondents like clear information (notifications and reminders), content presentation, and easy access to resources in LMS.  

### 3. The biggest challenge for respondents' comprehension is information overload
![image](https://github.com/user-attachments/assets/1a80d4ec-b28a-4ddd-8018-fd29df7b030f)
> The information overload is caused by **too much unstructured content (75%) and lack of visuals or interactive elements (56.3%)**.  

### 4. Respondents struggle with hard-to-read text and remembering information over time
![image](https://github.com/user-attachments/assets/30e81a0a-66a4-4399-a3ed-e567c4a2b51f)
> **68.8%** of respondents struggle with low-quality scanned documents and hard-to-read text, and **62.5%** of respondents struggle with remembering information over time, which could be caused by surface learning because **50%** of the respondents struggle to think critically about the materials.  

### 5. Respondents actively use AI tools and search for more resources to support their comprehension
![image](https://github.com/user-attachments/assets/18e995ff-c981-4b83-99e1-06e3d60eeeec)
> Most of the respondents use AI tools **(81.3%)**, search for more resources **(81.3%)**, and reread the materials **(56.3%)** to deepen their understanding of the learning contents.  

### 6. Further Insights:
- Common study methods to enhance comprehension include note-taking, task management, and removing distractions.
- AI tools that respondents often use are ChatGPT, Gemini, Claude.ai, DeepSeek, SciSpace, and NotebookLM to summarize, paraphrase, break down, cross-check, and brainstorm. Immersive Translate and AI Translation Tools to translate reading materials and unfamiliar words in real time.
- Instead of using AI in LMS, it's better to focus on reading comprehension aid since LMS is mostly used as a repository and task-tracking.
- Desired features for AI-enhanced learning assistant include **material structuring and organization, generating visuals to complement text-based information, controversy radar and additional resources, built-in translation features, learning roadmaps, and learning analytics**
- Current user workflow includes a) user downloads learning content from LMS; b) user uses document reader tools (Zotero, Adobe Acrobat, etc.) to read, annotate, and organize materials; c) user jumps to AI tools (ChatGPT, Gemini, Claude.ai, DeepSeek, SciSpace, NotebookLM, etc.) to summarize, paraphrase, break down, cross-check, brainstorm, or translate learning contents.

## Design Implication
Based on the insights from the need analysis, the design implications of our project are:  
1. AI tool that adapts to the learner’s prior knowledge, learning level, and pace, offering personalized guidance and content.
2. AI tool that provides Socratic method questions for users to deepen and widen their understanding of the concept. Ensuring that learners truly grasp the concept across various contexts.  

## Rapid Prototyping
We created the three main features of the tools:
1. [UI Prototype](https://docs.google.com/presentation/d/1TvTVOP62yK9dFGJzMGFjXJEIZtjMMfiiNW6y_tg0CWA/edit?usp=sharing)
3. [Interaction Prototype](https://colab.research.google.com/drive/11VSD-We5alK8JneeI8dcZ4SGC9F0iqqD?usp=sharing)

## User Flow
![image](https://github.com/user-attachments/assets/5655a7ad-acb9-4c7e-aac4-31cf49e4fd26)
This is the user flow of Cognizance. Open our [Miro document](https://miro.com/app/board/uXjVIQQ4Nl0=/) for a clearer and zoomable view.

## Ethical and Societal Implications
At Cognizance, we believe using AI in education should be as thoughtful and responsible as it is innovative. One key concern we’re addressing is the risk of narrowing learners’ perspectives or oversimplifying complex ideas. To support deeper understanding, our tool includes Socratic questioning and “Go Deeper” features that invite users to think beyond what’s written, asking what perspectives might be missing or how a concept could be challenged. These features encourage active, reflective reading rather than passive consumption.

Since our AI pulls from both course materials and relevant external sources, we’re especially mindful of transparency. Every response includes citations so students can see where the information comes from and assess its credibility for themselves. This not only reduces the risk of misinformation but also supports the development of research and evaluation skills. We’re also exploring ways to surface the AI’s reasoning—for example, explaining why a certain question or suggestion was made—so learners can better trust and critique the tool's logic.

Another area we’ve been careful about is language accessibility. For students who aren’t native English speakers or are reading outside their comfort zone, we don’t want translation to be a blunt tool. Instead of offering just a basic translation, we’re working toward features that also suggest synonyms or definitions to give users a richer, more contextualized understanding of terms. Inspired by tools like Grammarly, this approach gives learners choices and deepens comprehension rather than flattening meaning.
Finally, we’re committed to protecting student privacy. If features like note-taking or learning analytics are added, we’ll clearly communicate what data is collected, keep it anonymized, and ensure that participation is fully optional. Our design is grounded in respect for learners’ autonomy, diversity, and trust, because building AI for education isn’t just about improving performance; it’s about supporting meaningful, equitable, and empowering learning experiences.

#Current Prototype
You can access our prototype through this [Google Colab](https://colab.research.google.com/drive/1yxpv-fcxeDwtS5jPfws8E9OzxzrSh_cV?usp=sharing) file. Currently, we are trying to create a better UI for the tool. Please look forward to the development of Cognizance!

## References
1. Chi, M. T. H. (2009). Active-constructive-interactive: A conceptual framework for differentiating learning activities. Topics in Cognitive Science, 1(1), 73-105.
2. Graesser, A. C., McNamara, D. S., & VanLehn, K. (2005). Scaffolding deep comprehension strategies through automated questioning. Applied Cognitive Psychology, 19(5), 579-594.
3. McNamara, D. S., Levinstein, I. B., & Boonthum, C. (2012). iSTART: Interactive strategy training for active reading and thinking. Behavior Research Methods, Instruments, & Computers, 36(2), 222-233.
4. Snow, C. (2002). Reading for understanding: Toward an R&D program in reading comprehension. RAND Corporation.
5. Wood, D., Bruner, J. S., & Ross, G. (1976). The role of tutoring in problem-solving. Journal of Child Psychology and Psychiatry, 17(2), 89-100.

## AI-Usage Acknowledgement 
We use ChatGPT to brainstorm possible design directions, Copilot to critique possible features for the tools, and Grammarly for general language structure.

## Team Contribution  
1. Dira
   - Formulated survey questions and flow
   - Created user flow on Miro
   - Created project development plan
2. Rae
   - Finalized survey questions, collected key insights, and helped identify key design implications
   - Helped shape the project direction based on feedback for rapid prototyping
   - Found a slide template and drafted the presentation layout
3. Syika
   - Helped with survey questions and summary
   - Created and revised the prototype
   - Posting project updates on the project site
