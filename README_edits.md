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

> [!NOTE] 
> In order to use GitHub Codespaces, you need a GitHub account. Make one for free [here](https://github.com/).


#### Step 1: Navigate to the GitHub repository containing this introductory CLI module, [here](https://github.com/JLC2141/intro_to_cli).

#### Step 2: 

1. Select the green "Code" box
2. Select the Codespaces tab
3. Select the "+" icon to launch the codespace

![GitHub repo to start codespace](images/starting_codespace.png)

It will take a few minutes to set up your codespace. Once it's ready, you should see the following:

![Codespace environment](images/codespace_env.png)

Put simply, GitHub codespaces creates a virtual Linux environment and uses the Visual Studio Code (VS Code) editor as the primary interface.

More on [codespaces](https://docs.github.com/en/codespaces/about-codespaces/what-are-codespaces) and [VS Code](https://code.visualstudio.com/docs/editor/whyvscode), if interested. 

Put more simply, anyone who creates a codespace from this repo will be working within the same exact environment on a similarly simulated computer, putting us all at the same starting point for this tutorial.

> [!NOTE]
> GitHub codespaces will be the same environment we use to build and run bioinformatics pipelines during the in-person workshop
> But, there are other applications on your local computer where you can run these commands, as well. For example [terminal](https://en.wikipedia.org/wiki/Terminal_%28macOS%29) on macOS or [WSL](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux) on Windows.
> Plus, with codespaces, we can pre-install everything in a reproducible environment before the so you can get right to coding! 


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

> [!NOTE]
> This is just a test space to learn from.
> Anything you perform in this environment is self-contained and will be deleted at the end of the session.
> Which also means you're free to use this codespace on your own time to explore CLI functionality.


## 📋 CLI command: ls

![list](images/list.png)

Folders same as directories but we use directory terminology. Directories highlighted in green and files not

![list_l](images/list_l.png)

![list_lh](images/list_lh.png)


Then mention other useful flag such as -S (sort by size) and -t (sort by time)

* ls with * 

![list_wc](images/list_wc.png)


* clear command to clear terminal
* Cancel cntrl + c

## 📕 CLI command: man

![man](images/man.png)
![man_lh](images/man_lh.png)

* Note man works with other commands we'll learn, too

## 🎯 CLI command: pwd

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

Concept check:
Why doesn't cd /resources work? Because it's looking for resources at the root. 

* tabbing out
* cd home


## 📁 CLI command: mkdir

![mkdir](images/mkdir.png)


## 📃 CLI command: touch

![touch](images/touch.png)


Touch with relative path

<details>
<summary>Reveal solution, here</summary>
![touch_rel](images/touch_rel.png)

</details>

Attempt move with new relative path


## ↔️ CLI command: mv

### Moving files

![mv](images/mv.png)


![mv_check](images/mv_check.png)

### Renaming files with the move command

**Moving a file within the same directory will rename the file**

![mv_rename](images/mv_rename.png)

You can also move directories

### Moving directories

Take a moment to: 
1) Move the bin/ directory into test_dir/
2) Move the scripts/ directory into test_dir/

<details>
<summary>Reveal solution, here</summary>

![mv_dir](images/mv_dir.png)

I showed you a solution, not the only solution. Here's another way:

![mv_dir_alt](images/mv_dir_alt.png)

In this example, we:
1. Moved the bin/ directory into test_dir/
2. Changed into the test_dir/
3. Changed into the bin/ directory
4. Moved the scripts/ directory up to the parent directory (test_dir/)
5. Changed directory up into the test_dir/

This solution took more steps but it is not wrong. With the knowledge you're gaining with CLI, start to make the connection that there are mutliple ways to achieve the same goal.


</details>

## 📄 CLI command: cp

### Copying files

![cp](images/cp.png)

Recall the wild card character (*). We can also use that to copy a selection of files.

![cp_wc](images/cp_wc.png)

What if there were other files within modules/ directory? For example:

### Deeper dive into the wildcard

![wc_ls](images/wc_ls.png)

How would you use the wild card character (*) to: </b>

1. Only select files starting with "m"?
2. Only select txt files
3. Only select the module_1.txt, module_2.txt, and module_3.txt files

<details>
<summary>Reveal solution, here</summary>

![wc](images/wc.png)

</details>

<br>

As you can see, we performed this with the list (ls) command. The wild card character can be used with a variety of commands including: 

* ls 
* mv
* cp
* rm

Or, when we're running a bioinformatics program and we want to process all FASTQ files within a directory.


### Copying directories

Alright, as we saw with move, when we moved both files and directories, we can do the same with copy. Let's try to copy the resources/ directory into the test_dir/ directory:

![cp_dir_err](images/cp_dir_err.png)

Oops! We ran into an error and the command execution failed. It states that the flag "-r" is not specified, but what does that mean? Let's check the manual:

![cp_man](images/cp_man.png)

The "-r" flag stands for recursive and is required when copying directories because it is essentially telling your computer to copy the directory **and** everything inside it. 

It failed without the "-r" flag because cp only works at a single level and because the resources/ directory contains contents, the "-r" flag is used to permit traversing the entire directory tree within resources/

Let's re-try the copy command with the recursive flag:

![cp_r](images/cp_r.png)


Success!

## 🗑️ CLI command: rm

Remove deletes files and directories. The command for this is:

```
rm
```

followed by the file you want to delete:

```
rm file_to_delete.txt
```

### Removing a file


Within the intro_to_cli/ directory, let's go ahead and specify the samplesheet.csv file for deletion.

>⚠️ **Caution:** This action will delete all files (and directories) permanently. <br>
> ⚠️ **Caution:** There is no recycle bin when deleting via the CLI.


![rm](images/rm.png)


### Removing a directory

I'm sure it's been bugging you like it's bugging me. That pesky 'test dir' directory with a space in the name. 

You:


![rm_dir_loc](images/rm_dir_loc.png)


Yea you, your time is up. We know better now than to name our files and directories with a space

> [!TIP]
> Always add a hyphen "-" or an underscore "_" when naming to simplify navigating paths (e.g. this_is_a_good_file_name.txt).

Let's remove that directory:

![rm_dir_err](images/rm_dir_err.png)


Not again! 🤦‍♂️ Can you recall the flag we need to add in order to delete a directory?

<details>
<summary>Reveal solution, here</summary>

The recursive flag "-r"! 

![rm_dir_r](images/rm_dir_r.png)

And we see that the directory is gone. The directory was empty, but it doesn't matter. You need to add the recursive flag with trying to delete (or copy) a directory.

</details>

<br>

Okay, let's try to remove a directory with contents in it. Let's remove the test_dir/ directory:

![rm_dir_r_can](images/rm_dir_r_can.png)

Okay, I give up. I cancelled the command with:

```
ctrl + c
```

You see, each line was a prompt, asking if I wanted to delete a particular file or directory within the test_dir/:

* I had to type "yes" and hit enter, over and over again to confirm deletion
* This is time consuming if the directory has hundreds of contents

Add the force (-f) flag in combination with the recursive (-r) flag to remove prompts and delete the directory:

![rm_dir_rf](images/rm_dir_rf.png)

<br>

>⚠️ **Caution:** Do not run a command such as:
> ```
>rm -rf *
>```
> ⚠️ **Caution:** Unless you are certain of where you currently are located in the file system <br>
><br>
> **And definitely do not ever run**:
>```
>rm -rf /
>```
> ⚠️ **Caution:** Because this would delete everything starting at the root directory...so your whole computer.<br>
>There's typically a built-in safeguard if you try to remove from the root but it's best not to use that command at all


## 🔍 CLI command: cat, less, head, tail

We will now explore various techniques to view a file. 

### cat 

The first is cat, short for concatenate. This will read and write the entire contents of a file to your terminal if you type:

```
cat file_name.txt
```

For example, let's look at the contents of the log.txt file:

![cat](images/cat.png)

You'll notice this is only an image of the end of the file because it's a relatively long file. You can scroll up and down to navigate the contents.

> [!NOTE]
> This is just a mock log file of bioinformatics pipeline

### less

However, sometimes files may be thousands of lines long and you want more fine-tuned control of the navigation. For this we can use the command, less.

```
less logfile.txt
```

![less](images/less.png)

In contrast to cat, you'll notice the less command opens a full-screen terminal pager window that does not display the entire file. You start at the beginning of the file and can navigate with scroll. You can also search key words, for example, by entering the following: 

```
/STEP 4
```

For search results below your current location in the file or:

```
?BIOINFORMATICS
```
For search results above your current location in the file.

To exit terminal pager window, just type: 

```
q
```

### head

Sometimes, you just want to view the first part of a file. For example, the beginning of a log file to view summary information about a run. 

For this, we use the head command

```
head logfile.txt
```

![head](images/head.png)

By default, the head command will display the first 10 lines of your file.

If you want to display more lines, the first 20 lines for example, use the -n flag followed by the number of lines:

```
head -n 20 log.txt
```

![head_n](images/head_n.png)

And now we've displayed the first 20 lines of the log file.

### tail

Other times, you may want to only view the end of file to view, for example, to make sure that your bioinformatics pipeline completed successfully. For this, we use the tail command: 

```
tail log.txt
```

![tail](images/tail.png)

> [!NOTE]
> Tail also works with the -n # of lines command as shown with the head command.


## 📝 CLI command: nano

Nano is a text editor for Linux. Think of it like the notepad app you may be familiar with: 

![notepad](images/notepad.png)

We can start with the command and the name of the file we want to create.

```
nano test_file.txt
```

Press the enter key ↩

![nano_start](images/nano_start.png)

This initiates the editor. 

![nano](images/nano.png)

Add some notes to the first line. For example:

![nano_edit](images/nano_edit.png)


Now, let's try to save our new file. Press:

```
ctrl + x
```

To initiate exit. 

![nano_confirm](images/nano_confirm.png)

The editor prompt asks if we want to save. Press:

```
y
```

The final prompt allows us to name our file. 
![nano_save](images/nano_save.png)

We don't need to change the name. Save the file by pressing the enter key ↩ and exit the editor. 

Verify that your file has been created.

![nano_final](images/nano_final.png)

And view the final with any method you prefer.

![nano_view](images/nano_view.png)

Success! 

> [!NOTE]
> You can also edit files that have already been created
> Try editing the test_file.txt again, add a second line, save, and view the file

Where the nano editor really shines is when we want to create scripts to automate processes, as we'll see in the next section. 

## 🏃 CLI command: bash

Why create a script? We like automation for reproducibility and efficiency, and it just makes sense for throughput when you're going to be repeating an analysis on a regular basis.

A script is already in the intro_to_cli/ directory, aptly named, script.sh.

Let's start the script with the bash command:

```
bash script.sh
```

![bash](images/bash.png)

Notice in the image above that I first looked at the contents of the script prior to running the script. We see that it was a one line command to create a test_dir/ directory. 

The command line prompt "$" will appear on a new line once the script is complete. However, we can also add another command within the script to reassure us the script completed. 

> [!NOTE]
> The .sh extension is just convention. Other file extensions are also compatible with running the bash command 
> But, imagine one day someone will look at your code and try to understand how it functions
> Coding standards make reading code more streamlined and so the .sh extension tells others to look there for automated scripts


**Concept Check**

Take some time to re-edit the script.sh files to achieve the following objectives:

* Make a comment where they should take advantage of vs code text editor. Click on the file and use the VS code

1) Remove the first line
2) Make a new line that moves the test_file.txt into the results/ directory
3) Then, using relative paths, list the contents of test_file.txt in long format and make the output human-readable
4) Provide a message at the end of the script that says the script is completed

