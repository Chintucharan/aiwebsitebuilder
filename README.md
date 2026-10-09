# 🚀 Website Builder

An AI-powered website builder using **CrewAI** that creates complete websites with multiple specialized AI agents working together. It leverages Google's Gemini API for AI-powered content generation and Serper for web research.

## 🌟 Features

* 🤖 Automated website creation using AI agents
* 👥 Specialized agents for research, HTML, CSS, and JavaScript
* ⚙️ Configuration-based agent and task management
* 🛡️ Error handling and configuration validation
* 📁 File management utilities
* 📝 Type-safe Python codebase
* 🔄 Training and replay capabilities
* 🧪 Testing support
* 🧠 Powered by Google Gemini API
* 🔎 Web research using Serper API

## 📋 Prerequisites

* Python 3.8 or higher
* Google Gemini API key
* Serper API key for web search
* Internet connection

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/Chintucharan/Website-Builder.git
cd Website-Builder
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install the project

For basic usage:

```bash
python -m pip install -e .
```

For development dependencies, if configured:

```bash
python -m pip install -e ".[dev]"
```

### 4. Configure environment variables

Create a `.env` file in the project root, alongside `pyproject.toml`.

Add your API keys:

```dotenv
MODEL=gemini/gemini-1.5-pro-latest
GOOGLE_GEMINI_API_KEY=your_gemini_api_key
GEMINI_API_KEY=your_gemini_api_key
SERPER_API_KEY=your_serper_api_key
```

Replace the placeholders with your actual API keys.

**Security:** Never commit your `.env` file or expose API keys publicly. Add `.env` to `.gitignore`.

## 🔑 Setting Up Google Gemini API

1. Visit [Google AI Studio](https://aistudio.google.com/apikey).
2. Sign in with your Google account.
3. Create or obtain an API key.
4. Add the key to your `.env` file.

Refer to the [Gemini API documentation](https://ai.google.dev/gemini-api/docs) for model and API setup details.

## 🔎 Setting Up Serper API

1. Visit [Serper](https://serper.dev/).
2. Create an account or sign in.
3. Obtain your API key from the dashboard.
4. Add it to your `.env` file as `SERPER_API_KEY`.

Serper enables the research agent to search the web for relevant information.

## 💻 Usage

### Generate a website

Run the following command from the project root:

```bash
python -m website_builder.main run "Create a modern personal portfolio website"
```

For example:

```bash
python -m website_builder.main run "Create a business website with Home, About, Services, and Contact sections"
```

The AI agents collaborate to research the topic and generate HTML, CSS, and JavaScript files.

### Train the crew

```bash
python -m website_builder.main train 10 training_session.json "Create a portfolio website"
```

### Replay a task

```bash
python -m website_builder.main replay "task_id"
```

### Test the crew

```bash
python -m website_builder.main test 5 "gemini/gemini-1.5-pro-latest" "Create a portfolio website"
```

**Note:** These commands follow the project's CLI interface. Available arguments and model settings may depend on your installed CrewAI version and implementation.

## 🏗️ Project Structure

```text
Website-Builder/
├── src/
│   └── website_builder/
│       ├── config/
│       │   ├── agents.yaml
│       │   └── tasks.yaml
│       ├── utils/
│       ├── tools/
│       ├── main.py
│       └── crew.py
├── tests/
├── knowledge/
├── output/
├── db/
├── pyproject.toml
├── .gitignore
├── .env
└── README.md
```

*The exact folders and files may vary depending on your repository.*

## 🛠️ Technologies Used

* **Python** — core programming language
* **CrewAI** — multi-agent orchestration
* **Google Gemini API** — AI-powered generation
* **Serper API** — web search
* **HTML5** — website structure
* **CSS3** — website styling
* **JavaScript** — interactive functionality
* **PyYAML** — configuration management
* **pytest** — testing

## 🧪 Development

### Run tests

```bash
pytest
```

### Format code

If the development tools are installed:

```bash
black .
isort .
```

### Type checking

```bash
mypy .
```

### Linting

```bash
flake8
```

These commands require the corresponding tools to be installed and configured.

## ❓ Frequently Asked Questions

### What is CrewAI?

CrewAI is a framework for orchestrating AI agents that collaborate to complete tasks. This project uses specialized agents for research and website development.

### What types of websites can it generate?

The builder is designed to generate websites such as:

* Personal portfolios
* Business websites
* Landing pages
* Blogs
* Basic e-commerce websites

The results depend on the topic, task configuration, available tools, and AI model.

### Do I need coding knowledge?

No. You can describe the website you want in natural language. Basic HTML, CSS, and JavaScript knowledge is useful for customizing the generated files.

### Where are generated files saved?

The configured tasks save website files in the `output/` directory:

* `output/index.html`
* `output/style.css`
* `output/script.js`

Check your project configuration if your output paths differ.

### Why are API keys required?

The Gemini API provides AI generation capabilities, while Serper supports web research. API availability, usage limits, and charges depend on the providers' current plans.

## 🔐 Security

* Keep API keys in `.env`.
* Add `.env` and `.venv/` to `.gitignore`.
* Never hardcode API keys in source code.
* Never commit API keys to GitHub.
* Rotate any API key that has been exposed publicly.

## 🤝 Contributing

Contributions and suggestions are welcome.

1. Fork the repository.

2. Create a feature branch:

   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add a new feature"
   ```

4. Push your branch:

   ```bash
   git push origin feature/AmazingFeature
   ```

5. Open a pull request.

## 📄 License

This project is intended to use the MIT License. Add a `LICENSE` file containing the MIT License text if you have selected that license for your repository.

## 🙏 Acknowledgments

* **CrewAI** for the multi-agent AI framework.
* **Google** for Gemini AI capabilities.
* **Serper** for web search functionality.
* **Saptaparni Pal** for her contributions to `crew.py`.

## 👨‍💻 Author

**Gowni Venkat Charan**

* GitHub: [@Chintucharan](https://github.com/Chintucharan)
* Project: [Website Builder](https://github.com/Chintucharan/Website-Builder)

*Built with Python, CrewAI, Google Gemini, and Serper.*
