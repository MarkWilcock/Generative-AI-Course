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

_to do: Show tokener example_

LLMs are trained on a **massive** amount of text.
Given a series of words (tokens), an LLM predicts next word (token) based on probability.  It does not always choose the _most_ probable next word to simulate creativity. This is controlled by temperature setting, warmer=more creative. 

Once next word is added, to prompt, LLMs repeats the process
For example, here are three different completions of the next three words of a prompt "A tasty breakfast"
* could vary depending
* may include oatmeal
* includes scrambled eggs

### Some practical details of how test to use LLMs
LLMs generate text from scratch, starting with a prompt. The prompt could
- _provide an instruction_: summarise, review, plan...
- _ask a question_: Who was Neil Armstrong?
- _complete a text_: Einstein was important to physics because...
- and perform lots of technical/software tasks: e.g. explain an Excel formula, write Python code.

### Knowledge Check
Which of the following is true of LLMs?
1. They give exactly the same response every time?
2. They do things perfectly, you can trust results 100%!
3. They are good at initial first drafts - but treat with care and check.
 
