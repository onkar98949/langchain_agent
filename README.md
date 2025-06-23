LLM-Powered Tool-Augmented Q&A System
This project builds an intelligent agent using LangChain and Ollama, enabling a flexible, local-first question-answering system. The agent leverages a combination of pre-indexed vector embeddings, real-time search tools, and structured knowledge bases to respond effectively to user queries across domains like healthcare, supplements, and general knowledge.

Core Features
Local LLM Integration
Utilizes llama3.2:3b served via Ollama for fast, offline inference.

Embedding-Based Retrieval (RAG)
Embeds documents using nomic-embed-text and stores them in a FAISS vector store for similarity-based retrieval.

Multi-Tool Agent
Uses LangChain's create_tool_calling_agent to dynamically select the right tool for a given query.

Domain-Specific Knowledge
Incorporates a custom FAISS index for health and gym supplements to support deep domain understanding.

Web and Academic Search
Includes real-time search with Tavily and biomedical search with PubMed.

Structured Data Integration
Connects to a MongoDB instance to retrieve employee asset information via a dedicated tool.

Modular Design
Easily extendable tool system using LangChain’s @tool decorator.

Prompt Engineering
Uses a structured prompt to guide the agent in deciding whether to use tools or answer directly.

Available Tools
wikipedia_search: General-purpose search from Wikipedia

pubmed_search: Specialized search for medical and life sciences

tavily_search: Web-wide search for current and real-time information

health_supplements: Searches local FAISS index for supplement-related queries

get_assets_by_employee: Fetches employee asset data from MongoDB
