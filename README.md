# Thai-dialect ML-SUPERB speech translation experiment

This is the speech translation experiment from `THAI-DIALECT: LOW RESOURCE THAI DIALECTAL SPEECH TO TEXT CORPORA`, ML-SUPERB challenge, ASRU2023.

## experimental setup

We also utilzed S3PRL and ESPNet toolkit in this experiment. The Conformer and XLS-R were carried out to be our baselines. Conformer is Transformer-based encoder-decoder model using Conformer architecture as an encoder. XLS-R is conventional Auto-regressive Encoder-Decoder (AED) using XLS-R as a feature extraction. Configuration of each baseline model can be founded at `train_st_conformer.yaml` and `train_st_xls_r.yaml`.

In our paper, section 5, we described that we removed all spaces in transcriptions for ASR task since it can make the rote memorization. For ST task, spaces are kept for being possible to using BLEU score evaluation. 

## result


10min
|Model|Khummuang|Nan|Yno|Khmer|Korat|Laos|Krabi|Pattani|Phangnga|
|:----------|-:|-:|-:|-:|-:|-:|-:|-:|-:|
|Conformer  |6.0|3.0|7.5|2.1|0.8|5.1|58.4|1.3|1.2|
|XLS-R      |8.5|14.0|9.6|1.4|5.3|8.0|42.7|4.0|4.6|

1h
|Model|Khummuang|Nan|Yno|Khmer|Korat|Laos|Krabi|Pattani|Phangnga|
|:----------|-:|-:|-:|-:|-:|-:|-:|-:|-:|
|conformer|8.4|8.8|7.4|0.1|6.2|2.4|58.4|0.6|1.5|
|XLS-R|31.7|24.7|8.1|3.7|14.0|9.7|58.8|5.4|7.3|

## Acknowledgement

We would like to thank the PMU-C grant (Thai Language Automatic Speech Recognition Interface for Community E-Commerce, C10F630122)
for the support of this research. 
We also would like to acknowledge the Apex compute cluster team which provides compute support for this project.
