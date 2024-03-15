# How do LLMs work?

This section describes how LLMs work under the covers.  You don't need to know this to use LLMs effectively but it offer context as to their strengths and weaknesses.

 
##  How to build a LLM

 ### First step: self-supervised learning "guess the next word" 

Download a lot of text (a corpus), preferably the entire internet.  

Go through the next steps repeatedly for over the whole corpus in a process called self-supervised learning.
* Remove the last part of a sentence
* Let the LLM guess / predict the continuations - the next word(s).
* Adjust the model to match the actual continuations (the ground truth)  After a while the model gets really good
at this "guess the next word" game. 
This steps costs $100m, takes several months and generates several hundred tons of CO2.

### Next step: Re-inforcement learning with human feedback (fine-tuning)

At this point the model is pre-trained and will just continue / complete text.  Now we fine-tune the model to make it useful.  Humans provide questions and finetune the model so that it responds with something close to a model answer.  Another technique to fine tune is for the LLM to generate two different answers. People then indicate which response they prefer and this is fed back into the fine training.  

As the model grows in size, it shows  surprising “emergent behaviours”: 
* be able to crack jokes, 
* provide step-by-step instructions, 
* perform chain of thought reasoning
* act in a role
* write poetry
* solve algebraic equations
* provide strategic advice to directors of large organisations!



## How LLMs work
An LLM is based on an AI approach known as deep learning.  This uses a structure named a neutral net which looks like this.

![Neural Net Schematic](https://www.frontiersin.org/files/Articles/1290880/fphy-11-1290880-HTML/image_m/fphy-11-1290880-g001.jpg)
<br/>Source: https://www.frontiersin.org/files/Articles/1290880/fphy-11-1290880-HTML/image_m/fphy-11-1290880-g001.jpg

This contains nodes (or neurons, or simply numbers) and connections (lines, or sometimes called edges) between the nodes.  The nodes are arranged in several layers:
* the input layer – the values of these nodeas are set to the context of the words)
* Several hidden layers – these help the neural net to generalise
* the output layer – the output of the nodes in this layer makes the prediction of the next word.
A node is connected to *all* the  nodes in the previous layer by the connections. Each of these connections has a weight (a number) and it is these weights that are adjusted during the training so that the predictions and closer to the actual output values The output of the node is based on the total weights.

The node has an activation function that also determines the strength (weight) of its output based on the total of the weights of the input. (Typical ones are named RELU or Sigmoid).  This activation function helps the LLM to generalise and learn.

The neural net in the diagram is not very big – it has about 100 parameters. Most neural nets are much bigger, Chat GPT has about 1 billion parameters, about the same as a rat brain, but currently less than a human brain (100 billion parameters). Size matters.  Bigger is better.

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

*completion words*: through | the  | woods

### Tokenisation

LLMs work with numbers. Our prompt needs to be converted to number to input into teh model and the model out needs to be converted from numbers to text.  A tokenizer converts prompt to a sequence (array) at numbers. The tokenizer splits prompts into an array tokens (roughly word/word fragment).  

_to do: Show tokener example_


