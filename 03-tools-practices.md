---
title: "Tools and good practices for research software"
teaching: 60
exercises: 30
---

:::::::::::::::::::::::::::::::::::::: questions

- What tools and practices are available to help us develop good quality and FAIR research software?
- How do such tools and practices fit together to enable open and reproducible research?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives
After completing this episode, participants should be able to:

- Identify some key tools and practices to aid the development of quality research software
- Explain how can these tools help us work in a FAIR way

::::::::::::::::::::::::::::::::::::::::::::::::

## Good practices for developing research software

Along with the FAIR principles covered in the previous episode, other good practices exist for developing research 
software that foster open and reproducible research. We list some of them here and then cover them in more detail in the 
rest of the course.

### Use version control 

Using a version control system (like Git) is a fundamental best practice in software development, ensuring that changes to code are tracked,
managed, and reversible. Version control systems enable efficient collaboration and maintaining a history of modifications.

### Organise software project and structure code 

Structure your software project following community best practices and write clean, modular, and reusable code to enhance
readability, testing, extensibility, and reusability.

### Use reproducible software environments 

Using virtual development environments (e.g. Conda, venv) or containerisation (e.g. [Docker][docker]) ensures software can be developed and run 
consistently across different systems.

### Comply with coding conventions 

Applying relevant coding style guidelines (e.g. PEP8 for Python) is crucial for writing clean, readable, and maintainable code. 
These guidelines help ensure consistency across a codebase, making it easier for developers to understand and collaborate on projects.

Following coding conventions and guides for your programming language that is agreed upon by the community and other programmers
are important practices to ensure that others find it easy to read your code, reuse or extend it in their own examples and applications.

### Use standard data formats and communication protocols

Using standard data exchange, input and output formats and communication protocols helps create interoperable 
software that can more readily integrate with other tools into more complex pipelines - increasing its interoperability 
and reusability.

### Test your software 

Implement tests to validate code functionality, ensure result accuracy, and maintain result consistency over time when updating the code.
Testing ensures that your code is correct and does what it is set out to do.
When you write code you often feel very confident that it is perfect, but when writing bigger codes or code that is meant to do complex operations
it is very hard to consider all possible edge cases or notice every single typing mistake.

Testing also gives other people confidence in your code as they can see an example of how it is meant to run and be assured that it does work
correctly on their machine - helping with code understanding and reusability.

### Document your software 

Provide clear and comprehensive documentation, including code comments, API specifications, setup guides, and usage 
instructions, to ensure the software is easy to understand, use, and extend.

Software documentation varies in scope and intended audience (developers and contributors, end-users, 
system administrators, etc.), ranging from **code-level documentation** for developers and end-users looking to modify and extend 
the code to **project and product-level** documentation help different users discover the software, understand its 
functionality, legal terms, installation, contribution guidelines and project governance. 
More extensive documentation, including full websites with function definitions, usage examples, tutorials, and 
guides, can further support adoption.

While you may not need as much documentation as a large commercial product, ensuring your code is well-documented is 
essential for making it discoverable, reusable, and maintainable.

### License your software  

A licence is a legal document which sets down the terms under which the creator of work (such as written text,
photographs, films, music, software code) is releasing what they have created for others to use, modify, extend or exploit.
It is important to state the terms under which software can be reused - the lack of a licence for the software
implies that no one can reuse the software at all.

Use open-source licenses (e.g., MIT, BSD) to make your code freely accessible, modifiable, and redistributable.

### Share your software & encourage review 

Openly publish your research software with proper documentation, licence and storage in accessible repositories for reuse
and supporting reproducibility of your results.
Share your code on platforms like GitHub or GitLab to promote collaboration, transparency, and peer review 
to identify bugs, improve software correctness and quality, and promote knowledge sharing.

### Use persistent identifiers for your software

Using unique persistent identifiers, such as **Digital Object Identifiers** (DOIs) provided by [Zenodo][zenodo] or
[FigShare][figshare], or **SoftWare Heritage persistent IDentifiers** ([SWHID](swhid)) provided by [Software Heritage][software-heritage],
and similar digital archiving services help with uniquely identifying your software and its various versions.
Code sharing platforms such as [GitHub][github], [GitLab][gitlab] or [BitBucket][bitbucket] provide 
commit/tag/release identifiers which are very useful but typically only unique within a project or a repository and not globally. 

Identifiers also help with findability of your software, as well as citing your software (and getting credit for your work by providing citable references).

### Provide citation info for your software

Provide identification and citation information in documentation for your software (including its versions) to ensure that software can be
properly cited in publications and research outputs.

### Build community & encourage collaboration around your software

