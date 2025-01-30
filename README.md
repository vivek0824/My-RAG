# Retrieval-Augmented Generation (RAG) with ChromaDB and LLaMA 3

This repository implements a **Retrieval-Augmented Generation (RAG) pipeline** using **ChromaDB** as a vector database and **LLaMA 3** as the language model. The system processes documents, stores them in ChromaDB, retrieves relevant contexts, and generates responses using LLaMA 3.

## Features
- **Efficient Vector Search**: Uses ChromaDB for high-speed document retrieval.
- **Powerful Language Model**: Utilizes LLaMA 3 for generating intelligent responses.
- **Advanced Text Embeddings**: Employs Hugging Face embeddings for document representation.
- **Configurable Environment**: Supports `.env` files for easy configuration of paths and API keys.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/vivek0824/rag-chroma-llama3.git
   cd rag-chroma-llama3
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**:
   Create a `.env` file in the project root and specify necessary parameters:
   ```ini
   CHROMA_DB_PATH=./chroma_db
   LLAMA_MODEL=meta-llama/Meta-Llama-3-8B
   EMBEDDING_MODEL=sentence-transformers/all-MiniLM-L6-v2
   ```

## Usage

1. Ensure all required models are downloaded and cached.
2. Place the documents for indexing in the `./data` directory.
3. Export the jupiter notebook in the for of a python script.
4. Run the script:
   ```bash
   python rag_submission.py
   ```
5. The script reads queries from `queries.json` and generates responses based on retrieved contexts.

## Project Structure
```
├── rag_submission.py  # Main script
├── .env               # Environment variables
├── requirements.txt   # Dependency list
├── queries.json       # Query inputs
├── README.md          # Documentation
└── chroma_db/         # ChromaDB storage (auto-generated)
```

## License
This project is licensed under the **MIT License**.

## Contributing
Contributions are welcome! Feel free to submit pull requests or open issues for enhancements and bug fixes.

## Author
[Vivek Singh](https://github.com/vivek0824)

