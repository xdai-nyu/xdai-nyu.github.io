# Pathways370
###### AI-Accompanied Hyperlocalized, Community-Centered Audio Walks
Sana Alimohamed, Rebeca Arens, Mei Buzzell, Maitreyi Nandhakumar, Ashish Noble

## Table of Contents
[Abstract](#abstract)
[Introduction](#introduction)
[System Design] (#system-design)
[Prototype] (#prototype)
[Evaluation](#evaluation)
[Findings](#findings)
[Ethical Implications](#ethical-implications)
[Future Work](#future-work)
[References](#references)

## Abstract
With greater transience, a stronger digital presence, and the diminishment of third spaces, people are losing a sense of belonging to the spaces they inhabit. Pathways370 addresses this problem by designing an AI-accompanied system that transforms archival data and community knowledge into hyperlocalized, interactive audio walks. Community members contribute personal stories and historical materials, which AI synthesizes into personalized audio experiences that reconnect people with their surroundings. Our prototype integrates Gemini's text-generation API and OpenAI’s voice-to-text AI, allowing creators to upload content, organize location-based content blocks, and customize narration style.

## Introduction

### Target Audience
Any digitally literate individual interested in sharing and archiving local community knowledge (eg, Place-based history). These could include history enthusiasts, educators, museums and local heritage groups. Pathways370 aims to support these enthusiasts who might lack the technical skills required to share their interests and expertise with the masses, by providing a streamlined audio-walk creation experience. 

### Problem Statement
How might we design with AI to transform archival data into an embodied and interactive lived experience?

### Identified Learning Need
As physical third spaces fade and online ones take their place, the sense of community has moved into the digital realm, eroding our capacity to feel grounded and connected in the spaces we physically inhabit. Having a solid, stable connection to the space around them allows people to participate in a diversity of rich experiences, helping them form a strong local identity within their community of practice (Wenger 1999). Research has shown that a sense of community and identity fosters a deeper sense of interconnectedness (Pei et al., 2023), and that the feedback and dialogue that emerge from extended interactions among community members encourage inquiry-based experiential learning (Dewey, 1938). Shared experience through interpersonal relationships and interactions, such as discussions, storytelling, and games, are key to developing critical skills such as communication and collaborative problem-solving (Panqueva, 2000). Building a community through shared immersive experiences can help cultivate a deeper sense of belonging and learning.

- There is a need to **strengthen people’s connection to their surroundings** to support participation in diverse and meaningful experiences that shape identity within a community of practice (Wenger, 1999).
- There is a need to **foster a strong sense of community** and identity to enhance interconnectedness and support deeper learning (Pei et al., 2023).
- There is a need to **encourage continuous feedback and dialogue among community** members to promote inquiry-based experiential learning (Dewey, 1938).
- There is a need to **create opportunities for shared interpersonal experiences**, such as discussions, storytelling, and games, to develop essential skills like communication and collaborative problem-solving for learning (Panqueva, 2000).

### Prototype Design
Pathways370 is an AI-powered web-based tool that allows community members to transform archival materials into structured, location-based audio walks. The platform uses AI at multiple stages of the process to assist the user - extracting information from the resources, creating location specific text blurbs and finally generating a completed transcript and audio file that can be shared with the end users of the walk. The platform is designed to be simple and intuitive for users who have limited technical expertise around writing and production, and through this it aims to make the process of sharing knowledge more equitable and accessible. 

### Rationale for AI Assistance
A physical audio walk immerses learners in the authentic spaces of the history they are exploring, fostering both situated and embodied cognition to enrich understanding and retention (Bruner, 1991). While traditional audio walks rely on pre-existing narratives, incorporating AI allows learners to actively contribute to content creation by submitting archival knowledge, personal stories, or other resources about a place. The AI synthesizes these inputs into a coherent, immersive narrative, dynamically structuring content, guiding transitions between sites, and linking stories to physical locations. This process not only personalizes the learning experience but also preserves learner autonomy, prompting reflection, exploration, and socially mediated engagement through discussion prompts or challenges (Jian, 2023).

Incorporating AI into the audio walk experience allows learners to personalize their journey by submitting archival knowledge and preferences. This personalization enables the AI to curate content that aligns with individual interests and prior knowledge, thereby optimizing cognitive load and enhancing learning outcomes (Sun & Yu, 2018). Furthermore, situating curated content within physical spaces reinforces experiential and inquiry-based learning, enabling learners to construct knowledge actively while developing a sense of belonging within the community they are exploring (Dewey, 1938). In this way, AI transforms the traditional audio walk into a personalized, interactive, and reflective learning experience that bridges archival knowledge, learner input, and embodied engagement with the environment. (Originally drafted by Beca, revised by Sana, final draft via ChatGPT)

### Findings in Brief
We conducted a preliminary evaluation of the product through user testing sessions with six participants. The users were split into two groups, the first group was given free choice to determine the topic about which they wanted to create an audio walk, whereas the second group was provided a predetermined site with resources to upload. Despite usability challenges in the Categorize and Studio pages, all six participants agreed that Pathways370 could assist cultural preservation. The findings identified specific areas for improvement including instruction clarity, workflow sequencing, and AI accuracy in content generation.
___________________

## System Design
### Design Features
Our design features were thought out to provide the user with a sense of agency and ownership in the design process while also making the process seamless and more intuitive for those with limited technical expertise. The tool was designed such that users who are enthusiasts or experts on a particular space or topic can bring in their curated resources (pdfs and images) to the platform where the AI would help extract material, organise the locations and content, and finally create a transcript and audio to share with people interested in learning more about the space. 

| User Needs | Design Goals | Mapped Features |
|------------|--------------|-----------------|
| AI generated content is often a black box and experts want more control over the material they create. | Empower users to choose the content. | The AI pulls content from the curated resources that the user uploads to the platform. |
| Users want to be able to change the content the AI generates without going through the process all over. | Provide agency to edit and customize generated content. | The platform generates editable blurbs that the user can choose to use or ignore and order them in any way they desire. |
| Users may want to generate different versions of the walk depending on the target audience. | Allow personalisation and generation of multiple versions. | The Audio page allows users to determine the target audience, conversation style, choose between voices and speeds, and generate multiple versions. |

The audio-walk creation process is broken into five pages:
* **Welcome:** define walk, themes, duration, and description
* **Archive:** upload and classify resources
* **Categorize:** arrange content into location-based blocks
* **Studio:** generate and edit the narrative script
* **Audio:** generate and download audio files

## Prototype
![Prototype Video](https://drive.google.com/file/d/1jKhtp_tjLIHz5qs_rOc3STbyHhiGXCOZ/view?usp=drive_link)

When we started our project, we knew that we wanted to build a tool around the process of transforming archival data and community knowledge into an interactive audiowalk–something that connected community and place, that balances personalized and shared experiences. 

### Early Steps
Early prototypes started with a simple paper mapping of a user’s path as they created an audio walk. We then built a [Figma design](https://www.figma.com/design/a8wYjmeUE4JVJhVaaCrht8/Builder-Input?node-id=0-1&t=yIYPWkSAlJA4ReGG-1) to test the user’s journey, identify their input, and visualize what the interface would look like. From there we identified key moments where we could leverage AI to streamline the creation process.

After evaluating and agreeing on our early prototype, we split up into two groups: front-end and back-end. 

### The Split Process (Mid-Fidelity)
Our initial mid-fidelity prototypes focused on building and testing the core functions of Pathway370. Utilizing vibecoding and AI-powered design tools like Claude and Builder.io, we worked on our sections independently, using Github to share our code and changes. Our team placed a large emphasis on iterative design, and we worked to prototype the front end and back end in rapid iterations, until they were both at a level where they could be combined to form a fully-functional prototype. 

[Mid-Fidelity Prototype](Builder prototype link)

#### Key Elements:
- **Process Stages:** Five stages–Home, Archive, Categorize, Studio, and Narration–break the creation process into more manageable sections.
- **Customizable Inputs:** Users can preset details to direct the AI, including pre-set themes, open input, and setting limits to adjust the focus and length of AI-generated content.
- **Human Control:** Users are able to set locations within an audio walk and organize AI-generated content by dragging and dropping content blocks into their respective locations.
- **Transcript & Voice Customization:** Users are able to adjust their audience, tone, and include other key details to fine-tune the generated transcript.

#### Front-End (Mei & Beca)
The frontend team focused on the user interface and interactions, designing ways for the users to control the creation process and balancing the cognitive load of the frankly exhaustive task it is to create an audiowalk.

<center>![Initial Audio Page vs Mid-Fidelity Audio Page](https://drive.google.com/file/d/1BzW020XwhnhhdP514zFYb852QWM-bkpV/view?usp=sharing)</center>
<center>Initial Audio Page vs Mid-Fidelity Audio Page</center>

Through iterative refinement and identifying necessary adjustments, we added variables to the code based on user value selections, allowing user selections and inputs to be saved and communicated across pages.  Using Builder.io, we transformed updated Figma designs into code to create a functioning front-end prototype using React framework, and further customized it using HTML, CSS, and JavaScript. As the backend started to integrate our initial prototype with their code, we shifted our focus to improving the UI and looking for ways to improve usability and flexibility.

#### Back-End (Sana, Maitreyi, & Ashish)
The backend team focused on testing and training the AI functions we needed, identifying the best options for APIs and how to execute the calls we identified. We began building out the APIs and preparing to connect to the front end, as well as working on generating QR code tied to locations.

Upon merging codebases in Github, we began aligning the necessary API endpoints, and running tests on prototypes. However, we were challenged by problems that sprung up during integration–as a result, we pivoted to using Replit to help build our design. 

![Content block organization](https://drive.google.com/file/d/1ALvnWpx9BfYO7SWdc3dVd12GjyQByFIP/view?usp=sharing) ![Transcript creation](https://drive.google.com/file/d/1a1Xl7f9UD4dJ1g_kW8wdhUcAaOT9xObp/view?usp=sharing)

We were able to successfully integrate Gemini’s text generation API into required pages, allowing users to create transcripts based on user-sorted content blocks and audience, tone, and additional narration-focused user inputs. This allowed us to use a simple Wizard of Oz method for early testing of the text and audio generation functions, as we further develop the deep content generation APIs.

### High-Fidelity Prototype 
Based on user feedback, possibilities and limitations that the earlier prototyping sessions revealed, and our own evaluation of how well the current prototype aligned with our identified needs and goals, we developed our current prototype with an eye towards balancing user autonomy and control with AI efficiency. We used Replit to link the front- and back-ends to create a robust system that blended user actions and AI processes, sharing and preserving information across multiple pages and endpoints to create a cohesive final product: a smooth, intuitive process of creating audiowalks. 
[You can try out our prototype here.](https://27d20387-2280-459b-85ba-2a17a4e042fd-00-3m2y2ra7tpd0n.kirk.replit.dev)

#### Added Features:
**Two-Column Studio Organizer**
- Content blocks are side by side with the locations they can be dragged into, making it easier for users to move blocks where they want.
- Both columns scroll independently, improving visibility.
- Filter system uses assigned categories, making it easier to manage large amounts of content

**Content Editing**
- Content blocks and the final transcript are easily editable, allowing users to directly edit the AI-generated text.
- Improves user control and mitigates AI hallucinations by allowing users to correct or change information when needed.

**Audiowalk Variations**
- Create multiple audiowalks at once, using the same content they’ve already organized. 
- Adjust settings for each variation independently, and craft as many variations of the transcript as needed.
- Supports the creation of both personalized and intergenerational experiences by leveraging AI’s strength–personalization–to create complementary but unique transcripts.

**Increased Transparency**
Pages now include information about where, how, and to what extent AI is being used in the process of creating the audio walk.

### Team Contributions 
- All team members discussed and decided on the functions of the webpage after evaluating the Figma prototype;
- Beca and Mei are developing the front end of the webpage;
- Sana, Maitreyi, and Ashish are developing the back end and training the AI;
- Beca, Ashish, and Sana worked in Replit to integrate front-end and back-end;
- Maitreyi and Mei refined microcopy on AI transparency; 
- Beca and Mei wrote the group update.

## Evaluation Plan
To evaluate the impact and usability of Pathways370, we will measure how effectively the tool enables users to transform archival materials into engaging interactive audio walks. Specifically, we will assess whether the AI-assisted workflow helps users feel more connected to a place and the community, empowers them to tell and share their own stories, and gives them control over the narrative experiences they create locally.

### Hypothesis
Based on our original problem statement — *“How might we design with AI to transform archival data into an embodied and interactive lived experience?”* the primary hypothesis we are evaluating is:

**If users create an audio walk using an AI-powered system that synthesizes personal and archival materials, then they will feel more empowered to share their stories with others.**

### User Testing Approach
To collect this data, we will conduct user testing with two groups:

- **Controlled group:** Creates a 15-minute audio walk about 370 Jay Street using a curated set of 3–5 archival resources provided to them.
- **Variable group:** Creates an audio walk based on a personally meaningful location, using their own photos and PDFs.

Both groups will complete the same end-to-end workflow:

**Welcome → Archive → Categorize → Studio → Audio**

After completing the workflow, both groups will complete a survey measuring:

- Intuitiveness  
- Clarity  
- Satisfaction with AI  
- Sense of control in creating
- Likelihood of sharing an audio walk 
- Shifts in connection with to place  

[Survey link](https://docs.google.com/forms/d/e/1FAIpQLSd3_eUQNGVOj5Pn_61165OxWjw0kvZ0dV9fNmvW204wvt8_rA/viewform)

### Analysis
The combination of curated assets and self-chosen resources allows us to observe how Pathways370 supports different use cases and understand user behavior in more detail. Survey responses, along with observations and user questions,  will be analyzed to determine the tool’s effectiveness and guide future iterations.

## Findings
The user testing revealed consistent patterns across both controlled (370 Jay Street, n=2) and experimental (user-selected locations, n=3) conditions, with participants rating the overall intuitiveness at 4 out of 5 on average.

* **Categorize Page:** Three users expressed confusion about the purpose of tags as categories, questioning why they needed to manually review AI-generated tags and how selecting categories would refine the content.
* **Studio Page:** The same three participants expressed confusion regarding the studio page. One controlled participant titled locations thematically rather than geographically (e.g., "subway history" vs. "subway entrance"), and one experimental participant spent considerable time trying to intermix location-specific and general content blocks before realizing this wasn't possible. Two participants expressed confusion about whether physical transition instructions were required.
* **Narration Customization Features:** Users appreciated the ability to specify audience, tone, and voice style, though two users placed these details in the "additional details" box rather than using the dedicated menus. Four users appreciated the ability to specify audience, tone, and voice style.

The experimental group faced additional challenges, including:
* File upload limitations (10MB PDF size limit)
* Confusion about location specificity requirements
* Frustration when AI-generated content didn't align with their vision. One participant notably exclaimed "These places don't exist!" and "You're just saying random things to me, AI!" when the system hallucinated locations from photos.

However, both groups strongly agreed that Pathways370 could support community storytelling (average 4.17/5) and cultural preservation (average 4.33/5), with sharing likelihood averaging 3.5/5.

**Additional survey results revealed the following:**

**Overall Intuitiveness** (1-5 scale): Average rating of 3.83/5
* Participants found the process moderately intuitive, with most rating it a 4

**Instruction Clarity** (1-5 scale, where 1=Not at all clear, 5=Extremely clear):
* Locations: Average 4.5/5 (mostly "Extremely clear" or "Very clear")
* Themes: Average 4.3/5 (mostly "Extremely clear" or "Very clear")
* Content blocks: Average 3.8/5 (most confusion here - ranged from "Slightly clear" to "Extremely clear")
* Narration style: Average 4.7/5 (consistently "Extremely clear" or "Very clear")

**AI Performance:**
* AI authenticity in preserving resource materials: Average 4/5
* Control over customization: Average 4.2/5

**Connection & Impact** (Agree/Disagree scale):
* "Pathways370 can improve connection to place": 67% Agree or Strongly Agree

**Participants suggested improvements including:**
* Animated help icons
* AI-automated transition instructions using Google Maps
* Earlier designation of stops in the workflow
* Audio instructions for accessibility
* Source suggestions for users without materials

## Ethical Implications
The design of Pathways370 raises several ethical considerations that we hope to have addressed through intentional design decisions and transparent communication with users.

**Responsibility and Content Accuracy**
A primary concern is responsibility when users create audio walks containing inaccurate or misleading historical information. Pathways370 processes content from user-provided sources without fact-checking or verifying historical accuracy. This design choice reflects our tool's purpose: to facilitate the creation process rather than serve as an arbiter of historical truth. A prominent disclaimer states that the tool does not guarantee the validity of information and that users should verify their sources independently. This approach respects user autonomy while acknowledging the tool's limitations.

**Transparency in AI Processing**
Users need to understand how AI shapes their content. Pathways370 addresses this through multiple transparency measures. First, we explicitly inform users that AI is used at three key stages: analyzing and categorizing uploaded resources, generating narrative scripts based on user-organized content blocks, and converting text to speech. Second, users maintain control throughout the process as they can view AI-generated categories, rearrange content blocks, edit transcripts, and adjust narration parameters. Third, the interface clearly delineates which elements are AI-generated versus user-created, ensuring users recognize the collaborative nature of the authoring process.

**Beneficence and Community Impact**
Pathways370 aims to create a positive social impact by enabling community members to preserve and share local histories that might otherwise be lost. By lowering barriers to audio walk creation, the tool democratizes placemaking and storytelling, allowing diverse voices to contribute to collective memory. This supports our goal of fostering interconnectedness and strengthening people's sense of belonging to their physical communities.

**Privacy and Data Use**
All uploaded materials and generated content remain under user control. We do not store user content beyond the active session unless users choose to save their projects. Generated audio walks are exported directly to users as files they can download and share at their discretion. 

**Mitigating Risks**
While our current approach relies primarily on transparency and user responsibility, we recognize the need for additional safeguards. Future development aims to include: content responsibility acknowledgments before publishing, reporting mechanisms for listeners who encounter problematic content, guidelines encouraging users to cite sources and respect privacy, community moderation features, and partnerships with local historical societies to support content quality while preserving creative freedom.

## Future Work
The current prototype demonstrates the viability of creating AI-assisted audio walks, but significant development remains to create a fully functional, user-ready platform. Key next steps include:

- *Front-end and back-end integration*: Achieve seamless connection between the frontend, backend, and LLM API calls
- *User testing and design refinement*: Conduct comprehensive testing to improve design and flow
- *Public publishing platform*: Build a platform where creators can publish their audio walks, enabling discovery by listeners and fostering a community of both walk creators and users.
- *QR code functionality*: Implement location-based playback that allows listeners to access audio segments by scanning QR codes placed at physical sites along the walk route.
- *AI reliability screen*: Develop transparency features that help users understand AI confidence levels and source attribution for generated content.
- *Resource database*: Establish a secure database enabling users to save projects, manage multiple walks, and build libraries of archival materials over time.

## Other Content

### Secondary Research

### *Literature Review*

**To the Castle! A comparison of two audio guides to enable public discovery of historical events (Fitzgerald, Taylor, & Craven, 2013)**  
A local community history group created two audio guides aimed at informing the public about a local historical event (the 1831 Reform Riot in Nottingham, England): a human-led walk that provided spoken narratives at specific points, and a technology-led walk of geolocated audio files that provided similar information through a GPS-enabled smartphone. They sought to evaluate the differences between the two and if they were an effective learning experience. They found that participants on the technology-led walk liked the independence of the tour and the technological affordances, particularly the clearer listening experience and ability to play back the audio, and overall displayed similar levels of learning as the human-led walk. However, participants preferred shorter, less drier content, missed the opportunity to ask questions on the walk, and wanted different versions of the audio recordings to accommodate the listener (i.e. native vs non-native English speakers, children vs adults, levels of familiarity with the history). The researchers reached the conclusion that technology-led tours are a viable, scalable approach for community history groups to foster informal learning opportunities about local history, and we believe that AI could be leveraged to address user issues and support the aforementioned approach.

**The effect of audio tours on learning and social interaction: An evaluation at Carlsbad Caverns National Park (Novey & Hall, 2005)**  
Researchers evaluate the effect of an audio tour, using casual narration and ambient sound, on visitors at Carlsbad Caverns National Park. They compared audio tour users and nonusers on a 12-item knowledge quiz while evaluating other behaviors such as reading informational signs and interacting with one another, and found that audio tour users’ scores were roughly similar to the nonusers’ scores on fact-recall multiple choice, but that audio tour users were more likely to answer open-ended questions on the park’s main themes correctly. Audio tour users and nonusers’ social/interpretive behaviors (reading signs and interacting with others) did not differ substantially, though at audio-only stops nonusers were more likely to be interacting with other visitors. Overall, the audio tour was received positively, increased the length of the visit, and did not strongly impede social interaction while fostering deeper learning about the overall message and themes of the park.

**How the Use of Audio Walks as Creative Public Engagement Expands Access to Site-Based Heritage to a Diverse and Globalised Audience. (Reagan, 2024)**  
Reagan argues that the digital format of audio walks offers greater audience reach and flexibility compared to in-person tours, despite the drawback of lacking real-time dialogue with visitors. The chapter further analyzes the demographic data of the audio walks, revealing that a large percentage of listeners engage with the content remotely rather than taking the walks in situ, suggesting the content functions more as an "audio experience." Ultimately, Reagan encourages heritage sites to prioritize digital engagement offerings, recognizing that visitor interaction may differ significantly from initial expectations.

**Memoryscape: How Audio Walks Can Deepen Our Sense of Place by Integrating Art, Oral History and Cultural Geography. Geography Compass. Butler, Toby. (2007).**  
The article explores the history, practice, and theoretical implications of creating sound walks or "memoryscapes". It argues that audio walks serve as a powerful platform for sharing knowledge and amplifying diverse narratives within a community. They can be a vehicle for oral histories, allowing long-time residents to share their memories and perspectives with newer generations. This form of storytelling can be particularly impactful in preserving and disseminating the cultural heritage of a neighborhood.


### *Existing Commercial Solutions*

**Google Audio Walk Creator**  
https://artsandculture.google.com/experiment/talking-tours/8AGlfzgsYmBeIA?hl=en  
Google Audio Walk Creator allows users to choose specific streetviews at cultural landmarks, and generates audio insights.  
- *Location-Specific Analysis:* Google’s Gemini multimodal language models analyzes Street View images, GPS, and historical context.
- *Script Generation:* The AI audio model creates real-time audio tours, and allows users to generate new ones.
- *Query-Based Interactivity:* To learn more about a space, users can choose from 3 pre-generated questions or ask their own.

**Echoes**  
https://echoes.xyz/  
Echoes enables creators to build free or custom AR audio experiences through tailored apps, including locative audio walks, guided tours, or immersive sound experiences.  
- *Spatial Mapping:* Echoes offers geolocated audio playback, and uses live heatmaps to trigger a dynamic experience based on location 
- *Surround Sound:* Supports stereo, binaural, 3D, and ambisonic audio
- *Branching Narratives:* Adapts story progression to the listener's movement, direction, and spatial location, making it a a mechanism for narrative choice

**VoiceMap New York City**  
https://voicemap.me/tour/new-york-city  
VoiceMap NYC is a platform that allows users to access self-guided walking tours delivered through local storytelling, routed by real-time location on a map.  
- *Geo-Synced Narration:* GPS-based automatic audio narration is synced to listeners’ position through a mobile app.
- *Collaborative Storytelling:* Audio tours are contributed by a diverse community of journalists, artists, and locals, using soundscapes and narration to create immersion.

---

## Prototype

![Prototype Video](https://drive.google.com/file/d/1jKhtp_tjLIHz5qs_rOc3STbyHhiGXCOZ/view?usp=drive_link)

When we started our project, we knew that we wanted to build a tool around the process of transforming archival data and community knowledge into an interactive audiowalk–something that connected community and place, that balances personalized and shared experiences. 

### Early Steps
Early prototypes started with a simple paper mapping of a user’s path as they created an audio walk. We then built a [Figma design](https://www.figma.com/design/a8wYjmeUE4JVJhVaaCrht8/Builder-Input?node-id=0-1&t=yIYPWkSAlJA4ReGG-1) to test the user’s journey, identify their input, and visualize what the interface would look like. From there we identified key moments where we could leverage AI to streamline the creation process.

After evaluating and agreeing on our early prototype, we split up into two groups: front-end and back-end. 

### The Split Process (Mid-Fidelity)

Our initial mid-fidelity prototypes focused on building and testing the core functions of Pathway370. Utilizing vibecoding and AI-powered design tools like Claude and Builder.io, we worked on our sections independently, using Github to share our code and changes. Our team placed a large emphasis on iterative design, and we worked to prototype the front end and back end in rapid iterations, until they were both at a level where they could be combined to form a fully-functional prototype. 

[Mid-Fidelity Prototype](Builder prototype link)

#### Key Elements:
**Process Stages:** Five stages–Home, Archive, Categorize, Studio, and Narration–break the creation process into more manageable sections.
**Customizable Inputs:** Users can preset details to direct the AI, including pre-set themes, open input, and setting limits to adjust the focus and length of AI-generated content.
**Human Control:** Users are able to set locations within an audio walk and organize AI-generated content by dragging and dropping content blocks into their respective locations.
**Transcript & Voice Customization:** Users are able to adjust their audience, tone, and include other key details to fine-tune the generated transcript.

#### Front-End (Mei & Beca)
The frontend team focused on the user interface and interactions, designing ways for the users to control the creation process and balancing the cognitive load of the frankly exhaustive task it is to create an audiowalk.

<center>![Initial Audio Page vs Mid-Fidelity Audio Page](https://drive.google.com/file/d/1BzW020XwhnhhdP514zFYb852QWM-bkpV/view?usp=sharing)</center>
<center>Initial Audio Page vs Mid-Fidelity Audio Page</center>

Through iterative refinement and identifying necessary adjustments, we added variables to the code based on user value selections, allowing user selections and inputs to be saved and communicated across pages.  Using Builder.io, we transformed updated Figma designs into code to create a functioning front-end prototype using React framework, and further customized it using HTML, CSS, and JavaScript. As the backend started to integrate our initial prototype with their code, we shifted our focus to improving the UI and looking for ways to improve usability and flexibility.

#### Back-End (Sana, Maitreyi, & Ashish)
The backend team focused on testing and training the AI functions we needed, identifying the best options for APIs and how to execute the calls we identified. We began building out the APIs and preparing to connect to the front end, as well as working on generating QR code tied to locations.

Upon merging codebases in Github, we began aligning the necessary API endpoints, and running tests on prototypes. However, we were challenged by problems that sprung up during integration–as a result, we pivoted to using Replit to help build our design. 

![Content block organization](https://drive.google.com/file/d/1ALvnWpx9BfYO7SWdc3dVd12GjyQByFIP/view?usp=sharing) ![Transcript creation](https://drive.google.com/file/d/1a1Xl7f9UD4dJ1g_kW8wdhUcAaOT9xObp/view?usp=sharing)

We were able to successfully integrate Gemini’s text generation API into required pages, allowing users to create transcripts based on user-sorted content blocks and audience, tone, and additional narration-focused user inputs. This allowed us to use a simple Wizard of Oz method for early testing of the text and audio generation functions, as we further develop the deep content generation APIs.


### High-Fidelity Prototype 
Based on user feedback, possibilities and limitations that the earlier prototyping sessions revealed, and our own evaluation of how well the current prototype aligned with our identified needs and goals, we developed our current prototype with an eye towards balancing user autonomy and control with AI efficiency. We used Replit to link the front- and back-ends to create a robust system that blended user actions and AI processes, sharing and preserving information across multiple pages and endpoints to create a cohesive final product: a smooth, intuitive process of creating audiowalks. 

[You can try out our prototype here.](https://27d20387-2280-459b-85ba-2a17a4e042fd-00-3m2y2ra7tpd0n.kirk.replit.dev)

#### Added Features:
**Two-Column Studio Organizer**
- Content blocks are side by side with the locations they can be dragged into, making it easier for users to move blocks where they want.
- Both columns scroll independently, improving visibility.
- Filter system uses assigned categories, making it easier to manage large amounts of content

**Content Editing**
- Content blocks and the final transcript are easily editable, allowing users to directly edit the AI-generated text.
- Improves user control and mitigates AI hallucinations by allowing users to correct or change information when needed.

**Audiowalk Variations**
- Create multiple audiowalks at once, using the same content they’ve already organized. 
- Adjust settings for each variation independently, and craft as many variations of the transcript as needed.
- Supports the creation of both personalized and intergenerational experiences by leveraging AI’s strength–personalization–to create complementary but unique transcripts.

**Increased Transparency**
- Pages now include information about where, how, and to what extent AI is being used in the process of creating the audio walk.

### Team Contributions 
- All team members discussed and decided on the functions of the webpage after evaluating the Figma prototype;
- Beca and Mei are developing the front end of the webpage;
- Sana, Maitreyi, and Ashish are developing the back end and training the AI;
- Beca, Ashish, and Sana worked in Replit to integrate front-end and back-end;
- Maitreyi and Mei refined microcopy on AI transparency; 
- Beca and Mei wrote the group update.

---

### References:
- Bruner, J. S. (1991). The narrative construction of reality. *Critical Inquiry, 18*(1), 1–21. https://doi.org/10.1086/448619
- Butler, T. (2007). Memoryscape: How audio walks can deepen our sense of place by integrating art, oral history and cultural geography. *Geography Compass, 1*(3), 360–372. https://doi.org/10.1111/j.1749-8198.2007.00017.x
- Dewey, J. (1938). *Experience and education*. Macmillan.
- FitzGerald, E., Taylor, C. & Craven, M. To the Castle! A comparison of two audio guides to enable public discovery of historical events. *Pers Ubiquit Comput 17*, 749–760 (2013). https://doi.org/10.1007/s00779-012-0624-0
- Jian, M. J. K. O. (2023). Personalized learning through AI. *Advances in Engineering Innovation*, 5(1), 16–19. https://doi.org/10.54254/2977-3903/5/2023039
- Novey, L., & Hall, T. (2005). The effect of audio tours on learning and social interaction: An evaluation at Carlsbad Caverns National Park. *Science Education, 91*(2), 920–935. https://doi.org/10.1002/sce.20184
- Panqueva, G. (2000). *Play, puzzles and creativity: Learning engines for the knowledge society* (Technical Document ACE-01-00, Version 2, p. 452).
- Pei, L., Poortman, C., Schildkamp, K., & Benes, N. (2023). Teachers’ and students’ perceptions of a sense of community in blended education. *Education and Information Technologies*, 29(2), 2117–2155. https://doi.org/10.1007/s10639-023-11853-y
- Reagan, R. . (2024). Unlocking Heritage Stories: How the Use of Audio Walks as Creative Public Engagement Expands Access to Site-Based Heritage to a Diverse and Globalised Audience. In C. Wergin & S. Affeldt (Hrsg.), *Digitising Heritage: Transoceanic Connections between Australia and Europe* (S. 73-89). Heidelberg: Heidelberg University Publishing. https://doi.org/10.17885/heiup.1305.c18420
- Sun, J. C. Y., & Yu, S. J. (2018). Personalized wearable guides or audio guides: An evaluation of personalized museum guides for improving learning achievement and cognitive load. *International Journal of Human–Computer Interaction*, 35(4–5), 404–414. https://doi.org/10.1080/10447318.2018.1543078 
- Wenger, E. (1999). *Communities of practice and social learning systems. Organization*, 7(2), 225–246. https://doi.org/10.1177/135050840072002 

### Team Contributions
- All team members ideated together, then did preliminary research and ideated some more independelty; 
- Beca wrote the original sections;
- Ashish, Maitreyi, Mei, and Sana provided feedback on edits;
- Sana updated the description based on a group discussion. Rationale for AI Assistance was edited by chatgpt.


