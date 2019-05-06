---
title: "Summarizing EEG data measures across recordings"
teaching: 0
exercises: 0
questions:
- "How are group level summaries generated in EEGLAB via the STUDY structure?"
- "Organizing the data for the STUDY structure"
- "Plotting group level ERPs and making comparissons"
objectives:
- "Undertand how to summarize and visualize data across EEG sessions"
- "Understand the relationship of single session 'set' files in relation the STUDY structure"
- "Undertand how to explore the EEG data measures across groups, condiditons, etc."
keypoints:
- "Making summaries and comparisons of outcome measures"
---
## The STUDY structure in EEGLAB allows for the summary of mesures across set files

#### **EEGLAB's STUDY structure contains the information to coordinate across multiple files**

Having worked with single EEG files and then having scripted across files it is now a good time to explore how EEGLAB enables group summaries of set files. The process of building a STUDY structure and the defining designs within it allows users to summaries measures across multiple files or test differneces across independent variables.

The interface for building a STUDY structure in EEGLAB provides a method for indexing segmented *.set across subjects and independent variables.


![create study menu ]({{ page.root }}/fig/eeglab_study_menu_crop.png)

![create study gui ]({{ page.root }}/fig/create_study_gui.png)

![eeglab study summary ]({{ page.root }}/fig/eeglab_study_summary.png)

![eeglab design menu ]({{ page.root }}/fig/eeglab_design_menu_crop.png)

![design gui ]({{ page.root }}/fig/design_gui.png)

![eeglab precomp menu ]({{ page.root }}/fig/eeglab_precomp_menu_crop.png)

![precomp gui ]({{ page.root }}/fig/precomp_gui.png)

![study plot chan erp menu ]({{ page.root }}/fig/study_plot_chan_erp_menu_crop.png)

![study erp params gui ]({{ page.root }}/fig/study_erp_params_gui_crop.png)

![study chan erp fig ]({{ page.root }}/fig/study_chan_erp_fig_crop.png)

#### **STUDY structures can be created automatically from files loaded in EEGLAB**

![eeglab load multi brose ]({{ page.root }}/fig/eeglab_load_multi_browse.png)

The 'subject', 'group', 'condition' and 'session" fields of the EEG structure allow the STUDY import procedure to automatically populate the indexing of the independent variables in the STUDY design. 

![eeg indvars ]({{ page.root }}/fig/eeglab_eeg_indvars_note.png)

> ## Not really 'group', 'condition' and 'session'
> Although the fields of the EEG structure for automating the STUDY design population are named 'group', 'condition' and 'session' the indepentent variables that they refer to in practice could be anything (e.g. 'group' = 'up' in this case which is actually a property of the stimulus "upright"). It is best to think of these 'group', 'condition' and 'session' fields as "independent variable 1", "independent variable 2" and "independent variable 3".
>
> {: .source}
{: .callout}

Now load the multiple files for sub-s02 and sub-s03 as well. Then create a STUDY with the loaded set files.

![create study loaded sets menu ]({{ page.root }}/fig/study_loaded_sets_menu_crop.png)

This results in the pre-populated independent variable fields.

![study loaded sets gui ]({{ page.root }}/fig/study_loaded_set_gui.png)

Now looking at the STUDY design we have multiple indpenedent variables, one for 'condition' and another for 'group'.

![study design multi gui ]({{ page.root }}/fig/study_design_multi_gui.png)

![study multi erp param ]({{ page.root }}/fig/study_multi_erp_param.png)

![study multi erp fig ]({{ page.root }}/fig/study_multi_erp_fig_crop.png)

![study multi erp fig ]({{ page.root }}/fig/eeglab_save_study_menu_crop.png)

![save study browse ]({{ page.root }}/fig/save_study_browse.png)

{% include links.md %}


