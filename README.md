🧠 Mini GPT Chatbot using Ollama + DeepSeek-R1

A lightweight, fully local ChatGPT-like AI chatbot built using the DeepSeek-R1 model and Ollama, wrapped in an elegant Streamlit interface.

This chatbot features a real-time thinking phase, response streaming, and an intuitive chat UI — all in a single Python file!
🚀 Features

    🔮 Streamed Responses from DeepSeek-R1 via Ollama

    💡 "Thinking" Phase with expandable reasoning (mimics Chain-of-Thought)

    🧵 Chat History preserved across interactions

    🌐 Streamlit UI with modern layout and inline branding

    🖼️ Inline Logo Support with Base64 image encoding

🛠️ Requirements

    Python 3.9+

    Ollama (running locally)

    DeepSeek-R1 model pulled in Ollama:

ollama pull deepseek-r1

📦 Installation

    Clone the repository

git clone https://github.com/yourusername/mini-gpt-chatbot.git
cd mini-gpt-chatbot

    Install dependencies

pip install streamlit ollama

    Run Ollama server

Make sure Ollama is running locally (usually auto-started on install):

ollama run deepseek-r1

    Add Logo Image

Place your deep-seek.png logo in the project root. This will be used in the app header.
🧑‍💻 Usage

Run the Streamlit app:

streamlit run main.py

Interact via the chat interface. The assistant will first “think” (display reasoning in an expandable section) and then provide a final answer.
🧠 How It Works

   Messages are passed to the DeepSeek-R1 model via the Ollama API

   The model generates output in two phases:

   A reasoning phase enclosed in <think>...</think> tags

   A final answer after the reasoning

The UI shows the reasoning in an expandable box and the final response below it

Entire conversation state is cached in st.session_state

'''bash 

📁 Project Structure

mini-gpt-chatbot/
├── main.py               # Main Streamlit UI script
├── deep-seek.png         # Logo shown in the app header
└── README.md             # Project documentation

'''

📃 License

This project is open-source and available under the MIT License.
🙌 Acknowledgements
 Ollama for making local LLMs easy to run

 DeepSeek for the amazing open-source model

 Streamlit for the powerful UI framework
