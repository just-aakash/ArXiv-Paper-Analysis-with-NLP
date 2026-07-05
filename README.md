# ArXiv Paper Analysis with NLP

## Introduction

Finding relevant research papers and understanding their key ideas can be a challenging and time-consuming process. Researchers and students often have to read multiple papers before finding the information they actually need.

This project was built to make that process easier. It combines semantic search with modern Natural Language Processing (NLP) models to retrieve relevant research papers, generate summaries, extract important keywords, and answer questions directly from the retrieved paper abstracts.

Instead of manually searching through dozens of papers, users can simply enter a research topic and ask a question. The system finds the most relevant papers and provides useful insights within seconds.

---

## Features

The project provides the following functionalities:

* Semantic search for research papers using Sentence Transformers and FAISS.
* Retrieval of the most relevant papers based on the user's query.
* Automatic summarization of paper abstracts.
* Keyword extraction using KeyBERT.
* Question Answering using a pre-trained RoBERTa model.
* Similarity scores to indicate how closely each paper matches the search query.

---

## How It Works

The workflow of the project is straightforward:

1. The user enters a research topic.
2. The query is converted into vector embeddings using a Sentence Transformer model.
3. FAISS searches the vector database and retrieves the most similar research papers.
4. For each retrieved paper:

   * The title is displayed.
   * The similarity score is shown.
   * A summary of the abstract is generated.
   * Important keywords are extracted.
   * The user can ask a question related to the paper, and the Question Answering model attempts to answer it using the paper's abstract as context.

This creates an interactive research assistant that helps users understand research papers much faster.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Sentence Transformers
* FAISS
* Hugging Face Transformers
* KeyBERT
* PyTorch

---

## Models Used

| Task               | Model                          |
| ------------------ | ------------------------------ |
| Semantic Search    | Sentence Transformers          |
| Vector Search      | FAISS                          |
| Question Answering | deepset/roberta-base-squad2    |
| Summarization      | Hugging Face Transformer Model |
| Keyword Extraction | KeyBERT                        |

---

## Example

**Research Query**

```
Deep learning for medical image analysis
```

**Question**

```
What specific type of neural network is used?
```

For each relevant paper, the system returns:

* Paper title
* Similarity score
* Generated summary
* Extracted keywords
* Answer to the user's question

---

## Repository Structure

```
ArXiv-Paper-Analysis-with-NLP/
│
├── CBSOTSIP_P2.ipynb          # Complete project notebook
├── paper_embeddings.npy       # Precomputed embeddings
├── paper_faiss.index          # FAISS vector index
└── README.md                  # Project documentation
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/just-aakash/ArXiv-Paper-Analysis-with-NLP.git
cd ArXiv-Paper-Analysis-with-NLP
```

Install the required libraries:

```bash
pip install pandas numpy torch transformers sentence-transformers faiss-cpu keybert scikit-learn
```

Launch Jupyter Notebook and open **CBSOTSIP_P2.ipynb** to run the project.

---

## Future Improvements

Some features that can be added in future versions include:

* A web interface using Streamlit or Flask
* Support for uploading PDF research papers
* Multi-document question answering
* Interactive analytics dashboard
* Citation recommendation system
* Research paper visualization

---

## What I Learned

Working on this project helped me gain practical experience with:

* Semantic search
* Vector databases
* Information retrieval
* Transformer-based NLP models
* Question Answering systems
* Text summarization
* Keyword extraction
* Building end-to-end NLP pipelines

---

## Author

**Akash Tiwari**

GitHub: https://github.com/just-aakash

If you find this project useful, feel free to fork the repository or leave a star.
