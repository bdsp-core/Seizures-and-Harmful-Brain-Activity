---
layout: default
title: "Frequently Asked Questions"
permalink: /faq
---


**Q: In the contest description it says that the data is in 10 second segments, but in the notebook it appears that they are 50 second segments at 200hz?**

A: It is 50sec for all EEG segments (updated in the description attached). The expert labels only apply to the central 10sec, with 20sec before and after as context.
When labeled the EEG, experts did have the freedom to pan in time +/- 20-sec to make decision for the **central** 10-sec, plus a 10min spectrogram centered at the same time of EEG for more information especially for data evolution in larger time scale.
We provided all these in case teams also find this data useful for model training

**Q: Also there are 20 channels apparently.  Are the channels labeled?**

A: Yes, they are labelled in the order of Fp1 F3 C3 P3 F7 T3 T5 O1 Fz Cz Pz Fp2 F4 C4 P4 F8 T4 T6 O2 (EKG)

**Q: What are the spectrograms that are labeled?**

A: It is 10-min regional average spectrograms from bipolar data centered at the same time of EEG.

**Q: What montage did the readers use?**

A: The raw data is in C2 referential montage, with the 1st 19 channels being the EEG and the last channel being the EKG channel; the users were able to switch between bipolar and average montages. In our papers, the models were trained in bipolar montage.

**Q: What is the scale?**

A: In the unit of micro-volts

**Q: Is this the raw data or is it filtered?**

A: The data is raw data.

**Q: Is it 10 or 50 that the readers saw?**

A: All samples were parsed in 50sec, where the expert label only applied to the central 10sec, with extra 20sec before and after as contextual information in case teams also find this data useful for model training.

**Q: Why are different sample files different sizes?**

A: The duration of EEG is always 50sec, for spectrogram is always 10min. If we are talking about the physical file size, the "unlabeled" samples do not have the "vote" variable in the data structure, and also it may vary a lot due to the spectrogram – sometimes it is less than 10min (eg. at the beginning or the end of the recording), we just zero-padded the rest to have complete 10min.

**Q: Is unlabeled data also in 50 second segments?  Why and how was it selected?**

A: Yes, it is also in 50sec. They come from the same patient cohort without expert labels used in the paper: “Neurology. 2023 Apr 25;100(17):e1750-e1762. doi: 10.1212/WNL.0000000000207127. Epub 2023 Mar 6. Development of Expert-Level Classification of Seizures and Rhythmic and Periodic Patterns During EEG Interpretation”
