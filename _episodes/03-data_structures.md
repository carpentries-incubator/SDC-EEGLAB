---
title: "The EEG structure elements"
teaching: 0
exercises: 0
questions:
- "Where are the EEG properites stored in EEGLAB's EEG structure?"
- "How to work with the data array, events, channel coordinate, and ICA related fields"
objectives:
- "Learn to interact with all the aspects of an EEG data file in EEGLAB"
- "Establish a global view of the information layout in EEGLAB"
keypoints:
- "Where is all of the EEG recording information stored in the EEGLAB file structure?"
---
## How does EEGLAB organize all of the information from an EEG recording file?

#### **EEGLAB's EEG structure contains the information required to work with the EEG data**

Now that we have EEGLAB running inside of Matlab let's take a look under the hood to see how EEGLAB organizes the information that is contained in an EEG recording file. In order to do this we will need to load an EEG recording.

![EEGLAB Load set]({{ page.root }}/fig/eeglab_load_set_crop.png)

![Import load browser]({{ page.root }}/fig/eeglab_load_set_browse_crop.png)

![EEGLAB GUI summary]({{ page.root }}/fig/eeglab_gui_summary.png)

![EEGLAB scroll menu]({{ page.root }}/fig/eeglab_scroll_menu_crop.png)

![EEGLAB scroll]({{ page.root }}/fig/eeglab_scroll.png)

> ## Notice that there are some changes to the figure settings:
> These raw recordings have large voltage offsets and appear all over the figure axis (and outside of the figure axis) so we should modify a couple of the figure psettings.
> 1. Remove the DC offset.
> 2. Decrease the voltage
> 3. Increase the time length
>
> {: .source}
{: .callout}


![EEGLAB chanloc menu]({{ page.root }}/fig/eeglab_chanloc_menu_crop.png)

![EEGLAB chanloc topo]({{ page.root }}/fig/chanloc_topo.png)

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

~~~
EEG.chanlocs(1)
~~~
{: .source}

![EEG chanlocs structure]({{ page.root }}/fig/eeg_chanlocs_structure.png)

{% include links.md %}

