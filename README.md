---
marp: true
title: Your Hackathon Survival Kit
theme: gaia
class:
 - lead
 - invert
paginate: true
---


# The Survival Kit for your First Hackathon

### https://gitpitch.com/encima/learn-git

### Women++ 
### Chris Gwilliams https://github.com/encima


---

* Have you never been to a hackathon before? Afraid of what to expect, what is expected of you or that you do not have experience.

* SHUT THAT VOICE UP. Anyone, and I mean anyone, should feel welcome at a hackathon.

---

* But, if you want to contribute and you do not have such a technical background, then this workshop can help you hit the ground running.

![](https://media.giphy.com/media/7kn27lnYSAE9O/giphy.gif)

---

## Who Am I? You Might Ask

* What right do I have to `mansplain` the basics of a field that was originally dominated by women?
* Well...none
* But I taught these things to myself before, during and after university
* And I have been teaching since I was 21

I love teaching, tech and professionalism
I hate: memems, GIFs, awkward humour and pizza

---

![](https://media.giphy.com/media/bA5EUCvMgDBkc/giphy.gif)

And I am a **huge hypocrite**

---

## Topics

* The Command Line
* Git
* Github/Gitlab/Bitbucket etc
* Web Development Introduction

---

## Structure

![Freedom](https://media.giphy.com/media/S3sc3Pg9dFpUA/giphy.gif)

There is none! Ask if you need help, pee when you want and scream when you are frustrated.

---

## Go Go Go!

First, the command line, also known as:

* Terminal
* Bash
* Shell
* Cmd
* Command Prompt
* Console
* Barry (ok, not this one)

---

## What is the shell?

Before we had the magic of windows and Graphical User Interfaces,
we had to do things the old way... with words on a pleasant black screen with green font.

![](http://mewbies.com/geek_fun_files/bsdgames/bsdgames_hangman.png)

---

## We have GUIs now! Why not use them?

You can! Git has some pretty sweet Desktop applications.

### BUT

some things are just quicker in a terminal

---

![](https://media.giphy.com/media/kF6kHD7l9kXEBrPqPS/giphy.gif)

---
<!-- backgroundColor: black -->
<!-- color: green -->

## Start your engines

### Windows?

`Win+R` Type `cmd`
`Command Prompt`

### Mac?

`Terminal`

### Linux?

`Ctrl+Alt+T`
`Terminal`

---

## A Windows note!

Microsoft recently launched WSL (Windows Subsystem for Linux). This is a huge step that allows Windows 10 users to run Linux inside their Windows OS.

This workshop supports both Linux and Windows but, to make things easy, WSL makes life *so so so* much easier.

If you are running Windows 10, click [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to get set up.

(**NOTE**: If enough of the workshop wants to set this up, then we will take a 15 minute break to do it all together)

---

## Prompt

`$__`

The prompt is the part of the terminal that is just sitting and waiting for your input. 

Before we give it some, we should know where we are!

---

## PWD

```
$ pwd
/home/encima/
```

pwd - present working directory, this is where you are right now

Normall, this is your HOME directory:
* Linux: /home/USERNAME
* Mac: /Users/USERNAME

(**NOTE**: In Windows, it is `cd`)

---

## Slashes

Almost all of the world uses `/` to show a difference in path names

BUT

if you are a Windows User (using command prompt), then you must remember to use `\`

---

## Moving around!

### Change directories:
`cd /Users/patty/Documents`

### List Directory Contents:
`ls`

### Make a directory
`mkdir new_folder`

---

### Arguments

![](https://media.giphy.com/media/l41YkEBS3Br3PqqGI/giphy.gif)

---

### Arguments - The command line kind

Commands like `ls` and `cd` are `built-in commands`, this means that we can use them in the shell without needing to install anything

We can give them `arguments` to change their default behaviour.

---

### Show me **ALL** the things in the directory:
`ls -ahl`

a = all (show me hidden files and folders, please)
h = human readable (I am not a machine!)
l =  long listing format (Give me all the details!)

---

### Exercise Time:

![](https://media.giphy.com/media/l7EnApLyoAKwE/giphy.gif)

---

1. Change the directory to your home directory
2. Create a new folder called 'newDir'
3. Change into that directory
4. List the contents
5. Now list all the contents (showing all hidden files)

What is in there? What do you think they mean?

---

## Some extra commands

### Create a file
`touch myfile.txt`

### Remove a file
`rm myfile.txt`

### Remove a directory
`rm -r myfolder`

---

### Here Be Dragons!

* Notice how these things run with no confirmation or anything?
* This little black screen has the power to make...or break your computer
* Always double check what you type
* **NEVER** run a script from the internet or from someone you do not know

---

Your computer is like a relaxed Grandma. She will let you:

* eat all the sweets
* paint your own room
* destroy your own furniture

but she will **not**:

* Let you open the medicine cupboard
* Let you paint the lounge

![bg right contain](https://vignette.wikia.nocookie.net/courage/images/d/d9/Muriel_Bagge.png/revision/latest?cb=20181025053335)

---

### Lets' get **super**

To do the things Grandma won't let you do, you must __become__ Grandma

Everything outside of your home directory can contain important data.

Every folder at the root `/` level is protected and you cannot touch it.

---

### Superuser

To do these protected things:
* Modify system files
* Install programs
* Start and stop services

You must be an admin. Usually, in Linux, your account has admin rights but is stopped from doing these things by default.

In Linux, we call an Admin: `superuser` 

The default `superuser` account is: `root`

---

### I'm Sorry Dave, I'm Afraid I Can't Do That

Try running:
`hostname barry`

What happens? Why?

To run this command, you have 2 options:
1. `su`
2. `sudo`

---

### `SU`

SU = SUPERUSER

Typing this command will log you in as the `root` user on your system and give you full rights to everything.

It is **NOT** recommended.

---

### `SUDO`

SUDO = SUPERUSER DO

`sudo hostname barry`

SUDO asks your machine to run the command you like as the root user and then switch back to your user once it is done.

**USE THIS METHOD**

---

### Tips and Tricks

* History - your shell knows what you ran before:
`use the up and down keys to move through your history of commands`
* Completion - files and folders can be long
`use the TAB key to autocomplete commands and file paths - this is CASE SENSITIVE`
* SEARCH - For things you ran a long time ago
`press CTRL+r to start a search and type what you are looking for, you will be shown matching results as you type`


---
<!-- backgroundColor: gray -->
<!-- color: white -->
## LET'S GIT GOING

![bg contain](https://media.giphy.com/media/cnhpl4IeYgU7MCBdV2/giphy.gif)

---

### What is Git?

A Version Control System (VCS) that allows you to store files and access their  history at different points in time

TL;DR: A manual Dropbox that stops you from making:
* doc1.docx
* doc1_final.docx
* doc1_final_revised.docx

---

### Sounds Great! How Do I Git It?

[https://git-scm.com/downloads](https://git-scm.com/downloads)

* Linux: `apt/yum install git`
* OSX: `brew install git`

---