Foster a community and promote collaboration around your software by engaging with users, encouraging contributions, 
and providing clear guidelines for participation. 
Use platforms like GitHub or GitLab to facilitate discussions, issue tracking, and pull requests. 
Maintain clear documentation, respond to feedback, and recognise contributors to create an inclusive and supportive 
environment that encourages long-term involvement, maintenance and sustainability of your software.

## Tools & services for research software

There are various tools for the development of research software that support open and reproducible 
research and support the FAIR and other quality software principles.
These tools and practices work together - no single one will fully address one principle, and each one can contribute to multiple principles simultaneously.
It is important to understand that merely using these tools, without adhering to best practices and aligning their use 
with the FAIR principles, is not sufficient to create FAIR and quality software.

You should already have some of these tools installed on your machine by following the [setup instructions](./index.html#astronaut-data-and-analysis-code).
Here, we will provide an overview of some of the tools, and explain how their combined use with best practices can help you 
achieve the goal of research software that supports open and reproducible research.
The following list is not exhaustive — you should choose the best set of tools and practices based on your specific domain, 
problem and community.

### Software development environments

**Integrated development environments (IDEs)**, such as Visual Studio Code (VS Code) or PyCharm, help with reading, running, testing, and debugging code.
**Virtual software development environments** (such as `venv` for Python) further enable us to share our working environments with others, making it easier to reuse and extend our code.
IDEs often provide integrations with other tools, e.g. version control and command line terminals, enabling you to do many tasks from a single environment,
saving time in switching between different tools.

We have also mentioned [Docker][docker] - an open-source platform that allows developers to package software along with its 
dependencies (libraries, configurations, etc.) into a **container** that can be deployed and run on different operating 
systems. We will not cover Docker in this course, and will focus on environments for developing software.

### Command line tools

**Command line terminals** (e.g. Bash, GitBash) enable us to run and test our code without graphical user interfaces (GUI) afforded to us by IDEs -
this is sometimes needed for running our code remotely on servers and high-performance systems without a GUI provision, where time,
memory and processing power are expensive or in high demand.

**Version Control Systems** (VCS) are typically provided as **command line tools** and used from command line terminals 
to enter commands, interact with VCSs and access remote version control servers to back up and share our work. 
Many IDEs now provide integrations with VCSs too - making them accessible using a GUI instead of typing commands in a terminal.

Well designed command line tools support interoperability by using standard protocols for passing parameters, inputs and outputs.
Such tools integrate well with one another - allowing us to chain them and build up complex and reproducible workflows and analysis pipelines
using several tools in different steps.
If we write our software in a way which provides such an interoperable Command Line Interface (CLI) - we will be able to integrate it with 
other existing command line tools to automate and speed up our work.

### Version control tools

**Version control** means knowing what changes were made to your code, when and by whom - promoting code ownership, responsibility and credit.
When combined with software sharing and collaborative platforms such as [GitHub][github], [GitLab][gitlab] or [BitBucket][bitbucket], it facilitates code publication, sharing and findability,
teamwork and discussions about software and design decisions, provides backup facilities for your code and speeds up
collaboration on shared code by allowing edits by more than one person at a time.

### Software repositories and registries

Having somewhere to share or publish your code is fundamental to making it findable and accessible.
Your institution might have a code repository, your research field may have a practice of sharing code via a specific website, archive or journal,
or your version control system might include an online component that makes sharing different versions of your code easy.
You should check the rules or guidelines of your institution, grant or domain on publishing code, as well as any licenses of the code your software depends on or reuses.

Some examples of commonly used software repositories and registries include:

- general-purpose software repositories - [GitHub][github], [GitLab][gitlab] or [BitBucket][bitbucket]
- programming language-specific software repositories for publishing software packages and libraries- [PyPi][pypi] (for Python) and [CRAN][cran] (for R)
- software registries - [BioTools][biotools] (for biosciences) and [Awesome Research Software Registries][awesome-rs-registries], providing a list of research software registries (by country, organisation, domain and programming language) where research software can be registered to help promote its discovery

Platforms like GitHub, GitLab and BitBucket are more than just source code repositories - they provide social platforms 
to facilitate discussions, issue tracking, and collaboration around your software projects and promote long-term involvement, maintenance and sustainability of your software.

### Software identifying and archiving services

Services like [Zenodo][zenodo] help with publishing, archiving, and identifying research software and data (and their multiple versions) - 
supporting open access, making research software and data publicly available and promoting reproducibility. 
They provide DOI assignment services for proper citation and tracking (by providing globally unique identifiers and resolvable references) 
and permanent archiving (storage) ensuring long-term availability and accessibility of research outputs (even if code sharing services go offline for any reason). Zenodo also integrates with code sharing and development platform GitHub
allowing for automatic archiving of software repositories.

These services improve the visibility, credibility, and preservation of research software.
  
### Software citation tools

Software citation tools help researchers and developers properly cite software in publications, ensuring credit and 
reproducibility. 
These tools generate standardised citation formats and often integrate with repositories like GitHub, Zenodo, and DOI services.

There are multiple formats for providing citation information for software, such as including plain text files 
(e.g. `CITATION.txt`) or Markdown files (e.g. `CITATION.md`) or BibTeX files within the software and its repository.

[Citation File Format (CFF)][cff] and [CodeMeta][codemeta] are both standard formats for describing software metadata. 
CFF is a YAML format, while CodeMeta is a JSON format; there are related tools to generate them (e.g. `cffinit`)
Using `CITATION.cff` or `codemeta.json` files for software citation offers advantages by enabling richer metadata for 
citing code, making citation information more accessible and usable by both humans and machines and 
interoperability with various repositories. 

## Tools & practices summary

The table below provides a summary of some good practices that you should be adhering to when developing research software, 
together with different tools that can help with such practices and how they contribute to the the FAIR and other good software principles.

| Practices                                                                        | Tools                                                                                                                                    | FAIR | Readable/Understandable | Correct/Reliable  | Sustainable/Maintainable |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------|-------------------|--------------------------|
| Use version control                                                              | `git`, GitHub, GitLab, BitBucket                                                                                                         | F    |                         |                   |                          |
| Good software project & modular code structure                                   | Use conventional folder structures, write modular code with well defined interfaces                                                      | R    | x                       |                   | x                        |
| Connect reusable software modules into automated/reproducible software pipelines | Command line tools, CLI, workflow tools (Galaxy, Snakemake, WorkflowHub, CWL)                                                            | I, R |                         |                   |                          |
| Use reproducible software development environments                               | `venv`, `conda`, IDEs (integration with virtual envs.), Docker, etc.                                                                     | R    |                         |                   |                          |
| Format your code to comply with coding conventions                               | PEP8, IDEs (help with formatting and conforming with coding conventions)                                                                 | R    |                         |                   |                          |
| Use standard exchange data formats/communication protocols/interfaces            | CSV, YAML, JSON, CLI, REST, HTTP(S), etc.                                                                                                | I    |                         |                   | x                        |
| Test your software                                                               | Write unit, functional, integration, regression, etc. tests, IDEs (testing and debugging), CI/CD to run tests automatically in pipelines |      |                         | x                 |                          |
| Document your software                                                           | Comments and documentation strings, README, guides, contributions guidelines                                                             | R    | x                       |                   |                          |
| Share your software & encourage review                                           | Code sharing platforms/services (e.g. GitHub, GitLab, BitBucket) and their code review facilities                                        | F, A |                         |                   | x                        |
| License your software                                                            | Various open source licences for code (MIT, BSD, GPL, LGPL, etc.), LICENSE                                                               | R    |                         |                   |                          |
| Use persistent identifiers for your software                                     | DOIs, SWHIDs, Zenodo, FigShare, Software Heritage, etc.                                                                                  | F    |                         |                   | x                        |
| Provide citation & metadata info for your software                               | CITATION, DOIs, Zenodo, CFF, `cffinit`, CodeMeta, etc.                                                                                   | R    |                         |                   | x                        |
| Build community & encourage collaboration around your software                   | Code of Conduct, README, CONTRIBUTING, open source project governance processes                                                          |      |                         |                   | x                        |

Let's explore some of these practices and tools in detail over the next few episodes.

## Further reading

We recommend the following resources for some additional reading on the topic of this episode:

- [CodeRefinery: Reproducible research - preparing code to be usable by you and others in the future][coderefinery-tools]
- [Python IDEs and Code Editors (Guide) - Real Python][real-python-ides]
- [The Zenodo data repository][zenodo-org]
- [The Fair Cookbook - Depositing to generic repositories - Zenodo use case][fair-cookbook-zenodo]
- [The Turing Way "Handbook to reproducible, ethical and collaborative research"][ttw-handbook]

Also check the [full reference set](learners/reference.md#litref) for the course.

:::::::::::::::::::::::::::::::::::::::: keypoints

- Automating your analysis with shell scripts allows you to save and reproduce your methods.
- Version control helps you back up your work, see how data and code change over time and identify which analysis used which data and code.
- Programming languages each have advantages and disadvantages in different situations. Use the correct tools for your own work.
- Integrated development environments (IDEs) automate many coding tasks, provide easy access to documentation, and can identify common errors.
- Testing helps you check that your code is behaving as expected and will continue to do so in the future or when used by someone else.

::::::::::::::::::::::::::::::::::::::::::::::::::


