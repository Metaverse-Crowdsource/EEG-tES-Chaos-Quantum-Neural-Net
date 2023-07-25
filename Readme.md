<h1 align="center">EEG tES Chaos Neural Net</h1>

---

**Article:** [https://doi.org/10.1038/s41597-021-01046-y](https://doi.org/10.1038/s41597-021-01046-y)

**Dataset:** [https://zenodo.org/record/3840615#.ZK2hJdLMKRQ](https://zenodo.org/record/3840615#.ZK2hJdLMKRQ)

**Table of stimulation condition and stimulation intensity:** [https://www.nature.com/articles/s41597-021-01046-y/tables/2](https://www.nature.com/articles/s41597-021-01046-y/tables/2)

---

Data include within participant application of nine High-Definition tES (HD-tES) types, targeting three cortical regions (frontal, motor, parietal) with three stimulation waveforms (DC, 5 Hz, 30 Hz); more than 783 total stimulation trials over 62 sessions with EEG, physiological (ECG, EOG), and continuous behavioral vigilance/alertness metrics. Experiment 1 and 2 consisted of participants performing a continuous vigilance/alertness task over three 70-minute and two 70.5-minute sessions, respectively. Demographic data were collected, as well as self-reported wellness questionnaires before and after each session. Participants received all 9 stimulation types in Experiment 1, with each session including three stimulation types, with 4 trials per type. Participants received 2 stimulation types in Experiment 2, with 20 trials of a given stimulation type per session. Within-participant reliability was tested by repeating select sessions. This unique dataset supports a range of hypothesis testing including interactions of tDCS/tACS location and frequency, brain-state, physiology, fatigue, and cognitive performance.

Participants maintained a ball at the center of the screen and were periodically stimulated (with low-intensity noninvasive brain stimulation) for 30 secs with combinations of 9 stimulation montages.

---

| Variable       | Description                                                         |
|----------------|---------------------------------------------------------------------|
| DSamp          |                                                                     |
| triggers       | These are all the labeled EEG/Stimulation start/stop triggers       |
| EEGdata        | Contains the downsampled EEG/ECG/EOG voltage data dims: 35 channels X ~4E6 samples |
| fs             | The downsampled sampling frequency of the data: 1000 Hz             |
| fsOld          | The original sampling frequency of the data                         |
| time           | Time vector for the data. Should be 1 X ~4E6                        |
| label          | Contains the channel label information. BIP1= ECG, BIP2=EOG, RESP1= N/A |
| nchan          | The number of channels in the data                                  |
| rate           | Redundant to fs, sampling rate of data                              |
| npt            | Number of data points ~4E6                                          |
| Subj           | Subject and session that data belong to. I.e. 0302 - Subject 03 session 03 |
| ptrackerPerf   | The CTT data deviation/ the behavioral data                         |
| ptrackerTime   | Time vector for the CTT data                                        |
| ptrackerfs     | The sampling frequency for the CTT data: 100 Hz                     |

