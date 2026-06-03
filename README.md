# Agentic-AI
Building the Agentic AI chatbot project for the Products policy system where user can query and chatbot will provide the result

# Agentic AI Chatbot on Databricks

## Overview

This project demonstrates an end-to-end Agentic AI chatbot built on the Databricks platform. The solution combines both structured and unstructured enterprise knowledge, enabling users to interact with business data and documents through a single conversational interface.

Unlike traditional document-based chatbots, this solution leverages Agentic AI capabilities to intelligently determine the appropriate data source, retrieve relevant context, and generate accurate responses.

---

## Business Problem

Organizations store critical information across multiple systems:

* Unstructured documents (PDFs)
* Structured business data (csv -> Table)

Traditional search systems require users to manually navigate these sources, resulting in:

* Increased time spent searching for information
* Limited visibility across knowledge repositories
* Delayed decision-making
* Poor user experience

This solution addresses these challenges by providing a unified AI-powered assistant capable of querying both knowledge sources simultaneously.

---
## Solution Architecture

### Unstructured Knowledge Base

The unstructured data pipeline processes enterprise documents through:

1. Document Ingestion
2. Text Chunking
3. Embedding Generation
4. Vector Index Creation
5. Vector Search Endpoint

This enables semantic search and contextual retrieval using Retrieval-Augmented Generation (RAG).

### Structured Knowledge Base

Structured business information is stored in Delta Tables and accessed through Unity Catalog Functions.

---

## Architecture Flow

```text
PDF Documents
      │
      ▼
 Chunking
      │
      ▼
 Embeddings
      │
      ▼
 Vector Search Index
      │
      ▼
 Vector Search Endpoint
      │
      ▼
     Agent
      ▲
      │
 UC Functions
      ▲
      │
 Delta Tables
      │
      ▼
 Model Serving Endpoint
      │
      ▼
 Databricks App
      │
      ▼
 End User
```

---

## Key Components

### 1. Vector Search

Provides semantic retrieval capabilities for enterprise documents.

### 2. Delta Tables

Stores structured business data within the Databricks Lakehouse.

### 3. Unity Catalog Functions

Allows the AI agent to access and query governed business data.

### 4. Agent Framework

Responsible for:

* Understanding user intent
* Selecting appropriate retrieval methods
* Calling tools and functions
* Combining responses from multiple sources

### 5. Model Serving Endpoint

Hosts and serves Large Language Models (LLMs) for inference.

### 6. Databricks Apps

Provides the front-end interface for business users.

---

## Technology Stack

| Component         | Technology                 |
| ----------------- | -------------------------- |
| Data Platform     | Databricks                 |
| Storage Layer     | Delta Lake                 |
| Governance        | Unity Catalog              |
| Vector Database   | Databricks Vector Search   |
| LLM Serving       | Databricks Model Serving   |
| Agent Framework   | Databricks Agent Framework |
| Application Layer | Databricks Apps            |
| AI Pattern        | Agentic AI + RAG           |

---

## Benefits

* Single access point for enterprise knowledge
* Reduced manual searching effort
* Improved decision-making speed
* Better user experience
* Secure and governed data access
* Scalable architecture for enterprise adoption

---

## Future Enhancements

* Multi-agent architecture
* Workflow automation
* Action execution capabilities
* Real-time data integration
* Feedback learning loop
* Advanced observability and monitoring

---

## Author

Mill

Data Engineer | AI & ML Enthusiast

Focused on building Data Engineering, Agentic AI, and Generative AI solutions on modern cloud platforms.
