---
title: "Become a champion of open (data) science"
teaching: 30
exercises: 60
topics:
- "The Crisis of Confidence"
- "Open and Reproducible Research Practices"
- ""
objectives:
- "To understand the importance to share data and code"
- "To value code and data for what they are: the true foundations of any scientific statement."
- "To promote good practices for open & reproducible science"

keypoints:
- "Make your data and code available to others"
- "Make your analyses reproducible"
- "Make a sharp distincion between exploratory and confirmatory research"
---

## The Crisis of Confidence

The crisis of confidence poses a general problem across most empirical research disciplines and is characterized by an alarmingly low rate of key findings that are reproducible (e.g., Fidler et al. [2017](https://academic.oup.com/bioscience/article-abstract/67/3/282/2900173); Open Science Collaboration, [2015](https://science.sciencemag.org/content/349/6251/aac4716.short); Poldrack et al., [2017](https://www.nature.com/nrn/journal/v18/n2/abs/nrn.2016.167.html); Wager et at., [2009](https://www.sciencedirect.com/science/article/pii/S1053811908012111)). A low reproducibility rate can arise when scientists do not respect the empirical cycle. Scientific research methods for experimental research are based on the hypothetico-deductive approach (see e.g., de Groot, [1969](https://books.google.nl/books?hl=en&lr=&id=6hiBDwAAQBAJ&oi=fnd&pg=PR5&dq=de+groot+methologie&ots=GR5-EAw6pB&sig=Ej1MJgvsN1bHiQHio__ibrO4fkA&redir_esc=y#v=onepage&q=de%20groot%20methologie&f=false); Peirce, [1878](https://www.taylorfrancis.com/books/e/9781315823126/chapters/10.4324/9781315823126-7)), which is illustrated in Figure 1.


{% include figure.html url="../img/EmpiricalCycle.jpg" description="<strong>Figure 1.</strong> The two stages of the empirical cycle; after the initial stage of creative discovery and hypothesis generation (illustrated in the right panel), researchers test their hypotheses in a statistical context of justification (illustrated in the left panel). However, scientists fool themselves, if they test their new predictions on old knowledge and old data (dotted line)." %}


The empirical cycle suggests that scientists initially find themselves in "the creative context of discovery", where the primary goal is to generate hypotheses and predictions based on exploration and data-dependent analyses. Subsequently, this initial stage of discovery is followed by "the statistical context of justification". This is the stage of hypothesis-testing in which the statistical analysis must be independent of the outcome. Scientists may fool themselves whenever the results from the creative context of discovery with its data-dependent analyses are treated as if they came from the statistical context of justification. Since the selection of hypotheses now capitalizes on chance fluctuations, the corresponding findings are unlikely to replicate.

This suggests that the crisis of confidence is partly due to a blurred distinction between statistical analyses that are pre-planned and post-hoc, caused by the scientists degree of freedom in conducting the experiment, analyzing the data, and reporting the outcome. In a research environment with a high degree of freedom it is tempting to present the data exploration efforts as confirmatory (Carp, [2013](https://www.frontiersin.org/articles/10.3389/fnins.2012.00149)). Kerr ([1998](https://journals.sagepub.com/doi/abs/10.1207/s15327957pspr0203_4), p. 204) attributed this biased reporting of favorable outcomes to an implicit effect of a hindsight bias: "After we have the results in hand and with the benefit of hindsight, it may be easy to misrecall that we had really 'known it all along’, that what turned out to be the best post hoc explanation had also been our preferred a priori explanation."

To overcome the crisis of confidence the research community must change the way scientists conduct their research. The alternatives to current research practices generally aim to increase transparency, openness, and reproducibility. Applied to the field of ecology, Ellison ([2010](https://esajournals.onlinelibrary.wiley.com/doi/full/10.1890/09-0032.1), p. 2536) suggests that "repeatability and reproducibility of ecological synthesis requires full disclosure not only of hypotheses and predictions, but also of the raw data, methods used to produce derived data sets, choices made as to which data or data sets were included in, and which were excluded from, the derived data sets, and tools and techniques used to analyze the derived data sets." To facilitate their uptake, however, it is essential that these open and reproducible research practices are concrete and practical.

## Open and Reproducible Research Practices

In this section, we focus on open and reproducible research practices that researchers can implement directly into their workflow, such as data sharing, creating reproducible analyses, and the preregistration of studies.

### Data Sharing

International collaboration is a cornerstone for the field of ecology and thus the documentation, and archiving of large volume of (multinational) data and metadata is becoming increasingly important. Even though many scientists are reluctant to make their data publicly available, data sharing can increase the impact of their research. For instance, in cancer research, studies for which data were publicly available received higher citation rates compared to studies for which data were not available (Piwowar, Day, & Fridsma, [2007](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0000308)). This is due to the fact that other researchers can build directly on existing data, analyze them using utilize novel statistical techniques and modelling tools, and mine them from new perspectives (Carpenter et al., [2009](https://academic.oup.com/bioscience/article-abstract/59/8/699/256190)).

### Reproducibility of Statistical Results

One of the core scientific values is reprodicibility. The reproducibility of experimental designs and methods allows the scientific community to determine the validity of alledged effects.

The benefit of publishing fully reporducible statistical results (including the reporting of all data preprocessing steps) is that collaborators, peer-reviewers, and independent researchers can repeat the analysis --from raw data and to the creation of relevant figures and tables-- and verify the correctness of the results. Scientific articles are not free from typographical mistakes and it has been shown that the prevalence for statistical reporting errors is shockingly high. For instance, Nuijten et al. ([2015](https://link.springer.com/article/10.3758/s13428-015-0664-2)) examined the prevalence of statistical reporting errors in the field of psychology and found that almost 50% or all psychological articles papers contain at least one error. These reporting errors can lead to erroneous substantive conclusions and influence, for instance, the results of meta-analyses. Most importantly, however, is that these errors are preventable. Through tools, such as `git` and *RMarkdown*, researchers can automate their statistical reporting and produce fully reproducible research papers.

### Preregistration and Registered Reports

A blurred distinction between statistical analyses that are pre-planned and post-hoc causes many researchers to (unintentionally) use questionable research practices to produce significant findings (QRPs; John, Loewenstein, & Prelec, [2012](https://journals.sagepub.com/doi/abs/10.1177/0956797611430953)). The most effective method to combat questionable research practices is preregistration, a procedure to curtail scientists’ degrees of freedom (e.g., Wagenmakers & Dutilh, [2016](https://osf.io/crg29/). When preregistering studies, scientists commit to an analysis plan in advance of data collection. By making a sharp distinction between hypothesis generating and analyzing the data, preregistration eliminates the confusion between exploratory and confirmatory research.

Over the last years, preregistration has quickly gained popularity and has established itself over several platforms and formats. Scientists can now choose to preregister their work either independently —for instance on platforms like https://asPredicted.org or the Open Science Framework (OSF)— or preregister their studies directly in a journal in the format of a Registered Report as promoted by Chris Chambers ([2013](https://science.sciencemag.org/content/348/6242/1422.short)). Currently about 200 journals —including *Nature: Human Behaviour*— accept Registered Reports either as a regular submission option or as part of a single special issue (see https://cos.io/rr/ for the full list).

Preregistration is encouraged in the transparency and openness promotion (TOP) guidelines (Nosek et al., [2015](https://science.sciencemag.org/content/348/6242/1422.short) and represents the standard for the analysis of clinical trials; for instance, in the New England Journal of Medicine —the world’s highest impact journal— the registration of Clinical Trials is a prerequisite for publication.

### Challenges

- Data sharing: ethical concerns (share data that harm others, e.g., lowering property values or private data that are collected, for instance, through satellites); Solution = share anonimized data, policies need to be developed
- Preregistration: Loosing the flexibility to adapt analysis plans to unexpected peculiarities of the data; Solution = data blinding, which is standard practice in astrophysics)
- Reproducibility: Additional costs associated with the time it takes to adequatly annotate and archive the code so that independent researchers can understand and reproduce fugures and results; Solution = reproducible workflow, for instance by working in Git and Rmarkdown

### Potential Exercises on this Topic

Ideas for exercises are taken from [Sarafoglou, A., Hoogeveen, S., Matzke, D., & Wagenmakers, E.-J. (2019). Teaching Good Research Practices: Protocol of a Research Master Course. Psychology Learning & Teaching](https://doi.org/10.1177/1475725719858807). This article describes the full course catalogue of the Research Master course 'Good Research Practices' which is taught at the University of Amsterdam. The description of in-class assignments can be found here: https://osf.io/5xjfh/

Potential in-class assignments are:
- Ivestigate the Transparency of Empirical Articles: https://osf.io/p7xtj/
- Hidden Flexibility in Data Analysis: https://osf.io/y4h25/

## Three messages

If there are 3 things to communicate to others after this workshop, I think they would be:

**1. Data science is a discipline that can improve your analyses**

- There are concepts, theory, and tools for thinking about and working with data.
- Your study system is not unique when it comes to data, and accepting this will speed up your analyses.

*This helps your science:*

- Think deliberately about data: when you distinguish data questions from research questions, you'll learn how and who to ask for help
- Save heartache: you don’t have to reinvent the wheel
- Save time: when you expect there’s a better way to do what you are doing, you'll find the solution faster. Focus on the science.


**2. Open data science tools exist**

- Data science tools that enable open science are game-changing for analysis, collaboration and communication.
- Open science is "the concept of transparency at all stages of the research process, coupled with free and open access to data, code, and papers" ([Hampton et al. 2015](http://onlinelibrary.wiley.com/doi/10.1890/ES14-00402.1/abstract))
- For empirical researchers: transparency checklist (https://eltedecisionlab.shinyapps.io/TransparencyChecklist/)
- Repositories such as the Open Science Framework (https://osf.io/preregistration) offer preregistration templates and the tools to archive your projects

*This helps your science:*

- Blogpost: Seven Reasons To Work Reproducibly (written by the Center of Open Science): https://cos.io/blog/seven-reasons-work-reproducibly/
- Have confidence in your analyses from this traceable, reusable record
- Save time through automation, thinking ahead of your immediate task, reduced bookkeeping, and collaboration
- Take advantage of convenient access: working openly online is like having an extended memory
_ Making your data and code publicly available can increase the impact of research.

**3. Learn these tools with collaborators and community (redefined):**

- Your most important collaborator is Future You.
- Community should also be beyond the colleagues in your field.
- Learn from, with, and for others.

*This helps your science:*

- If you learn to talk about your data, you'll find solutions faster.
- Build confidence: these skills are transferable beyond your science.
- Be empathetic and inclusive and build a network of allies

## Build and/or join a local coding community

Join existing communities locally and online, and start local chapters with friends!

Some ideas:

- [Amsterdam Science Park Study Group Slack workspace](https://join.slack.com/t/scienceparkstudygroup/signup): join this workspace to ask questions and network with other biologists on programming and data analysis topics. [Slack](https://slack.com/intl/en-fr/features) is a collaboration software used mostly by companies that has more than 10 million users worldwide.

- [Amsterdam Science Park Study Group](www.scienceparkstudygroup.info): this local [Mozilla Study Groups](https://science.mozilla.org/programs/studygroups) is regularly organising local training workshops for biologists that are either beginners or more advanced in scientific programming. [A publication describing the intention of these study groups and how to implement them has been published in 2018 in PLoS Biology](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.2005561).

- [RLadies](https://rladies.org/). Informal but efficient communities centered on R data analysis meant to be inclusive and supportive. The [RLadies Amsterdam](https://www.meetup.com/rladies-amsterdam/) chapter is quite active in Amsterdam!

These meetups can be for skill-sharing, showcasing how people work, or building community so you can troubleshoot together. They can be an informal "hacky hour" at a cafe or pub!

## Going further / Bibliography
- [The Replication Crisis in Wikipedia](https://en.wikipedia.org/wiki/Replication_crisis)
- [A special issue in Science on Reproducibility](https://www.nature.com/collections/prbfkwmwvz/)
- [Open Science And Reproducibility: presentation by Alexandra Sarafoglou (PhD student, UvA)](../presentations/OSCA2019_OpenResearchPractices.pdf)

<!---
## Other lessons

### Naming files

Now is a good interlude to talk about naming things.

We are going to take five minutes to talk through [Jenny Bryan's three principles for naming files](https://speakerdeck.com/jennybc/how-to-name-files):

1. machine readable
1. human readable
1. play well with default ordering
--->
