# Class for Kojima2024A dataset management. P300 dataset

Class for Kojima2024A dataset management. P300 dataset.

## Dataset Overview

- **Code**: Kojima2024A
- **Paradigm**: p300
- **DOI**: 10.7910/DVN/MQOVEY
- **Subjects**: 11
- **Sessions per subject**: 1
- **Events**: Target=1, NonTarget=0
- **Trial interval**: [-0.5, 1.2] s
- **Runs per session**: 6
- **File format**: BrainVision
- **Number of contributing labs**: 1

## Acquisition

- **Sampling rate**: 1000.0 Hz
- **Number of channels**: 64
- **Channel types**: eeg=64, eog=2
- **Channel names**: AF3, AF4, AF7, AF8, AFz, C1, C2, C3, C4, C5, C6, CP1, CP2, CP3, CP4, CP5, CP6, CPz, Cz, F1, F2, F3, F4, F5, F6, F7, F8, FC1, FC2, FC3, FC4, FC5, FC6, FCz, FT10, FT7, FT8, FT9, Fp1, Fp2, Fz, O1, O2, Oz, P1, P2, P3, P4, P5, P6, P7, P8, PO3, PO4, PO7, PO8, POz, Pz, T7, T8, TP10, TP7, TP8, TP9, hEOG, vEOG
- **Montage**: standard_1020
- **Hardware**: Brain Amp DC (Brain Products GmbH, Germany) and MR plus (Brain Products GmbH, Germany)
- **Reference**: right earlobe
- **Ground**: left earlobe
- **Sensor type**: eeg
- **Line frequency**: 50.0 Hz
- **Online filters**: {'bandpass': '0.1 Hz to 100 Hz'}
- **Cap manufacturer**: EASYCAP GmbH
- **Electrode material**: Ag-AgCl
- **Auxiliary channels**: EOG (2 ch, vertical, horizontal)

## Participants

- **Number of subjects**: 11
- **Health status**: healthy
- **Age**: mean=22.5, min=22.0, max=23.0
- **Gender distribution**: male=10, female=1
- **Species**: human

## Experimental Protocol

- **Paradigm**: p300
- **Task type**: auditory selective attention
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Tasks**: attend to Stream 1, attend to Stream 2, attend to Stream 3
- **Study design**: within-subject
- **Study domain**: auditory BCI
- **Feedback type**: none
- **Stimulus type**: auditory musical tones
- **Stimulus modalities**: auditory
- **Primary modality**: auditory
- **Synchronicity**: synchronous
- **Mode**: offline
- **Training/test split**: False
- **Instructions**: Subjects were requested to attend to one of three streams and to count the number of target stimuli in the attended stream
- **Stimulus presentation**: method=Digital signal processor (System3, Tucker-Davis Technologies, USA) and headphones (HDA200, Sennheiser), ear=right ear only, tone_generator=Software synthesizer (Piano tones Grand Piano 1 SE from SampleTank3, IK multimedia Production, Italy)

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300
- **Number of targets**: 3
- **Stimulus onset asynchrony**: 180.0 ms

## Data Structure

- **Blocks per session**: 6
- **Block duration**: 300.0 s
- **Trials context**: Each task block had 3 runs (5 minutes each). Subjects counted target stimuli in Streams 1, 2, and 3 on the 1st, 2nd, and 3rd measurements respectively. Task block was repeated twice.

## Preprocessing

- **Data state**: raw
- **Preprocessing applied**: False

## Signal Processing

- **Classifiers**: Logistic Regression, Minimum Distance to Mean (MDM)
- **Feature extraction**: xDAWN spatial filtering, Riemannian geometry covariance matrices
- **Frequency bands**: analyzed=[1.0, 40.0] Hz
- **Spatial filters**: xDAWN

## Cross-Validation

- **Method**: 10-fold cross validation
- **Folds**: 10
- **Evaluation type**: within-subject

## Performance (Original Study)

- **Description**: Classification accuracy over 80% for 5 subjects, over 75% for 9 subjects
- **Metric**: MCC (Matthews correlation coefficient)

## BCI Application

- **Applications**: communication
- **Environment**: laboratory
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: auditory
- **Type**: EEG, P300, BCI

