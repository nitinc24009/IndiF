 INDICA: An Audio Indic-Language Telecom Fraud Analysis Benchmark

<p align="center">
  <b> Multilingual |  Audio + Text |  Benchmark for Fraud Detection</b>
</p>


<p align="center">
  <img src="https://img.shields.io/badge/Dataset-189K%2B%20Samples-blue">
  <img src="https://img.shields.io/badge/Languages-10-green">
  <img src="https://img.shields.io/badge/Tasks-3-orange">
  <img src="https://img.shields.io/badge/Modalities-Audio%20%2B%20Text-purple">
</p>



⸻

Overview

INDICA is a comprehensive benchmark for telecom fraud call analysis in Indic languages.
It is built on the IndiF dataset, the first large-scale multilingual dataset for fraud detection in telecom conversations.

This benchmark enables research in:
	•	 Scenario Classification
	•	 Fraud Call Detection
	•	 Fraud-Type Classification

INDICA addresses key challenges in existing systems:
	•	Lack of multilingual datasets
	•	Limited reproducibility
	•	Poor cross-lingual generalization

⸻

 Key Contributions
	•	IndiF Dataset
	•	189,420 samples across 10 Indic languages
	•	Audio + text modalities
	•	Fine-grained annotations
	•	 INDICA Benchmark
	•	Evaluation across speech, text, and multimodal models
	•	Standardized experimental setup
	•	 Multilingual Setup
	•	Enables robust cross-lingual evaluation

⸻

 Dataset: IndiF

 Languages

Assamese, Bengali, English, Gujarati, Hindi, Kannada, Malayalam, Odia, Tamil, Telugu

⸻

 Dataset Statistics

Property	Value
Total Samples	189,420
Languages	10
Samples per Language	18,942
Modalities	Audio + Text
Tasks	3


⸻

 Annotations
	•	Scenario Classification (7 categories)
	•	Fraud vs Non-Fraud (Binary)
	•	Fraud-Type Classification (7 types)

⸻

 Tasks

1️⃣ Scenario Classification

Classify the type of telecom conversation:
	•	Customer Service
	•	Delivery
	•	Ride-hailing
	•	Retail Transactions
	•	Appointment Scheduling
	•	Food Ordering
	•	Traffic Information

⸻

2️⃣ Fraud Detection

Binary classification:

Fraud vs Non-Fraud


⸻

3️⃣ Fraud-Type Classification
	•	Banking Fraud
	•	Customer Service Impersonation
	•	Investment Scam
	•	Phishing
	•	Lottery Scam
	•	Kidnapping
	•	Identity Theft

⸻

 Models

 Speech Models (SPTMs)
	•	Wav2Vec2
	•	WavLM
	•	HuBERT
	•	Whisper
	•	XLS-R

⸻

 Text Models (TPTMs)
	•	XLM-RoBERTa
	•	IndicBERTv2
	•	MuRIL

⸻

 Methodology

🔹 Unimodal Approaches
	•	Fully Connected Network (FCN)
	•	CNN-based architectures

🔹 Multimodal Fusion
	•	Concatenation
	•	Cross-Attention

⸻

 Training Setup

Optimizer: AdamW
Learning Rate: 1e-3
Batch Size: 32
Epochs: 5
Validation: 5-Fold Cross Validation


⸻

 Key Findings
	•	 Text models outperform audio and multimodal approaches
	•	 Fraud Detection is the easiest task
	•	 Fraud-Type Classification is the most challenging
	•	 Performance varies across languages (high-resource > low-resource)

⸻

 Limitations
	•	Synthetic audio generated via TTS
	•	Limited speaker diversity
	•	Restricted to Indic languages
	•	Uniform dataset distribution (not real-world skewed)

⸻

 Future Work
	•	Real-world multilingual telecom datasets
	•	Improved multimodal fusion strategies
	•	Better low-resource language representations
	•	Fine-grained fraud intent modeling

⸻

 Project Structure

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


⸻

 Resources
	•	Dataset: https://huggingface.co/datasets/vikrant-vikram/INDICA/tree/main, https://drive.google.com/drive/folders/1kis1b8sVOypv4xNb-QhB8pch4J9gYVZ-?usp=share_link
	•	Paper: INDICA: An Audio Indic-Language Telecom Fraud Analysis Benchmark

⸻

---

## Description

- **Gujarati_audio.tar.gz** — Gujarati speech audio files  
- **Hindi_audio.tar.gz** — Hindi speech audio files  
- **Tamil_audio.tar.gz** — Tamil speech audio files  
- **Text_samples.tar.gz** — Text transcriptions corresponding to audio samples  

---

## How to Use

### 1. Download files

Using Hugging Face CLI:

```bash
hf download vikrant-vikram/INDICA Gujarati_audio.tar.gz
hf download vikrant-vikram/INDICA Hindi_audio.tar.gz
hf download vikrant-vikram/INDICA Tamil_audio.tar.gz
hf download vikrant-vikram/INDICA Text_samples.tar.gz


Extract the files 
tar -xzf Gujarati_audio.tar.gz
tar -xzf Hindi_audio.tar.gz
tar -xzf Tamil_audio.tar.gz
tar -xzf Text_samples.tar.gz

Expected structure after extraction

Audio_samples/
├── Gujarati/
├── Hindi/
├── Tamil/

Text_samples/
├── Gujarati/
├── Hindi/
├── Tamil/


 Authors
	•	Nitin Choudhury
	•	Samyuktha Chilaka
	•	Bikrant Bikram Pratap Maurya
	•	Arun Balaji Buduru



 Citation

@inproceedings{indica2026,
  title={INDICA: An Audio Indic-Language Telecom Fraud Analysis Benchmark},
  author={Choudhury, Nitin and Chilaka, Samyuktha and Maurya, Bikrant and Buduru, Arun},
  year={2026}
}


