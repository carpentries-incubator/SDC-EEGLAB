---
title: Setup
---

### Download and install MATLAB

You will need a fairly recent version of MATLAB (procedure tested on MATLAB 2012b and newer versions). For detailed installation instructions, click [here](https://www.mathworks.com/help/compiler/install-the-matlab-runtime.html).

### Obtain lesson materials

1. Download the Face13 tutorial dataset from this [google drive](https://drive.google.com/file/d/1AWgN0DOstCw7UB5puxHL_beddNzPZ__v/view?usp=sharing). 
2. Download the initalization suite from this [google drive](https://drive.google.com/file/d/1p1OCsOdu27Tg_QYhNx_mJIkNm3ygyekr/view?usp=sharing)
3. Create a folder called `Face13` on your Desktop.
4. Move the downloaded folders to `Face13`.
5. Unzip the folders. 

You should see two folders called `sourcedata` and `code` in the `Face13` directory on your Desktop. The `sourcedata` folder contains the EEG data and standard montages that are used during initialization. The `code` folder contains a version of EEGLAB and the necessary scripts to intialize the data into a BIDS compliant folder structure.

### Initalizing data into the BIDS standard

To run through this EEGLAB tutorial, the data needs to be initialized and in the BIDS standard. The following steps to initialize the data assume familiarity with BIDS and Matlab console use. If you do not have experience using BIDS or Matlab, more detailed steps for intilizing data can be found in the [BIDS-EEG-EEGLAB tutorial](https://carpentries-incubator.github.io/SDC-BIDS-EEG-EEGLAB/).

1. In Matlab, navigate to the `Face13` folder.
2. To set the path and open EEGLAB, in Matlab Command Window type:
    ~~~
    >> addpath code/BIDS-Init-Face13-EEGLAB
    >> addpath code/BIDS-Init-Face13-EEGLAB/eeglab
    >>eeglab
    ~~~
    {: .source}
3. To make the data compliant with BIDS, run the `bids_face13.m` script in the Matlab Command Window:
    ~~~
    >> bids_face13
    ~~~
    {: .source}
4. In the file chooser window that pops up when running the `bids_face13.m` scipt, select the **Face13** directory. This will create `sub-*/eeg/` folders in the `Face13` directory.

{% include links.md %}
