# Speech-to-sentiment-analysis
<br>
Project Title

Speech-to-Sentiment Analysis System

Project Overview

This project implements an end-to-end voice analytics pipeline that takes raw speech audio as input and produces:

Automatic speech transcription

Text-based intent classification

Sentiment analysis of the spoken content

The system is designed for offline/local inference and demonstrates how modern transformer-based models can be integrated into a practical application using a lightweight graphical interface.

Problem Statement

Unstructured voice data is widely used in customer support, surveys, and conversational systems. Extracting actionable insights such as what the user said, what they intend, and how they feel requires a combination of speech processing and natural language understanding.

This project addresses that problem by building a unified pipeline that converts speech into structured textual and emotional information.

System Architecture (High Level)

Audio Input

User uploads an audio file (.wav)

Audio is normalized internally to a standard format

Speech-to-Text (ASR)

Converts speech into textual transcription

Natural Language Processing

Intent classification from text

Sentiment analysis of the transcribed text

User Interface

Streamlit-based interface to upload audio and display results

Technologies and Libraries Used
Programming Language

Python

Speech Processing

OpenAI Whisper (Transformer-based ASR)

Used for automatic speech recognition

Robust to accents and background noise

FFmpeg

Used for audio format conversion and resampling

Natural Language Processing

Hugging Face Transformers

Pretrained transformer models for:

Text classification (intent)

Sentiment analysis

PyTorch

Backend framework for model inference

Application Framework

Streamlit

Used to build an interactive graphical user interface

Allows audio upload and real-time inference visualization

Supporting Libraries

torch, torchaudio

librosa, soundfile

accelerate

ffmpeg-python

Key Design Decisions

Offline inference
The system avoids external APIs and runs entirely on local resources to ensure reproducibility and no dependency on paid services.

Model persistence
Pretrained models are saved once and reused for inference, following production-style ML workflows.

Format-agnostic audio handling
Users are not required to preprocess audio; the system handles conversion internally.

Separation of concerns
Model preparation and application inference are decoupled, reflecting industry best practices.

Use Cases

Voice-based customer feedback analysis

Call-center conversation analytics

Survey and interview sentiment evaluation

Conversational AI preprocessing pipeline

Limitations (Honest and Professional)

Intent classification uses a generic text classifier and can be replaced with a task-specific intent model for higher accuracy.

Large ASR models increase storage and startup time, making public deployment less practical.
