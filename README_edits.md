# Introduction to command line interface (CLI) - Part I

## Welcome to an intro to CLI, a virtual training offered prior to the 2026 Midwest Bioinformatics Training 

> [!NOTE]
> This is an optional training series prior to the in-person training.
> If you are already comfortable with using the CLI, then you do not need these pre-training modules

## Table of contents
- [Overview](#-overview)
- [Getting started in GitHub Codespaces](#-getting-started-in-github-codespaces)
- [CLI command: ls](#-cli-command-ls)
- [CLI command: man](#-cli-command-man)
- [CLI command: pwd](#-cli-command-pwd)
- [CLI command: cd](#-cli-command-cd)
- [CLI command: mkdir](#-cli-command-mkdir)
- [CLI command: touch](#-cli-command-touch)
- [CLI command: mv](#-cli-command-mv)
- [CLI command: cp](#-cli-command-cp)
- [CLI command: rm](#-cli-command-rm)
- [CLI command: cat, less, head, tail](#-cli-command-cat-less-head-tail)
- [CLI command: nano](#-cli-command-nano)
- [CLI command: bash](#-cli-command-bash)
- [CLI command: wget](#-cli-command-wget)


## 📖 Overview

This introduction module introduces you to CLI for purposes of:

* Navigation and directory management
* File operations
* Viewing files
* External file retrieval
* Editing files
* Starting a bash script

By the end of this module, you should understand and be comfortable using the following commands:

* ls
* man
* pwd 
* cd
* mkdir
* touch 
* mv
* cp
* rm
* cat
* less
* head
* tail
* nano
* bash
* wget

And be familiar with concepts and best practices such as:

* Flags to modify CLI commands 
* Full paths vs relative paths 
* Providing relative paths for faster navigation
* Tabbing out for autocomplete when navigating paths
* Providing "-" or "_" when naming files/directories to prevent spaces
* Automation of CLI commands


## 💻 Getting Started in GitHub Codespaces

> [!NOTE] In order to use GitHub Codespaces, you need a GitHub account. Make one for free [here](https://github.com/).


#### Step 1: Navigate to the GitHub repository containing this introductory CLI module, [here](https://github.com/JLC2141/intro_to_cli).

#### Step 2: 

1. Select the green "Code" box
2. Select the Codespaces tab
3. Select the "+" icon to launch the codespace

![GitHub repo to start codespace](images/starting_codespace.png)

It will take a few mintues to set up your codespace. Once it's ready, you should see the following:

![Codespace environment](images/codespace_env.png)

Put simply, GitHub codespaces creates a virtual Linux environment with Visual Studio Code (VS Code) editor:

More on [codespaces](https://docs.github.com/en/codespaces/about-codespaces/what-are-codespaces) and [VS Code](https://code.visualstudio.com/docs/editor/whyvscode), if interested. 

Put more simply, anyone who creates a codespace from this repo will be working within the same exact environment on a similarly simulated computer, putting us all at the same starting point.

Notes about why it would be more difficult to do this locally, windows vs mac, WSL vs Mac terminal? Likely leave out

In the orange box, you'll see the file explorer with the following directory structure:

## 📂 Directory Structure

```
intro_to_cli/
│
├── reads/
│  
├── resources/
│   ├── documentation/
│   │   └── notes.txt
│   ├── metadata/
│   │   └── sample_metadata.csv
│   └── modules/
│       ├── module_1.txt
│       ├── module_2.txt
│       └── module_3.txt
│
├── results/
│
├── test dir/
├── LICENSE
├── README.md
├── log_file.txt
├── samplesheet.csv
└── script.sh
```

---

This parellels to the same functionality you may be used to when, for example, using the file explorer on your computer, such as this:

![File explorer](images/file_explorer.png)

We refer to this as a **G**raphical **U**ser **I**nterface, or GUI (pronounced gooey), for short.

And here's a GUI:

![Excel](images/excel.png)

And there's a GUI:

![NCBI](images/ncbi.png)

Everything you use to interact with your computer or the web via point and click is a GUI

That's in contrast to the purple box:

![Codespace environment](images/codespace_env.png)

This is the terminal application window that allows us to run commands via the command-line interface (CLI), the most common way that bioinformaticians interact with a computer's operating system

Everything you're used to doing here: 

![File explorer](images/file_explorer.png)

To change folders, make new ones, copy files, move files, etc., you can also perform via CLI. 

Back to the purple box- that "$" in the terminal window is a prompt telling us that it is ready to accept commands. So let's get started with CLI! 


## 📋 CLI command: ls

![list](images/list.png)

Folders same as directories but we use directory terminology. Directories highlighted in green and files not

![list_l](images/list_l.png)

![list_lh](images/list_lh.png)


Then mention other useful flag such as -S (sort by size) and -t (sort by time)

* ls with * 

GET IMAGE!

* clear command to clear terminal

## 📕 CLI command: man

![man](images/man.png)
![man_lh](images/man_lh.png)

* Note man works with other commands we'll learn, too

## 🎯CLI command: pwd

![pwd](images/pwd.png)

* Discuss root / and forward slash

## 📂 CLI command: cd

Recall we looked at the contents of the directory
![list](images/list.png)

Let's change directory into the resources directory

![cd_down](images/cd_down.png)


Go back to the original directory

![cd_up](images/cd_up.png)


NEED TO ADD CONCEPTS

* Relative paths
* tabbing out
* cd home


## 📁 CLI command: mkdir

![mkdir](images/mkdir.png)


## 📃 CLI command: touch

![touch](images/touch.png)


Touch with relative path

hidden answer

![touch_rel](images/touch_rel.png)


## ↔️ CLI command: mv

![mv](images/mv.png)


![mv_check](images/mv_check.png)

![mv_rename](images/mv_rename.png)


## 📄 CLI command: cp
## 🗑️ CLI command: rm
## 🔍 CLI command: cat, less, head, tail
## 📝 CLI command: nano
## 🏃 CLI command: bash
## 📨 CLI command: wget


