# FastSpeech2-Based English and Telugu Text-to-Speech

## Project Overview
This project explores FastSpeech 2-based Text-to-Speech synthesis for English and Telugu.

## Datasets
- **English:** Svarah – [Kaggle dataset](https://www.kaggle.com/datasets/sirichandana6281/fastspeech2-english-training)
- **Telugu:** IndicTTS Telugu – [Hugging Face](https://huggingface.co/datasets/SPRINGLab/IndicTTS_Telugu)

## Telugu Implementation
Telugu speech samples were generated using a pretrained multilingual FastSpeech 2 model from [Fastspeech2_HS](https://github.com/utkarsh2299/Fastspeech2_HS).

Five test samples were generated. Duration, pitch and energy predictions were extracted and visualized for the five samples.

**Note:** The Telugu checkpoint is pretrained; it was not trained from scratch for this assignment.

## English Implementation
The Svarah preprocessed dataset and train/validation feature files are available through the linked Kaggle dataset. Five English test audio samples were prepared.

**Limitation:** A verified English FastSpeech 2 acoustic checkpoint and training/validation loss curves are not currently available.

## Important Limitations
The available artifacts do not establish successful from-scratch training of both language models. Pretrained inference and dataset preparation are documented separately from model training.

## Telugu Model Attribution
The pretrained model is from the Speech Technology Consortium/Bhashini ecosystem. Refer to the upstream repository for licensing and attribution requirements.

## Repository
https://github.com/Siri6281/FastSpeech2-English-Telugu-TTS
