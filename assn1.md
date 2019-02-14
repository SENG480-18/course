---
Title: Undergraduate Assignment handout
Author: Neil Ernst
---
Due: **Thurs, Feb 14 11:59pm** as a Github commit. We mark the last commit unless told otherwise.

Note:

* Assignments are to be completed individually.
* Format your submission as a PDF document. Note that tools such as Pandoc allow you to write in Markdown (i.e. what this document was created in) and "compile" your text to a PDF.

## Presentation Guidelines

* marks will be deducted if not followed
* First page should be a cover page that indicates your name and student number, title of your project, <strike>problem statement for the project</strike> (edit: not necessary) and a table of contents for the document.
* Include page numbers, i.e. 1 of 10 and your name 
* Include clear section headings that match the assignment description (e.g. “Part A: Domain model and glossary”)
* For each section, include a short introductory paragraph explaining the section content (e.g. "in this section I describe the 10 most important requirements for the client. For each requirement I include information such as ... ").
* We are reading code; like in English, support your assertions with reference to specific lines of code or chunks of code. Cite this using hyperlinks. For example, "ActionView's [prepare_context](https://github.com/rails/rails/blob/7ca3ab415d409ba39b07ff5a96da06d68098069b/actionview/lib/action_view/context.rb#L22) method has a potential buffer underflow problem"

# Overview
For one of the projects in the course, pick a quality attribute, create a quality attribute scenario, and document how the project source code realizes this scenario. Provide discussion on how the project can handle changes in this scenario in the future.

# Objectives
* Read more code!
* Map quality attributes onto source code and vice versa.
* Learn about code that can tolerate change and uncertainty.
* Practice architecture analysis and refactoring.

# Requirements
1. Choose a [Project](https://github.com/SENG480-18/course/wiki/Project-Group-Mapping) (not your own)
2. For that project, pick one of the following quality attributes, and create a simple scenario for it. I have provided some detail, but you should make it clear who creates the stimulus, what the response and response measure could be. In some cases (e.g. time to deploy) you will not be able to find the *actual* values, so make a reasonable guess (2 days is likely too slow; 10 minutes is too quick).
	  1. **Maintainability** - Time required to deploy to production. This requires examining the project's DevOps and CI infrastructure.
	  2. **Performance** - Latency. This requires understanding the project's performance goals, picking a good latency measure, and showing how the code supports that.
	  3. **Security** - Intrusion Detection. How has this project prepared to detect intruders. Keep in mind intruders are well equipped with counter-measures.
	  4. **Modifiability** - Time required to make change, test it, and commit it. Requires knowledge of module dependencies and project test plans.
	
3. Once you have your scenario, play architecture consultant. Pretend that you have been called in to advise the development team whether or not the current architecture meets the scenario. Document your findings with an appropriate view and surrounding documentation.
4. Most of the scenarios we've covered in the course are "use case scenarios". These are the basic, normal operations/functionality scenarios. It is also useful to consider "growth scenarios", that is, scenarios that test what happens if the system experiences growth (e.g, moves from 1000 requests per second to 100,000 requests.) [^other] Building on the use case scenario you chose above, construct a reasonable growth scenario (you can 'ratchet' the use case scenario if you wish) and explain where and how the code base will handle this change.

> For example, if my growth scenario is "users double in one year", I can show that our deployment infrastructure is managed by Chef/Puppet/Kubernetes etc. in order to say this scenario is manageable.

# Deliverables
1. Introduction describing the project you chose
2. Detailed use case QAS (chosen from 4 above) complete with project specific stimulus, response/response measure.
3. Expansion of QAS for growth; indicate what aspects change (response measure for example).
4. For each scenario (use case and growth):
	1. Introduce your approach to code investigation: where did you start, what views were necessary
	2. Present <s>one view</s> one diagram showing/tracing how the code (as-is) handles/doesn't handle the scenario. <font color="red">Include a key.</font>
	3. Text that explains the diagram; explains what elements are present; and a causal chain explaining your reasoning for concluding how well the architecture handles that scenario. Link to specific code elements. <font color="red">There is no need to follow the [view template](https://github.com/SENG480-18/course/blob/master/lectures/6-cc.md#representing-views) in the assignment---that is part of the project instead.</font>

# Hints
<font color="red">Remember we are interested in answering a question. Here, the question is some version of "How well does our current design support this scenario". Start by refining the scenario for your project to a specific response measure. Then draw a diagram that will help answer the question. Don't worry about making the diagram conform to a view style just yet. Finally, your diagram should be specific to this particular scenario. But don't forget to include important context (e.g., if you are talking about deployability, mentioning AWS would be relevant).</font>

[^other]: The third type of scenario is "exploratory", where we test unanticipated changes to the system, e.g. the Netflix Chaos Monkey approach.
