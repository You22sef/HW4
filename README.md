
# Homework 4 – Part II: Programming

## Student Information

- **Student Name:** Yousef Aldandani
- **Student ID:** 700783505
- **Course:** CS 5720 – Neural Network & Deep Learning

## Assignment Overview

This assignment focuses on Natural Language Processing (NLP) and attention mechanisms using Python.

The programming section includes three tasks:

1. NLP Preprocessing Pipeline using NLTK.
2. Named Entity Recognition (NER) using spaCy.
3. Scaled Dot-Product Attention using NumPy.


## Q1: NLP Preprocessing Pipeline

### Objective
Perform basic NLP preprocessing using the NLTK library.

### Implementation
The Python function `preprocess_text()` performs three steps:

1. **Tokenization:** Splits the input sentence into individual words and punctuation.
2. **Stopword Removal:** Removes common English stopwords and punctuation.
3. **Stemming:** Uses PorterStemmer to reduce words to their root forms.

### Input Sentence
"NLP techniques are used in virtual assistants like Alexa and Siri."

### Output
The program prints:
- Original Tokens
- Tokens Without Stopwords
- Stemmed Words

### Libraries Used
- NLTK


## Q2: Named Entity Recognition with spaCy

### Objective
Identify and extract named entities from a sentence using the spaCy library.

### Implementation
The program uses the pre-trained English language model `en_core_web_sm` to detect named entities.

For each detected entity, the program prints:

1. **Entity Text:** The name or text of the entity.
2. **Entity Label:** The category, such as PERSON, ORG, GPE, or DATE.
3. **Start Position:** The starting character index.
4. **End Position:** The ending character index (exclusive).

### Input Sentence
"LeBron James as the NBA player of the United States in Laker and won the NBA Final MVP in 2020."

### Output
The program identifies entities such as:
- LeBron James (PERSON)
- NBA (ORG)
- the United States (GPE)
- 2020 (DATE)

The detected entities and their character positions are displayed in the notebook.

### Libraries Used
- spaCy
- en_core_web_sm (English language model)


## Q3: Scaled Dot-Product Attention

### Objective
Implement the scaled dot-product attention mechanism using NumPy.

### Implementation
The Python function `scaled_dot_product_attention()` performs four steps:

1. **Dot Product:** Computes the attention scores by multiplying Q by the transpose of K (QK^T).
2. **Scaling:** Divides the attention scores by the square root of the key dimension.
3. **Softmax:** Converts the scaled scores into attention weights.
4. **Weighted Sum:** Multiplies the attention weights by V to produce the final output.

### Input Matrices
Q = [[1, 0, 1, 0], [0, 1, 0, 1]]

K = [[1, 0, 1, 0], [0, 1, 0, 1]]

V = [[1, 2, 3, 4], [5, 6, 7, 8]]

### Output
The program prints:

**Attention Weights Matrix:**
```
[[0.731 0.269]
 [0.269 0.731]]
```

**Final Output Matrix:**
```
[[2.076 3.076 4.076 5.076]
 [3.924 4.924 5.924 6.924]]
```

### Libraries Used
- NumPy


## Requirements

The assignment was developed using Python in JupyterLab.

Required Python libraries:
- NumPy
- NLTK
- spaCy

Required language resources:
- NLTK: punkt_tab and stopwords
- spaCy: en_core_web_sm

## Installation

Install the required Python libraries:

```bash
pip install numpy nltk spacy
```

Download the required NLTK resources:

```python
import nltk
nltk.download('punkt_tab')
nltk.download('stopwords')
```

Download the spaCy English language model:

```bash
python -m spacy download en_core_web_sm
```

## How to Run

1. Install Python and JupyterLab.
2. Install the required libraries and language resources.
3. Open JupyterLab.
4. Open the `HW4.ipynb` notebook.
5. Select **Kernel → Restart Kernel and Run All Cells**.
6. Review the outputs for Q1, Q2, and Q3.

## Files

- `HW4.ipynb` – Python code, outputs, and short-answer questions.
- `README.md` – Assignment description and execution instructions.
