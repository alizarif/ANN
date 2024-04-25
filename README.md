# ANN
Approximate Nearest Neighbors Algorithms

## Overview
This code provides a process for extracting text from PDF files, preprocessing the text, and applying Natural Language Processing (NLP) techniques to vectorize words using different transformer models. The main purpose of this code is to find the nearest neighbot of "1" word (for example in this case Inflation) and uses `annoy`, `faiss`, and `hnswlib` as three algorithm to find the nearest neighbors of that word.

## Key Features
- **PDF Text Extraction**: Utilizes `PyPDF2` to read PDF files and extract text.
- **Text Tokenization and Preprocessing**: Tokenizes the extracted text and filters out non-alphabetic tokens using `nltk`.
- **Model Loading and Vectorization**: Uses multiple transformer models (GPT-2, RoBERTa, BERT) in the small version and (GPT-2 (small, medium,large), RoBERTa(small,large), BERT (small,large) and xlnet) to tokens into vectors as tokenizers.
- **Index Building**: Creates indexes using Annoy, FAISS, and HNSWlib for efficient nearest neighbor searches.
- **Nearest Neighbor Search**: Implements search functionality to find words closest to a given target word in the vector space.
- **Result Saving**: Outputs the nearest neighbors' results to CSV and Excel for further analysis.

## Example Workflow
The script processes specified PDF files to find nearest neighbors of a target word using selected NLP models. Results are saved and summarized in Excel format, making it easy to review and analyze the output.

## Dependencies
Make sure to install the required libraries using:
```bash
pip install numpy torch PyPDF2 nltk faiss-cpu hnswlib annoy pandas transformers
