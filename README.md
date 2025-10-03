# 🔤 Advanced Text Processing System 🤖

## 📜 Project Overview
A Natural Language Processing (NLP) project implementing n-gram language models for:

- Spelling correction
- Text auto-completion
- Text generation

Accessible through a clean Gradio web interface, this system demonstrates how probabilistic language modeling can power advanced text processing applications.

## 🎯 Key Objectives

1. **🔍 Language Modeling:**
   - Train n-gram models with add-k smoothing on text corpora for probabilistic word prediction.
2. **🛠️ Text Correction:**
   - Combine edit distance, phonetic matching (Soundex), and keyboard-aware correction for robust spell checking.
3. **✍️ Text Generation & Completion:**
   - Provide auto-completion suggestions and generate text sequences using statistical sampling from the n-gram distribution.
4. **🖥️ Interactive Web Interface:**
   - Deliver all functionalities in real time via an intuitive Gradio UI.

## ⚙️ Tech Stack
- **Python** (core implementation)
- **NumPy** (efficient computations)
- **Gradio** (web interface)
- **Multiprocessing** (parallel model training)
- **Regex** (text preprocessing)

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

## 💻 Features

- **Spelling Correction** : Edit distance-based correction + phonetic matching with Soundex algorithm + keyboard adjacency.
- **Auto-completion** : Predicts next word(s) from n-gram context.
- **Text Generation**: Iterative probabilistic word sampling (add-k smoothing).
- **Web App**: Four tabs → Correction, Completion, Combined, Generation.


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
