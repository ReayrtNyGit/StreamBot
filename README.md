# Gradio Chat Interface Demo
This code is a demo showcasing the use of Gradio's Chat interface with OpenAI models. It allows users to have interactive conversations with the AI model.

The code is based on the example provide on the [sentdex](https://youtu.be/m1feTAvlXxw?si=4OqNBhZbiYkflWTs) YouTube channel which included sample [code](https://huggingface.co/spaces/Sentdex/StableBeluga-7B-Chat/blob/main/app.py) for providing a text streaming web interface for a locally run Large Language Model.


## System Prompt
A system prompt can be used to guide the behavior of the model. You can choose from the provided prompts or write your own. Some unusual system prompts are include to help test alignment and guard-railing. 

## OPENAI System Model
```
gpt-3.5-turbo: This model is fast and provides inexpensive responses.
gpt-3.5-turbo-16k: This model provides a large context window for long conversations.
gpt-4: This model provides the best quality responses but is slow and expensive.
```
Usage
Select a system prompt from the dropdown menu or enter your own prompt.
Choose the model you want to use from the dropdown menu.
Start the conversation by typing your message in the chat interface.
The AI model will respond based on the prompt and the conversation history.

**Note:** The current conversation history can be stored in the prompt.txt file if the save_file function is uncommented. This can be useful for debugging.
```python
save_file('prompt.txt', yaml.dump(prompt, sort_keys=False))
```

### Example Prompts
"You are a helpful AI."
"You are a mean AI. Phrase all replies as insults."
"Based on the user description and any included code write a markdown README file."
"As a professional writer please summarize the following text..."
"Speak as much as possible with as much annoying corporate jargon as you can."
"You are a helpful AI that will help the user create interesting blog posts in Markdown..."
"You are a honest and open AI. Whenever possible, always answer the question..."
### Example Models
```
gpt-3.5-turbo
gpt-3.5-turbo-16k
gpt-4   - may require an additional subscription
```
## Running the Demo
This demo also requires a openai api key. The best way to integrate into the python code with depend on the user's operating system and preferences. The various methods are set out on [opeanai's website](https://help.openai.com/en/articles/5112595-best-practices-for-api-key-safety)
To run the demo using python first install gradio and openai python modules. These modules require dependencies that are included in the requirement.txt file that may be useful for debugging but shouldn't need to be installed separately unless a dependency conflict arises. Run the the code with;
```
python StreamBot.py
``` 


The Gradio chat interface will open when then ip address is ctrl-clicked, allowing you to interact with the AI model via a web interface on your local machine.

## Alignment and guard-railing
Large Language Models (LLMs) like GPT-3 can be a powerful tool, but they also present challenges in terms of alignment and guard-railing. Here are some methods to ensure alignment and guard-railing:

1. Pre-training and Fine-tuning: Pre-training involves training the model on a large corpus of internet text, while fine-tuning is done on a narrower dataset with human reviewers following specific guidelines. This two-step process helps in aligning the model's behavior with human values.

1. Clear Guidelines for Reviewers: Providing clear and explicit guidelines to human reviewers during the fine-tuning process can help in better alignment. These guidelines can include instructions on how to handle potential biases, controversial topics, and misinformation.

1. Regular Feedback Loops: Regular interaction and feedback loops with the reviewers can help in continuously improving the model's responses over time.

1. System Improvements: Improvements can be made to the system to reduce both glaring and subtle biases in how the AI responds to different inputs.

1. User Interface Enhancements: The user interface can be designed in a way that allows users to customize the AI's behavior within broad bounds.

# Testing these methods can be done through:

1. A/B Testing: This involves comparing two versions of the model to see which one performs better.

1. User Feedback: Collecting and analyzing user feedback can provide valuable insights into the model's performance.

1. Third-party Audits: Independent audits can help in assessing the effectiveness of the alignment and guard-railing methods.

1. Internal Reviews: Regular internal reviews can help in identifying any issues or areas of improvement.

1. Remember, while these methods can help in ensuring alignment and guard-railing, they are not foolproof. There can still be instances where the model might produce outputs that are undesirable or unexpected. It's important to continuously monitor and improve the model to minimize such instances.