---
layout: post
title: Best practices organizing data science projects
categories: [Data Science]
tags: [Data Science, organizing-projects]
description: BEST PRACTICES ORGANIZING DATA SCIENCE PROJECTS
---

# BEST PRACTICES ORGANIZING DATA SCIENCE PROJECTS

Data science projects imply in most of the cases a lot of data artifacts (like documents, excel files, data from websites, R files, python files), and requires repeating and improving each step, understanding the underlying logic behind each decision.

So, we need to consider,

Reproducibility: most of the cases all the procedures should be executed again in order not just to catch a mistake, but to reproduce the complete procedure, improve and execute again.
More artifacts: images, documents, data, and all those artifacts could be separated in tidy artifacts and working artifacts (many versions until to reach the best version for delivery.)
One of the most important aspects of being productive in any field is staying organized. Moreover, a big part of staying organized is managing files; then there are some practices applicable to data science projects.


## 1. OBJECTIVES FOR A DATA ORGANIZATION

There are several objectives to achieve:

- Optimization of time: we need to optimize time minimizing lost of files, problems reproducing code, problems explain the reason-why behind decisions.
- Reproducibility: There is an active component of repetitions for data science projects, and there is a benefit is the organization system could help in the task to recreate easily any part of your code (or the entire project), now and perhaps in some moment in the future (6 months, 1 year, 2 years …)
- Improve the quality of the projects: organized projects usually mean detailed explanations along the process. During the process of documentation and under the necessity to explain the reason behind each step is more probable find bugs and inconsistencies.


## 2. STARTING A NEW PROJECT: THE BEGINNING

Since the very beginning, it is a good practice to start with a good organization for a data science project, and instead of considering that as a waste of time, we can see that as a savvy approach to saving times in different ways.

The next ideas are that just ideas, to find the right structure for each project and organization, because at the end no matter how is final structure, the necessity is for developing a folder structure to organize the documentation of the project.

When we speak about teaming up with others, everyone has different workflows & ways to work. For a shared project is a good idea to achieve a real consensus about not only the folder structure but the expected content for each folder.


### 2.1 CREATING A FOLDER STRUCTURE

These folders represent the four parts of any data science project.

Data – is the folder for all the data collected or been given to analyze.
Figures – is the folder for plots, data pictures, and other images created to show data to other people.
code – is the folder for code files used for collecting, cleaning up, or analyzing data.
Products – is the folder for any reports, presentations created for sharing with other people


### 2.2 CREATING TIDY AND WORKING DIRECTORIES FOR FILES
For the previous structure we need an extra step: divide each folder into two directories: one for tidy files and other for working files.

data/
- raw_data/
- tidy_data/

code/
- raw_code/
- final_code/

figures/
- exploratory_figures/
- tidy_figures/

products/
- writing/


### 2.3 CONSTANT IMPROVEMENT: KEEP WORKING ON CREATE THE STRUCTURE

Nothing is static, and the organization of workflows, something that moves and changes all the time is precisely a good example of something dynamic.

Periodically, during the lesson learned meetings (if the project is using PMI methodology), or during the spring retrospective (if the project is using SCRUM) think about how to improve your organization.

Is there something that can do better? So, make a real evaluation if there is a real chance to implement the possible improvement during the next weeks or the next stage for a project. After the implementation of the change, evaluate the obtained results. That is an excellent way to obtain real feedback. There is always some room for a rollback. 😉


## 3. USE CONTROL VERSION

Why is it necessary to use a control version? To delegate basic tasks like:

To have an automatized backup system for the work, and just for that the necessary work to implement that is highly valuable.
For handling changes on the files during all the project. Also, return to previous versions in order to check something. Version control systems can solve the problem of reviewing and retrieving previous changes and allow single files to be used rather than duplicated.
To facilitate the process of working with others making it easy to share files and keep working on them.
Some of the most popular tools are GIT, SVN, Subversion… no matter the final choice the best idea is to implement it.


## 4. DOCUMENT EVERYTHING

When we are speaking about the documentation we are referring about:

documents included for analysis
intermediate datasets
intermediate versions of your code

Special consideration for the raw datasets: always keep the raw data as the project received for the first time. If for any reason the raw data is modified not using a script, document the process step by step and maintain separated files, and save the intermediate datasets to save time.

The most challenging decision is determining how much time to invest in a document: too much time and yes, it is a waste of time, too little and the documentation will be incomplete and useless.


## 5. IMPROVE THE PROCESS

The fundamental idea is to evaluate the process and improve the workflow.

At the moment to finish a project, or delivery something is a good idea to evaluate if there is something to improve: a better organization for the files, or correct the way to document, no matter what at the end the idea is to understand that any process is in constant movement and you need to improve it.


## CONCLUSIONS

Managing the organization of a data project means to evaluate what are the objectives into an organization system, how to structure the data, the best way to establish a backup system and version control and finally how to document all the processes.

## REFERENCES

There are several sources to read more about how to organize a project, especially in this case different ideas and practical approaches could be beneficial in order to create a tailored organization system for each company.

[Principles of research code](http://www.theexclusive.org/2012/08/principles-of-research-code.html)

[Cookiecutter Data Science – opinions: Great and straightforward advice about how to manage data science projects.](https://drivendata.github.io/cookiecutter-data-science/#opinions)

[A Quick Guide to Organizing Computational Biology Projects: Excellent article about how to organize a project by William Stafford Noble (2009)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424)

[Why use a control version: a detailed article enumerating the reasons for using a control version. (2014)](https://mikemcquaid.com/2014/01/18/why-use-version-control/)

[Chromebook data science MOOC](https://leanpub.com/universities/set/jhu/chromebook-data-science) – 12 MOOCs offered by faculty members in the Johns Hopkins Department of Biostatistics, Bloomberg School of Public Health. Course 3 is about how to organize data science projects.

[Thinkingondata]