## Documentation

- **Description**: A 3-class auditory BCI using three tone sequences based on auditory stream segregation. Musical tones were presented to subjects' right ear, and subjects attended to one of three streams while counting target stimuli. P300 activity was elicited by target stimuli in the attended stream.
- **DOI**: 10.1371/journal.pone.0303565
- **Associated paper DOI**: 10.1371/journal.pone.0303565
- **License**: CC0-1.0
- **Investigators**: Simon Kojima, Shin'ichiro Kanoh
- **Senior author**: Shin'ichiro Kanoh
- **Contact**: nb21106@shibaura-it.ac.jp
- **Institution**: Shibaura Institute of Technology
- **Department**: Graduate School of Engineering and Science; College of Engineering
- **Address**: Koto-ku, Tokyo, Japan
- **Country**: JP
- **Repository**: Harvard dataverse
- **Data URL**: https://doi.org/10.7910/DVN/MQOVEY
- **Publication year**: 2024
- **Funding**: JSPS KAKENHI Grant Number JP23K11811
- **Ethics approval**: Review Board on Bioengineering Research Ethics of Shibaura Institute of Technology; Declaration of Helsinki
- **Keywords**: auditory BCI, P300, auditory stream segregation, selective attention, oddball paradigm, Riemannian geometry

## External Links

- **Source**: https://doi.org/10.7910/DVN/MQOVEY
- **Paper**: https://doi.org/10.1371/journal.pone.0303565

## Abstract

In this study, we attempted to improve brain-computer interface (BCI) systems by means of auditory stream segregation in which alternately presented tones are perceived as sequences of various different tones (streams). A 3-class BCI using three tone sequences, which were perceived as three different tone streams, was investigated and evaluated. Each presented musical tone was generated by a software synthesizer. Eleven subjects took part in the experiment. Stimuli were presented to each user's right ear. Subjects were requested to attend to one of three streams and to count the number of target stimuli in the attended stream. In addition, 64-channel electroencephalogram (EEG) and two-channel electrooculogram (EOG) signals were recorded from participants with a sampling frequency of 1000 Hz. The measured EEG data were classified based on Riemannian geometry to detect the object of the subject's selective attention. P300 activity was elicited by the target stimuli in the segregated tone streams. In five out of eleven subjects, P300 activity was elicited only by the target stimuli included in the attended stream. In a 10-fold cross validation test, a classification accuracy over 80% for five subjects and over 75% for nine subjects was achieved. For subjects whose accuracy was lower than 75%, either the P300 was also elicited for nonattended streams or the amplitude of P300 was small. It was concluded that the number of selected BCI systems based on auditory stream segregation can be increased to three classes, and these classes can be detected by a single ear without the aid of any visual modality.

## Methodology

Musical tones generated by a digital auditory workstation were used as auditory stimuli. Piano tones from a MIDI sound source were presented using a digital signal processor and headphones to participants' right ear only. Three tone streams were created using auditory stream segregation, each consisting of standard (90% probability) and deviant (10% probability) tones. The duration of each tone was 150 ms with stimulus onset asynchrony of 180 ms. The 64-channel EEG and 2-channel EOG signals were recorded at 1000 Hz. Each experiment consisted of two task blocks with three runs each (5 minutes per run). Subjects counted target stimuli in different streams across runs. Data analysis involved bandpass filtering (0.1-40 Hz for ERP analysis, 1-40 Hz for classification), baseline correction, artifact rejection (±100μV for EEG, ±500μV for EOG), xDAWN spatial filtering, and classification using Riemannian geometry with covariance matrices and logistic regression. Performance was evaluated using 10-fold cross validation with accuracy and Matthews correlation coefficient (MCC) metrics.

## References

Kojima, S. (2024). Replication Data for: An auditory brain-computer interface based on selective attention to multiple tone streams. Harvard Dataverse, V1. DOI: https://doi.org/10.7910/DVN/MQOVEY

Kojima, S. & Kanoh, S. (2024). An auditory brain-computer interface based on selective attention to multiple tone streams. PLoS ONE 19(5): e0303565. DOI: https://doi.org/10.1371/journal.pone.0303565
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
