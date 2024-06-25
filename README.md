# Basic Chatbot

This is a simple rule-based chatbot implemented in Python. The bot responds to user inputs based on predefined keywords and message probabilities.

## Features

- Responds to common greetings and farewells
- Answers questions about the bot's status
- Acknowledges thanks
- Provides predefined responses for specific queries
- Can be easily extended with more responses

## Installation

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/basic-chatbot.git
    ```
2. Navigate to the project directory:
    ```bash
    cd basic-chatbot
    ```
3. Ensure you have Python installed. The script is compatible with Python 3.x.

## Usage

1. Run the script:
    ```bash
    python chatbot.py
    ```
2. Type your messages and press Enter. The bot will respond based on the predefined responses.

## Code Explanation

The main functionality is provided by the following functions:

### `message_probability`

This function calculates the probability that a user message matches a predefined set of recognized words. It considers both the presence of required words and the overall percentage of recognized words in the user message.

### `check_all_messages`

This function checks the user message against all predefined responses and returns the best match based on the calculated probabilities.

### `get_response`

This function splits the user input into words, processes it through `check_all_messages`, and returns the appropriate response.

### `long_responses.py`

This module contains longer responses that can be imported and used in the chatbot. Make sure you have a `long_responses.py` file in the same directory with the following content:

```python
R_ADVICE = "Here's some advice..."
R_EATING = "I like to eat code for breakfast!"

def unknown():
    return "Sorry, I didn't understand that."
