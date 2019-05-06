---
title: "Scripting from the history"
teaching: 0
exercises: 0
questions:
- "How can processing steps be automated from EEGLAB?"
- "How is interactive use of EEGLAB translated to scripts?"
- "How are scripts executed?"
objectives:
- "Understand how to use EEGLAB from the Command Line Interface (CLI) rather than the Graphical User Interface (GUI)"
- "Understand how to automate tasks"
keypoints:
- "Get the computer to work for you in accomplishing EEGLAB procedures"
---
## Translating interactive EEGLAB procedures into scripts

#### **EEGLAB procedures that are called from the GUI usually save their command line completion to the EEG.history field**

Running a procedure on one file in EEGLAB is a good way explore the data and the process, but once a project goes into production there are several benefits to scripting the procedures. EEGLAB helps with the scripting by storing the command line completion of procedures in the EEG.history field. 

![eeg history]({{ page.root }}/fig/eeg_history.png)

#### **Copy the history string from the Command Window and add it to a script**

Use the "edit" function to create a new empty script and open it in the editor:

~~~
edit erpproc
~~~
{: .source}

![edit erpproc script]({{ page.root }}/fig/edit_erpproc.png)

When copying the history from the Command Window there may be several function calls that are not required when running the script. Copy from the point that the data were loaded into EEGLAB (pop_loadset), up to the point where the processed data file was saved (pop_saveset). Once that the "erpproc.m" is pasted to the Editor, it can be saved then executed from the Command Window by calling its name at the ">>" prompt.

~~~
erpproc
~~~
{: .source}
 
> ## Matlab needs to know where the script is!
> Remember that Matlab will execute functions or scripts stored in *.m files if it knows where the file is. This is to say that Matlab needs to be able to find the *.m files if it is going to be able to execute it from the Command Window. By default new scripts are save to the Current Folder where Matlab sees the scripts by default. If stored elswhere the directory will need to be included in Matlab's "path" in order for it to be found.
>
> {: .source}
{: .callout}


#### **Editing the script so that it is more generalizable**

When EEGLAB stores the Command Line completion of procedures generated from the GUI it does not always store them in a way that is generalizable. Specifically, sometimes there are parameters saved in the function call of the history string that only apply to specific instance that executed while the history was being created. A good example of this is the pop_rejepoch call in the script.

In fact there are several inputs to functions in this script that may not generalize to other situations (e.g. running a different input file).

![edit erpproc script]({{ page.root }}/fig/edit_erpproc_note_ins.png)

In order to find out what inputs are more appropriate for generalizable calls to the functions we can use the "help" call in the Command Window.

~~~
help pop_rejepoch
~~~
{: .source}

![help pop_rejepoch]({{ page.root }}/fig/help_pop_rejepoch.png)

Once all of the identified input generalizations are identified and alternative parameters are determined the script should look like the following:

![help pop_rejepoch]({{ page.root }}/fig/edit_erpproc_fix_ins.png)

#### **Run the script on multiple files by editing the input and output 'filename' parameters**


When EEGLAB stores the Command Line completion of procedures generated from the GUI it does not always store them in a way that 

> ## Each partiticpants files are savein a unique location
> Given that this example EEG project is stord in accordance with the Brain Imaging Data Structure (BIDS) standard each participant has their files stored within a sub## directory. It is important for this exercise that when editing this script to run different files the 'filepath' parameter of the load and save functions are also modified accordingly. 
>
> {: .source}
{: .callout}

{% include links.md %}


