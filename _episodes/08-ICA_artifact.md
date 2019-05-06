---
title: "ICA artifact isolation (removal)"
teaching: 0
exercises: 0
questions:
- "How can ICA be used to isolate signal from noise?"
- "What types of EEG artifacts can be isolated with ICA"
- "How are ICA corrections performed?"
objectives:
- "Understand how ICA can be used to clean EEG from specific types of artifacts"
keypoints:
- "Some EEG artifacts in EEG can be isolated with ICA"
---
## An ICA model provides a signal factor layer to the EEG file

#### **With an ICA model present in the EEG structure factors can be purged from the data instead of channels or time points**

Explore the components in relation to the scalp data.

![load ll browse ]({{ page.root }}/fig/eeglab_load_ll_browse.png)

![marks sel menu]({{ page.root }}/fig/eeglab_marks_sel_menu_crop.png)

![marks sel gui]({{ page.root }}/fig/mark_sel_gui.png)

![marks sel gui]({{ page.root }}/fig/scroll_art_topo.png)

![ica scroll]({{ page.root }}/fig/ica_scroll_fig.png)

![ica dipfit]({{ page.root }}/fig/dipfit_fig.png)


> ## How to generate the ica plots
> ![ica scroll]({{ page.root }}/fig/eeglab_ica_scroll_menu_crop.png)
> ![ica topo]({{ page.root }}/fig/eeglab_ica_topo_menu_crop.png)
> ![dipfit menu]({{ page.root }}/fig/eeglab_dipfit_menu_crop.png)
> ![dipfit gui]({{ page.root }}/fig/dipfit_gui.png)
>
> {: .source}
{: .callout}

Remove ICs.

![remove ic menu]({{ page.root }}/fig/eeglab_rm_comp_menu_crop.png)

![remove ic gui]({{ page.root }}/fig/rm_comp_gui.png)

![remove ic confirm]({{ page.root }}/fig/rm_comp_conf_crop.png)

![remove ic scroll]({{ page.root }}/fig/rm_comp_scroll.png)

{% include links.md %}

