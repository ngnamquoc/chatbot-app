# Chatbot Application

This is a simple chatbot application built using the Hugging Face Transformers library. The chatbot leverages the `facebook/blenderbot-400M-distill` model to generate conversational responses.

## Features
- Interactive chatbot that maintains conversation history.
- Uses a pre-trained sequence-to-sequence model for generating responses.
- Easy to extend and customize with other Hugging Face models.

## How It Works
The chatbot processes user input, tokenizes it, and generates a response using the BlenderBot model. The conversation flow is as follows:

![Chatbot Flow](static/chatbot-diagram.png)

1. **User Input**: The user provides input to the chatbot.
2. **Transformer**: The input is tokenized into numerical representations.
3. **Large Language Model**: The model processes the tokens and generates a response.
4. **Transformer**: The response is converted back into human-readable text.
## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ngnamquoc/chatbot-app.git
   cd chatbot-app
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv my_env
   source my_env/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Web Interface
1. Start the Flask server:
   ```bash
   flask run
   ```
2. Open your browser and navigate to `http://127.0.0.1:5000` to interact with the chatbot.

### Command Line Interface Alternative
1. Run the chatbot script:
   ```bash
   python3 chatbot.py
   ```
2. Start typing your messages, and the chatbot will respond based on the conversation history.

## Customization

To use a different model, update the `model_name` variable in `app.py` or `chatbot.py` with the desired Hugging Face model. Ensure the model is compatible with `AutoModelForSeq2SeqLM`.

Example:
```python
model_name = "google/flan-t5-base"
```

## Requirements
- Python 3.10 or higher
- Flask
- Flask-CORS
- Hugging Face Transformers
- PyTorch


## License
This project is licensed under the MIT License.