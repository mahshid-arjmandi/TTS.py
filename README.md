# Text-to-Speech Translation

**Overview**

This project is a text-to-speech translation application that utilizes:

Text translation (using pre-trained translation M2M100 model)

Text-to-speech conversion (via Microsoft Edge TTS)

Language detection
It allows translating text into various languages and converting it into speech.



---

**Features**

Translate text into multiple languages (Persian, English, French, German, Italian ... .)

Convert translated text to audio files and play them automatically

Automatically detect the input text language

Choose the target language for speech output

Download the generated audio file to the Downloads folder



---

**Requirements**

To run this project, you need:

Python 3.8+

Required libraries:

pip install edge-tts nest_asyncio pygame langdetect

Translation models located in the path:
(https://huggingface.co/facebook/m2m100_418M/tree/main)



---

**How to Use**

Run the Application

1. Clone the repository:

git clone 
cd 


2. Run the textToSpeech.py file:

python textToSpeech.py


Input

Enter text as input (e.g., "Elle regarde la télévision tous les soirs.").


Output

The translated text in your chosen language.

An audio file named output_File.mp3 will be generated, played automatically, and saved in the Downloads folder.



---

**Project Structure**

main.py: The main script to execute the application

LanguageSelector: A class to select the target speech language

LanguageDetector: A class to detect the language of the input text

TextToSpeechApp: A class to generate and manage the audio file

Speech: A class to handle translation and speech output processes



---

**Examples**

Input:

Elle regarde la télévision tous les soirs.

Output:

1. Detected language: French


2. Translated text to Persian: او هر شب تلویزیون تماشا می‌کند.


3. Audio file generated and played automatically.



1. When text is provided in any language, the speech will be in Persian (since the system's default speech is in Persian).
Example:



Text: Bonjour
The voice you hear: Salam


2. When text is provided in Persian and the user selects the speech language, the response will be in the selected speech language.
Example:



Text: Salam
If the user wants to hear the response in French, it will play: Bonjour


3. When text is provided in any language, and the user selects the speech language, the response will be in the selected speech language.
Example:
Suppose the user enters text in French and wants to hear the response in English:



Text: Bonjour
The voice you hear: Hello


4. When text is provided in any language and the user does not select the speech language or selects it incorrectly, the speech will be in Persian.
Example:



Text: Hello
If the user selects the wrong speech language:
The voice you hear: Salam


---

**Error Handling**

Possible Issues:

If the translation model is missing from the specified path, the program will not run.

If the selected voice type is unavailable, the default voice (Persian) will be used.



# Multilingual Translation

**Overview**

This project is a simple and efficient multilingual translation tool built using:

Hugging Face Transformers (M2M100 model for multilingual translation)

Langdetect (for language detection)


The application automatically detects the source language of the input text and translates it into the desired target language using the M2M100 translation model.


---

**Features**

Automatic Language Detection: Detects the source language of the input text using langdetect.

Multilingual Translation: Supports translation between multiple languages.

Hugging Face Integration: Utilizes the M2M100 model for state-of-the-art translation.



---

**Requirements**

Dependencies

Install the required Python libraries:

pip install transformers langdetect torch

Model Setup

Download the M2M100 model and place it in the directory specified in the code:

https://huggingface.co/facebook/m2m100_418M/tree/main


---

**How to Use**

Running the Script

1. Clone the repository:

git clone 
cd 


2. Run the script:

python main.py



Input

Enter the target language code (e.g., en for English, fr for French, etc.).

Provide the text to translate.


Output

The translated text will be displayed in the console.



---

**Code Overview**

Main Components

1. Translator Class:

Loads the M2M100 model and tokenizer.

Detects the source language of the text.

Translates the text into the target language.



2. get_translation Function:

Simplifies the translation process by initializing the Translator class and returning the translated text.



3. Script Execution:

Prompts the user to input the target language and text.

Displays the translation.





---

Example

Input:

Target Language: en
Text: Bonjour tout le monde.

Output:

Translation: Hello everyone.


---

**Customization**

Model Path: Update the model_path variable to point to the directory where your M2M100 model is stored.

Target Language: Add or modify language codes supported by the M2M100 model.



---

**Error Handling**

Potential Issues

1. Language Detection Error:

If langdetect fails, ensure the input text is long enough for reliable detection.



2. Model Path Error:

Verify that the M2M100 model exists at the specified model_path.



3. Unsupported Language:

Check if the target language is supported by the M2M100 model.




# Audio Anonymization and Conversion Toolkit

A comprehensive toolset designed for audio file conversion, voice anonymization, and playback, focusing on seamless integration with Python-based audio processing libraries.

**Features**
- **Audio Conversion**: Convert between MP3 and WAV formats.
- **Voice Anonymization**: Apply pitch shifting for anonymizing audio recordings.
- **Playback Support**: Play anonymized audio files in MP3 format using `pygame`.
- **Modular Design**: Extendable and reusable code structure for developers.

**Requirements**
To run this project, ensure that you have the following libraries installed:

- Python 3.7 or higher
- Required libraries:
  - `librosa` (for audio processing)
  - `soundfile` (for reading and writing WAV files)
  - `pydub` (for audio format conversion)
  - `pygame` (for audio playback)

You can install the necessary dependencies by running:


pip install -r requirements.txt

Installation and Setup

1. Clone the Repository:

git clone https://github.com/yourusername/audio-anonymization-toolkit.git
cd audio-anonymization-toolkit


2. Install Dependencies: Create and activate a virtual environment, then install the required dependencies:

pip install -r requirements.txt


3. Running the Project: To start processing audio files, run the following command:

python anonymize_voice_Main.py



**Usage**

Convert and Anonymize Audio

You can easily convert and anonymize MP3 files as follows:

from main import process_audio

**Input and output MP3 file paths**
input_mp3_file = "input_file.mp3"
output_mp3_file = "anonymized_output.mp3"

**Process the audio**
process_audio(input_mp3_file, output_mp3_file)

Play Anonymized Audio

To play the output audio, you can use the play_audio.py script:

python play_audio.py

Customizing the Anonymization

You can modify the pitch_shift_steps parameter in the anonymize_voice function to adjust the degree of anonymization by pitch shifting.

def anonymize_voice(input_file, output_file, pitch_shift_steps=4):
    """Applies pitch shifting to anonymize the audio."""
    # Customize the pitch shift by changing the pitch_shift_steps

**Project Structure**

The project is organized as follows:


├── audio_anonymization.py    # Module responsible for voice anonymization

├── audio_conversion.py       # Module for converting between MP3 and WAV

├── playing_anonymized_sound.py             # Module to handle audio playback

├── requirements.txt          # List of required Python packages

├── anonymize_voice_Main.py                   # Main entry point to process and convert audio

**Running Tests**

To verify the functionality of the project, run the main.py script, which will handle conversion, anonymization, and playback:

python anonymize_voice_main.py

## X-vector Extraction and Voice Conversion with SpeechT5

**Overview**

This project consists of two main components:

1. X-vector Extraction: Extract speaker embeddings (X-vectors) from an audio file using a neural network-based approach.


2. Voice Conversion: Use Microsoft’s SpeechT5 model to perform voice conversion by mapping the characteristics of a target speaker’s voice onto the audio of a source speaker.



This repository provides Python scripts for both functionalities.


---

**Features**

1. X-vector Extraction:

Extract speaker embeddings (X-vectors) from audio files using a custom implementation of a TDNN (Time Delay Neural Network).

The embeddings can be saved as .npy files for later use in tasks like speaker verification or voice conversion.


2. Voice Conversion:

Perform voice conversion using Microsoft's SpeechT5.

Uses pre-trained models from the Hugging Face Transformers library for both feature extraction and vocoding.

Allows specifying target speaker embeddings (e.g., X-vectors) to map the voice characteristics of the target speaker onto a given audio input.



---

**Prerequisites**

Libraries Required

Torch: Neural network computations.

Librosa: Audio processing and feature extraction.

NumPy: Array manipulation.

SpeechBrain: Neural network modules (used for CNNs and pooling).

Transformers: Access to pre-trained SpeechT5 models.

PyDub: Audio manipulation.

SoundDevice: Playback of generated audio.

TorchAudio: Audio I/O and processing.



---

**Installation**

1. Clone the repository:

git clone https://github.com/Chatbot.git
cd Chatbot


2. Install the required Python libraries:

pip install torch librosa numpy speechbrain transformers pydub sounddevice torchaudio


3. For Windows users, ensure ffmpeg is installed for PyDub. You can download it from FFmpeg.org.


├── anonymize_voice_Main.py # Main entry point to process and convert audio

Running Tests

To verify the functionality of the project, run the main.py script, which will handle conversion, anonymization, and playback:

python anonymize_voice_main.py
