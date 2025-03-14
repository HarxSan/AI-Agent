**AI Agent Demo using Langraph & Tavily**


Overview
---

This repository contains a demo AI agent built using Langraph and Tavily, designed to enhance conversational AI by improving long-term memory and retrieval. The agent intelligently processes user queries, fetches relevant information using Tavily's search tool, and maintains contextual memory using a memory saver, ensuring personalized and efficient responses.

```mermaid
graph TD;
    A["User Input"] --> B["AI Agent"];
    B --> C["Check Memory"];
    C --> D["Retrieve Context"];
    D --> B;
    B --> E{"Use Tavily Search?"};

    E -- Yes --> F["Fetch Results from Tavily"];
    F --> G["Return Search Results"];
    G --> B;
    
    E -- No --> H["Generate Response using LLM"];
    H --> B;

    B --> I["Final Response to User"];
    
    subgraph "External APIs"
      F
    end

    subgraph "Memory System"
      C
      D
    end

```

Features
---

✅ Intelligent Web Search – Uses Tavily for real-time web data retrieval.

✅ Memory-Enhanced Conversations – Saves user interactions for improved context retention.

✅ Efficient State Management – Langraph optimizes agent flow for seamless interactions.

✅ Scalable & Modular Design – Easily extendable to support various AI applications.


Tech Stack
---

Langraph – Manages agent workflows and execution.

Tavily API – Enables real-time web search capabilities.

Memory Saver – Stores past conversations for better personalization.

Python – Core language for implementation.


Installation & Setup
---

1. Clone the Repository

```
git clone https://github.com/HarxSan/AI-Agent
cd AI-Agent
```

2. Install Dependencies

```
pip install langraph tavily openai
```


3. Set Up API Keys

Add your Tavily API Key and LLM credentials as environment variables:

```
export TAVILY_API_KEY="your_tavily_api_key"
export OPENAI_API_KEY="your_openai_api_key"
```

4. Run the AI Agent

Start a conversation with the agent.

It retrieves real-time information using Tavily when needed.

The memory module ensures personalized and context-aware responses.

Future Enhancements
---

🔹 Multi-Agent Collaboration – Enable AI agents to work together on tasks.

🔹 Advanced Memory Optimization – Improve long-term context handling.

🔹 Enhanced Search Filtering – Fine-tune Tavily queries for better accuracy.

Contributing
---

Fork the repository

Create a feature branch (feature/new-enhancement)

Commit your changes

Open a pull request
