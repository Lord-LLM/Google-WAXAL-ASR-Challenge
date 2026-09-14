# Google WAXAL ASR Challenge 🎙️🌍

An Automatic Speech Recognition (ASR) project developed for the **Google WAXAL ASR Challenge** hosted on [Zindi](https://zindi.world/competitions/google-waxal-asr-challenge).

---

##  Overview

The **Google WAXAL ASR Challenge** focuses on advancing speech recognition technologies for underrepresented African languages. By building robust, generalized speech-to-text models, the initiative aims to bridge linguistic gaps, improve accessibility, and empower native speakers with digital tools in their local languages.

---

##  Target Languages

The competition highlights speech datasets across key African languages:
- **Luganda (`lug`)** – Widely spoken in Uganda
- **Lingala (`lin`)** – Spoken across the Democratic Republic of the Congo and the Republic of the Congo
- **Shona (`sna`)** – Spoken predominantly in Zimbabwe

---

##  Challenge Objective

The goal is to develop machine learning and deep learning models that can transcribe spoken audio recordings into accurate text transcriptions across unseen acoustic conditions and speakers.

---

## Evaluation Metric

Submissions are evaluated on the test dataset using a combination of standard speech recognition error metrics:

- **Word Error Rate (WER)** (50% weight) – Measures word-level transcription accuracy.
- **Character Error Rate (CER)** (50% weight) – Measures character-level robustness, accounting for spelling variations and phonetic nuances.

The final evaluation score reflects the weighted combination:
$$\text{Score} = 1 - \frac{\text{WER} + \text{CER}}{2}$$

*(Higher score indicates better transcription quality and fewer errors)*

---

## Repository Contents

| Component | Description |
| :--- | :--- |
| **`WAXAL_EDA.ipynb`** | Exploratory Data Analysis covering audio durations, sampling rates, vocabulary distributions, and waveform visualizations. |
| **`Waxal_Challenge_Starter_Code.ipynb`** | Starter pipeline for data loading, audio preprocessing, and benchmark setup. |
| **`WHISPER_BASELINE.ipynb`** | ASR pipeline utilizing OpenAI's Whisper model. |
| **`WAVE2VEC_BASELINE.ipynb`** | Fine-tuning and evaluation using Facebook's Wav2Vec 2.0 acoustic representations. |
| **`MMS_1B_BASELINE.ipynb`** | High-capacity multilingual transcription pipeline using Meta's Massively Multilingual Speech (MMS 1B) model. |
| **`Train.csv` / `Test.csv` / `Test_Phase2.csv`** | Dataset metadata files linking audio IDs to transcripts and phase splits. |
| **`waxal_eda_overview.png` / `waxal_waveforms.png`** | Exploratory plots illustrating waveform samples and dataset attributes. |

---

## Modeling Strategies & Approaches

1. **Exploratory Analysis & Preprocessing**: Audio resample normalization (16 kHz), silence trimming, transcript text cleaning, and vocabulary mapping.
2. **Transfer Learning**: Leveraging state-of-the-art pretrained multilingual speech foundation models (Whisper, Wav2Vec2, and MMS 1B).
3. **Language-Specific Fine-Tuning**: Adapting acoustic encoders and connectionist temporal classification (CTC) / seq2seq decoders to African phonetic structures.
