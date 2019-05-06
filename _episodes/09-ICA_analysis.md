---
title: "ICA hypothesis testing"
teaching: 0
exercises: 0
questions:
- "How can hypothesis testing be performed on ICs instead of scalp signals?"
- "What tools are available for visualizing ICA ERPs?"
- "How can we examine ICs across subjects in a group analysis?"
objectives:
- "Perform data summaries and statistics on ICs in a addition to scalp channels"
keypoints:
- "Increasing the measurement specificity by analysing ICs"
---
## If ICA is able to isolate stationary signals for artifacts it may also be able to isolate cortical sources

#### **How can we identify cortical components?**

We can examine which independent components account for specific ERP patterns by comparing the scalp ERPs with topographies to the the ERP component envelope plots. In order to accomplish this we can load segmented files one at a time and examine which ICs account for various ERPs patterns. Lets start with sub-s01.


![load ll browse ]({{ page.root }}/fig/eeglab_load_ic_test.png)

![ic id menu]({{ page.root }}/fig/eeglab_ic_id_scalp_menu_crop.png)

![erp topo gui]({{ page.root }}/fig/erp_scalp_topo_gui.png)

![erp top fig]({{ page.root }}/fig/erp_scalp_topo_fig.png)

![ic topo fig]({{ page.root }}/fig/erp_ic_topo_fig.png)


> ## How to generate the ICA plots
> ![ica scroll]({{ page.root }}/fig/erp_ic_topo_menu_crop.png)
> ![ica topo]({{ page.root }}/fig/erp_ic_topo_gui.png)
>
> {: .source}
{: .callout}

## Identify the dominant ICs accounting for the P100 and N170 in each recording
1. sub-s01		P100: 1		N170: 4,8
2. sub-s02		P100: 3, 9, 13	N170: 1, 7
3. sub-s03		P100: 2		N170: 3
4. sub-s04		P100: 2		N170: 1
5. sub-s05		P100: 2, 13	N170: 1
6. sub-s06		P100: 1		N170: 4
7. sub-s07		P100: 6, 10	N170: 4, 16
8. sub-s08		P100: 2, 5	N170: 1, 7, 19
9. sub-s09		P100: 21, 22	N170: 1, 6, 13
10. sub-s10		P100: 1, 3, 4	N170: 2

## Load a STUDY structure and cluster components

![load study menu]({{ page.root }}/fig/eeglab_load_study_menu_crop.png)

![load study browse]({{ page.root }}/fig/load_study_browse.png)

![study design menu]({{ page.root }}/fig/eeglab_study_design_menu_crop.png)

![study design gui]({{ page.root }}/fig/study_design_gui.png)

![study pre compute IC menu]({{ page.root }}/fig/eeglab_pre_comp_menu_crop.png)

![study pre compute IC gui]({{ page.root }}/fig/pre_comp_gui.png)

![study pre clust menu]({{ page.root }}/fig/eeglab_pre_clust_menu_crop.png)

![study pre clust gui]({{ page.root }}/fig/pre_clust_gui.png)

![clust comp menu]({{ page.root }}/fig/eeglab_clust_comp_menu_crop.png)

![clust comp gui]({{ page.root }}/fig/clust_comp_gui.png)

![edit clust comp new gui]({{ page.root }}/fig/edit_clust_new_gui_crop.png)

![new clust gui]({{ page.root }}/fig/new_clust_gui.png)

![new clust n170 gui]({{ page.root }}/fig/new_clust_n170_gui.png)

![reasgn comp gui sel]({{ page.root }}/fig/reasgn_comp_gui_sel_crop.png)

![reasgn comp gui p100]({{ page.root }}/fig/reasgn_gui_p100.png)

![reasgn comp gui ok]({{ page.root }}/fig/reasgn_comp_gui_ok.png)

![save study clust]({{ page.root }}/fig/eeglab_save_study_clust_menu_crop.png)

![save study clust browse]({{ page.root }}/fig/save_study_clust_browse.png)

![plot clust menu]({{ page.root }}/fig/eeglab_plot_clust_menu_crop.png)

![plot clust gui]({{ page.root }}/fig/plot_clust_gui.png)

![plot clust figs]({{ page.root }}/fig/clust_plot_figs.png)

![plot clust topo figs]({{ page.root }}/fig/clust_topo_figs.png)

{% include links.md %}

