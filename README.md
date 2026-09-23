# 🤍 EMMo. — Emotional Support Companion

> A multilingual NLP-based emotional support companion that provides a safe space for users to express their feelings, analyzes emotional states, and generates supportive responses.

## 🌱 Overview

**EMMo. (Emotional Support Companion)** is a web-based emotional support application designed to provide users with a simple and anonymous space to express their thoughts and feelings.

The project combines **Natural Language Processing (NLP), sentiment analysis, keyword-based emotion detection, multilingual emotion support, and an interactive web interface** to analyze the emotional tone of user input and provide an appropriate supportive response.

EMMo. currently supports six languages:

- 🇬🇧 English
- 🇮🇳 Telugu
- 🇮🇳 Tamil
- 🇮🇳 Kannada
- 🇮🇳 Hindi
- 🇮🇳 Marathi

> **Note:** EMMo. is an academic prototype designed for supportive interaction and is not intended to replace professional mental-health care.

---

## ✨ Key Features

### 🧠 Sentiment Analysis

EMMo. uses **TextBlob** to analyze the sentiment of user-generated text and calculate a sentiment polarity score.

The sentiment score is used together with keyword-based analysis to help identify the user's emotional state.

### 💭 Emotion Detection

The system uses predefined multilingual emotion keywords along with sentiment scores to detect different emotional states.

Currently supported emotions include:

- 😊 Joy
- 😡 Anger
- 😣 Irritation
- 😔 Sadness
- 💪 Motivation
- 😐 Neutral

### 🌍 Multilingual Support

EMMo. supports emotion detection for six languages:

| Language | Code |
|----------|------|
| English | `en` |
| Telugu | `te` |
| Tamil | `ta` |
| Kannada | `kn` |
| Hindi | `hi` |
| Marathi | `mr` |

This allows users to express their feelings using multiple Indian languages.

### 🔒 Anonymous Sharing

The project is designed around anonymous emotional sharing.

### Basic processing flow

User Input
    ↓
Sentiment Analysis
    ↓
Emotion Detection
    ↓
Emotion Classification
    ↓
Supportive Response

### System Architecture

                         ┌─────────────────────┐
                         │      User Input     │
                         │   Feelings / Story  │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │  Language Selection │
                         │ EN / TE / TA / KN   │
                         │ HI / MR             │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │   Text Processing   │
                         └──────────┬──────────┘
                                    │
                       ┌────────────┴────────────┐
                       ▼                         ▼
              ┌─────────────────┐      ┌──────────────────┐
              │    TextBlob     │      │ Keyword-Based    │
              │    Sentiment    │      │ Emotion Detection│
              │    Analysis     │      │                  │
              └────────┬────────┘      └────────┬─────────┘
                       │                         │
                       └────────────┬────────────┘
                                    ▼
                         ┌─────────────────────┐
                         │ Emotion Classification│
                         │ Joy / Anger /       │
                         │ Sadness / Irritation│
                         │ Motivation / Neutral│
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │ Supportive Response │
                         │      Generator      │
                         └─────────────────────┘

### 📂 Project Structure

EMMo/
│
├── Backend.py
│   └── Python backend containing sentiment analysis,
│       emotion detection, multilingual emotion keywords,
│       and supportive response generation
│
├── index.html
│   └── Main web interface of EMMo.
│
├── script.js
│   └── Handles frontend interactions and user events
│
├── style.css
│   └── Defines the visual design, layout, and styling
│
└── README.md
    └── Project documentation
    
# 🔄 How the System Works

## Step 1 — User Shares Feelings

The user enters their thoughts or experiences through the EMMo. interface.

Example:

```text
I am feeling very sad and alone today.
```

## Step 2 — Sentiment Analysis

The input text is analyzed using TextBlob.

```text
User Text
    ↓
TextBlob
    ↓
Sentiment Polarity Score
```

The polarity score provides an indication of the overall sentiment of the input.

## Step 3 — Emotion Detection

The system checks the input against predefined emotion keywords.

For example:

```text
sad
alone
crying
hopeless
```

These keywords can contribute to identifying the emotional state as **sadness**.

## Step 4 — Emotion Classification

The system combines keyword matching and sentiment information to determine an emotional category.

```text
Input Text
    ↓
Keyword Matching
       +
Sentiment Score
    ↓
Detected Emotion
```

## Step 5 — Supportive Response

Once an emotion is detected, an appropriate predefined response is selected.

Example:

```text
Detected Emotion: Anger

Response:
It sounds like you're really upset right now.
Take a deep breath.
```

## Step 6 — Anonymous Community Sharing

The project also includes a community section where user experiences can be represented anonymously.

```text
Anonymous User: Today I feel very sad...
```

---

# 🧠 Emotion Detection Logic

EMMo. uses a **hybrid rule-based approach** that combines keyword matching and sentiment analysis.

```text
                    User Text
                        │
                        ▼
                Sentiment Analysis
                        │
                        ▼
                 Polarity Score
                        │
             ┌──────────┴──────────┐
             │                     │
             ▼                     ▼
      Keyword Matching       Score Evaluation
             │                     │
             └──────────┬──────────┘
                        ▼
                Emotion Category
                        │
                        ▼
               Supportive Response
```

