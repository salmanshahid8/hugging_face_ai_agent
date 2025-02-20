# hugging_face_ai_agent

This repo serves to take notes and to execute codes of an AI agent.

## What is an AI agent?

An Agent is a system that leverages an AI model to interact with its environment in order to achieve a user-defined objective. It combines reasoning, planning, and the execution of actions (often via external tools) to fulfill tasks. An agent has 2 main parts.

- The brain (AI model)
    - This is where all the thinking happens. The AI model handles reasoning and planning. It decides which Actions to take based on the situation.
- The body (Capabilities and Tools)
    - This part represents everything the Agent is equipped to do. The scope of possible actions depends on what the agent has been equipped with. For example, because humans lack wings, they can’t perform the “fly” Action, but they can execute Actions like “walk”, “run” ,“jump”, “grab”, and so on.

The most common AI model found in Agents is an LLM (Large Language Model), which takes Text as an input and outputs Text as well.

##  What is a Large Language Model?
An LLM is a type of AI model that excels at understanding and generating human language. They are trained on vast amounts of text data, allowing them to learn patterns, structure, and even nuance in language. These models typically consist of many millions of parameters.

Most LLMs nowadays are built on the Transformer architecture—a deep learning architecture based on the “Attention” algorithm, that has gained significant interest since the release of BERT from Google in 2018.

## Attention is all you need
A key aspect of the Transformer architecture is Attention. When predicting the next word, not every word in a sentence is equally important; words like “France” and “capital” in the sentence “The capital of France is …” carry the most meaning.

## Messages: The Underlying System of LLMs

### System Messages

System messages (also called System Prompts) define how the model should behave. They serve as persistent instructions, guiding every subsequent interaction.

For example:

```
system_message = {
    "role": "system",
    "content": "You are a professional customer service agent. Always be polite, clear, and helpful."
}
```