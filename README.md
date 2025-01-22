# **Medical-RAG-Question-Answering-System**
This project implements a Retrieval-Augmented Generation (RAG) system using LangChain, Hugging Face models, and Chroma for document embedding and retrieval. The system processes PDF documents, splits them into manageable chunks, stores their embeddings in a vector database, and retrieves relevant context to answer user queries. It also leverages conversational memory for context-aware question-answering.

## **Features**
1. RAG Architecture: Combines document retrieval with a language model for context-aware answers.
2. Extracts text from PDF documents using PyPDFLoader.
3. Splits text into chunks for efficient processing and embedding.
4. Embeds document chunks using Hugging Face sentence transformers.
5. Stores and retrieves document embeddings with Chroma vector database.
6. Supports conversational memory to track context across multiple queries.
7. Utilizes Hugging Face google/flan-t5-large for language generation.
8. Customizable prompt templates for improved responses.

# **Code Workflow**

1. ## **PDF File Loading:**

Extracts content from all PDF files in a directory using PyPDFLoader.

2. ## **Text Splitting:**

Splits extracted text into smaller chunks with overlap for better embedding and retrieval.

3. ## **Embedding Creation:**

Uses Hugging Face’s all-MiniLM-L6-v2 model to generate embeddings for document chunks.

4. ## **Vector Database Creation:**

Stores embeddings in a Chroma vector database for efficient retrieval.

5. ## **Retrieval-Augmented Generation (RAG):**

Combines retrieved context from Chroma with the language model to generate context-aware answers.

Implements conversational memory to track and use previous interactions for better responses.

6. ## **Question-Answering:**

Answers user queries by retrieving relevant information and generating responses.

Example:

**Question: What is Acromegaly and gigantism?**

**Answer:** Acromegaly is a disorder in which the abnormal release of a particular chemical from the pituitary gland in the brain causes increased growth in bone and soft tissue, as well as a variety of other disturbances throughout the body.

# **Customizing the Project**

Replace google/flan-t5-large with another Hugging Face model if needed.

Adjust chunk_size and chunk_overlap in the text splitter for optimal performance based on your documents.

Modify the RAG prompt template to suit your use case.

