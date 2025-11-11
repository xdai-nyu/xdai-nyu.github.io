# MathSparkPlay
## An AI-powered math “playground” for user-directed recreation and discovery learning in mathematics.
Bair + Penny Hays

<br>



---

### Needs Assessment | Overview of Problem Space

<br>

American students are struggling in math. Our literature review surfaced the following snapshot of issues facing K-12 mathematics in the U.S. today:



* Researchers have measured **“sharp, steep declines” in competency scores** between 2019 and 2023 (Carr, 2024). This is partially attributable to education disruptions during the COVID19 pandemic, but declines were seen prior to the pandemic (Schwartz, 2024) and studies show a mixed picture and minimal recovery post-pandemic (NAEP, 2024).
* **Students broadly report** **disinterest** in academic mathematics. 49% of middle and high school respondents reported losing interest in math about half or more of the time, and 75% reported losing interest for at least some class time (Schwartz, et al, 2025). This loss of interest is consistent across genders and racial and ethnic groups (Schwartz et al, 2025).
* **Rates of math anxiety are increasing**, worldwide and in the U.S. (Schwartz, 2024).
* Standardized assessment is a major component of current K-12 math pedagogy. Stakeholders need ways to measure what students can do, discover gaps, and discern whether current teaching is effective (Jimenez & Modaffari, 2021). But a 2021 report by The Center for American Progress shows that our current means of achieving these goals is impacting *what* and *how* students learn, pushing classroom instruction away from best practices:
  > “The tests result in teaching to the test. Is this claim true or false? It is true. A 2007 review of 49 studies found that 80 percent of the studies saw a change in curriculum and increased focus on teacher-led instruction (McMurrer, 2007). Generally, “teaching to the test” means “teaching in a manner that is not considered optimal for learning standard content or skills, but is believed to improve test performance (Phelps, 2016)”. (Jimenez & Modaffari, 2021)
* Current assessment methods tend to operationalize procedural fluency rather than conceptual understanding. Pedagogy thus shifts to **favor top-down learning of procedures - often unintentionally stripped of context, meaning or relevance - over bottom-up activities that cultivate conceptual understanding, such as conjecture, discussion, and diverse strategizing** (Boaler & LeBlanc, 2025). 

* **Traditional scope and sequence** (algebra > geometry > algebra 2 > trigonometry > calculus) remains relevant to some professions but** is** **increasingly irrelevant** for the majority of students in their educational and career pathways, **while more universally necessary, useful, relevant disciplines like data science are often left out** of K-12 curricula (Boaler & LeBlanc, 2025):
  > “The [University of California] five years ago accepted data science as an alternative to algebra 2. Kids could take data science and statistics maybe instead of going algebra, algebra, trig, calculus. And it was all going okay until actually one of your faculty at Berkeley heard about it and went on a campaign to have it shut down. They went and they petitioned and UC said okay no longer can kids take data science. Well, the argument's given - and this is a backwards argument in my view - the argument is given that it is inequitable to offer kids a different pathway. It will stop black and brown kids from doing well in life because it will pull them off the calculus pathway and the calculus pathway is what is so important. So they share that argument - that this is an inequitable set of affairs, offering kids data science. And people believe it. But actually what you see is when data science pathways are in high schools, they bring in a lot more kids who are more diverse, who haven't been traditionally successful - they take a course in data science and they start to see that maths can be really relevant and they get really into it and they go into STEM. So, it's frustrating.”	- Jo Boaler, on unSILOed podcast with Gregory LaBlanc, Episode 551, Jun 11, 2025, 29:11

* Anecdotal accounts suggest **students often feel mathematics is irrelevant to their lives.** K-12 math also **tends to center extrinsic motivators** like placements, scores and grades, and external indicators like “performance” and “achievement”, rather than intrinsic motivators like enjoyment, or satisfactions related to Self Determination Theory such as autonomy and competence (Samuelsson, 2021). Yet a 2011 study by Maltese and Tai found that “interest in and perceptions of the usefulness of mathematics and science, rather than achievement or course enrollment, was most predictive of degree choice” (Leyva et al., 2022), suggesting **intrinsic motivators may make a stronger impression on math learners than extrinsic ones.**

  <br>
  
