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
3. Data files:
   - A sample text corpus (`big_data.txt`) is provided in the repository for testing and demonstration purposes.
   - A keyboard graph file (`qwerty_graph.txt`) describing keyboard layout adjacencies is also included.
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

## 📸 Demo Screenshots
#### 📝 Spelling Correction
<img width="1256" height="604" alt="Image" src="https://github.com/user-attachments/assets/9b416b3b-16b6-45e5-ba1f-32d676e59954" />

#### 🔮 Auto-completion
<img width="1288" height="638" alt="Image" src="https://github.com/user-attachments/assets/ba69a842-4b51-4fe1-9956-8731c3940195" />

#### ✨ Text Generation
<img width="1256" height="624" alt="Image" src="https://github.com/user-attachments/assets/b5982574-de8f-45ec-b845-2baa973f5159" />

#### ⚡ Combined Correction + Auto-completion
<img width="1253" height="656" alt="Image" src="https://github.com/user-attachments/assets/33570f1c-4bbf-406e-975c-6fb130751783" />

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
**Note:**     The quality and accuracy of the text processing results depend significantly on the size and quality of the corpus used for training. A larger and more diverse corpus typically leads to better language modeling, more accurate spelling corrections, and more natural text generation. While the sample corpus included in this repository is sufficient for demonstration, using a larger corpus for production applications is recommended.
---

## 👥 Contributors
- El Guelta Mohamad Saber
- El Hadifi Soukaina

## 📧 Contact
For questions or suggestions, feel free to reach out: <br>
- elhadifi.soukaina@gmail.com <br>
- medsaberelguelta@gmail.com <br>
