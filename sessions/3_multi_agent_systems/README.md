# 3.1 Multi-Agent Financial Research System

## Summary

This notebook demonstrates how to build a specialized multi-agent system for financial research and analysis. The system combines RAG (Retrieval Augmented Generation), web search, and code generation capabilities to provide comprehensive financial insights with built-in quality controls.

## Key Components

1. **Setup and Configuration**

   - Installation of required packages (langchain-community, langchain-openai, chromadb, e2b)
   - Configuration of API keys (OpenAI, Tavily, E2B, Langchain)
   - Import of necessary libraries and components

2. **RAG Index**

   - Vector index built from financial PDF documents
   - Document retrieval and embedding systems
   - Document splitting and processing

3. **Intelligent Routing**

   - Question router for directing queries to appropriate data sources
   - Retrieval grader for assessing document relevance
   - Hallucination detection and answer validation

4. **Code Interpretation**

   - Python code interpreter integration
   - Graph state management
   - Visualization capabilities

5. **Graph-Based Workflow**

   - State-based graph workflow implementation
   - Conditional routing based on document relevance
   - Integration of web search and vector store retrieval

6. **Interactive Interface**
   - Gradio-based user interface
   - Visual workflow representation
   - Step-by-step execution tracking

## Key Features

- Document analysis and retrieval
- Multi-stage answer generation
- Quality assessment and validation
- Dynamic visualization capabilities
- Interactive research (RAG / Web) and code generation

## Prerequisites

- Python 3.10+
- OpenAI API key
- Tavily API key (for web search)
- E2B API key (for code interpretation)
- Langchain API key (for Langsmith tracing / interpretability)

## Required Packages

pip install langchain-community==0.3.1
pip install langchain-openai==0.2.0
pip install chromadb==0.5.11
pip install e2b==1.0.2
pip install e2b-code-interpreter==1.0.1
pip install langgraph==0.2.23
pip install pypdf==5.1.0
pip install gradio

## Getting Started

1. Clone this repository
2. Configure your API keys
3. Upload `3_1_multi_agent_system.ipynb` to Google colab or open locally (install dependencies in a virtual environment if running locally)

## Example Usage

Basic question about company revenue
question = "What is the revenue trend for NVIDIA in the past 4 years?"
The system will:

1. Route the question to appropriate data source
2. Retrieve and validate relevant information
3. Validate the response quality
4. Generate a response with visualization
5. You can run the same request through the Gradio interface

## Notes

- The system requires valid PDF documents for RAG functionality
- Web search is used as fallback when local documents don't contain relevant information
- Code generation is used for creating visualizations of financial data
- Quality controls help ensure accurate and relevant responses
