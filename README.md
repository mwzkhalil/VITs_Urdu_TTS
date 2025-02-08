# VITs_Urdu_TTS

## Introduction
This repository contains code for training a Text-to-Speech (TTS) model specifically for Urdu language using the VITS model. The VITS model is known for its high quality speech synthesis capabilities. 

## Installation
To get started with training the Urdu TTS model, follow these steps:

1. Install the Coqui TTS toolkit by following the instructions provided [here](https://docs.coqui.ai/en/latest/installation.html).

2. Ensure that the Urdu dataset is available inside the `Dataset` folder. The Urdu data i used is audiobooks of urdu. The data should be formatted in a manner similar to LJSpeech_1.1 dataset for compatibility.

3. Install all required libraries for phonemizing Urdu alphabets. **Espeak** library is particularly useful for this purpose.

4. Adjust the parameters in the code according to your requirements. The rest of the parameters should already be updated accordingly for the Urdu dataset.

## Dataset
The dataset provided in the `Dataset` folder contains text data and corresponding Wav files in Urdu language. It follows the same format as the LJSpeech 1.1 dataset for consistency. Ensure that the dataset is properly formatted and organized before proceeding with training.

## Training
To train the TTS model for Urdu language, run the `train_tts.py` file. This file contains the necessary code for training the model using the VITS architecture. Make sure all dependencies are installed and the dataset is properly configured before initiating the training process.

```python
nvidia-smi   #to check the GPUS available
CUDA_VISIBLE_DEVICES="5" python train_tts.py  #Mention the GPU to run on and the training file
```

## Inference

```python
pip install TTS

tts --text "آپ آج شام کو ان کے فلیٹ پر ضرور تشریف لائیے" \
    --model_path path/to/model.pth \
    --config_path path/to/config.json \
    --out_path folder/to/save/output.wav
```
