---
title: "Basic ERP processing"
teaching: 0
exercises: 0
questions:
- "How is data loaded into EEGLAB's EEG structure"
- "How can data be viewed from EEGLAB"
- "How can Event Related Potentials be generated in EEGLAB"
objectives:
- "Understand how to view and process data in EEGLAB"
keypoints:
- "Working with the data in EEGLAB"
---
## How to generate ERPs from an EEG recording using a basic procedure

#### **Import or Load a set file into EEGLAB**

Let's start with a new set file. Here is how to clear existing EEG structures from workspace:

![eeglab clear]({{ page.root }}/fig/eeglab_clear_crop.png)

Now open a new file (perhaps participant 02) and lets process this one file though until we have an Event Related Potential (ERP).

#### **Rereference to the average channel**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_reref_menu_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/reref_gui.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/reref_rename.png)

#### **Filter the data**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_filt_menu_crop.png)
#### **Parameters for the 1Hz high pass**
![Matlab Integrated Development Environment]({{ page.root }}/fig/filt_hp1_gui.png)
#### **Repeat for the 30Hz low pass**
![Matlab Integrated Development Environment]({{ page.root }}/fig/filt_lp30_gui.png)

#### **Remove bad channels**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_chanrej_menu_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/chanrej_gui.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/chanrej_scroll.png)

#### **Rereference to the average channel**


#### **Segment the data relative to face stimulus events**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_epoch_menu_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/epoch_gui.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/epoch_bl_gui.png)

#### **Remove bad time segments (epochs)**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_rmep_menu_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/rmep_gui_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/rmep_scroll.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_rmep_rej.png)

#### **save the segmented data**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_save_menu_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_save_browser.png)

#### **plot scalp ERPs**

![Matlab Integrated Development Environment]({{ page.root }}/fig/eeglab_plotERP_menu_crop.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/plotERP_gui.png)
![Matlab Integrated Development Environment]({{ page.root }}/fig/plotERP_fig.png)

{% include links.md %}

