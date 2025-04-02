---
title: "Course introduction"
teaching: 30
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is open and reproducible research?
- Why are these practices important, in particular in the context of software used to support such research?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

After completing this episode, participants should be able to:

- Understand the concept of open and reproducible research
- Understand why these principles are of value in the research community 
- Setup their machine with software and data used to teach this course

::::::::::::::::::::::::::::::::::::::::::::::::

## Jargon busting
Before we start with the course, below we cover the terminology and explain terms, phrases, and 
concepts associated with software development in reproducible research that we will use in this course.

* **Reproducibility** - the ability to be reproduced or copied; the extent to which consistent results are obtained 
when an experiment is repeated (definition from [Google’s English dictionary is provided by Oxford Languages][google-oxford-dict])
* **Computational reproducibility** - obtaining consistent results using the same input data, computational methods (code),
and conditions of analysis; work that can be independently recreated from the same data and the same code 
([definition][ttw-reproducibility-def] 
by the [Turing Way's "Guide to Reproducible Research"][ttw-guide-reproducible-research])
* **Reproducible research** - the idea that scientific results should be documented in such a way that their deduction
is fully transparent ([definition][wiki-reproducibility-def] from Wikipedia)
* **Open research** - research that is openly accessible by others; concerned with making research more transparent, 
more collaborative, more wide-reaching, and more efficient 
([definition][wiki-open-research-def] from Wikipedia)
* **FAIR** - an acronym that stands for Findable, Accessible, Interoperable, and Reusable
* **Sustainable software development** - software development practice that takes into account longevity and 
maintainability of code (e.g. beyond the lifetime of the project), environmental impact, societal responsibility and ethics in 
our software practices. 

:::::::::::::::::::::::::::::::::::::::: callout
## Computational reproducibility

In this course, we use the term "reproducibility" as a synonym for "computational reproducibility".
:::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: discussion

### Motivation
Think about the questions below. Your instructors may ask you to share your answers in a shared notes document and/or
discuss them with other participants.

- What motivated you to attend this course? Did you come by choice or were you advised to attend?
- What do you hope to learn or change in your current research software practice? Describe how your knowledge,
  work or attitude may be different afterwards.

::::::::::::::::::::::::::::::::::::::::::::::::

## What is reproducible research?

[The Turing Way's "Guide to Reproducible Research"][ttw-guide-reproducible-research]
provides an [excellent overview of definitions of "reproducibility" and "replicability"][ttw-reproducibility-def] found in literature, 
and their different aspects and levels. 

In this course, we adopt the Turing Way's definitions: 

* **Reproducible research**: a result is reproducible when the same analysis steps performed on the same data 
consistently produce the same answer.
  * For example, two different people drop a pen 10 times each and every time it falls to the floor. Or, we run the same code multiple times on different machines and each time it produces the same result.
* **Replicable research**: a result is replicable when the same analysis performed on different data produces 
qualitatively similar answers.
  * For example, instead of a pen, we drop a pencil, and it also falls to the floor. Or, we collect two different datasets as part of two different studies and run the same code over these datasets with the same result each time. 
* **Robust research**: a result is robust when the same data is subjected to different analysis workflows to answer the 
same research question and a qualitatively similar or identical answer is produced.
  * For example, I lend you my pen and you drop it out the window, and it still falls to the floor. Or we run the same analysis implemented in both Python and R over the same data and it produces the same result.
* **Generalisable research**: combining replicable and robust findings allow us to form generalisable results 
that are broadly applicable to different types of data or contexts.
  * For example, everything we drop - falls, therefore gravity exists.

![*The Turing Way project illustration of aspects of reproducible research by Scriberia, used under a CC-BY 4.0 licence, [DOI: 10.5281/zenodo.3332807][ttw-illustrations]*](https://raw.githubusercontent.com/the-turing-way/the-turing-way/refs/heads/main/book/website/figures/reproducible-definition-grid.svg){alt='Four cartoon images depicting two researchers at two machines which take in data and output the same landscape image in 4 different ways. These visually describe the four scenarios listed above.'}

In this course we mainly address the aspect of reproducibility - i.e. enabling others to run our code to obtain the same results.

We can also further differentiate between:

* **Computational reproducibility**: when detailed information is provided about code, software, hardware and 
implementation details.
* **Empirical reproducibility**: when detailed information is provided about non-computational empirical scientific 
experiments and observations. In practice, this is enabled by making the data and details of how it was 
collected freely available.
* **Statistical reproducibility**: when detailed information is provided, for example, about the choice of 
statistical tests, model parameters, and threshold values. This mostly relates to pre-registration of study design to prevent p-value hacking and other manipulations.

In this course, we are concerned with computational reproducibility, i.e. when the application of computer science and 
software engineering is used to aid solving research problems.


::::::::::::::::::::::::::::::::::::: discussion

### What does open and reproducible research mean to you?
Think about the questions below. Your instructors may ask you to share your answers in a shared notes document and/or
discuss them with other participants.

- What do you understand by the words "open" and "reproducible" in the context of research?
- How many people or groups can you list that might benefit from your work being open and reproducible?
- How many times did you wish that someone else's work you came across was more open or accessible to you?
  Can you provide some examples?

::::::::::::::::::::::::::::::::::::::::::::::::


## Why do reproducible research?

Scientific transparency and rigor are key factors in research. Scientific methodology and 
results need to be published openly and replicated and confirmed by several independent parties.
However, research papers often lack the full details required for independent reproduction or replication. 
Many attempts at reproducing or replicating the results of scientific studies have failed in a variety of disciplines 
ranging from psychology ([The Open Science Collaboration (2015)][replication-crisis-osc]) to 
cancer sciences ([Errington et al (2021)][replication-crisis-errington]).
These are called [**the reproducibility and replicability crises**][reproducibility-crisis] - ongoing
methodological crises in which the results of many scientific studies are difficult or impossible to repeat.

Reproducible research is a practice that ensures that researchers can repeat the same analysis multiple times with the 
same results. It offers many benefits to those who practice it:

* Reproducible research helps researchers remember how and why they performed specific tasks and analyses; 
this enables easier explanation of work to collaborators and reviewers. 
* Reproducible research enables researchers to quickly modify analyses and figures - this is often 
required at all stages of research and automating this process saves loads of time. 
* Reproducible research enables reusability of previously conducted tasks so that new projects 
that require the same or similar tasks become much easier and efficient by reusing or reconfiguring previous work. 
* Reproducible research supports researchers' career development by facilitating the reuse and citation of all research outputs - including both code and data.
* Reproducible research is a strong indicator of rigor, trustworthiness, and 
transparency in scientific research. This can increase the quality and speed of peer review, because reviewers can 
directly access the analytical process described in a manuscript. It increases the probability that errors are caught 
early on - by collaborators or during the peer-review process, helping alleviate the reproducibility crisis.  

However, reproducible research often requires that researchers implement new practices and learn new tools.
This course aims to teach some of these practices and tools pertaining to the use of software to conduct 
reproducible research.

## Software in research and research software
Software is [fundamental to modern research][ssi-survey-2014] - some of it would even be impossible without software. 
From short, thrown-together temporary scripts written to help with day-to-day research tasks, 
through an abundance of complex data analysis spreadsheets, to the hundreds of software engineers and millions of lines of code behind international efforts such as the Large Hadron Collider, there are few areas of
research where software does not have a fundamental role.

However, it is important to note that not all software that is used in research is "research software". 
We define "research software" as software or code that is used to generate, process or analyse results of a research 
for publication. 
For example, software used to guide a telescope is not considered "research software". 
On the other hand, formulas or macros in spreadsheets used to analyse data are considered "research code" as they are a form of computer programming that allow one to create, calculate, and change data sets in a number of different ways.

![*Definition of "research software" from the FAIR4RS working group, image by the Netherlands eScience Center licensed under CC-BY 4.0*](https://raw.githubusercontent.com/esciencecenter-digital-skills/research-software-support/611da359cbe1d04ecf056545ee07f977ae536273/modules/researchsoftware/media/definition.png){alt='Quote: Research Software includes source code files, algorithms, scripts, computational workflows and executables that were created during the research process or for a research purpose. Software components (e.g., operating systems, libraries, dependencies, packages, scripts, etc.) that are used for research but were not created during or with a clear research intent should be considered software in research and not Research Software.'}


In the [software survey conducted by the Software Sustainability Institute in 2014][ssi-survey-2014], 
92% of researchers indicated they used some kind of software to aid or conduct their research.
This was not limited to researchers from [computational science][computational-science] 
(aka scientific computing), the "hard" sciences or to those involved in “traditional” uses of computing infrastructure such as running simulations or developing computational methods. The **use of research software is ubiquitous and fairly even across all disciplines**.

Research software is increasingly being developed - researchers do not just use “off the shelf” software and
the majority of researchers develop their own. 
In order to be able to produce quality software that outputs correct and verifiable results and 
that can be reused over time - researchers require training.

This course teaches good practises and reproducible working methods that are agnostic of a 
programming language (although we will use Python code in our examples) and aims to provide 
researchers with the tools and knowledge to feel confident when writing **good quality and sustainable 
software** to support their research. 
Some aspects of such software are described as **FAIR** (Findable, Accessible, Interoperable, Reusable) - 
in the rest of the course, we will explore FAIR and various other practices for good quality research software, 
why it is important to use these practices and what tools can help us along this journey.


## Software and data used in this course

We are going to follow a fairly typical experience of a new PhD or postdoc joining a research group.
They were emailed some data and analysis code bundled in a `.zip` archive and written by another group member
who worked on similar things but has since left the group.
They need to be able to install and run this code on their machine, check they can understand it and then adapt it to
their own project.

As part of the [setup for this course](./installation-instructions.html#astronaut-data-and-analysis-code), you should have downloaded a `.zip` archive containing the software project
the new research team member was given.
Let's unzip this archive and inspect its content in VS Code.
The software project contains:

(1) a JSON file (`data.json`) - a snippet of which is shown below - with data on extra-vehicular activities
(EVAs or spacewalks) undertaken by astronauts and cosmonauts from 1965 to 2013 (data provided by NASA
via its [Open Data Portal](https://data.nasa.gov/Raw-Data/Extra-vehicular-Activity-EVA-US-and-Russia/9kcy-zwvn/about_data))
![JSON data file snippet showing EVA/spacewalk data including EVA id, country, crew members, vehicle type, date of the spacewalk, duration, and purpose)](episodes/fig/astronaut-data-json-snippet.png){alt='JSON data file snippet showing EVA/spacewalk data including EVA id, country, crew members, vehicle type, date of the spacewalk, duration, and purpose'}
(2) a Python script (`my code v2.py`) containing some analysis.
![A first few lines of a Python script](episodes/fig/astronaut-analysis-bad-code-screenshot.png){alt='A first few lines of a Python script used as example code for the episode'}

The code in the Python script does some common research tasks:

* Read in the data from the JSON file
* Change the data from one data format to another and save to a file in the new format (CSV)
* Perform some calculations to generate summary statistics about the data
* Make a plot to visualise the data

## Checking your setup

Let's check your setup now to make sure you are ready for the rest of this course.

::::::  challenge

## Checking your setup

Open a command line terminal and look at the prompt.
Compare what you see in the terminal with your neighbour, does it look the same or different?
What information is it telling you and why might this be useful?
What other information might you want?

Run the following commands in a terminal to check you have installed the tools listed in the Setup page.
Compare the output with your neighbour and see if you can see any differences.

Checking the command line terminal:

1. `$ date`
2. `$ echo $SHELL`
3. `$ pwd`
4. `$ whoami`

Checking Python:

5. `$ python --version`
6. `$ python3 --version`
7. `$ which python`
8. `$ which python3`

Checking Git and GitHub:

9. `$ git --help`
10. `$ git config --list`
11. `$ ssh -T git@github.com`

Checking VS Code:

12. `$ code`
13. `$ code --list-extensions`

::: hint

The prompt is the `$` character and any text that comes before it, that is shown on every new line before you type in
commands.
Type each of the commands one at a time and press enter.
They should give you a result by printing some text in the terminal.

:::

::: solution

The expected out put of each command is:

1. Today's date
2. `bash` or `zsh` - this tells you what shell language you are using. In this course we show examples in Bash.
3. Your "present working directory" or the folder where your shell is running
4. Your username
5. In this course we are using Python 3. If `python --version` gives you Python 2.x you may have two versions of Python installed on your computer and need to be careful which one you are using.
6. Use this command to be certain you are using Python version 3, not 2, if you have both installed.
7. The file path to where the Python version you are calling is installed.
8. If you have more than one version these should be different paths, if both 5. and 6. gave the same result then 7. and 8. should match as well.
9. The help message explaining how to use the `git` command.
10. You should have `user.name`, `user.email` and `core.editor` set in your Git configuration. Check that the editor listed is one you know how to use.
11. This checks if you have set up your connection to GitHub correctly. If is says `permission denied` you may need to look at the instructions for setting up SSH keys again on the Setup page.
12. This should open VSCode in your current working directory. macOS users may need to first open VS Code and [add it to the PATH](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line).
13. You should have the extensions GitLens, Git Graph, Python, JSON and Excel Viewer installed to use in this course.

:::

::::::


You may have noticed that our researcher has received the software project they are meant to be working as
a `.zip` archive via email. This is not very good practice for several reasons - email does not track changes, does not allow 
for multiple people to work on the same file, code reviews or issue tracking, attachments can be mistakenly sent with 
outdated versions and may have storage and scalability limitations. 
In the rest of the course, we will learn some better practices for developing, sharing, tracking changes and 
collaborating on a software project. 



## Further reading

We recommend the following resources for some additional reading on the topic of this episode:

- [The Turing Way's "Guide for Reproducible Research"][ttw-guide-reproducible-research]
- [A Beginner's Guide to Conducting Reproducible Research][beginner-guide-reproducible-research],
  Jesse M. Alston, Jessica A. Rick, Bulletin of The Ecological Society of America 102 (2) (2021), https://doi.org/10.1002/bes2.1801
- ["Ten reproducible research things" tutorial][10-reproducible-research-things]
- [FORCE11's FAIR 4 Research Software (FAIR4RS) Working Group][fair4rs-working-group]
- ["Good Enough Practices in Scientific Computing" course][good-enough-practices]
- [Reproducibility for Everyone's (R4E) resources][repro4everyone], community-led education initiative to increase 
adoption of open research practices at scale
- [Training materials on different aspects of research software engineering][intersect-rse-training] (including open source, reproducibility,
research software testing, engineering, design, continuous integration, collaboration, version control, packaging,  etc.), compiled by the [INTERSECT project](https://intersect-training.org/) 
- [Curated resources][forrt-resources] by the [Framework for Open and Reproducible Research Training](https://forrt.org/) (FORRT)

## Acknowledgements and references
The content of this course borrows from or references [various work](learners/reference.md#litref).
