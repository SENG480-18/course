---
Title:  Documenting and Understanding Software Systems
Subtitle: CRN 2366{2,3,4} - SENG 480A/CSC485A/CSC578A - A01
Author: Neil Ernst
---

# Schedule and Topics - Spring 2019

The following schedule is subject to change, and will change.

| Module | Topics | Other Resources | Readings  | Deadlines |
| ------ | --------------------------------------------------------- | --------- | ---------------- |------- |
| | Intro; introductions; Project outlined. [What is Software Architecture](https://github.com/SENG480/course/blob/master/lectures/1-intro.md)? | | text chapter 1 | |
| | [Software arch overview](https://github.com/SENG480/course/blob/master/lectures/2-arch.md). | | text chapter 2 | |
| | Omar - Github/Git tutorial || |
||  Group project meetings (in class) || |
| | [Reading Code.](https://github.com/SENG480/course/blob/master/lectures/3-reading.md) | | chapter 3 text, source code of [web crawler]( https://github.com/aosabook/500lines/tree/master/crawler/code) | | 
| | [Architecture Stakeholders and Requirements](https://github.com/SENG480/course/blob/master/lectures/4-req.md). | | text chapter 16  | **M0 due** |
| | Guest lecture - Dr. Rick Kazman  |||
| | [Views on Architecture - Modules](https://github.com/SENG480/course/blob/master/lectures/5-modules.md) | | text chapter 18 | **M1 due Feb 3** |
|| [Views part 2 - C&C](https://github.com/SENG480/course/blob/master/lectures/6-cc.md) | [SEI view example](https://wiki.sei.cmu.edu/sad/index.php/OPC_Module_Uses_View) | text chapter 4 | | 
|| [Architecture and Design](https://github.com/SENG480/course/blob/master/lectures/7-design.md) | [What is Architectural Design](http://www.informit.com/articles/article.aspx?p=2738304&seqNum=2) | text chapter 17  |  | |
|  | | | |**M2 due**||
| | Project & assignment working session || |
| | | | | Grad students send in proposed topic. Undergrad  **A1 due** |
| | [Documenting behavior](https://github.com/SENG480/course/blob/master/lectures/8-behavior.md)  | | [SEI behavior tech report](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=5847) | || |
| | Midterm | | | **Midterm** |
||  [API and Interface documentation](https://github.com/SENG480/course/blob/master/lectures/9-interfaces.md).  | | [Interface documentation](https://resources.sei.cmu.edu/asset_files/TechnicalNote/2002_004_001_13973.pdf) |   |
| | [Architecture analysis](https://github.com/SENG480/course/blob/master/lectures/12-analysis.md) | | ch 21 **M3 due ** |
|| [Documenting Ops](https://github.com/SENG480/course/blob/master/lectures/13-ops.md)  | | <!--RW text has chap 21 ; allocation views; Len's book -->  |  |
| |  [Technical Debt and Metrics](https://github.com/SENG480/course/blob/master/lectures/10-td.md) | | my [Field Study of TD](https://insights.sei.cmu.edu/sei_blog/2015/07/a-field-study-of-technical-debt.html) • [metrics and TD](https://almossawi.com/firefox/prose-part-two/) | **M4 due Mar 17**|
| | [Human-centric docs](https://github.com/SENG480/course/blob/master/lectures/11-review.md) | | [A Structured Approach for Reviewing Architecture Documentation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.645.6497&rep=rep1&type=pdf) | | | 
| | [Microservice styles; the latest research](https://github.com/SENG480/course/blob/master/lectures/14-new.md) | | | **M5 due Mar 24** |
| | Doc Exercise in class | | | |
| | In class Project presentations: groups  2, 3, 7, 8, 11 | |
| |  In class Project presentations: groups 1, 4, 6, 9, 10, 13 | | |  |
|  |  no class  || |
|  | || | **M6 and M7 due in repo** | 
|  |  ||| **Grad assignment due** |

# Syllabus
Software is a long-lived and complex thing. This course is about understanding software in the large. We use the SEI text as a framework for understanding large-scale software systems. Topics include

* what is architecture? Who are architects?
* what structures are important to understand?
* views on software systems
* software quality attributes
* architecture analysis and recovery
* architecture-driven design
* agile architecture
* design, architecture, and technical debt

(the official course syllabus is [distributed via HEAT (SENG480a link)](https://heat.csc.uvic.ca/coview/outline/2018/Spring/SENG/480A))

## Recommended/Required Text:
SEI Software Architecture in Practice, Len Bass, Paul Clements, Rick Kazman. 3rd Edition. 2013.

### Other texts
* Design It! From Programmer to Software Architect, by Michael Keeling, Pragmatic Programmers 2017.
* Just Enough Software Architecture, by George Fairbanks, Marshall and Brainerd, 2010.
* Documenting Software Architectures, by Paul Clements et al., Addison-Wesley, 2011.
* Designing Software Architecture, A Practical Approach, by Humberto Cervantes and Rick Kazman, Addison-Wesley 2017.
* Software Systems Architecture: Working with Stakeholders Using Viewpoints and Perspectives, by Nick Rosanski and Eoin Woods, Addison-Wesley, 2011.
* Applied Software Architecture, Christine Hofmeister, Rod Nord, Dilip Soni, Addison-Wesley, 2000. 
* Essential Software Architecture, by Ian Gorton, Springer, 2011.
* Software Architecture: Perspectives on an emerging discipline, Mary Shaw and David Garlan, Prentice-Hall, 1996.
* Architecture of Open-Source Applications, Amy Brown and Greg Wilson, eds. http://aosabook.org

## Past versions:

* last semesters of this course (see tag Spring18,Spring19)
* DelftSWA: https://delftswa2018.github.io/assignment/
* past deliverables, similar in form to what this course will produce,  from the TU Delft IN4315 course, are available at https://delftswa.github.io and https://www.gitbook.com/@delftswa. These are both modeled on the AOSA book -- http://aosabook.org

## Instructors

* [Neil Ernst](http://neilernst.net), instructor. Office ECS 560, office hours after class Thursday or DM me.
* Omar Elazhary, teaching assistant

# Course Overview

After the course, students are able to:

* begin to reason about and evaluate software design tradeoffs
* capture software architecture in modern documentation approaches
* work together in teams, with modern software tools.
* use a views and beyond approach to capture software architecture.
* compare and contrast different architectural styles, including product lines, microservices, MVC.
* explain and recognise technical debt.

# Deliverables
The class will use [Github](https://github.com/SENG480) and [Slack](https://seng480.slack.com) to work on the project. Students will have to register their Github username (either a permanent one or a throwaway) with the instructors. Those with an objection to using Github please contact the instructor for workarounds. All Github activity is private to the class organization. Please see the privacy notice on the Connex site.

[Slack](https://seng480.slack.com) will be the primary mechanism used for communication in the class. My rationale (apart from being tools used in practice) is to expose the class as a whole to questions about projects, assignment, and lectures. 

University and department policies on professional conduct and integrity are applicable. In particular, [sexualized violence](https://www.uvic.ca/sexualizedviolence/policy/index.php) and [harassment](https://www.uvic.ca/equity/discrimination-harassment/index.php) will not be tolerated. Feel free to see me in person, or via UVic email, for personal questions.

## Overview
The final mark is weighted as following:
- 15% assignment, 
- 25% midterm
- 10% participation,
- 50% substantial group project

### Participation
Participation is worth 10% - demonstrated by:
- activity on Slack, 
- contributions (and attendance, natch) in class. 
- Send Slack and Dr. Ernst a reading on software architecture and software comprehension. This can include blog posts, lengthy twitter chains, new books, Youtube videos, or podcasts.
- Participate in the in-class exercise, optionally as part of the study.
- Participation in the project is marked separately.

## Assignment Undergrad
*Undergrads*: One individual assignment worth **15%** of final mark. Due date as above. 

For some project on Github, pick a quality attribute, create a (fully developed) quality attribute scenario, and document how the project source code realizes this scenario. Provide discussion on how the project can handle changes in this scenario in the future.

Details are in [assn1.md](assn1.md).

## Assignment Grad
Value: **15%**. Due end of term, as shown above.

Details are in [assn2.md](assn2.md).



## Group Project
The primary deliverable is a group project. You and your team will select a software project (OSS on Github/Bitbucket), and document important views on the software. The end result will be a set of documentation about the software system and a deep understanding of how it is constructed. **50%** of final mark. Students will be assigned to teams and document an open source software system. Due dates in calendar above. See [the Project outline](https://github.com/SENG480/course/blob/master/project.md).

*Nota Bene*: your individual mark in the project will be adjusted, possibly significantly, based on instructor assessment of your effort and peer reviews.

## Midterm
One midterm, worth **25%**. Scheduled as above.

## Final
No final.


