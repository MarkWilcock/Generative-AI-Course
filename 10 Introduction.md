# Introduction to Generative AI

## Some definitions
Let's start with some informal definitions
* AI – a computer does something that a person would normally do
* Generative – it creates _new_ content
This content can be audio, video (images and movies) and text.  We are going to focus on text.

Generative AI differs from "traditional" AI.  Traditional AI happens when the bank approves a credit card transaction or Amazon / YouTube / Netfix reccomend a book / video / movie.  It uses patterns in data and algorithms to estimate how much / many  of a thing (regression) or is a thing of a particular class e.g. is the image that of a dog, a cat, or neither (classification).  Traditional AI labels data but does not create new data. 

## The shortest history of Generative AI

Generative AI seems to have arrived suddenly but in fact it has a long gestation.  Here are a few moments of history.
* 1956, Artificial Intelligence (AI), ambition to create intelligent machines at the [Dartmouth Workshop](https://en.wikipedia.org/wiki/Dartmouth_workshop)
* 1997, Machine Learning (ML), _statistical_ learning from **data and predictions.**
* 2000s, commercial use of early single purpose Genertive AI Google Translate (2006),  Siri (2011), autocompleter when texting on a phone
* 2017, Deep Learning, a ML technique inspired by the wiring in our brains.  "Neurons" are connected into layers and the weights of the connections between neurons can be adjusted so that the neural net (NN) can "learn".
* 2021, Generative AI, create new content, which could be text, audio or video, given a prompt.  An extension of NNs using the transformer architecture.

Given that long history, what is the reason for the recent excitement? These LLMs have become more powerful.  In 2023, OpenAI released ChatGPT-4 which can do some very impressive things:
•	Score more highly on the SAT, a US-based university entrance exam, better than 90% of people
•	Pass some university level exams in Law, medicinine,
•	Do useful things that a person may need: examples:
•	Set out arguments in favour and against a certain thing e.g. vaping
•	Play an expert role e.g. act a a Python expert and write code to…
•	Write a job description
Anybody can use ChatGPT and with a few hours training can use it very effectively - no coding proficiency or technical skills are required. 
Because of these two factors,  ChatGPT took only 2 months to reach 100m users (compared to TikTok with 9 months and Uber wth 70 months)


## Large Language Models (LLMs)

A large language model is a type of Generative AI program designed to understand, generate, and interact with human language. It's trained on vast amounts of text data.  It repeatedly predicts the next word in a sentence to build a response to a prompt.  It can answer questions, write essays, and create code. 
Here are a couple of useful terms
* *prompt*  - input to the LLM, usuual a sentecnce or paragraph
* *completion* - the output (or response) from the LLM  

A large language model is trained on vast amounts of text data.  It repeatedly predicts the next word in a sentence to build a response to a prompt.  It can answer questions, write essays, and create code. 
Here are a couple of useful terms
* *prompt*  - input to the LLM, usuual a sentecnce or paragraph
* *completion* - the output (or response) from the LLM  

LLMs work with numbers. Our prompt needs to be converted to number to input into teh model and the model out needs to be converted from numbers to text.  A tokenizer converts prompt to a sequence (array) at numbers. The tokenizer splits prompts into an array tokens (roughly word/word fragment).  

_to do: Show tokener example_

LLMs work by language modelling.  They are trained on a **massive** amount of text.
Given a series of words (tokens), an LLM predicts next word (token) based on probability.  It does this by statistical analysis of a lot of text.  It does not always choose the _most_ probable next word to simulate creativity. This is controlled by temperature setting, warmer=more creative. 


For example, here are three different completions of the next three words of a prompt "A tasty breakfast"
* could vary depending
* may include oatmeal
* includes scrambled eggs

Another example: given the prompt “She walked through”
Possible continuations, with made-up probabilities,  are
1. fire (10%)
2. hell with a smile (5%)
3. the (4%)
*  --- the  park (3%)
*  --- the fair (2%)

### Some practical details of how test to use LLMs
LLMs generate text from scratch, starting with a prompt. The prompt could
- _provide an instruction_: summarise, review, plan...
- _ask a question_: Who was Neil Armstrong?
- _complete a text_: Einstein was important to physics because...
- and perform lots of technical/software tasks: e.g. explain an Excel formula, write Python code.
There will be a practical exercise to use LLMs effectively.


### Knowledge Check
Which of the following is true of LLMs?
1. They give exactly the same response every time?
2. They do things perfectly, you can trust results 100%!
3. They are good at initial first drafts - but treat with care and check.
 

 
###  How to build a LLM
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


### Multi model models
Models can take in data and respond in several formats (text, audi, images, video).  Current examples:
* text to text
* text to image: such as Open AIs DALL-E, MidJourney
* image to image
* image to text
* text to audio
* audi to text e.g transcription in Microsoft Teams
* Text to Video for example, https://openai.com/sora
Some models are multi modal.  For example ChatGPT4 does text to text and image to text (it can describe an image)

### Models vs Products
We interact with a LLM through a user interface or an application.  The UI talks directly to the model.  The UI may provide certain helpful capabilities.  For example, the ChatGPT web User interface and app keep note of the previous prompts and responses in a conversation and submits those with the latest prompt so that the LLM always has the entire conversation history.

If needed, we can talk directly with the model, typically using a Python script.

For example, what do you think this Python snippet does?
> completion = client.chat.completions.create(  
>    model="gpt-3.5-turbo",  
>    messages=[  
>      {"role": "system", "content": "You are a poet and an expert in Python."},  
>      {"role": "user", "content": "Compose a poem that explains the list, dics and tuples."}  
>    ]  
> )  


### How to we make AI do what we want to do 

One framework is the HHH framework
-	Helpful – LLM follows instructions, gives answers,
-	Honest – LLM is factual, provides accurate information, acknowledges when it is unsure
-	Harmless – do not exhibit bias or is offensive.  Does not suggest harmful or dangerous activities
More fine tuning is done to make the model be more HHH.


### Problems with LLMs

LLMs are not a perfect technology.  There have a few drawbacks:
* LLMs have ready pretty much the entire internet – both the "good" and "bad" stuff. It’s not possible to guid them to read just the “good” stuff.
* LLMs will make things up.  A famous example is Google’s Bard mistakenly stating that the James Webb telescope took the first picture of an exo-planet, which when refuted led a a $9bn drop in Google’s share price.
* Generative AI may be used by bad actors to generate untrue messages, articles, to do bad things e.g. interfere with elections
* Jobs will be lost (and some will be won) but there will be economic disruption



## How do LLMs work?
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




