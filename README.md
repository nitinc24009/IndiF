# INDICA: An Audio Indic-Language Telecom Fraud Analysis Benchmark

<p align="center">
  <b>Multilingual | Audio + Text | Benchmark for Fraud Detection</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Dataset-189K%2B%20Samples-blue">
  <img src="https://img.shields.io/badge/Languages-10-green">
  <img src="https://img.shields.io/badge/Tasks-3-orange">
  <img src="https://img.shields.io/badge/Modalities-Audio%20%2B%20Text-purple">
</p>

---

## Overview

INDICA is a comprehensive benchmark for telecom fraud call analysis in Indic languages.  
It is built on the IndiF dataset, the first large-scale multilingual dataset for fraud detection in telecom conversations.

This benchmark enables research in:
- Scenario Classification
- Fraud Call Detection
- Fraud-Type Classification

INDICA addresses key challenges:
- Lack of multilingual datasets  
- Limited reproducibility  
- Poor cross-lingual generalization  

---

## Key Contributions

- **IndiF Dataset**
  - 189,420 samples across 10 Indic languages  
  - Audio + text modalities  
  - Fine-grained annotations  

- **INDICA Benchmark**
  - Evaluation across speech, text, and multimodal models  
  - Standardized experimental setup  

- **Multilingual Setup**
  - Enables robust cross-lingual evaluation  

---

## Dataset: IndiF

### Languages
Assamese, Bengali, English, Gujarati, Hindi, Kannada, Malayalam, Odia, Tamil, Telugu

### Dataset Statistics

| Property | Value |
|---------|------|
| Total Samples | 189,420 |
| Languages | 10 |
| Samples per Language | 18,942 |
| Modalities | Audio + Text |
| Tasks | 3 |

### Annotations

- Scenario Classification (7 categories)  
- Fraud vs Non-Fraud (Binary)  
- Fraud-Type Classification (7 types)  

---

## Tasks

### Scenario Classification
- Customer Service  
- Delivery  
- Ride-hailing  
- Retail Transactions  
- Appointment Scheduling  
- Food Ordering  
- Traffic Information  

### Fraud Detection

```
Fraud vs Non-Fraud
```

### Fraud-Type Classification

- Banking Fraud  
- Customer Service Impersonation  
- Investment Scam  
- Phishing  
- Lottery Scam  
- Kidnapping  
- Identity Theft  

---

## Models

### Speech Models
- Wav2Vec2  
- WavLM  
- HuBERT  
- Whisper  
- XLS-R  

### Text Models
- XLM-RoBERTa  
- IndicBERTv2  
- MuRIL  

---

## Methodology

### Unimodal Approaches
- Fully Connected Network (FCN)  
- CNN-based architectures  

### Multimodal Fusion
- Concatenation  
- Cross-Attention  

---

## Training Setup

```
Optimizer: AdamW
Learning Rate: 1e-3
Batch Size: 32
Epochs: 5
Validation: 5-Fold Cross Validation
```

---

## Key Findings

- Text models outperform audio and multimodal approaches  
- Fraud Detection is the easiest task  
- Fraud-Type Classification is the most challenging  
- Performance varies across languages (high-resource > low-resource)  

---

## Limitations

- Synthetic audio generated via TTS  
- Limited speaker diversity  
- Restricted to Indic languages  
- Uniform dataset distribution  

---

## Future Work

- Real-world multilingual datasets  
- Improved multimodal fusion  
- Better low-resource modeling  
- Fine-grained fraud intent understanding  

---

## Project Structure

```
INDICA/
│── dataset/
│   ├── Audio_samples/
│   ├── Text_samples/
│   ├── metadata/
│   │   ├── audio_metadata.csv
│   │   ├── text_metadata.csv
│   │   └── final_multimodal_dataset.csv
│
│── scripts/
│   ├── generate_audio_metadata.py
│   ├── generate_text_metadata.py
│   ├── merge_audio_text_metadata.py
│
│── models/
│── notebooks/
│── results/
│
│── README.md
│── requirements.txt
```

---

## Resources

- Dataset: https://huggingface.co/datasets/vikrant-vikram/INDICA  
- Google Drive: https://drive.google.com/drive/folders/1kis1b8sVOypv4xNb-QhB8pch4J9gYVZ-?usp=share_link  
- Paper: INDICA: An Audio Indic-Language Telecom Fraud Analysis Benchmark  

---

## Dataset Files

- Gujarati_audio.tar.gz — Gujarati audio  
- Hindi_audio.tar.gz — Hindi audio  
- Tamil_audio.tar.gz — Tamil audio  
- Text_samples.tar.gz — Text data
- ....... 

---

## How to Use

### Download

```bash
hf download vikrant-vikram/INDICA Gujarati_audio.tar.gz
hf download vikrant-vikram/INDICA Hindi_audio.tar.gz
hf download vikrant-vikram/INDICA Tamil_audio.tar.gz
hf download vikrant-vikram/INDICA Text_samples.tar.gz
......
```

### Extract

```bash
tar -xzf Gujarati_audio.tar.gz
tar -xzf Hindi_audio.tar.gz
tar -xzf Tamil_audio.tar.gz
tar -xzf Text_samples.tar.gz
....
```

### Structure

```
Audio_samples/
├── Gujarati/
├── Hindi/
├── Tamil/
....

Text_samples/
├── Gujarati/
├── Hindi/
├── Tamil/
....
```

---

## Authors

- Nitin Choudhury  
- Samyuktha Chilaka  
- Bikrant Bikram Pratap Maurya  
- Arun Balaji Buduru  

---

## Citation

```bibtex
@inproceedings{indica2026,
  title={INDICA: An Audio Indic-Language Telecom Fraud Analysis Benchmark},
  author={Choudhury, Nitin and Chilaka, Samyuktha and Maurya, Bikrant and Buduru, Arun},
  year={2026}
}
```