>[!TIP]
> Start each command on a new line

<details>
<summary>Reveal solution, here</summary>

```
mv test_file.txt results
ls -lh results/test_file.txt
echo "Script completed"
```

And showing this on the CLI:

![bash_script](images/bash_script.png)

> [!NOTE]
> Notice the hashed (#) lines in the image (orange arrows)
> The hash prevents the lines from being read and executed in the script
> Use hash lines to provide a human-digestible comment on what your code is doing

</details>

It's okay if you didn't get last line. The point of this exercise is that you're not always going to have me. So I want to take this moment to introduce you to someone much smarter than me:

![ai_chat](images/ai_chat.png)

On the right in the green box is [GitHub Copilot](https://docs.github.com/en/copilot/get-started/what-is-github-copilot), an AI coding assistant.

**If you do not see this window, then click on the "toggle secondary side bar" icon (orange arrow)**


And then set the following preferences: 

1. Set the agent to "Ask"

![ai_set_agent](images/ai_set_agent.png)

Agent will try to change your code automatically while agent will just provide suggestions.

2. Set the model to Claude

![ai_set_model](images/ai_set_model.png)

The model is like choosing you flavor of an AI assistant.

You should now see the following configuration: 

![ai_config](images/ai_config.png)

Now, put AI to use!

![ai_prompt](images/ai_prompt.png)

Things to note: 

1) I removed the echo command that I originally had from script.sh
2) Click on script.sh in the file explorer pane to add the file to the chat. Now, when you ask the AI assistant your question, it will answer it in the context of the contents of this file you specified.
3) Provide question to the AI agent and enter


> [!NOTE]
> This echo line works in the sense the it outputs a message, but it's really not an optimal solution
> A much better solution would be

```
if [ $? -eq 0 ]; then
    echo "Script completed successfully!"
else
    echo "Script failed!"
    exit 1
fi
```

I encourage you make use of the AI agent to better understand why this is a better solution. Then, really challenge yourself by trying to understand what how this "if statement" works and then implement and run it in your script.






## 📨 CLI command: wget
or save for part II?

Part II
* wget
* for loop
* bash variable
* cat >
* line breaks with a command
    * ls -l \
         -h \
        results/test_file.txt


