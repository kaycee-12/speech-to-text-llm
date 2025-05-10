
# 🎤 Emotion-Aware Speech Recognition System

This project combines **OpenAI's Whisper** for speech recognition and a **machine learning-based emotion classifier** to detect the emotional tone of spoken audio from `.mp4` video files.

---

## 📌 Features

- Transcribes speech from `.mp4` files using Whisper.
- Converts audio to `.wav` format using MoviePy.
- Extracts MFCC and pitch features using Librosa.
- Detects emotional tone (`happy`, `sad`, `angry`, `neutral`) using an SVM classifier.

---

## 🚀 Installation

Make sure you're using Python 3.11 or later. Then install the dependencies:

```bash
pip install openai-whisper librosa scikit-learn moviepy numpy
```

If using in Google Colab, ensure these are installed in a code cell:

```python
!pip install openai-whisper librosa scikit-learn moviepy numpy
```

---

## 📁 Project Structure

```
emotion_aware_speech_recognition/
├── your_notebook.ipynb  # Jupyter notebook or Colab file
├── temp_audio.wav       # Temporary file created during processing
├── sample.mp4           # Input video file (replace with your own)
```

---

## 🧠 Model Workflow

1. **Convert Video to Audio**: Extracts audio from an `.mp4` file using MoviePy.
2. **Transcription**: Uses Whisper to transcribe audio and detect the language.
3. **Feature Extraction**: Extracts 13 MFCC + 13 pitch features using Librosa.
4. **Emotion Classification**: A support vector machine (SVM) classifies the emotion based on features.
5. **Output**: Prints the detected language, transcription, and emotion.

---

## ✅ Example Usage

```python
audio_path = "/content/happy voice.mp4"
emotion_aware_speech_recognition(audio_path)
```

Sample Output:

```
Detected Emotion: happy
Transcription: I'm so glad you're here today!
Language Detected: en
```

---

## 📌 Notes

- This version uses **randomly generated training data** for the SVM classifier as a placeholder.
- For production use, you should replace this with a pre-trained model trained on real emotional audio datasets like **RAVDESS**, **CREMA-D**, or **Emo-DB**.
- Whisper supports multiple models (`tiny`, `base`, `small`, `medium`, `large`). You can switch from `base` to another for improved accuracy or faster inference.

---

## 📜 License

MIT License
