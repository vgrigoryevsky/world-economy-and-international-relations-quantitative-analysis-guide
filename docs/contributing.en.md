# Contribution Guide

The project accepts contributions via GitHub Pull Requests (described below). Each Pull Request shall be raised against
the specific
GitHub [Issue(-s)](https://github.com/vgrigoryevsky/world-economy-and-international-relations-quantitative-analysis-guide/issues) (
see below for more information). This document outlines some conventions on submission workflow, commit message
formatting, contact points, and other resources to make it easier to get your contribution done and accepted.

## What to contribute

There are several ways of how one can contribute to the Project:

* **Content** -- creating new content
* **Translations** -- translating existing content to other languages

All the items, which require contribution, are tracked
as [Issues](https://github.com/vgrigoryevsky/world-economy-and-international-relations-quantitative-analysis-guide/issues)
. Look for the "good first issue" tag in order not to lose yourself in plenty of items.

### Propose changes

Open
an [Issue](https://github.com/vgrigoryevsky/world-economy-and-international-relations-quantitative-analysis-guide/issues)
with a detailed description of your proposal, the motivation for it and alternatives considered. Please note we may
close this issue or ask you to create a Pull Request if this is not something we see as a sufficiently high priority.

## Contributor License Agreement

By contributing to this repository you agree to the [Individual Contributor License Agreement (ICLA)](ICLA.md).

In order to show your agreement with the ICLA, you should include at the end of a commit message your signature (
described below).

## Contributing steps

### GitHub set up

#### Info

* **GitHub** -- is a provider of internet hosting for source code version using
  Git. [[Wikipedia: GitHub]](https://en.wikipedia.org/wiki/GitHub)
* **Git** -- is software for tracking changes in any set of files, usually used for coordinating work among programmers
  collaboratively developing source code during software
  development. [[Wikipedia: Git]](https://en.wikipedia.org/wiki/Git)

#### Steps

1. [Optional: if you don't have GitHub account] [Register](https://github.com/signup)
2. Find
   an [Issue](https://github.com/vgrigoryevsky/world-economy-and-international-relations-quantitative-analysis-guide/issues)
   to resolve, or create a new one.
    1. [ALT Forking] You can follow GitHub standard contributing flow
       and [fork the repository](https://docs.github.com/en/get-started/quickstart/contributing-to-projects).
3. For the selected Issue - click [Create a branch] button. Make a note of the branch name, you will use it in the next
   step.
    1. [ATL: Forking] Instead of this step follow the flow described in the prev. cl.

### IDE set up

#### Info

* **IDE** -- integrated development environment -- is a software application that provides comprehensive facilities to
  computer programmers for software
  development. [[Wikipedia: IDE]](https://en.wikipedia.org/wiki/Integrated_development_environment)

#### Steps

1. Download [IDE PyCharm Community Edition](https://www.jetbrains.com/pycharm/download/)
    1. _Community Edition_ is a free version, which is good enough for this project
        1. You can also [get a free license for the _Professional
           Edition_ version](https://www.jetbrains.com/community/education/) if you work in Academia or study
    2. There are specific reasons why we recommend using PyCharm
        1. The MkDocs library which we use to manage the documentation is Python-based and has dependencies on Python
           packages, so it will be easier to manage them automatically using PyCharm (see more details below)
        2. Most of the code-based examples in this Guide are done in Python, so it will be useful for you to get use to
           this IDE, to practice how to work with Git repositories, Python-dependencies etc.
    3. If you already have any other IDE installed, you can use it
    4. Also, you can work without an IDE, but this will not make your life easier
2. Clone the repository from the GitHub at the branch you created for your Issue earlier;
   see [Tutorial](https://blog.jetbrains.com/idea/2020/10/clone-a-project-from-github/)
    1. [ALT: Forking] If you earlier forked the repository, clone your fork instead.
3. PyCharm automatically determines that the project is a PipEnv project and will try to set the Python virtual
   environment automatically
    1. PipEnv is needed to separate you local machine environment from the development environment for this project to
       prevent potential conflicts
    2. More info about the [PipEnv here](https://realpython.com/pipenv-guide/)

Congratulations! You can finally work on the content/ translations.

### Understanding repository structure

#### MkDocs info

* To manage project content we use the library [MkDocs](https://www.mkdocs.org/).
* To enable more feature we use a `theme: material` ([mkdocs-material](https://squidfunk.github.io/mkdocs-material/)).
* To enable localisation (multi-language support) we
  use `plugins: i18n` ([mkdocs-static-i18n](https://github.com/ultrabug/mkdocs-static-i18n)).
    * Additional information is provided in
      the [MkDocs static i18n plugin demo](https://ultrabug.github.io/mkdocs-static-i18n/).

#### Project structure

```
docs
├── assets           <-- this is where images and custom stylesheets are stored
├── methodology
│   ├── main.en.md   <-- this is a Main page in English
│   └── main.ru.md   <-- this is a Main page in Russian
├── faq.en.png       <-- this is an FAQ page in English
├── faq.ru.png       <-- this is an FAQ page in Russian
├── ...
├── index.en.md      <-- this is a starting page in English
├── index.md         <-- this is a starting page in default language (Russian)
mkdocs.yml           <-- this is a config file; it defines used plugins, nav structure and nav translations
```

#### Writing content in Markdown

* **Markdown** -- is a lightweight markup language for creating formatted text using a plain-text
  editor. [[Wiki: Markdown]](https://en.wikipedia.org/wiki/Markdown)
    * For hints, see the [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet)

### View your changes

1. Locally view the changes you made to verify them before sending to GitHub
    1. In your IDE, open the `Terminal` window (bottom section) and execute the following command
        1. `mkdocs serve`
    2. You will see in the terminal
        1. `INFO - [21:56:12] Browser connected: http://127.0.0.1:8000/world-economy-and-international-relations-quantitative-analysis-guide/`
    3. Click the link and verify your changes
    4. If you continue editing the markdown files, website content is updated automatically when you remove the cursor
       from the editor section
        1. If you feel your changes are not applied, refresh the browser page
        2. If this does not help, rerun the `mkdocs serve` command
2. To stop the local website, enter `Ctrl+C` in your `Terminal` Window

### Send changes to GitHub

1. If you created new files, in the IDE right-click on the file -> [Git] -> [Add]
2. [Commit and push your changes](https://www.jetbrains.com/help/idea/commit-and-push-changes.html)
    1. Format of the Commit Message -- the commit summary must start with "add"/"upd"/"rm":
        1. "`add...`" -- content was added
        2. "`upd...`" -- content was updated
        3. "`rm...`" -- content was removed
    2. If you have a lot of files changed, you can make multiple atomic commits.
    3. Don't forget to sign your commit off (find `'Sign-off commit'` on the same page for instructions)

### Create Pull Request

1. In GitHub, navigate to your issue
   and [create a Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
    1. [ALT: Forking] [Create a Pull Request from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)
        1. Mention which issue you're resolving.
2. Wait for your Pull Request to be commented/ resolved.
   