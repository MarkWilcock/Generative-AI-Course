# How does Generative AI work?

This section describes how generative AI work under the covers.  You don't need to know this to use LLMs effectively but it helps to understand the reasons for their strengths and weaknesses.  Most of the AI tools we use in this course are based on large language model (LLM).

##  How to build a LLM

 ### First step: self-supervised learning "guess the next word" 

Download a lot of text (a corpus), preferably the entire internet.  

Go through the next steps repeatedly for over the whole corpus in a process called self-supervised learning.  This will cost $100m, takes several months and generate several hundred tons of CO<sub>2</sub>.
* Remove the last part of a sentence.
* Let the LLM guess / predict the continuations - the next word(s).
* Adjust the model to match the actual continuations (the ground truth).  After a while the model gets really good at this "guess the next word" game. 

### Next step: Re-inforcement learning with human feedback (fine-tuning)

At this point the model is pre-trained and will just continue / complete text.  Now we fine-tune the model to make it useful.  Humans provide questions and finetune the model so that it responds with something close to a model answer.  Another technique to fine tune is for the LLM to generate two different answers. People then indicate which response they prefer and this is fed back into the fine training.  

As the model grows in size, it shows  surprising “emergent behaviours”: 
* be able to crack jokes, 
* provide step-by-step instructions, 
* perform chain of thought reasoning,
* act in a role,
* write poetry,
* solve algebraic equations and
* provide strategic advice to directors of large organisations!

## How LLMs work
An LLM is based on an AI approach known as deep learning.  This uses a structure named a neutral net which looks like this.

![Neural Net Schematic](https://www.frontiersin.org/files/Articles/1290880/fphy-11-1290880-HTML/image_m/fphy-11-1290880-g001.jpg)
<br/>Source: https://www.frontiersin.org/files/Articles/1290880/fphy-11-1290880-HTML/image_m/fphy-11-1290880-g001.jpg

This contains nodes (or neurons, or simply numbers) and connections (lines, or sometimes called edges) between the nodes.  The nodes are arranged in several layers:
* the input layer – the values of these nodes are set to the words at  the start of the sentence
* several hidden layers – these help the neural net to generalise
* the output layer – the output of the nodes in this layer makes the prediction of the next word.

A node is connected to *all* the  nodes in the previous layer by the connections. Each of these connections has a weight (a number) and it is these weights that are adjusted during the training so that the predictions and closer to the actual output values. 

The node has an activation function that also determines the strength (weight) of its output based on the total of the weights of the input. (Typical ones are named RELU or Sigmoid).  This activation function helps the LLM to generalise and learn.

The neural net in the diagram is tiny – it has about 30 parameters. Most neural nets are much bigger, Chat GPT has about 1 billion parameters, about the same as a rat brain, but currently less than a human brain (100 billion parameters). Size matters.  Bigger is better.

GPT stands for 
* Generative 
* Pre-Trained 
* Transformer.

A transformer architecture looks like below (read top to bottom_)

*prompt words:* she | walked | through

< Token Embedding: convert words and their position in the sentence to numbers >

[ Self Attention Neural Net - determines the most important words in the prompt history to pay attention to ]

[ Feed Forward Neural Net - guesses the next word]

< Token Embedding: convert numbers into words >

*completion words*:  the  | woods

### Tokenisation

LLMs work with numbers. Our prompt needs to be converted from text to numbers to be input into the model and the model output needs to be converted from numbers to text.  A tokenizer converts text to a sequence (array) at numbers. The tokenizer splits text into an array tokens (roughly word/word fragment).  

This page from OpenAI shows what a tokenizer does. https://platform.openai.com/tokenizer


