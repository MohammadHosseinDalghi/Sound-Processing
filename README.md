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

```bash
pip install pyaudio numpy matplotlib
