# ICS 435 Final Project: Fine-Tuning Open AI Whisper For Korean Language Transcription

## Introduction

---

The purpose of this project was to explore the capabilities of the Whisper ASR model for speech recognition when data is limited. The paper detailing the model and the research can be found [here.](https://cdn.openai.com/papers/whisper.pdf) The model was fine-tuned on the Korean Language portion of the Common Voice [dataset](https://commonvoice.mozilla.org/en) which only contains 1045 instances.

## Requirements

---

### Dependencies

* Python 3.9: Target version for compatability and performance
* datasets[audio] 1.15.0: Library from Hugging Face for accessing and managing datasets
* transformers 4.14.2: Hugging Face library that provides pre-trained models including Whisper
* evaluate 0.4.2: Used for calculating the Word Error Rate
* torch version: to prepare batches of input audio features and label sequences for training

Add dependencies using `!pip install -r requirements.txt` in the notebook.
If conflicts arise, the following can be used: `!pip install --upgrade datasets[audio] transformers accelerate evaluate jiwer tensorboard gradio`

### Other

A hugging face account is required in order to access the Common Voice dataset and to save or load model checkpoints during training.