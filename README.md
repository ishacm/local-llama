# Local Llama

A local chatbot application built with Chainlit and Ollama (Llama vision 3.2), featuring vision capabilities for image processing and natural conversation.

## Features

- No cloud dependencies
- Image analysis capabilities
- Real-time streaming responses
- Conversation memory


## Prerequisites

- Python 3.8 or higher
- Ollama installed on your system
- At least 16GB RAM recommended

## Installation

1. Clone this repository:

2. Install required packages:
```bash
pip install chainlit ollama
```

3. Install Ollama and pull the required model:
```bash
# Install Ollama from https://ollama.ai
ollama pull llama3.2-vision
```

## Usage

1. Start the application:
```bash
python -m chainlit run app.py
```

2. Open your browser and navigate to your localhost

3. Start chatting! You can:
   - Send text messages
   - Upload images for analysis
   - Get real-time streaming responses

## Code Structure

- `@cl.on_chat_start`: Initializes the chat session with a system prompt
- `@cl.step(type="tool")`: Handles message processing and model interaction
- `@cl.on_message`: Manages incoming messages and image processing


## Troubleshooting

Common issues and solutions:

1. If Chainlit command isn't recognized:
```bash
# Use Python module execution instead
python -m chainlit run app.py
```

2. If Ollama model fails to load:
```bash
# Verify model is installed
ollama list
# Pull model if missing
ollama pull llama3.2-vision
```

## Limitations

- Requires local computing resources
- Image processing capabilities depend on model support
- Response time may vary based on hardware specifications

