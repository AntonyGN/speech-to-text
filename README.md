# Speech-to-Text Recognition in Python
This is a simple Python script that demonstrates how to perform speech-to-text recognition using a microphone and the ```speech_recognition``` library. It uses Google's speech recognition service to transcribe the audio.

## Requirements
To use this script, you'll need the following dependencies installed on your system:

- Python 3.x
- ```speech_recognition``` library
- ```pyaudio``` library (for microphone input)

## Installation
## For Windows
1. Install Python 3.x from the [official website](https://www.python.org/downloads/).

2. Install ```pip```, the package installer for Python, by following the instructions in the [official documentation](https://pip.pypa.io/en/stable/installation/).

3. Install ```pyaudio``` library by running the following command in a terminal or command prompt:

```bash
pip install pyaudio
```
If you encounter an error during installation, you may need to install ```portaudio``` separately. You can download ```portaudio``` from the [official website](http://www.portaudio.com/download.html) or install it using a package manager such as [Chocolatey](https://community.chocolatey.org/packages?q=404).

4. Install ```speech_recognition``` library by running the following command in a terminal or command prompt:

```bash
pip install SpeechRecognition
```
## For Mac OS
1. Install Homebrew by following the instructions on the [official website](https://brew.sh/).
2. Install Python 3.x by running the following command in a terminal:

```bash
brew install python
```
3. Install ```pyaudio``` library by running the following command in a terminal:

```bash
brew install portaudio
pip install pyaudio
```
If you encounter an error during installation, you may need to specify the path to ```portaudio``` manually. You can do this by running the following command instead:
```bash
pip install --global-option='build_ext' --global-option='-I/usr/local/include' --global-option='-L/usr/local/lib' pyaudio
```
4. Install ```speech_recognition``` library by running the following command in a terminal:
```bash
pip install SpeechRecognition
```

## Usage
1. Open Jupyter Notebook and create a new notebook.
2. Copy the following code into a cell:

```bash
import speech_recognition as sr
r = sr.Recognizer()
with sr.Microphone() as source:
    print("Speak Anything :")
    audio = r.listen(source)
    try:
        text = r.recognize_google(audio)
        print("You said : {}".format(text))
    except:
        print("Sorry could not recognize what you said")
```


