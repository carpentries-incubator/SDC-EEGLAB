---
title: "Summarizing EEG data measures across recordings"
teaching: 0
exercises: 0
questions:
- "How are group level summaries generated in EEGLAB via the STUDY structure?"
- "Organizing the data for the STUDY structure"
- "Plotting group level ERPs and making comparisons"
objectives:
- "Understand how to summarize and visualize data across EEG sessions"
- "Understand the relationship of single session 'set' files in relation the STUDY structure"
- "Understand how to explore the EEG data measures across groups, conditions, etc."
keypoints:
- "Making summaries and comparisons of processed EEG measures"
---
## The STUDY structure in EEGLAB allows for the summary of measures across set files

#### **EEGLAB's STUDY structure contains the information to index processed files in an EEG project**

Having worked with single EEG files and then having scripted across files it is now a good time to explore how EEGLAB enables group summaries of set files. The process of building a STUDY structure and then defining designs within it allows users to summarize measures across multiple files or test differences across independent variables.

The interface for building a STUDY structure in EEGLAB provides a method for indexing segmented *.set files across subjects and independent variables.

#### **Building a study structure**

The STUDY structure in EEGLAB holds indexes for the segmented *.set files according to their participant ID as well as other independent variables. This information can be added manually while adding *.set files from a browsing interface.

![create study menu ]({{ page.root }}/fig/eeglab_study_menu_crop.png)

![create study gui ]({{ page.root }}/fig/create_study_gui.png)

Once a STUDY structure is present in the workspace the EEGLAB panel provides a brief summary of the STUDY structure properties.

![eeglab study summary ]({{ page.root }}/fig/eeglab_study_summary.png)

#### **Examine the STUDY Design**

Since a STUDY structure can index multiple independent variable it is possible to create several "Designs" that control how the indexed *.set files relate to each other in subsequent summary procedures.

![eeglab design menu ]({{ page.root }}/fig/eeglab_design_menu_crop.png)

![design gui ]({{ page.root }}/fig/design_gui.png)

#### **Pre-compute channel measures**

Once that the STUDY is created and the design reflects the intended analysis, channel measures can be calculated from the indexed segmented *.set files.

![eeglab precomp menu ]({{ page.root }}/fig/eeglab_precomp_menu_crop.png)

![precomp gui ]({{ page.root }}/fig/precomp_gui.png)

#### **Plot channel measures**

Having pre-computed channel measures, summary figures can be generated.

![study plot chan erp menu ]({{ page.root }}/fig/study_plot_chan_erp_menu_crop.png)

![study erp params gui ]({{ page.root }}/fig/study_erp_params_gui_crop.png)

![study chan erp fig ]({{ page.root }}/fig/study_chan_erp_fig_crop.png)

#### **Created STUDY structure automatically from files loaded in EEGLAB**

When segmented *.set files are indexed into a STUDY structure information is added into their EEG structure. Specifically, fields for "subject", "group", "condition" and "session" are populated. If these fields are populated during the segmentation of the data (or at some other point in script) then the STUDY structure can be created automatically from *.set files that are loaded into the workspace. We can accomplish this by loading data files that had their STUDY variable fields populated during their segmentation script execution.

![eeglab load multi brose ]({{ page.root }}/fig/eeglab_load_multi_browse.png)

The 'subject', 'group', 'condition' and 'session" fields of the EEG structure allow the STUDY import procedure to automatically populate the indexing of the independent variables in the STUDY design. 

![eeg indvars ]({{ page.root }}/fig/eeglab_eeg_indvars_note.png)

> ## Not really 'group', 'condition' and 'session'
> Although the fields of the EEG structure for automating the STUDY design population are named 'group', 'condition' and 'session' the independent variables that they refer to in practice could be anything (e.g. 'group' = 'up' in this case which is actually a property of the stimulus "upright"). It is best to think of these 'group', 'condition' and 'session' fields as "independent variable 1", "independent variable 2" and "independent variable 3".
>
> {: .source}
{: .callout}

Now, load the multiple files for sub-s02 and sub-s03 as well. Then create a STUDY with the loaded set files.

![create study loaded sets menu ]({{ page.root }}/fig/study_loaded_sets_menu_crop.png)

This results in the pre-populated independent variable fields.

![study loaded sets gui ]({{ page.root }}/fig/study_loaded_set_gui.png)

#### **Examine the multi-variable STUDY Design**

With this new STUDY design we have multiple independent variables, one for 'condition' (face vs. house) and another for 'group' (inverted vs. upright).`With the STUDY Design editor we can manipulate the way that summaries are build and comparisons are made across indexed variables.

![study design multi gui ]({{ page.root }}/fig/study_design_multi_gui.png)

#### **Build summary figures that overlay conditions**

Having established the STUDY Design figures can be generated that present and compare the indexed segmented *.set files in various ways. There are also options for running statistics within this interface.

![study multi erp param ]({{ page.root }}/fig/study_multi_erp_param.png)


![study multi erp fig ]({{ page.root }}/fig/study_multi_erp_fig_crop.png)

#### **Save the STUDY file**
The STUDY structures established can be save to file. The *.study files contain the indexing of all the *.set files to their independent variables as well as all the Design in the workspace at the time of the save. 

![study multi erp fig ]({{ page.root }}/fig/eeglab_save_study_menu_crop.png)

![save study browse ]({{ page.root }}/fig/save_study_browse.png)

> ## This is a good time to explore the STUDY and Design plotting capabilities
> Some favorites:
> 1. Topographical comparisons 
> 2. Exploratory statistical summaries
> 3. Single subject overlays
> 4. etc...
>
> {: .source}
{: .callout}

{% include links.md %}


