# 🔤 Advanced Text Processing System 🤖

## 📜 Project Overview
Advanced Text Processing System is a comprehensive NLP project that provides powerful text processing capabilities. The system implements n-gram language modeling to power various natural language processing tasks including spelling correction, text auto-completion, and text generation, all accessible through an intuitive web interface built with Gradio.

## 🎯 Key Objectives
1. **🔍 Language Modeling:**
   - Implement n-gram language models with add-k smoothing for probabilistic text prediction.
   - Train models on large text corpora to learn word patterns and relationships.

2. **🛠️ Text Processing & Correction:**
   - Develop multiple spelling correction algorithms including edit distance, phonetic matching, and keyboard-aware correction.
   - Process and clean text data for NLP applications.

3. **✍️ Text Generation & Completion:**
   - Generate coherent text continuations based on trained language models.
   - Provide intelligent auto-completion suggestions for partial text input.

4. **🖥️ Interactive Web Interface:**
   - Create a user-friendly interface with Gradio to make NLP capabilities accessible.
   - Enable real-time text correction and completion through an intuitive UI.

## ⚙️ Tech Stack
- **Python**: Core programming language for the entire system.
- **NumPy**: For efficient numerical computations and array operations.
- **Gradio**: For building the interactive web interface.
- **Multiprocessing**: For parallel processing during model training.
- **Regular Expressions**: For text preprocessing and cleaning.

## 🚀 Getting Started
1. Clone this repository to your local machine.
2. Install dependencies:
   ```bash
   pip install numpy gradio
   ```
3. Prepare your data files:
   - A text corpus file (large text collection for training)
   - A keyboard graph file (describing keyboard layout adjacencies)
4. Run the application:
   ```python
   from text_processor import TextProcessor, TextProcessorApp

   processor = TextProcessor(
       corpus_path="path/to/corpus.txt",
       keyboard_graph_path="path/to/keyboard_graph.txt",
       ngram_size=2,
       smoothing_k=0.1,
       min_frequency=2
   )

   app = TextProcessorApp(processor)
   app.launch()
   ```

## 💻 Features in Detail
- **N-gram Language Modeling**: Creates probabilistic models of language
- **Spelling Correction**: Uses multiple methods:
  - Edit distance-based correction
  - Phonetic matching with Soundex algorithm
  - Keyboard layout-aware correction
- **Text Generation**: Produces contextually relevant text continuations
- **Auto-completion**: Predicts likely next words in a sentence
- **Web Interface**: Four functional tabs for different text processing tasks:
  1. Text Correction
  2. Auto-completion
  3. Correction + Auto-completion
  4. Text Generation

## 📊 Keyboard Graph Format
The keyboard graph file represents adjacent keys on a keyboard layout:
```
a s w q
b v g n
c x d f
...
```
Each line starts with a key followed by its adjacent keys on the keyboard.

---
**Note:** This project demonstrates advanced NLP techniques and can be adapted for various text processing applications.
---

## 👥 Contributors
- El Hadifi Soukaina
- El Guelta Mohamad Saber

## 📧 Contact
For questions or suggestions, feel free to reach out: <br>
- elhadifi.soukaina@gmail.com <br>
- medsaberelguelta@gmail.com <br>