The system first checks for emotion-specific keywords.

If relevant keywords are detected, the corresponding emotion is identified. If no matching emotion keyword is found, the sentiment score is used to help classify the input as positive, negative, or neutral.

---

# 🌍 Multilingual Emotion Dictionary

The backend contains predefined emotion keywords for six languages.

```python
emotions_keywords = {
    "en": {...},
    "te": {...},
    "ta": {...},
    "kn": {...},
    "hi": {...},
    "mr": {...}
}
```

The keyword dictionary contains categories for:

* Anger
* Irritation
* Sadness
* Joy
* Motivation

This allows the system to identify common emotional expressions across multiple languages.

---

# 🎯 Project Objectives

The main objectives of EMMo. are:

1. Create a simple and supportive environment for emotional expression.
2. Analyze the sentiment of user-generated text.
3. Detect different emotional states using NLP techniques.
4. Generate supportive responses based on detected emotions.
5. Support multiple Indian languages.
6. Encourage anonymous sharing of experiences.
7. Demonstrate the practical application of NLP in emotional-support systems.

---

# 📊 Example

## Input

```text
I am feeling very angry and irritated today.
```

## Processing

```text
Language → English

Sentiment Analysis
        ↓
Negative Sentiment

Keyword Detection
        ↓
"angry"
"irritated"

        ↓
Emotion: Anger
```

## Output

```text
It sounds like you're really upset right now.
Take a deep breath.
```

---

# 🔐 Privacy Considerations

EMMo. is designed with anonymous interaction in mind.

The application represents shared experiences using an anonymous identifier rather than requesting the user's identity.

However, the current implementation is an **academic prototype** and should not be considered a fully secure anonymous platform.

A production-ready system would require additional security measures such as:

* Secure data storage
* Encryption
* Authentication and authorization
* Server-side privacy controls
* Secure API communication
* Data-retention policies

---

# ⚠️ Current Limitations

The current prototype has several limitations:

* Emotion detection relies heavily on predefined keywords.
* TextBlob sentiment analysis is primarily designed for English text.
* Multilingual sentiment analysis is not language-specific.
* The frontend and Python NLP logic are currently separate components and require proper API integration for complete browser-to-backend communication.
* The number of supported emotion categories is limited.
* Complex context, sarcasm, mixed emotions, and indirect expressions may not be detected accurately.
* The anonymous community concept requires proper database and privacy controls for production deployment.

---

# 🚀 Future Enhancements

## 🤖 Advanced NLP Models

The current keyword-based approach can be enhanced using multilingual transformer-based models such as:

* BERT
* DistilBERT
* XLM-RoBERTa
* IndicBERT

## 🧠 Machine Learning-Based Emotion Classification

A dedicated machine learning model can be trained to identify a wider range of emotional states, such as:

```text
Joy
Sadness
Anger
Fear
Anxiety
Stress
Neutral
```

## 🗣️ Conversational AI

A conversational AI system can be integrated to generate more contextual responses instead of relying only on predefined messages.

## 🌐 Backend API Integration

The frontend can be connected to the Python backend using a web framework such as:

* Flask
* FastAPI
* Django

Future architecture:

```text
HTML / CSS / JavaScript
          │
          ▼
       REST API
          │
          ▼
    Python Backend
          │
     ┌────┴────┐
     ▼         ▼
Sentiment   Emotion
Analysis    Detection
     │         │
     └────┬────┘
          ▼
Supportive Response
```

## 📱 Mobile Application

EMMo. could be extended into an Android or iOS application to make the emotional-support interface more accessible.

## 📈 Emotion Analytics

A privacy-conscious dashboard could be developed to visualize emotional trends over time while following appropriate data-protection practices.

---

# 💡 Why EMMo.?

Many people may find it difficult to openly communicate their emotions.

EMMo. explores how **Natural Language Processing and multilingual AI technologies can be used to create an accessible digital space for emotional expression and supportive interaction.**

The core concept is:

> **Listen → Understand → Respond → Support**

---

# 🛠️ Installation

## 1. Clone the Repository

```bash
git clone <your-repository-url>
cd EMMo
```

## 2. Install Python Dependencies

Install the required Python packages:

```bash
pip install textblob googletrans
```

## 3. Run the Python Backend

```bash
python Backend.py
```

## 4. Open the Frontend

Open:

```text
index.html
```

in a web browser.

> **Note:** The current prototype contains the frontend and Python NLP logic as separate components. Full browser-to-Python communication can be implemented using Flask or FastAPI as a future enhancement.

---

# 📌 Project Status

**Status:** Prototype / Academic Project

EMMo. currently demonstrates:

* Multilingual emotion keyword detection
* Sentiment analysis
* Rule-based emotion classification
* Supportive response generation
* Anonymous sharing concept
* Interactive web interface

# 👩‍💻 Author

## Pranjali Mali

**AI & Machine Learning Engineering Student**

### Areas of Interest

* Artificial Intelligence
* Machine Learning
* Natural Language Processing
* Explainable AI
* AI-powered Applications

EMMo. aims to evolve from a rule-based emotional-support prototype into a **privacy-conscious, multilingual AI companion capable of understanding emotional context and providing responsible, supportive interactions.**

> **EMMo. — A space to express, a system designed to understand.**
