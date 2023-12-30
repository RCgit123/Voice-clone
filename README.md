# Voice-clone
### run the following command to copy the repo and install the dependencies 
### install the latest version.
```bash
!pip3 install -U scipy
!git clone https://github.com/jnordberg/tortoise-tts.git
%cd tortoise-tts
!pip3 install -r requirements.txt
!pip3 install transformers==4.19.0 einops==0.5.0 rotary_embedding_torch==0.1.5 unidecode==1.3.5
!python3 setup.py install
```
**run the cells in the ipynb notebook to train and run the voice cloning model**

---

## PESQ (Perceptual Evaluation of Speech Quality)

**Overview:**

PESQ, or Perceptual Evaluation of Speech Quality, is a widely used objective metric for assessing the perceived quality of speech signals. It quantifies the degradation in speech quality caused by various factors such as compression, noise, or signal processing techniques. PESQ is commonly employed in the field of telecommunications and audio processing to objectively evaluate the impact of different technologies on speech quality.

**How it Works:**

PESQ works by comparing an original, unprocessed speech signal with a degraded or processed version of the same signal. It takes into account various perceptual aspects, including distortion and noise, and produces a score that reflects the perceived quality of the degraded speech relative to the original.

**Scoring:**

PESQ scores typically range from -0.5 to 4.5, with higher scores indicating better perceived speech quality. The interpretation of scores is often categorized into ranges, such as poor, fair, good, and excellent.

**Usage:**

In the context of our project, PESQ is utilized to objectively assess the quality of generated speech produced by our Tortoise model. By comparing the generated speech with the original, we can quantitatively measure how well the model preserves the quality of the input speech.

**Note:**

While PESQ provides an objective measure of speech quality, it's important to complement it with subjective evaluations, especially when user perception is a critical factor in your application.

---

# Mel Cepstral Distortion (MCD)

**Overview:**

Mel Cepstral Distortion (MCD) is a metric commonly used in speech processing to quantify the difference between two sets of Mel-frequency cepstral coefficients (MFCCs). MFCCs are widely employed in speech and audio signal processing for capturing the spectral characteristics of a signal. MCD measures the distortion or dissimilarity between the MFCCs of a reference (original) signal and a target (generated) signal.

**How it Works:**

MCD is calculated by comparing the frame-wise MFCCs of the reference and target signals. It quantifies the average Euclidean distance between corresponding feature vectors in the time domain. Lower MCD values indicate better similarity between the two signals.

**Scoring:**

MCD is typically reported in decibels (dB). The lower the MCD value, the closer the match between the reference and target signals.

**Usage:**

In our project, MCD serves as a valuable metric to assess the quality of generated speech. By calculating the distortion between the MFCCs of the original and generated speech, we gain insights into how well our Tortoise model preserves the spectral characteristics of the input speech.

**Note:**

Visit [GitHub](https://github.com/neonbjb/tortoise-tts) for more information about TORTOISE TTS.


MCD is one of several metrics that collectively provide a comprehensive evaluation of the performance of our TTS (Text-to-Speech) model. It is particularly useful for analyzing the accuracy of spectral features in the generated speech.

---
