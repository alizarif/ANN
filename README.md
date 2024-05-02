# ANN
Approximate Nearest Neighbors Algorithms

## Overview
This code provides a process for extracting text from PDF files, preprocessing the text, and applying Natural Language Processing (NLP) techniques to vectorize words using different transformer models. The main purpose of this code is to find "15" nearest neighbors of only "1" word (for example in this case Inflation) and uses `annoy`, `faiss`, and `hnswlib` as three algorithm to find the nearest neighbors of that word.

## Steps
- **PDF Text Extraction**: Utilizes `PyPDF2` to read PDF files and extract text.
- **Text Tokenization and Preprocessing**: Tokenizes the extracted text and filters out non-alphabetic tokens using `nltk`.
- **Model Loading and Vectorization**: Uses multiple transformer models as tokenizers (GPT-2 (small, medium,large), RoBERTa(small,large), BERT (small,large) and XLNet) to convert tokens into vectors.
- **Index Building**: Creates indexes using Annoy, FAISS, and HNSWlib for efficient nearest neighbor searches.
- **Nearest Neighbor Search**: Implements search functionality to find words closest to a given target word in the vector space.
- **Result Saving**: Outputs the nearest neighbors' results to CSV and Excel for further analysis.

## Requirements
Make sure to install the required libraries:
```bash
pip install numpy torch PyPDF2 nltk faiss-cpu hnswlib annoy pandas transformers
```

This code is part of a larger project about LLMs and AI Agents. 
