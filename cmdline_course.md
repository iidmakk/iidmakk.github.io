---
layout: default
---

# Command-line course: brief overview

![Linux learning meme](https://preview.redd.it/summarizing-my-learning-experience-with-linux-with-one-meme-v0-k24j027na1t11.png?auto=webp&s=508c8ec5c2213ef32879af5335f65ca84d12ce87)

## Introduction

I attended the Command-Line Course during my first year as a DH master's student. During the course I learned how to use the command line to navigate files, process text, use CSC remote servers and use GitHub and version control. I also learned how to build and publish a simple websit using Jekyll and GitHub pages. 
The course introduced some tools that will most likely be usefull in my master's thesis and course projects in the future.

### Module 1: Introduction to Command-line Environments

During the first week we learned about the command-line environment. We got to know the basic commands, how to change directory and manage files. We also briefly covered file permissions and terminal-based text editors.

_Example:_ Here are some of the basic commands used:
```bash
pwd
ls
cd
mkdir
cp life_of_bee.txt life_of_bee_backup.txt
mv life_of_bee_backup.txt backup.txt
```
* `pwd` command displays the current working directory.
* `ls` lists files in the current working directory.
* `cd` command changes directories.
* `mkdir` creates a directory.
* `cp` copies a file.
* `mv` is used to move or rename files.

This week helped me to get comfortable with working with a terminal and understand how file systems work. I have very limited previous experience in using something outside a graphical user interface, so everything was very new to me. Learning these basics provided me the foundation for the later modules on this course.

### Module 2: The UNIX file system

During this module we focused on text processing, regular expressions and pipelines. We explored commands like grep, sed, sort, uniq, cut, and wc.
These tools are especially relevant to e.g. corpus linguistics, because they allow large collections of text to me analysed.

_Here is an example of pipelines:_
```bash
sort words.txt | uniq -c | sort -nr
```
This pipeline sorts the input lines, counts the lines that are identical, and output is a list sorted by frequency in descending order.

I learned that the relatively simple commands can be combined to perform more complex tasks. I also learned how these skills can be applied and started to think how I can operationalize these skills in my future studies. As mentioned before, these skills are useful in corpus linguistics, which is something I'm interested in.

### Module 3: Scripting, Configuration Files and Installing Programs

In the 3rd module we learned to write our own scripts, how the if statement works, giving commands as the root user, installing python packages and more. We also learned how to create a virtual environment which helped with the course tasks.

_Example:_
```bash
#!/bin/bash
echo "${1}er"
```
This script takes an English adjective  ending in a consonant and prints the comparative form by adding -er.
 
This module showed me how to make workflow more efficient by using scripts. I also learned that environments can be useful when installing packages. I think these concepts will be useful when I start to develop more complex computational research workflows.

### Module 4: Using ssh, scp and Version Control

In this module, we were introduced to GitHub, copying files from a server, killing processes and using SSH. We also learned version control, which helps with larger projects where many people are working with the same code. 

This command kills a bash process:
```
kill -9 PID
```
The PID number can be found by using the command `ps`. This is used to identify which process you want to kill.

During this module I learned how to use GitHub and work with remote repositories. I also learned the benefits of using version control and why it is important to record how a project changes over time. I also gained good experience with working local and remote repositories. 

### Final week

During the final week we had to apply our knowledge of GitHub into creating a webpage on GitHub pages.  I published a website about a made-up person attending university and taking classes in made-up subjects. 
This was done by using Jekyll, a static site generator. We also had to learn simple Markdown and use that knowledge in formatting the text on the created website.

_Example:_ If I have installed Jekyll, I can preview the website locally by running:

```bash
bundle exec jekyll serve
```

This command gives me a local address which I can use to  check the website before publishing changes.

This experience helped me connect the different command-line skills. I have some previous html experience, so working with the files was fun and nostalgic. I also learned the importance of previewing changes locally, before pushing them to GitHub. 

##  Useful commands 

| Task | Command | Description |
|---|---|---|
| Find current directory | `pwd` | Prints the current working directory |
| List all  files | `ls -la` | Lists all files in the working directory, including hidden files |
| Navigate directories | `cd` | Changes the current directory |
| Create a directory | `mkdir` | Creates a new directory |
| Read a text file | `less file.txt` | Displays a file page by page |
| Check Git changes | `git status` | Shows all the edits made |
| Push commits | `git push origin master` | Pushes local commits to the remote master branch |
| Preview a website | `bundle exec jekyll serve` | Starts the local Jekyll server | 
