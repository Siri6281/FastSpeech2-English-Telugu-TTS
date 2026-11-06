# Telugu Text-to-Speech using FastSpeech 2

## Project Overview
Telugu speech is generated from text using a pretrained FastSpeech 2 model and HiFi-GAN vocoder.

## Model Details
- Architecture: FastSpeech 2
- Vocoder: HiFi-GAN
- Language: Telugu
- Voice: Female
- Model repository: https://github.com/utkarsh2299/Fastspeech2_HS
- Dataset: https://huggingface.co/datasets/SPRINGLab/IndicTTS_Telugu
- License: CC BY 4.0. Refer to LICENSE for details.

The checkpoint is pretrained. This project performs inference and analyzes predicted duration, pitch and energy. It does not claim training this checkpoint from scratch.

## Dataset
- Original recordings: 8,576
- Original duration: approximately 36.71 hours
- Prepared training subset: 2,036 recordings
- Prepared validation subset: 376 recordings
- Prepared audio sampling rate: 22,050 Hz

The prepared dataset backup and phoneme metadata are stored separately in Google Drive under Telugu_FastSpeech2_Backup.

## Implementation
1. Telugu text preprocessing
2. Phonetic text conversion
3. FastSpeech 2 acoustic feature generation
4. HiFi-GAN waveform generation
5. WAV audio output

## Generated Audio
Five Telugu test sentences were synthesized:
- T1.wav
- T2a.wav
- T2b.wav
- T3.wav
- T4.wav

The files are stored in Audio/.

## Variance Adaptor Analysis
The model inference outputs include duration, pitch and energy predictions. Raw arrays are stored in Prediction_Data/ as NPZ files. Visualizations are stored in Variance_Adaptor_Plots/.

The plots show predictions against token positions.

## Folder Structure
- Audio/: five generated WAV files
- Code/: inference and text preprocessing scripts, pronunciation dictionary and HiFi-GAN source
- Model/: pretrained Telugu FastSpeech 2 checkpoint and configuration
- Vocoder/: HiFi-GAN checkpoint and configuration
- Prediction_Data/: raw duration, pitch and energy predictions
- Variance_Adaptor_Plots/: prediction visualizations
- README.md: original repository documentation
- LICENSE: original repository license

## Reproducibility
The inference pipeline requires Python, PyTorch, ESPnet and the dependencies of the original repository. Refer to the original repository for setup instructions and expected model directory structure.

## Limitations
- The Telugu checkpoint is pretrained; training from scratch is not claimed.
- Duration, pitch and energy are model predictions at token positions.
- Generated speech should be evaluated for pronunciation, intelligibility and naturalness.
- Numbers in T4 were manually expanded into Telugu words before inference.

## References
FastSpeech 2 model: https://github.com/utkarsh2299/Fastspeech2_HS

Telugu dataset: https://huggingface.co/datasets/SPRINGLab/IndicTTS_Telugu

Original model attribution: Speech Technology Consortium, Bhashini, MeitY and IIT Madras.
