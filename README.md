🤖 AI Chat Agent with Tool Calling (LangGraph + Gemini)

An intelligent AI chat agent built using LangGraph, LangChain, and Google Gemini, featuring tool calling, persistent memory, and multi-tool orchestration.

This project demonstrates how to build a production-style LLM agent capable of reasoning, calling external tools, and maintaining conversation state using a graph-based execution model.

🚀 Project Overview

This system is an AI-powered conversational agent that can:

Understand natural language queries

Decide when to call external tools

Execute tools like search, calculator, and stock price lookup

Maintain long-term memory using SQLite

Orchestrate reasoning using LangGraph workflows

The agent is built using a graph-based architecture instead of simple prompt chains, making it scalable, modular, and production-ready.

🧠 Core Architecture

The system is powered by:

LangGraph for agent workflow orchestration

LangChain for tool integration

Google Gemini (gemini-2.5-flash) as the LLM

SQLite for persistent memory

Tool calling for real-world actions

🔧 Features

✔ Graph-based AI agent (LangGraph)
✔ Tool calling with dynamic routing
✔ Persistent chat memory (SQLite)
✔ Google Gemini LLM integration
✔ External API integrations
✔ Modular tool architecture

🛠️ Tools Integrated

The agent can automatically decide when to use these tools:

🔍 DuckDuckGo Search

Real-time web search for information retrieval.

🧮 Calculator Tool

Supports:

Addition

Subtraction

Multiplication

Division

📈 Stock Price Tool

Fetches live stock prices using Alpha Vantage API.

🏗️ System Design

The agent is implemented using a state-driven execution graph.

Workflow:
User Input → LLM Reasoning → Tool Decision
              ↓
          Tool Execution
              ↓
        LLM Final Response

Graph Nodes:

chat_node → Handles LLM reasoning and tool selection

tools → Executes selected tools

Conditional routing via tools_condition

💾 Persistent Memory

Conversation history is stored using:

SQLite database (chatbot.db)

LangGraph SqliteSaver checkpointer

Thread-based conversation tracking

This enables:

Long-term conversation memory

Multi-session chat history

Stateful AI interactions

⚙️ Tech Stack

Python

LangGraph

LangChain

Google Gemini (Generative AI)

SQLite

DuckDuckGo Search API

Alpha Vantage API

Requests

dotenv

📁 Project Structure
Chat_AI_Agent_with_tool_calling/
│
├── backend.py
├── frontend.py
├── frontend_2.py
├── chatbot.db
├── requirements.txt
├── .env
└── README.md

▶️ How to Run
1. Install dependencies
pip install -r requirements.txt

2. Create .env file
GOOGLE_API_KEY=your_gemini_api_key

3. Run backend
python backend.py

4. Run frontend
python frontend.py

🔮 Future Enhancements

Web UI (Streamlit / React)

FastAPI backend

Tool marketplace

RAG integration

Vector database memory

Agent analytics dashboard
