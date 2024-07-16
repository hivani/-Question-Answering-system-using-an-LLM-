# Question Answering System

## Setup Instructions

1. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

2. Run the system:
    ```sh
    streamlit run app.py
    ```

3. Ensure Milvus is running:
    ```sh
    milvus_server start
    ```

## Dependencies

- spacy
- sentence-transformers
- pymilvus
- transformers
- streamlit
