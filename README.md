# Three Chatbot Conversation

A Jupyter notebook experiment where three AI personas take turns in one conversation:

- **Blake**: an argumentative NVIDIA Nemotron chatbot served through OpenRouter.
- **Charlie**: a polite, conciliatory chatbot powered by Gemini.
- **Alex**: a second argumentative persona, also served through OpenRouter.

The notebook keeps a shared conversation history and displays each response as Markdown.

## Requirements

- Python 3.9 or newer
- Jupyter Notebook or JupyterLab
- A Google AI API key with access to the configured Gemini model
- An OpenRouter API key with access to the configured Nemotron model

## Setup

1. Clone this repository and open its folder in a terminal.
2. Create and activate a virtual environment (recommended).
3. Install the Python packages:

   ```bash
   python -m pip install jupyter openai python-dotenv requests
   ```

4. Create a `.env` file in the project folder:

   ```dotenv
   GOOGLE_API_KEY=your_google_api_key
   OPENROUTER_API_KEY=your_openrouter_api_key
   ```

   Keep `.env` private. Do not commit API keys or paste them into the notebook.

## Run

Start Jupyter from the project folder and open `three_chatbot.ipynb`:

```bash
jupyter notebook
```

Run the cells from top to bottom. The notebook loads credentials from `.env`, configures the Gemini and OpenRouter clients, and then runs individual calls and a short turn-taking conversation. Model calls require network access and may be subject to provider rate limits or pricing. Check your providers' current model availability and terms before running.

## Configuration

The model identifiers and persona prompts are defined in the notebook. The conversation loop currently runs for two rounds; change its `range(2)` value to adjust the number of rounds.
