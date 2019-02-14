---
Title: Project Requirements
Author: Neil Ernst 
---

# Overview
The course project is a semester long effort to apply the ideas behind code reading and communication to a realistic project.

Your team gets to choose the project you will work on (subject to some restrictions). In general the project must be *active* (daily commits), *moderately large* (>100 stars on GH, but not intractably complex), and *open-source*. Since other teams have done this type of course, you cannot select from the [banned project list](https://github.com/SENG480-18/course/blob/master/banned.md). This is to avoid annoying hard-working and under-compensated OSS maintainers.  

## Dates
See [the syllabus for all due dates](https://github.com/SENG480/course/blob/master/README.md). 

## Milestones

- **M0.** team formation and Github (0%, -10 if not done)
- **M1.** identify project stakeholders and business goals (5%). Report on project ethics and privacy. (5%) 
- **M2.** identify architecturally significant requirements and utility tree (10%)
- **M3.** module view (20%)
- **M4.** C&C view (20%)
- **M5.** assess project code quality and technical debt (15%)
- **M6.** present report in class, deliver final chapter proof-edited and well organized (5%)
- **M7**: using your knowledge of the project, submit a pull request that improves the project. (20%)

## Teams

- Instructor assigned - see Slack
- If you are having trouble with your team (lazy group members, poor communication, technical trouble, etc.) **come see me or Omar as early as possible**. We cannot help you if you don't let us know. Telling me in April that the team was not effective will not be an excuse.
- A regular meeting schedule is highly recommended to keep everyone on track. You might want to follow a [Scrum style standup](https://www.mountaingoatsoftware.com/agile/scrum/meetings/daily-scrum): each team member says:
    -   What did you do since last meeting?
    -   What will you do before the next meeting?
    -   Are there any impediments in your way?
- You can organize how you wish, but everyone must contribute, and one person should be in charge of overall planning. 

All students are expected to participate equally in discussions, design and development. The instructor will make marking adjustments for individual students where this participation has not occurred; this may result in a failing grade for the project. At the mid-point and conclusion of the project you will be asked to evaluate your colleagues on the team. Your peer review score and participation on Github/Slack will strongly influence what percentage of the project mark you get. 

# Formats and Logistics
The final team deliverable is a *book chapter* that we will publish on [Gitbook](https://www.gitbook.com/). Gitbook accepts both Markdown and ASCIIdoc; both of these are described on [the Gitbook help pages](https://toolchain.gitbook.com/structure.html). You will write the submissions in a Github team repository with standard text editors. Markdown and ASCIIdoc editors are also plentiful. I like [Byword](https://bywordapp.com) and [Marked](http://marked2app.com). 

Your final presentation will be an architecture presentation, of the system you chose, to the entire class. Keynote/Powerpoint etc are suitable here. 

# Milestones
Note that since we are *documenting and communicating*, good technical writing practices (spelling, grammar, organization, clarity) are always required and will be subject to lost marks if not followed. You can always reach out to the [Center for Academic Communication](https://www.uvic.ca/learningandteaching/home/home/centre/index.php) if you need extra assistance.

## 0. Github (-10% if not done)
### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
- Create a repository using the Github Classroom link
- send your Github IDs to Omar
- update the Readme with your team's name, and 3 projects of interest.

### Marking Guide
Simple. Do the above.

## 1. Identifying project stakeholders and business goals (5%). Privacy and ethics report (5%).
This deliverable will serve as an introduction to the project you have chosen to focus on. You will read project documents and related material (e.g., StackOverflow) to get a sense for who the stakeholders are, and what the project wants to accomplish. Use your judgment, plus available sources, to create a plausible set of stakeholders and business goals. NB: Since we don't have direct access to the stakeholders, our business goals are necessarily a guess. But it should be an informed guess.

After that, you will examine project policies around privacy, security and ethics, and write a 2 page summary of this. Use the [ACM Code of Ethics](https://www.acm.org/code-of-ethics), assess how the system you are studying currently complies with this Code, and identify places where future ethical conflicts may arise. 

### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
1. Identify stakeholders for the system you chose. Complete a [stakeholder profile table](https://www.viewpoints-and-perspectives.info/home/stakeholders/), and explain why those people/job titles are stakeholders for that role.
2. Create a list of at least 5 business goals (see chap 16) for this system. We will use those in M2 as well.
3. 2 page report on privacy and ethics concerns for this project:
   1. Title
   2. Introduction
   3. Potential Privacy and Security COncerns
   4. Ethical Dilemmas
   5. Summary
   6. Sources (issue tracker discussion, wiki/web pages, commit comments, media reports). 


### Marking Guide	
- completeness and relevance of stakeholders.
- properly thought out business goals, based on empirical data (project docs, tech pubs, etc.)
- proper formatting and references supporting concl	usions
- evidence of critical assessment of possible ethical dilemmas

## 2. Architecturally significant requirements (ASRs) and utility tree (10%)

### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
1. The list of ASRs
2. A fully worked out utility tree, with at least 7 prioritized quality attribute scenarios, 3 (of the 7) in template form.

### Marking Guide
- Relevance of the ASRs to the project. 
- Appropriateness of scenarios.
- Quality of scenarios.

## 3. Module View (20%)
A [module view](https://github.com/SENG480-18/course/blob/master/lectures/5-modules.md) (see Chapter 18 in the text) describes implementation units of the system. In this milestone, you are to create a software architecture view that shows the module structure of your system. Your deliverable will be a Markdown document that follows the template described in Section 18.6 of the text. 

The purpose of this document is to support analysis of some of the key quality attributes you identified in Milestone 2. The reader will be someone who is not very familiar with the code or project, so be sure to explain it to an interested outsider (e.g. someone who just joined the dev team).

Your deliverable should be laid out and contain material very similar to [this one from the SEI](https://wiki.sei.cmu.edu/sad/index.php/OPC_Module_Uses_View).

### Suggested Steps

1. Identify QAS that pertain to implementation units and responsibilities. Some obvious categories include modifiability, portability, use of 3rd party frameworks.
2. Choose a view type that supports analysis of these QAS. Some of the view types we discussed were Layers, Uses, Data Models (see lecture notes). Others include Decomposition and Generalization (is-a).
3. Create a primary presentation of that view (the main diagram). Remember the key. Please use a tool of some kind to create the diagram. I suggest Visio, Powerpoint, Omnigraffle, or some of the open source alternatives. As you do this create the element catalog describing each element/relation.
4. Outline the context diagram for that view, using the same 'language' (i.e., for a 'uses' diagram, the context shows the external elements 'used').
5. Document the view's key behavioral questions in a [behavior diagram](http://repository.cmu.edu/cgi/viewcontent.cgi?article=1680&context=compsci). For example, you might want to show the way in which login code interacts with a 3rd party authentication framework.
6. Give 2 important interfaces for this view. We have not discussed interface notations yet, so this element **will be for bonus marks**. You can read the [SEI whitepaper for the details](https://resources.sei.cmu.edu/asset_files/TechnicalNote/2002_004_001_13973.pdf).
7. Typically one includes a variability guide, but we will skip this section. A variability guide describes how and why the view might change.
8. Finally, provide at least 500 words of rationale explaining why you think the designers organized the system's modules this way. You should explain this with specific reference to the quality attribute scenarios in M2.

### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
A fully worked module view according to the SEI view templates. Includes interface and behavior documentation. Deliver this as a Markdown document in your repository.

### Marking Guide
- all required sections are present and well-organized. Include a table of contents (see [this tool](https://github.com/jonschlinkert/markdown-toc)).
- view's primary presentation (diagram) is thorough and understandable. This means key elements are labeled, relations are typed, color is used appropriately. Use of UML or other diagram notations is not mandatory. 
- view and element catalog answers key analysis questions implied by QAS (M2).
- behavior diagram is appropriate and clearly answers important questions from the QAS.
- rationale is well-reasoned and any obvious assumptions are documented.

### Relevant Readings
1. [Architecture Reconstruction of J2EE Applications: Generating Views from the Module Viewtype](https://resources.sei.cmu.edu/asset_files/TechnicalNote/2003_004_001_14186.pdf) Liam O' Brien Vorachat Tamarree. 2003. *Describes a case study of generating module views from an existing system*
2. [A7e Case Study](http://www.informit.com/content/images/9780321815736/downloads/Bass_2E_ch03_CaseStudy.pdf). *From the 2nd edition, this case study shows how a module decomposition and uses views can answer QAS questions.* 
3. [SEI example](https://wiki.sei.cmu.edu/sad/index.php/OPC_Module_Uses_View). *A hypertext example of a fully worked out module view (and other parts of the documentation package).*

## 4. Component and Connector View (20%)

Like the module view in M3, choose a C&C view to answer important questions from your QAS in M2. Deliverables will be identical to M3, except your primary presentation will be a C&C view (Pipe-Filter, Client-Server, Service, and so on.) You will also include interface documentation and a short variability guide.

Note in particular the aspects of M3 that you lost marks on. In general, this was typically having a primary presentation that was much too complex; failing to correctly link elements in the Github source code to the diagram; and failing to show how the view can answer key questions in your QAS. Remember, your task is to simplify the details in the codebase so I can understand it.

Focus on a single quality attribute scenario from M2, and make sure your diagram explains that. 
### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
A fully worked C&C view according to the SEI view templates. Includes interface and behavior documentation.

### Marking Guide
Identical to M3.  No bonus marks. Ultimately I need to be convinced your team has a good understanding of important run-time functionality of your system. A good way to do this is to get the system running and trace a simple end-to-end run of core parts of the code. For example, in Toyplot I might walk through a simple tutorial and explain how each component in Toyplot gets called in turn to get a plot displayed. Running tests is another way to simulate this. 

## 5. Code Quality and Technical Debt (15%)
Assess your project's code quality using automated tools like Pylint, FindBugs, CppLint, Sonarqube, CodeScene. The last two are more tricky to configure so start early. Then write a report documenting what you have found, and any possible technical debt the project might be facing.

### Suggested steps
By now you ought to have a good grasp of the internal structure of your projects, and some idea of what exactly its architecture is. Recall from class lectures that *technical debt* reflects the short-term decisions with potential high longer term costs.

1. Run one of the tools suggested above; feel free to find a different one (but let me know). 
2. Search the project's issue tracker looking for shortcuts; good keywords include "technical debt" and "tradeoff". You can likely think of others.
3. Search the project's code for instances of "Fixme", "Hack", etc. Keep in mind, however, that we are really looking for *design* flaws, not just bad coding practice.
4. Have one or two team members report on the code quality tool report. Read the report, and summarize what you find. This should be prepared as though you were giving a 10 min summary to an executive. 
5. Other team mates should combine the output of steps 2/3 and their knowledge of the design from previous milestones, in order to report on possible design problems due to technical debt. Make sure your reporting uses evidence from the code/issues/other docs to make the case. Nearly every project maintainer would love more time to just refactor the codebase, so figure out where they would spend that time.

### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
1. Code quality report. Include the output of the tool, plus your summary of the results.
2. Based on your architecture documents, analyze potential technical debt in the project. Report at least 2 potential shortcuts or design tradeoffs that might have long-term consequences.

### Marking Guide
- insightfulness of your analysis
- plausibility of the design debt you identified
- 2% project bonus for using SonarQube and pointing me to a Sonarqube instance

## 6. Final Presentation and Report  (10%)
In class presentation of ~15 minutes; final report polished and cleaned up (e.g. add introduction, conclusions, references). Not everyone needs to present, but everyone needs to work on the milestone.

### Presentation Schedule
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Presentation Outline
* Introduction (1-2 minutes)
	- Business goals, elevator pitch to set context and why its cool
* QAS (1-2 minutes)
	- QA, scenarios, present utility tree here
* Technical content (7-8 minutes)
	- Brief technical overview: explain what language it is written in, key drivers and constraints
	- Implementation/ module view (M3)
	- C&C View (M4)
* Technical Debt and Quality (1-2 minutes)
* Reflection (1-2 minutes)
	- Challenges
	- What worked well
* Questions

### Other aspects to keep in mind
* Audience: technical people
* VGA adaptor
* Projector not widescreen

### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
Use the GitBook toolchain to ensure your chapter compiles to something readable on the site. 

Presentation must be attended by all group members, all of whom may be asked questions about the project.

### Marking Guide
* Presentation organization
* Presentation competently run
* Presentation on time.
* Report compiles to PDF/Gitbook
* Report has all necessary sections.
* Report has fixed comments from previous submissions.

## 7. Pull Request (15%)

### Deadline
See [the syllabus](https://github.com/SENG480/course/blob/master/README.md). 

### Deliverables
Link to a pull request for your case study, showing an improvement. The PR does not need to be accepted.

### Marking Guide
Silly or trivial pull requests will lose marks. It does not have to be complex, but does have to demonstrate you understand the project and are not just annoying the maintainers.

# Helpful Links
* [Student's Guide to SE projects](http://www.cdf.toronto.edu/~csc301h/fall/csc301.pdf) 
* [Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [GWT](http://www.gwtproject.org/doc/latest/tutorial/index.html)
