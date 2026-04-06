# agentic-rag-optimised

This will be my playground for optimising my RAG architecture that I will eventually use in production. The goal is to learn. So this will need to be constantly iteratedover, tracked and built upon. I will use libraies only where applicable and will try to build in house wherever possible

### V1.0 The Beginning
- Data source: Fabricated Markdown documents. 76 files total in 4 folders locally.
- Data preprocessing: Adding Metadata and source headers using Langchain directory loader
- Chunking: Langchain RecursiveCharacterTextSplitter chunking (chunk_size=1000, overlap=200)
- Embeddings: OpenAI text-embedding-3-small
- Vector store: ChromaDB with 4 separate collections (employees, contracts, company, products), persisted locally
- Retrieval: Top-3 chunk retrieval per collection using LangChain retriever
- Agent: OpenAI gpt-4.1-nano with function calling (tool_choice=auto), iterative tool loop up to 10 steps
- Tools: 4 typed retrieval tools — search_employees, search_contracts, search_company, search_products
- UI: Gradio ChatInterface
