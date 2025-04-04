# Chatbot using NLP and TensorFlow

## Overview
This chatbot is built using Python, TensorFlow, and NLTK to recognize user input and respond with appropriate answers based on predefined intents. The model is trained on an `intents.json` file that contains categories of questions and their respective responses.

## Features
- Tokenization and stemming of words using NLTK
- Neural network model built with TensorFlow and TFLearn
- Training of the chatbot with intent-based pattern matching
- Interactive chat session with the chatbot

## Prerequisites
Before running the chatbot, ensure you have the following dependencies installed:

```sh
pip install nltk numpy tensorflow tflearn
```

## Project Structure
```
├── intents.json  # File containing training data with patterns and responses
├── chatbot.py    # Main chatbot script
├── model.tflearn # Saved trained model (after running the script)
```

## How It Works
1. **Data Preprocessing:**
   - Loads `intents.json` containing different conversation intents.
   - Tokenizes and stems words using the Lancaster Stemmer.
   - Converts text patterns into numerical feature vectors.

2. **Model Training:**
   - Constructs a neural network using TFLearn.
   - Trains the model with input data (bag of words) and outputs (intent categories).
   - Saves the trained model.

3. **Chat Functionality:**
   - Accepts user input.
   - Processes input to identify the best matching intent.
   - Responds with a suitable response from `intents.json`.

## Usage
1. Run the chatbot script:

```sh
python chatbot.py
```

2. Start chatting with the bot. Type your message and receive responses.
3. To exit the chat, type `quit`.

## Example Interaction
```
You: Hello
Bot: Hi there! How can I help you?

You: What is your name?
Bot: I'm a chatbot created to assist you!

You: quit
```

## Customization
To customize the chatbot:
- Modify `intents.json` to add new patterns and responses.
- Retrain the model by running `chatbot.py` after modifying `intents.json`.

## Limitations
- The chatbot relies on predefined intents and cannot handle out-of-scope queries.
- Requires retraining for new data additions.

## Future Improvements
- Implementing more advanced NLP techniques like transformers.
- Adding a database for dynamic conversation handling.
- Enhancing response generation with machine learning models.

