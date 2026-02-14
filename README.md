RAG-Ready Data Lakehouse
Project Overview

Moving from traditional BI to AI requires a new type of data pipeline. This project automates the transformation of unstructured PDF/Markdown data into a Vector Database (Pinecone), enabling Large Language Models to perform semantic search on private company data.
The Technical Workflow

    ETL for Text: Extracts text from varied sources and utilizes LangChain’s RecursiveCharacterTextSplitter for optimal chunking (1000 tokens with 200 overlap).

    Embedding Generation: Pass chunks through OpenAI’s text-embedding-3-small model to create 1536-dimensional vectors.

    Vector Upsert: Efficiently batches vector writes into Pinecone, including metadata tags (Source URL, Timestamp, Page Number) for filtered retrieval.

    Retrieval Test: Includes a query.py script to demonstrate a similarity search against the stored vectors.

Detailed Tech Stack

    LLM Framework: LangChain / LlamaIndex

    Vector DB: Pinecone

    Processing: Python (Pandas/PyPDF)

    Cloud Storage: AWS S3 for raw document persistence
