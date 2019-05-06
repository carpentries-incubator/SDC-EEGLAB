---
title: "The EEG structure elements"
teaching: 0
exercises: 0
questions:
- "Where are the EEG properties stored in EEGLAB's EEG structure?"
- "How to work with the data array, events, channel coordinate, and ICA related fields"
objectives:
- "Learn to interact with all the aspects of an EEG data file in EEGLAB"
- "Establish a global view of the information layout in EEGLAB"
keypoints:
- "Where is all of the EEG recording information stored in the EEGLAB file structure?"
---
## How does EEGLAB organize all of the information from an EEG recording file?

#### **EEGLAB's EEG structure contains the information required to work with the EEG data**

Now that we have EEGLAB running inside of Matlab let's take a look under the hood to see how EEGLAB organizes the information that is contained in an EEG recording file. In order to do this we will need to load an EEG recording from GUI.

![EEGLAB Load set]({{ page.root }}/fig/eeglab_load_set_crop.png)

... Then select the *.set file in the sub-s01/eeg folder.

![Import load browser]({{ page.root }}/fig/eeglab_load_set_browse_crop.png)

#### **Exploring properties of the EEG data file**

Once that a file is loaded into EEGLAB the main GUI figure provides some basic properties of the file such as the number of channels and sampling rate. The goal of this lesson is to be able to interact with all of the EEG properties from within the Command Window.

![EEGLAB GUI summary]({{ page.root }}/fig/eeglab_gui_summary.png)

Beyond the basic EEG file property preview on the main EEGLAB window, there are also several tools available for plotting properties of the data via the "Plot" menu. Scrolling the scalp data can be accomplished as follows:

![EEGLAB scroll menu]({{ page.root }}/fig/eeglab_scroll_menu_crop.png)

![EEGLAB scroll]({{ page.root }}/fig/eeglab_scroll.png)

> ## Notice that there are some changes to the figure settings:
> These raw recordings have large voltage offsets and appear all over the figure axis (and outside of the figure axis) so we should modify a couple of the figure psettings.
> 1. Remove the DC offset
> 2. Decrease the voltage range
> 3. Increase the time length
>
> {: .source}
{: .callout}

The channel locations can also be viewed in their topographical layout.
 
![EEGLAB chanloc menu]({{ page.root }}/fig/eeglab_chanloc_menu_crop.png)

![EEGLAB chanloc topo]({{ page.root }}/fig/chanloc_topo.png)

#### **Editing EEG file properties from the GUI**

Working from the command line any property of the EEG file (e.g. data voltage, event label or time, channel location, etc) can be modified. The GUI also provides tools for modifying some of the data properties, such as the channel location via the "Edit" menu. 
![EEGLAB edit chanloc menu]({{ page.root }}/fig/eeglab_edit_chanloc_menu_crop.png)

![edit chanloc gui]({{ page.root }}/fig/edit_chanloc_gui_crop.png)

![edit chanloc 3d]({{ page.root }}/fig/edit_chanloc_3d.png)

#### **Exploring the EEG properties from the Command Line**
Although many of the EEG data properties are available for viewing and editing from the command line everything is also available within the EEG structure in the Workspace and can be explored in the Command Window.

Let's list all of the fields in the EEG structure:
~~~
EEG
~~~
{: .source}

![EEG structure]({{ page.root }}/fig/eeg_structure.png)

Now specific fields of a structure can be accessed using the "." notation, and Structure fields can also be indexed like numeric arrays. For example, we can retrieve the properties of the first channel as follows:

~~~
EEG.chanlocs(1)
~~~
{: .source}

![EEG chanlocs structure]({{ page.root }}/fig/eeg_chanlocs_structure.png)


> ## For fun: try to set latency of the 10th event to 100, and then replot the scalp scroll plot:
> Hint: the event information is in "EEG.events"
>
> {: .source}
{: .callout}


{% include links.md %}

