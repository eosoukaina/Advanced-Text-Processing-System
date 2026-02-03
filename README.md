---
title: Smart Text Assistant
emoji: ✨
colorFrom: purple
colorTo: blue
sdk: gradio
sdk_version: 4.19.2
app_file: app.py
pinned: false
license: mit
tags:
  - nlp
  - text-generation
  - bert
  - gpt2
  - text-correction
  - auto-completion
  - writing-assistant
---

# ✨ Smart Text Assistant

> **Production-ready NLP application combining deep learning transformers (BERT, GPT-2) with statistical models for intelligent text processing and generation.**

[![Live Demo](https://img.shields.io/badge/🤗-Live%20Demo-blue)](https://huggingface.co/spaces/eosoukaina/SMART-TEXT-ASSISTANT)
[![Python 3.11](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📊 Project Overview

An enterprise-grade text processing system leveraging **ensemble learning** to combine:
- **Deep Learning**: BERT (Masked Language Modeling) + DistilGPT-2 (Autoregressive Generation)
- **Statistical NLP**: N-gram models with Add-k smoothing
- **Hybrid Architecture**: Confidence-based model selection for optimal performance

**Use Case**: Real-time writing assistance with automatic error correction, context-aware text completion, and guided text generation.

## 🎯 Features

### ✍️ Smart Writing
- **Automatic Error Correction**: Errors are fixed as you type using BERT + Edit Distance
- **Smart Completion**: Complete your text with AI-generated suggestions
- **Real-time Processing**: Instant feedback while you write

### 🎯 Guided Writing
- **Word-by-Word Generation**: Choose from 5 AI-suggested words at each step
- **Context-Aware**: Suggestions adapt based on what you've written
- **Full Control**: You guide the AI to create exactly what you want

## 🏗️ Architecture & Technical Implementation

### **Model Ensemble**
| Model | Parameters | Purpose | Techniques |
|-------|-----------|---------|-----------|
| **BERT** | 110M | Typo Correction | Masked Language Modeling, Edit Distance |
| **DistilGPT-2** | 82M | Text Generation | Autoregressive LM, Beam Search |
| **N-gram** | Custom | Baseline | Bigram with Add-k Smoothing, Multiprocessing |

### **Key Engineering Features**
- **Parallel Processing**: Multiprocessing for n-gram training (~10s for 3.3MB corpus)
- **Model Optimization**: Transformer caching and efficient tokenization
- **Ensemble Logic**: Confidence-based model selection with fallback strategies
- **Production UI**: Gradio interface with real-time processing
- **Corpus**: 47,962 Twitter-like messages (3.3MB) for domain-specific training

## 🚀 Quick Start

### **Local Installation**
```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/SMART-TEXT-ASSISTANT.git
cd SMART-TEXT-ASSISTANT

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run application
python app.py
```

### � Performance Metrics

- **Correction Accuracy**: ~20% improvement over baseline edit distance
- **Processing Speed**: <100ms for real-time corrections
- **Model Loading**: 2-3 min (first run), <10s (cached)
- **Memory Footprint**: ~800MB (all models loaded)

## 🔧 Tech Stack

**Core Technologies:**
- **Languages**: Python 3.11
- **Deep Learning**: PyTorch 2.2.0, Transformers 4.38.0 (Hugging Face)
- **Models**: BERT (bert-base-uncased), DistilGPT-2
- **NLP Libraries**: NLTK, NumPy, SentencePiece
- **Interface**: Gradio 4.19.2
- **Deployment**: Hugging Face Spaces, Docker-ready

**Data Engineering:**
- Custom corpus preprocessing pipeline
- Parallel n-gram training with multiprocessing
- Efficient tokenization and caching strategies
- Model versioning and dependency management

## 📁 Project Structure

```
Advanced-Text-Processing-System/
├── app.py                          # Application entry point
├── app_simple.py                   # Gradio interface implementation
├── text_processor_enhanced.py      # Core AI processing engine
├── requirements.txt                # Python dependencies
├── big_data.txt                    # Training corpus (47K messages)
├── qwerty_graph.txt               # Keyboard adjacency graph
├── LICENSE                         # MIT License
└── README.md                       # Documentation
```

## 🎯 Data Engineering Highlights

✅ **Pipeline Design**: Modular architecture with clear separation (data/models/interface)  
✅ **Scalability**: Multiprocessing for parallel corpus processing  
✅ **Model Management**: Automated transformer download and caching  
✅ **Production Ready**: Error handling, logging, and graceful degradation  
✅ **Deployment**: CI/CD-ready with containerization support  
✅ **Documentation**: Comprehensive code comments and type hints

## 👥 Authors

**El Guelta Mohamad Saber** · **El Hadifi Soukaina**

Data Engineers specializing in NLP, Machine Learning, and Production AI Systems

## 📧 Contact

- 📬 elhadifi.soukaina@gmail.com
- 📬 medsaberelguelta@gmail.com

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**⭐ If you find this project useful, please consider giving it a star! ⭐**

*Built with ❤️ for the NLP and Data Engineering community*

</div>
- Click words to build: `The` → `future` → `is` → `bright` → ...

## 👥 Authors

**El Guelta Mohamad Saber** · **El Hadifi Soukaina**

## 📧 Contact

- elhadifi.soukaina@gmail.com
- medsaberelguelta@gmail.com

## 🔧 Tech Stack

Python · PyTorch · Transformers · BERT · DistilGPT2 · Gradio

---

**Note:** First run may take 2-3 minutes to load AI models. Subsequent runs are much faster!
