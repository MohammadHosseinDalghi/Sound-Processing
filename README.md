# **Real-Time Audio Recording and FFT Analysis with PyAudio**

This project demonstrates real-time audio recording using PyAudio, performing Fast Fourier Transform (FFT) on the recorded audio data for frequency analysis, and saving the audio to a `.wav` file. The project also includes playback of the recorded audio through the computer's output device.

## **Table of Contents**
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Breakdown](#code-breakdown)
  - [1. Audio Recording](#1-audio-recording)
  - [2. FFT Analysis](#2-fft-analysis)
  - [3. Playback and Saving](#3-playback-and-saving)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)

## **Project Overview**
This Python script captures audio from a microphone, processes it to extract key frequency components using FFT, and then saves the audio into a `.wav` file. Additionally, it enables playback of the captured audio. This project is built using the PyAudio and NumPy libraries for audio stream management and signal processing.

## **Features**
- Real-time audio recording from the microphone.
- Conversion of the audio data into a frequency spectrum using Fast Fourier Transform (FFT).
- Playback of the recorded audio.
- Saving the recorded audio to a `.wav` file.
  
## **Installation**

Before running the script, ensure that you have the required libraries installed. You can install them using `pip`:

```py
pip install pyaudio
pip install numpy
pip install matplotlib
```
Make sure your device supports audio input/output.

## **Usage**
1. Clone the repository:

```
git clone https://github.com/MohammadHosseinDalghi/Sound-Processing.git
```

2. Navigate to the project directory:

```bash
cd Sound-Processing
```

3. Run the Jupyter file

## **Code Breakdown**

**1. Audio Recording**

The script uses PyAudio to capture audio data in real time:

```py
stream = p.open(format=pyaudio.paInt16, channels=1, rate=16000, input=True, frames_per_buffer=chunk)
```
* The audio is recorded in chunks of 1024 frames, with a sampling rate of 16kHz.


**2. FFT Analysis**

After capturing audio, the Fast Fourier Transform (FFT) is applied to convert the time-domain signal into a frequency-domain representation:
```py
out_fft = np.fft.fft(data2)
```
* This provides a frequency spectrum that can be visualized or further analyzed.

**3. Playback and Saving**

Once the audio has been processed, it can be played back through your system’s output device and saved to a `.wav` file:
