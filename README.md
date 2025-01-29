# 📌 About the Project  

This project implements AI-powered agents capable of retrieving financial data and performing web searches. Using the **Phi AI** framework, it integrates **Groq LLaMA-3.3-70B**, **YFinance**, and **DuckDuckGo** to provide accurate and insightful responses. The project features a **Playground** for interactive agent interactions.  

## ✨ Key Highlights  

- 🤖 **AI Agents**: Two specialized agents:  
  - **Finance AI Agent**: Retrieves stock market data, analyst recommendations, fundamentals, and company news.  
  - **Web Search Agent**: Fetches relevant online information with source citations.  

- 🏗 **Built with Phi AI Framework**: Leveraging `phi.agent`, `phi.model.groq`, and `phi.tools` for AI capabilities.  

- 📊 **Financial Data Analysis**: Uses `YFinanceTools` for real-time stock market insights.  

- 🌍 **Web Search Integration**: Utilizes `DuckDuckGo` to fetch and summarize online information.  

- 🚀 **Interactive Playground**: A user-friendly interface to interact with agents.  

## 🛠 Technologies Used  

- **Python**  
- **Phi AI Framework**  
- **Groq LLaMA-3.3-70B Model**  
- **YFinance API**  
- **DuckDuckGo Search API**  
- **FastAPI**  
- **dotenv (for environment variables)**

## 🏗 Architecture  

The project follows a modular **AI agent-based architecture** designed for efficient data retrieval and interaction.  

### 1️⃣ **Agent Layer**  
- **Finance AI Agent**:  
  - Retrieves real-time stock market data, analyst recommendations, company news, and financial insights.  
  - Uses **YFinanceTools** for fetching stock-related data.  

- **Web Search Agent**:  
  - Searches the web for relevant information and provides source citations.  
  - Uses **DuckDuckGo** for online data retrieval.  

### 2️⃣ **Model Layer**  
- Utilizes **Groq LLaMA-3.3-70B**, a high-performance large language model, to process and generate responses.  

### 3️⃣ **Tool Integration Layer**  
- **YFinanceTools**: Fetches stock prices, financial fundamentals, and analyst insights.  
- **DuckDuckGo**: Provides web search functionality with relevant citations.  

### 4️⃣ **Application Layer (API & UI)**  
- **FastAPI via Phi Playground**:  
  - Hosts the AI agents through an interactive API-based playground.  
  - Provides a user-friendly interface for seamless agent interactions.  

### 5️⃣ **Deployment Layer**  
- Uses `serve_playground_app` to deploy the AI agents locally or in a production environment.  
- Supports **scalable and modular** AI agent management.  

---

### **🖼 Architecture Diagram**  

               ┌────────────────────────┐
               │       User Input       │
               └──────────┬─────────────┘
                          │
    ┌─────────────────────┴─────────────────────┐
    │            AI Agent Layer                 │
    │  ┌────────────────────┐   ┌──────────────┐│
    │  │ Finance AI Agent   │   │ Web Search   ││
    │  │ (YFinanceTools)    │   │ Agent        ││
    │  └────────────────────┘   └──────────────┘│
    └─────────────────────┬─────────────────────┘
                          │
    ┌─────────────────────┴─────────────────────┐
    │             Model Layer                   │
    │   ┌───────────────────────────────┐       │
    │   │  Groq LLaMA-3.3-70B Model     │       │
    │   └───────────────────────────────┘       │
    └─────────────────────┬─────────────────────┘
                          │
    ┌─────────────────────┴─────────────────────┐
    │       Tool Integration Layer              │
    │   ┌──────────────┐   ┌─────────────────┐  │
    │   │ YFinance API │   │ DuckDuckGo API  │  │
    │   └──────────────┘   └─────────────────┘  │
    └─────────────────────┬─────────────────────┘
                          │
    ┌─────────────────────┴─────────────────────┐
    │       Application Layer (API & UI)        │
    │   ┌───────────────┐   ┌────────────────┐  │
    │   │ FastAPI       │   │ Phi Playground │  │
    │   └───────────────┘   └────────────────┘  │
    └─────────────────────┬─────────────────────┘
                          │
                ┌─────────┴─────────┐
                │  Deployment Layer │
                │  (Local & Cloud)  │
                └───────────────────┘
