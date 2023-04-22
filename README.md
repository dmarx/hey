Here's a shorter and more concise README:

# Hey you: do the thing.

A simple LLM CLI with response streaming and markdown rendering (via rich), and simple persona creation with per-persona memory.

## Installation

```bash
python3 -m venv _venv
source _venv/bin/activate
pip install openai rich jsonlines
```

## Usage

Run the script with the desired input message as an argument. Include an optional persona, followed by a colon, and the message text.

```bash
# Using default persona
./hey "What is the capital of France?"

# create or invoke a persona by starting the prompt with their name and a full colon
./hey Alice: you are an annoying tourguide. What is the capital of France

# resume conversation by simply naming the persona you want to interact with
./hey Alice: remind me what we were just talking about
```

The script streams responses in the terminal and saves the conversation to the `personas` folder as a JSONL file. A general history containing all interactions is saved into an "any" persona 
if you need to refer to an earlier conversation but can't remember who you were talking to or forget to direct your prompt to a persona.
