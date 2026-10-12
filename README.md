# AI Chatbot

AI Chatbot is a small Python app that lets you chat with an OpenAI model in your browser. It builds on my [OpenAI Prompt Demo](https://github.com/tomiaishasadiq/openai-prompt-demo), which sends one prompt and prints one reply. This is a personal project, written as a learning exercise in going from prompting to building a chatbot.

## From prompt to chatbot

The two are different things:

- **Prompt script**: sends one system prompt and one user prompt, and prints one response. There's no memory of earlier messages.
- **Chatbot**: takes input from the user each turn and keeps the conversation history (a list of messages), so the model can follow what was said before.
- The model has no memory of its own(promting). A prompt script sends a fixed list of two messages (system and user) once, while the chatbot rebuilds the message list on every turn, with the full conversation HISTORY in between, which is how it "remembers" earlier questions.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the requirements in the terminal.

```bash
pip install openai python-dotenv gradio
```

Then create a `.env` file in the project folder and add your own OpenAI API key:

```
OPENAI_API_KEY=your-key-here
```

## Usage

To RUN the app (use `python3` on Mac if needed):

```bash
python main.py
```

Then open the local URL printed in the terminal (usually http://127.0.0.1:7860) and start chatting. To test the memory, tell it your name and then ask what your name is.

To change how the chatbot behaves, edit `system_message` in `main.py`:

```python
# tells the AI who it is and how it should answer
system_message = "You are a helpful assistant"
```

## Try asking

Because the chatbot keeps the conversation history, follow-up questions also work. Examples to try:

### Sample Questions

1. Question: "What are the top 10 universities in Ireland?"
2. Question: "What's the difference between supervised and unsupervised learning? Give me one example of each."
   Follow Up Question: "Which one would I use to group customers by buying habits?"
3. Ask: "Give me a 3-day itinerary for Dublin."
   Follow Up Question: "Make day 2 cheaper."
4. Ask: "My name is  _______ and I'm studying _________ at ________. What certifications should I get?"
   Follow Up Question: "What's my name and what/where am I studying?"


## Contributing

This is a personal learning project, but suggestions are welcome.
