# Voice-Controlled Web Search Assistant

This is a Python script that uses **speech recognition** to capture voice input from the user and performs a **Google web search** based on the recognized speech. It also uses **text-to-speech (TTS)** to interact with the user via voice.

## Features

- Captures voice input using your microphone.
- Converts speech to text using Google's speech recognition API.
- Performs a Google search for the recognized text.
- Provides voice feedback using text-to-speech.

## Requirements

Make sure you have Python 3 installed.

Install the following Python libraries before running the script:

```bash
pip install SpeechRecognition
pip install pyttsx3
pip install pyaudio
```

> **Note**: If you face issues installing `pyaudio`, you may need to install it using a precompiled binary for your system. On Windows, you can use:
> ```bash
> pip install pipwin
> pipwin install pyaudio
> ```

## How to Use

1. Connect a microphone to your computer.
2. Run the script:
   ```bash
   python voice_search.py
   ```
3. When prompted, speak your search query.
4. The script will recognize your speech and open the corresponding Google search results in your default web browser.

## Code Overview

- `speak(text)`: Converts text to spoken audio.
- `take_command()`: Listens for voice input and returns recognized text.
- `search_web(query)`: Opens a Google search for the given query.

## Example

```bash
$ python voice_search.py
Listening...
(You say: "Weather in New York")
Opening browser to: https://www.google.com/search?q=Weather+in+New+York
```

## License

This project is open-source and free to use under the MIT License.
