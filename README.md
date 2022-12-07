# File System Traversal

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
[![Language: Python](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/1013818801281839184?logo=discord)](https://discord.gg/9VfCdqffu6)

## Introduction

This project introduces the steps that you must take to implement, build, and
run a Python program called `tree` command that can display details about the
nesting of directories in a specified directory and then the size of all of the
files recursively found in the specified directory. This means that the `tree`
command should perform a recursive traversal that starts at the specified
directory and then continues until no more files and directories are available.

## Seeking Assistance

Even though the course instructor will have covered all of the concepts central
to this project before you start to work on it, please note that not every
detail needed to successfully complete the assignment will have been covered
during prior classroom sessions. This is by design as an important skill that
you must practice as you explore the depth and breadth in the field of operating
systems. If you have questions about this project, please schedule a meeting
with the course instructor during office hours.

## Project Overview

After cloning this repository to your computer, please take these steps:

- Make sure that your computer has `python` and `poetry` installed correctly.
  Please ensure that you are using at least Python 3.10 and the most recent
  version of the `poetry` command.
- After changing into the directory that contains the `pyproject.toml` file run
  the command `poetry install` to install all of the project dependencies.

Next, please make sure that you read the chapters in the OSTEP book about file
systems and review the slides on the course web site for more information about
the concepts needed to implement the `tree` program! You can also learn more
about how a `tree` program would work by using the one installed on your computer.

### Program Implementation

The easiest way to understand how the `tree` program works is to observe its
output for specific command-line arguments when it is run in a specific context.
For instance, when you run the program in the directory that contains the
`input` directory and use the command `poetry run tree --input-directory input`
it should produce the following output in the terminal window. It is worth
noting that the `tree` command should also recognize that `.` is the current
working directory so as to ensure that the command `poetry run tree
--input-directory .` will produce the same output when it is run from the
directory that contains the `input` directory.

```text
📂 input
┣━━ 📂 dir_one
┃   ┣━━ 📄 f1 (2.1 kB)
┃   ┣━━ 📄 f2 (710 bytes)
┃   ┗━━ 📄 f3 (103 bytes)
┣━━ 📂 dir_three
┃   ┗━━ 📂 dir_four
┃       ┣━━ 📄 f1 (1.0 kB)
┃       ┣━━ 📄 f2 (814 bytes)
┃       ┗━━ 📄 f3 (710 bytes)
┗━━ 📂 dir_two
    ┣━━ 📄 f1 (415 bytes)
    ┣━━ 📄 f2 (207 bytes)
    ┗━━ 📄 f3 (0 bytes)
```

It is also worth noting that if you run `tree` and specify a directory that does
not exist the program should present an error message like the following one:

```text
🤷 Either input directory was not specified or it is not valid!
Aborted.
```

### Project Reflection

As you work on this project, you should regularly take time to reflect on the
steps that you are taking and why you are taking them. Each time you run a
program you should think about the inputs, outputs, and behavior of that
program, jotting down notes to help you remember these insights. When you are
writing Python and Go programs, please reserve time to reflect on the features
of the language that you are learning and how the languages are similar to and
different from each other. As you complete this project, make sure that
you reflect on your own strengths and weaknesses and how you can improve in
advance of the next project. Finally, as you implement the `tree` program
you should adopt the viewpoint of the operating system so as to ensure that you
can correctly create a program that will run correctly on your laptop and,
additionally, other laptops that also have Python installed but for a different
operating system. Finally, you should confirm that your program runs correctly
when it is used in GitHub Actions.

### Automated Assessment

Please review the following notes about the way in which your project will be
automatically assess in GitHub Actions:

- If you have already installed the
  [GatorGrade](https://github.com/GatorEducator/gatorgrade) program that runs
  the automated grading checks provided by
  [GatorGrader](https://github.com/GatorEducator/gatorgrader) you can, from the
  repository's base directory, run the automated grading checks by typing
  `gatorgrade --config config/gatorgrade.yml`.
- You may also review the output from running GatorGrader in GitHub Actions.
- Don't forget to provide all of the required responses to the technical writing
  prompts in the `writing/reflection.md` file.
- Please make sure that you completely delete the `TODO` markers and their
  labels from all of the provided source code. This means that instead of only
  deleting the `TODO` marker from the code you should delete the `TODO`
  marker and the entire prompt and then add your own comments to demonstrate
  that you understand all of the source code in this project.
- Please make sure that you also completely delete the `TODO` markers and their
  labels from every line of the `writing/reflection.md` file. This means that
  you should not simply delete the `TODO` marker but instead delete the entire
  prompt so that your reflection is a document that contains polished technical
  writing that is suitable for publication on your professional web site.
