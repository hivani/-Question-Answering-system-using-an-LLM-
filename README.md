# Question Answering System
This project demonstrates a system that processes scraped data, chunks it based on semantic similarity, creates a vector database using FAISS, retrieves and re-ranks data based on a query, and finally uses a language model to provide answers to the queries.

# Table of Contents
1. Setup Instructions
2. Dependencies
3. Running the System
4. Explanation of Code

## Setup Instructions

1. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

2. Run the system:
    ```sh
    streamlit run app.py
    ```

3. Ensure faiss is running:
    ```sh
    milvus_server start
    ```

## Dependencies

-faiss-cpu==1.7.2
numpy==1.21.4
sentence-transformers==2.1.0
streamlit==0.88.0
transformers==4.12.3
