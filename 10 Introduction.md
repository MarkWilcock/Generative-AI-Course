# Introduction to Generative AI

Generative AI seems to have arrived suddenly but in fact it has a long gestation.  Here are a few moments of history.

* 1956, Artificial Intelligence (AI), ambition to create intelligent machines at the [Dartmouth Workshop](https://en.wikipedia.org/wiki/Dartmouth_workshop)
* 1997, Machine Learning (ML), _statistical_ learning from **data and predictions.**
* 2017, Deep Learning, a ML technique inspired by the wiring in our brains.  "Neurons" are connected into layers and the weights of the connections between neurons can be adjusted so that the neural net (NN) can "learn".
* 2021, Generative AI, create new content, which could be text, audio or video, given a prompt.  An extension of NNs using the transformer architecture.

## Large Language Models (LLMs)

A large language model is a type of AI program designed to understand, generate, and interact with human language. It's trained on vast amounts of text data.  It repatedly predicts the next word in a sentence to build a response to a prompt.  It can answer questions, write essays, and create code. 
Here are a couple of useful terms
* *prompt*  - input to the LLM, usuual a sentecnce or paragraph
* *completion* - the output (or response) from the LLM  

A large language model is a type of AI program designed to understand, generate, and interact with human language. It's trained on vast amounts of text data.  It repatedly predicts the next word in a sentence to build a response to a prompt.  It can answer questions, write essays, and create code. 
Here are a couple of useful terms
* *prompt*  - input to the LLM, usuual a sentecnce or paragraph
* *completion* - the output (or response) from the LLM  

LLMs work with numbers. Tokenizer converts prompt to a sequence (array) at numbers. Tokenizer splits prompt into an array tokens (roughly word/word fragment).
Show tokener example
LLMs are trained on a **massive** amount of text.
Given a series of words (tokens), LLM predicts next word (token).
Uses probability to do this.
Does not always choose the most probable next word (to simulate creativity). This is controlled by temperature setting, warmer=more creative. 
Once next word is added, to prompt, LLMs repeats
"A tasty breakfast"
could|vary|depending
may|include|oatmeal...
include|scrambled|eggs|...

### **Some practical details of how test to use LLMs**
LLMs generate text from scratch, starting with a prompt. 
- **Instruction**: summarise, review, plan...
- **Ask a question**: Who was Neil Armstrong?
- **Complete a text**: "Einstein was important to physics because..."
- and lots of technical/software tasks: e.g. write Excel formulas, build PBI dashboard, write Python code.

**Knowledge check**
Which of the following is true?
1. They give exactly same response every time
2. They do think perfectly, you can trust results 100%
3. they are good at initial first drafts - but treat with care and check
 
