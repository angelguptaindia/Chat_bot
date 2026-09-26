# Chat_bot 🤖

A simple, lightweight AI chatbot built with **Streamlit** and powered by **Google's Gemini API** (`gemini-2.5-flash`). Type a message in the sidebar and get an instant AI-generated response, with the full conversation history displayed on the page.

To try out yourself click [here](https://angelschatbot.streamlit.app/)

## Features

- 💬 Real-time conversational chat interface
- ⚡ Powered by Google's Gemini 2.5 Flash model
- 🗂️ Persistent chat history within a session
- 🔐 Secure API key handling via environment variables or Streamlit secrets
- 🎈 Minimal, easy-to-read Streamlit UI

## Tech Stack

- [Python](https://www.python.org/)
- [Streamlit](https://streamlit.io/) — web app framework
- [google-generativeai](https://pypi.org/project/google-generativeai/) — Gemini API client
- [python-dotenv](https://pypi.org/project/python-dotenv/) — environment variable management

## Prerequisites

- Python 3.8 or higher
- A Google Gemini API key ([get one here](https://aistudio.google.com/app/apikey))

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/angelguptaindia/Chat_bot.git
   cd Chat_bot
   ```

2. **Create a virtual environment (recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

## Configuration

The app looks for your Gemini API key in one of two places:

**Option 1: `.env` file (local development)**

Create a `.env` file in the project root:

```env
API_KEY=your_gemini_api_key_here
```

**Option 2: Streamlit secrets (deployment, e.g. Streamlit Community Cloud)**

Create a `.streamlit/secrets.toml` file:

```toml
API_KEY = "your_gemini_api_key_here"
```

> ⚠️ Never commit your `.env` or `secrets.toml` file to version control. Add them to `.gitignore`.

## Usage

Run the app locally with:

```bash
streamlit run app.py
```

Then open the URL shown in your terminal (typically `http://localhost:8501`) in your browser. Enter a message in the sidebar text box and press Enter to start chatting.

## Project Structure

```
Chat_bot/
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
├── .gitignore
└── README.md
```

## How It Works

1. On startup, the app loads your Gemini API key from `.env` or Streamlit secrets.
2. A Gemini chat session is initialized using the `gemini-2.5-flash` model.
3. User messages entered in the sidebar are sent to the Gemini API.
4. Responses are appended to the session's chat history and rendered in the main panel.

## Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project currently has no license specified. Consider adding one (e.g., [MIT](https://choosealicense.com/licenses/mit/)) to clarify how others can use your code.

## Author

**Angel Gupta** — [@angelguptaindia](https://github.com/angelguptaindia)
