# Question Answering System
This project demonstrates a system that processes scraped data, chunks it based on semantic similarity, creates a vector database using FAISS, retrieves and re-ranks data based on a query, and finally uses a language model to provide answers to the queries.

# Table of Contents
1. Setup Instructions
2. Dependencies
3. Running the System
4. Explanation of Code

## Setup Instructions

1. Clone the Repository:
    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Create a Virtual Environment:
    ```sh
    Create a Virtual Environment
    ```

3. Install Dependencies:
    ```sh
   pip install -r requirements.txt
    ```
4. Download SentenceTransformer Model:
   ```sh
   from sentence_transformers import SentenceTransformer
   model = SentenceTransformer('all-MiniLM-L6-v2')
   ```
5. Set Up FAISS:
   ```sh
   pip install faiss-cpu
   ```
## Dependencies
```sh
-faiss-cpu==1.7.2
numpy==1.21.4
sentence-transformers==2.1.0
streamlit==0.88.0
transformers==4.12.3
```
# Explanation of Code
  # Data Chunking and Vector Database Creation
  1. Load JSON Data:
     Load the scraped data from a JSON file:
  2. Initialize Sentence Transformer:
     Initialize the SentenceTransformer model
  3.  Chunk Data
      Define a function to chunk data based on semantic similarity and apply it to all documents
  4.  Convert to Embedding Vectors:
  5.  Create FAISS Index
  # Retrieval and Re-ranking
  1.  Query Expansion
  2.  Retrieve Data Using FAISS:
  3.  Re-rank Retrieved Data
  # Question Answering
  1. Initialize QA Pipeline
  2. Pass Data to LLM for Answering
  # User Interface    
```python
# Save the following code in a file named app.py

import streamlit as st
from sentence_transformers import SentenceTransformer
import faiss
import numpy as np
from transformers import pipeline

# Initialize Sentence Transformer
model = SentenceTransformer('all-MiniLM-L6-v2')

# Create FAISS index and load data
# ...

# Initialize QA pipeline
qa_pipeline = pipeline('question-answering')

# Define Streamlit UI
def main():
    st.title('Semantic Search and Question Answering System')

    # Add code for UI components and user interaction
    # ...


if __name__ == "__main__":
    main()
```

After creating the `app.py` file, you can run the Streamlit app using the following command in Google Colab:
```sh
!streamlit run app.py
```

Running the Streamlit code will generate a link. You can access the Streamlit app via that link, and it will generate a port number to access this link.

