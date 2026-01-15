# LingoLingo - Expression Learner Agent

A conversational AI agent designed to help users learn English idioms, slang, and expressions through natural conversation.

## Project Overview

The Expression Learner is an intelligent language learning platform that:
- Engages users in natural conversations with a native speaker persona (US/UK variants)
- Teaches idioms and expressions in context through real-world topics
- Uses RSS feeds to propose relevant discussion topics (News, Tech, Culture)
- Provides interactive learning with highlighted expressions and tooltips
- Visualizes the agent's reasoning process using the ReAct pattern

## Architecture

This is a monorepo containing:

### Backend (`/backend`)
- **Technology**: Python 3.13+, FastAPI, LangGraph, LangChain
- **Purpose**: AI orchestration, API endpoints, and Azure OpenAI integration
- **Key Features**:
  - State-based conversation management with LangGraph
  - RSS feed integration for topic generation
  - Expression extraction and highlighting
  - Streaming responses with Server-Sent Events

### Frontend (`/frontend`)
- **Technology**: React, Vite, TypeScript, Tailwind CSS
- **Purpose**: Interactive user interface for learning sessions
- **Key Features**:
  - Session setup and variant selection
  - Real-time chat interface
  - Interactive expression tooltips
  - Agent thought process visualization

### Infrastructure (`/infra`)
- **Technology**: Azure Bicep
- **Purpose**: Deployment configuration for Azure Container Apps

## Getting Started

### Prerequisites
- Python 3.13 or higher
- Node.js 20.0.0 or higher
- Azure OpenAI access

### Backend Setup

```bash
cd backend
pip install -e ".[dev]"
```

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

## Development

### Backend Development
```bash
cd backend
# Run tests
pytest
# Lint code
ruff check .
# Type checking
mypy .
```

### Frontend Development
```bash
cd frontend
# Start dev server
npm run dev
# Build for production
npm run build
# Lint code
npm run lint
# Type checking
npm run type-check
```

## Configuration

Required environment variables:
- `AZURE_OPENAI_ENDPOINT`
- `AZURE_OPENAI_DEPLOYMENT_NAME`
- `AZURE_OPENAI_API_VERSION`
- `AZURE_CLIENT_ID` (for Managed Identity)

## Contributing

This project uses Mayor West Mode for autonomous GitHub Copilot development workflows. Please refer to `AGENTS.md` for agent guidelines.

## License

[License information to be added]