At the same time, positive early experiences with math, including enjoyment and experiences of autonomy and competence (Ryan & Deci, 2017) can promote a positive attitude and positive self-concept with regard to math, including coming to consider oneself “a math person” (Schwartz et al, 2025). This, in turn, has been shown to have a strong positive impact on later math engagement, resilience and performance (Schwartz et al, 2025). 


### 
<br>

---



### Needs Assessment | Market Analysis
<br>

Most tech-based mathematics applications available today aim to address one or more of the issues listed above, and/or learners’ experience of them. They help students navigate and keep up with academic math as it is, rather than shift or expand learners’ notion, experience, or understanding of mathematics. Most fall into quadrants 1 & 2 in the matrix diagram shown below, occupying the ***goal-oriented*** end of the *purpose + method* (y-axis) continuum. 

They fall on every point along the *content level* (x-axis) spectrum from early to advanced. But they rarely, if ever, offer content beyond the traditional U.S. mathematics curriculum. The [list of Khan Academy’s math content offerings](https://www.khanacademy.org/math) is a good example - it’s extensive, but all within the current U.S. scope and sequence. These offerings are informed by [Khan Academy](https://www.khanacademy.org/)’s business plan. Like most tech-based math learning applications, they’re offering a service to parents, teachers, and learners themselves: to **help learners catch up or get/stay ahead of their cohort in terms of performance and achievement in traditional K-12 academic mathematics**. Their marketing materials promise “real results” by “filling gaps” and “accelerating learning.” 

Other math learning applications aimed at improving and enhancing learner performance in academic settings include [IXL](https://www.ixl.com/membership/administrators/RTI?partner=google&campaign=17316844499&adGroup=140949641036&gad_source=1&gad_campaignid=17316844499&gbraid=0AAAAADp4qSIgrOK7geJgU2gKwFEI2zU_4&gclid=CjwKCAjwxrLHBhA2EiwAu9EdM0NfhNQAc65zkSvVp-wiQWaqiMHUCw6MrvnsrTRj_W0ycHPJS2ypHhoC9M0QAvD_BwE), [DreamBox Learning](https://www.dreambox.com/) and [Varsity Tutors](https://www.varsitytutors.com/?network=g&matchtype=e&keyword=varsity%20tutors&creative=658311591108&device=c&devicemodel=&placement=&position=&capaignid=20125389110&adgroupid=145896265661&loc_physical_ms=9060351&loc_interest_ms=&keywordId=kwd-19291120192&zip=&accountid={123-208-7597}&vtbu=core&gad_source=1&gad_campaignid=20125389110&gbraid=0AAAAADkqTpTJyKViihYxixpGMhRewnq5e&gclid=CjwKCAjwxrLHBhA2EiwAu9EdMzdk4eoluEciNjml0_nWkBtUQO1iyNxNnF1ZQAvnBr3CAuHKnm_QqxoCs_IQAvD_BwE).

Other applications aim to** improve learner fluency with mathematics procedures and facts** - sub-skills that contribute to math performance and achievement - often using games and/or gamification to encourage increased duration of fluency-building practice. Applications that do this include [Prodigy Math](https://www.prodigygame.com/main-en/parents), [Reflex](https://reflex.explorelearning.com/), and [Delta Math](https://www.deltamath.com/).

Still other applications offer **instant support for specific problems**. A use case example: a student, “stuck” on a homework problem, enters it into a problem-solving app to see how the problem is done, uses this *worked example* to reverse-engineer an understanding of the process, then applies this understanding to other problems. [Photomath](https://photomath.com/) and [Mathway](https://www.mathway.com/Algebra) are some good examples.


<br>

---

### Engaging Quadrants 3 & 4 | Exploratory, Self-Directed, Playful, & Recreational Mathematics 
<br>

While “recreational mathematics” generally indicates something outside the realm of formal education (Wikipedia, 2025), it can be richly educational. As a pure category, it would presumably involve activities like puzzles and games engaged exclusively for recreation or entertainment. But this is a bit of a false notion. As the Mathematical Association of America asserts:


> “Recreational mathematics is not easily defined because it is more than mathematics done as a diversion or playing games that involve mathematics. Recreational mathematics is inspired by deep ideas that are hidden in puzzles, games, and other forms of play.” (MAA, 2013)

Engagement with “deep ideas” is key to attraction, motivation, pleasure and enjoyment in recreational mathematics. The pull of “deep ideas” inspires a self-directed, self-motivated exploratory process, while the recreational context preserves a playful valence. The presence of “deep ideas” deepens the potential energy of competence and autonomy satisfactions that enhance intrinsic motivation and, in turn, enhances learning (Ryan & Deci, 2017). This kind of exploration can be geared toward any age or level of sophistication, and can inspire further study of mathematics in general or of a specific subject or content area within mathematics (Kulkarni, 2013). 

A small number of tech-based math learning applications on the market today appear to be moving in this direction, away from the ***goal-oriented*** end of the *purpose + method* (y-axis) continuum. They’re a bit more playful and curiosity-driven and a bit less goal-oriented than the mainstream (see “play around” instructions from Synthesis Tutor, at right). They position themselves as **deepening engagement with conceptual ideas in mathematics** rather than scaffolding and sharpening specific procedures or skills. Marketing materials for these applications emphasize how they recruit visualizations, multisensory experiences and manipulable elements to cultivate “deep understanding”, offer “warm, patient, encouraging” adaptable tutors to reduce feelings of intimidation and anxiety, and go “much further” than standard K-5 math curriculum. Their instructional language and user interfaces center *exploration *of math rather than *performance *or* achievement *in math. But while they seem less overtly focused on helping students “catch up” or “keep up”, it’s clear this is still important, and that “results” matter. They also generally include some use of gamification to motivate engagement, suggesting engagement isn’t purely intrinsically motivated. But wherever they might sit on the *purpose + method* continuum, these applications are **overwhelmingly geared toward early math content**, most commonly K-5. Examples include [Synthesis tutor](https://www.synthesis.com/tutor) (note complimentary soft skills program and link to SpaceX school),  [Constructor Tech / Calcularis](https://constructor.tech/lp/calcularis-dyscalculia?utm_term=math%20intervention%20programs&utm_campaign=B2C+Schools_Calcularis_Free+trial_USA_Dyscalculia&utm_source=adwords&utm_medium=ppc&hsa_acc=6722240133&hsa_cam=22641709194&hsa_grp=186336927491&hsa_ad=756786644285&hsa_src=g&hsa_tgt=kwd-304302361149&hsa_kw=math%20intervention%20programs&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gad_source=1&gad_campaignid=22641709194&gbraid=0AAAAABe1wbx4LnU2eod7rwjgiKUJHkn_W&gclid=CjwKCAjwxrLHBhA2EiwAu9EdM5BUYudxywu-eKKkTNj5H7CzNSeHdNJpEakRwMy4pqRPOcameCk0WxoCmQ4QAvD_BwE) (app for dyscalculia), and [Amplify](https://amplify.com/).


Learners of all ages have engaged in self-teaching, exploration, play and recreation with mathematics throughout recorded history. In the 20th century, these activities were supported by printed guides, games, puzzles, and 3D manipulables including the wildly popular Rubick’s Cube (at right) (Wikipedia, 2025). Mathematician [Martin Gardner](https://en.wikipedia.org/wiki/Martin_Gardner) contributed a regular "Mathematical Games" column to *Scientific American* magazine for over 25 years, and penned over 100 books, many devoted to recreational mathematics, with titles like *Mathematics, Magic and Mystery*, *Hexaflexagons and Other Mathematical Diversions*, and *Aha! Gotcha: Paradoxes to Puzzle and Delight *(Wikipedia, 2025).

In the 21st century, self-directed engagement with exploratory, playful and recreational mathematics moved online, supported by many blogs and audio or video series including:



* [Cut-the-Knot](https://en.wikipedia.org/wiki/Cut-the-Knot) by [Alexander Bogomolny](https://en.wikipedia.org/wiki/Alexander_Bogomolny)
* [Futility Closet](https://en.wikipedia.org/wiki/Futility_Closet) by Greg Ross
* [Mathologer](https://youtube.com/@Mathologer) by [Burkard Polster](https://en.wikipedia.org/wiki/Burkard_Polster)
* [The videos](https://vimeo.com/vihart) of self-described “Mathmusician” [Vi Hart](https://en.wikipedia.org/wiki/Vi_Hart) 
* [Stand-Up Maths](https://www.youtube.com/user/standupmaths) by [Matt Parker](https://en.wikipedia.org/wiki/Matt_Parker)
* [Numberphile](https://en.wikipedia.org/wiki/Numberphile) by [Brady Haran](https://en.wikipedia.org/wiki/Brady_Haran)
* [Riddler](https://fivethirtyeight.com/tag/the-riddler/) by Zach Wissner-Gross

Examples of exploring math outside of an academic context, yet still directly useful for academic contexts, include: 



* [3Blue1Brown](https://www.3blue1brown.com/) by Grant Sanderson
* [Euclidia](https://www.euclidea.xyz/) (and its social media accounts)

Edge case where “fun” and academia come together:



* [Michael Penn Math on YouTube](https://www.youtube.com/@MichaelPennMath) (Not even ODEs and PDEs can escape clickbait YouTube thumbnails) 

But while the tools of the past 100+ years offer a rich variety of present-day opportunities for exploration, learning and fun with math, **there are significant gaps in what is available to support self-directed, exploratory and recreational mathematics engagement:**



* There are many wonderful videos and podcasts, but these **aren’t interactive**, so they don’t directly support learning by playing, doing, exploring or experimenting.

* Interactive puzzles like Rubik's Cubes, Sudoku puzzles and the like are fun, but the math skills involved are decoupled and decontextualized from mathematics as a whole. Plus, these puzzles present the same basic challenge over and over. There's **no opportunity to progress, grow or learn new things.**

* Books, puzzles and games are great for exploring math in a fun, novel way, but **can’t offer dynamic or just-in-time support.** If you get stuck, have a question, or don't know the math you need to be able to keep going, the fun and learning are done.

* Platforms like [Manim](https://www.manim.community/) and [Wolfram Mathematica](https://www.wolfram.com/mathematica/) support mathematics exploration and experimentation, but have high barriers of entry (you have to know a lot to be able to engage with them), and offer little to no guidance on how to follow a learner-generated line of inquiry. 

<br>



---


### Needs Analysis | Interpretation of Findings

Our analysis surfaced plenty of tech-based applications that facilitate goal-oriented math learning, with the goal being to perform and achieve in the current K-12 U.S. math curriculum. We also found that pedagogy and content in the K-12 U.S. math curriculum tends to be quite narrow as a result of assessment and other pressures, and that, by extension, math learning experiences offered by these goal-oriented applications is thus, also, quite narrow. We found a small number of applications that are somewhat more playful, less goal-driven, more focused on conceptual understanding, that seemed more intrinsically motivating than the others. Perhaps this is an emerging market. But their content is overwhelmingly geared toward early math. We found a rich variety of opportunities, both online and offline, for self-guided exploratory learning outside the traditional K-12 math curriculum that is intrinsically motivated/motivating, playful, pleasurable, and can cultivate conceptual understanding. But these can have high barriers of entry, or lack interactability and participatory engagement, effective learner support functionalities, or the ability to progress and grow in one’s learning. Our design intends to respond to the need for a self-guided exploratory learning platform that offers positive experiences with math that have a low barrier to entry and are interactive, offer just-in-time learner support, and the opportunity to progress, grow or learn new concepts and skills in math. 

Now we’ll take a closer look at a few AI-assisted math learning applications to see what we can learn from them that we might apply to our own design.




---


### A Closer Look at an AI-Assisted Application | *Synthesis Tutor*

The tutor still uses mostly direct instruction, albeit with some nice embedding of reflection questions. It does FEEL more like a guided exploration of mathematics, but it is clearly split into digestible modules that adhere to existing school curricula. There is not really any explorative freedom given to the learner, as most of the learner inputs are restricted to clicking a pre-made response, usually 1 of 2 or 3 responses. The only thing “AI” about this tutor appears to be the voice over. All other instructional elements could be mapped using a decision tree (Eg: correct response leads to a response and incorrect leads to some other response). 

The manipulatives are nice, especially the hammer tool in the fractions module. But these manipulatives do not give much learner freedom. The consistent design choices towards restriction of learner actions is age appropriate and makes sense given that the goal of this tutor is to help with school math.



---


### A Closer Look at an AI-Assisted Application | *Khanmigo*

Marketing materials for Khan Academy’s “AI-powered tutor” *Khanmigo* evince the same basic goal orientation and market positioning as standard Khan Academy materials. But their marketing vignettes also show how Khanmigo uses newly-available affordances of AI chatbots to model and scaffold learner attitudes and behaviors shown to enhance learning. For example, self-talk that cultivates and sustains a growth mindset (Boaler, 2024). 

Providing learners with the opportunity to customize the Khanmigo avatar simultaneously leverages affordances for sociocultural design (Tam & Pawar, 2020) and offers a gamification opportunity - by participating in learning activities, learners earn points they can exchange for greater customization options.


---


### A Closer Look at an AI-Assisted Application | *ChatGPT “Study Mode”*

We tested 2 difficult use cases for study mode: geometric constructions and introduction to the derivative. We also tested two different levels of math competency, low and high. These levels were directly communicated to ChatGPT prior to the study session. These highly visual forms of mathematics were incredibly difficult to communicate to ChatGPT. For constructions, there was no differentiation between high and low level math competency. In fact, ChatGPT gave the choice to start with harder constructions for the low level learner, whereas the high level learner was not given that choice. The low level learner was then walked through the construction with A LOT of intermediate check-ins. The instructional method was full DI. When we attempted to ask a what if question, ChatGPT lost where it was in the construction, assuming that the what if question was a different, but more common what if question. 

For the high level learner, ChatGPT decided to check-in a lot less. It also had multiple errors, requiring us to run the inquiry again. We also tested putting in a solution step that sounded correct but was not, and ChatGPT treated it as a correct step, congratulating us on a job well done. 

For intro to derivatives, we decided to use one of the GPTs available on ChatGPT: IB Math Tutor: AA SL Edition By [ibmind.ai](http://ibmind.ai). It was hard (nearly impossible) to get the tutor to move away from academic definitions (probably by design). When asked to teach us what a derivative was, the tutor stuck to algebraic definitions mostly. Again, the instructional method was full DI. When asked to generate a diagram, it was incomprehensible (too much information, none of which was labeled). 


### 

<br>

---


### How *MathSparkPlay* Functions

<br>

As a user, your primary interaction with MathSparkPlay is **text chat**. You might begin by posing a question or asking to explore a domain within mathematics. If you did this with a standard chat bot, such as Gemini Study Mode, you might get something like this…


Like most existing chat bots, Gemini simply answers your question. This is useful, but not particularly recreational. There’s not much fun in simply asking questions and getting answers. Nor is this kind of activity optimal for learning. It *is* learner-directed - the learner is charting the path, led by their own questions and interests. But the process is missing key attributes of effective exploratory learning that are also key to intrinsic motivation and reward systems 



* Discovery, experience, hands-on-ness
* Choice-making
* Mistake-making
* Multiple solutions

MathSparkPlay, by contrast, DOES NOT directly give the information. Instead, it asks a few questions to gauge what related information the user may already know, then asks guiding questions that help the user make inferences and connections, encouraging them to identify, apply or extend what they may already know to the new concept they wish to explore. As the user responds, the bot affirms any correct inferences and offers new guiding questions to help redirect incorrect ones. 

Text exchanges with MathSparkPlay help users “mentally unpack” what they may already know and apply it to the new query-situation, supporting connection- and inference-making that gets them closer and closer to their goal. This process of *mathematical reasoning* is undergirded by a set of attitudes (I can do this, I like math, I am a math person) and skillsets (“math sense” or “number sense”, logical thinking, self-reflexive learning) that are cultivated and trained while using MathSparkPlay. The process of mathematical reasoning involves some disequilibrium - uncertainty, unknowns, ambiguity. Disequilibrium is shown to be beneficial for math learning (CITE!), and can actually be *fun* in the right context. Video game play, for example, is full of uncertainty, unknowns and ambiguity, which is part of the appeal. But in other contexts, disequilibrium can be distressing and damaging - for example, when one’s disequilibrium is discoverable in a social context or setting like a classroom or a tutoring session. A well-designed chat bot offers the opportunity to preserve playful disequilibrium in a context that still provides presence and support. As chat bot interactions create an illusion of reciprocity, they are undeniably parasocial. Considering this social context, our bot’s communications should be warm and encouraging. But they should also be quite simple, sparse, and neutral. This “lack of noise” reduces cognitive load for the user, affording more bandwidth for recall, reasoning, and the building of new mental models.



Other elements of the MathSparkPlay interface help support various aspects of the user experience:



* **Visual Display:** Supports the user’s emerging understanding of the specific concept(s) under discussion by displaying any relevant or clarifying visuals.
* **Resources:** Links to related resources are shared here for the user to explore to beyond their MathSparkPlay session.
* **Concept Map** (not shown): As the learner begins to construct new mental models from the information and insights they gain via the text exchange, MathSparkPlay relates and connects these to the broader world of mathematics by beginning to build a concept map of mathematics originating with the current query. It starts with a detail-view, showing where the current query sits in that web and a few of the surrounding nodes. As the user returns and logs more inquiry sessions, this map will build, extend, and connect the new areas covered, showing the user…
    * How all of mathematics is related
    * “Neighbor” concepts, that may add context and meaning to the current exploration
    * Motivation to explore in more areas and build the map further
    * A sense of relationship and belonging in the world of mathematical practice.

<br>

---



 ### References:

Boaler, J. (2024). Transforming Mathematics Education Through Mindset-Based Teaching. Stanford Graduate School of Education. [doi.org/10.33548/SCIENTIA1000](http://doi.org/10.33548/SCIENTIA1000)

[https://www.youcubed.org/wp-content/uploads/2024/09/Scientia-article.pdf](https://www.youcubed.org/wp-content/uploads/2024/09/Scientia-article.pdf)

Deutsch, M. (2017, Jan 9). *M2M Day 69: Decoding Rubik’s Cube Algorithms*. Medium. [https://medium.com/@maxdeutsch/m2m-day-69-decoding-rubiks-cube-algorithms-6ea7e7704ec9](https://medium.com/@maxdeutsch/m2m-day-69-decoding-rubiks-cube-algorithms-6ea7e7704ec9)

Jimenez, L. & Modaffari, J. (2021, Sep 16). Future of Testing in Education: Effective and Equitable Assessment Systems. Center for American Progress. [https://www.americanprogress.org/article/future-testing-education-effective-equitable-assessment-systems/](https://www.americanprogress.org/article/future-testing-education-effective-equitable-assessment-systems/)

LeBlanc, G. (2025, June 11). 551. The Math Mindset and How to be Math-ish feat. Jo Boaler. [YouTube Video]. unSILOed Podcast. [https://www.youtube.com/watch?v=kq4YXpWUTRo](https://www.youtube.com/watch?v=kq4YXpWUTRo)

Leyva, E., Walkington, C., Perera, H., Bernacki, M. (2022). Making Mathematics Relevant: An Examination of Student Interest in Mathematics, Interest in STEM Careers, and Perceived Relevance. Int. J. Res. Undergrad. Math. Ed. 2022;8(3):612–41. doi: 10.1007/s40753-021-00159-4. Epub 2022 Feb 2. PMCID: PMC8807670.

Maltese A.V. & Tai, R.H. (2017.) Pipeline persistence: Examining the association of educational experiences with earned degrees in STEM among US students. Science Education. 2011;95(5):877–907. doi: 10.1002/sce.20441. 

McMurrer, J. (2007). Choices, Changes, and Challenges: Curriculum and Instruction in the NCLB Era. Washington: Center on Education Policy. [https://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=593580376CAA72933F4BB739B7C12DBD?doi=10.1.1.643.5250&rep=rep1&type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=593580376CAA72933F4BB739B7C12DBD?doi=10.1.1.643.5250&rep=rep1&type=pdf)

NAEP. 2024. NAEP Mathematics Assessment, aka “Nation’s Report Card”, a Congressionally Mandated National Assessment Program. Institute of Education Sciences. [https://www.nationsreportcard.gov/reports/mathematics/2024/g4_8/?grade=8](https://www.nationsreportcard.gov/reports/mathematics/2024/g4_8/?grade=8)

Phelps, R. P. (2016). Teaching to the Test: A Very Large Red Herring. *Nonpartisan Education Review* 12 (1). [https://www.nonpartisaneducation.org/Review/Essays/v12n1.htm.](https://www.nonpartisaneducation.org/Review/Essays/v12n1.htm)


Recreational mathematics. (last edited 2025, August 18). In *Wikipedia. *[https://en.wikipedia.org/wiki/Recreational_mathematics ](https://en.wikipedia.org/wiki/Recreational_mathematics)**

**Internal citation within Wikipedia:** Kulkarni, D. [Enjoying Math: Learning Problem Solving With KenKen Puzzles](http://www.matholympiad.info/Documents/TeachingWithKenKen.pdf) [Archived](https://web.archive.org/web/20130801080339/http://www.matholympiad.info/Documents/TeachingWithKenKen.pdf) 2013-08-01 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine), a textbook for teaching with KenKen Puzzles.

**Internal citation within Wikipedia:** [Special Interest Groups of the MAA](https://www.maa.org/community/sigmaas) [Archived](https://web.archive.org/web/20130718123507/https://www.maa.org/community/sigmaas) 2013-07-18 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine) Mathematical Association of America (MAA)

Ryan, R. M., & Deci, E. L. (2017). [Self-Determination Theory: Basic Psychological Needs in Motivation, Development, and Wellness](https://www.google.com/search?sca_esv=bffb88f62265f716&rlz=1C5CHFA_enUS534US534&cs=0&q=Self-Determination+Theory%3A+Basic+Psychological+Needs+in+Motivation%2C+Development%2C+and+Wellness&sa=X&ved=2ahUKEwjvkNb48IuQAxW_K1kFHScUMlMQxccNegQIGxAB&mstk=AUtExfD7MahJTtxx3rxkyS7Bcp55dOUKtiMXfItkXFU_dwXOVizQPEy8X1x3mLFZyb2cQGJD6up6JnrcpEmuXHn-JCMZJbwfPYJykbf1bpjOSe_Vr4jDPnp5gQ9XMhI-N5jS2e702FHzV5dFun5ON9C3ev2pvmsoZCy08L1W_kUZ04VFfTMVggrN1P_NUlKOFz5AaJ1w&csui=3). New York: Guilford Press. [SCIRP Open Access](https://www.scirp.org/reference/referencespapers?referenceid=2531959) 

Samuelsson, J. (2021). Developing students’ relationships with mathematics. *Educational Action Research*, *31*(2), 180–194. [https://doi.org/10.1080/09650792.2021.1899012](https://doi.org/10.1080/09650792.2021.1899012)

Schwartz, H., Bozick, R., Diliberti, M. K., Ohls, S. (2025, June 17). Students Lose Interest in Math: Findings from the American Youth Panel. Rand Corporation. Funded by the Gates Foundation. [https://www.rand.org/pubs/research_reports/RRA3988-1.html](https://www.rand.org/pubs/research_reports/RRA3988-1.html)

Schwartz, S., (2024, November 25). *Which Nation’s Students Are Defying the Math Anxiety Trend?*. Education Week. [https://www.edweek.org/teaching-learning/which-nations-students-are-defying-the-math-anxiety-trend/2024/11#:~:text=By%20Sarah%20Schwartz%20%E2%80%94%20November%2025,Canada%20who%20studies%20mathematical%20thinking.](https://www.edweek.org/teaching-learning/which-nations-students-are-defying-the-math-anxiety-trend/2024/11#:~:text=By%20Sarah%20Schwartz%20%E2%80%94%20November%2025,Canada%20who%20studies%20mathematical%20thinking)

Schwartz, S., (2024, December 4). *‘Sharp, Steep Declines': U.S. Students Are Falling Behind in Math and Science*. Education Week. [https://www.edweek.org/leadership/sharp-steep-declines-u-s-students-are-falling-behind-in-math-and-science/2024/12](https://www.edweek.org/leadership/sharp-steep-declines-u-s-students-are-falling-behind-in-math-and-science/2024/12) 

Smith, J., Fotou, N., & Sharpe, R. (2025). Changes in mathematics anxiety and mathematics confidence. *International Journal of Mathematical Education in Science and Technology*, 1–19. [https://doi.org/10.1080/0020739X.2025.2475928](https://doi.org/10.1080/0020739X.2025.2475928) 
[https://www.tandfonline.com/doi/full/10.1080/0020739X.2025.2475928#d1e127](https://www.tandfonline.com/doi/full/10.1080/0020739X.2025.2475928#d1e127)

Tam, F. & Pawar, S. (2020) Emerging Design Factors in Game-Based Learning: Incentives, Social Presence, and Identity Design. In J.L. Plass, R.E. Mayer, and B.D. Homer, (Eds.), [Handbook of Game-based Learning (https://mitpress.mit.edu/9780262043380/handbook-of-game-based-learning/), pp. 153 - 176. Cambridge: MIT Press.
