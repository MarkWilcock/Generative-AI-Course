# Introduction to Generative AI

## Generative AI and Large Language Models in a nutshell

Let's start with some informal definitions
* AI – a computer does something that a person would normally do
* Generative – create _new_ content.  This content can be audio, video (images and movies) or text.  We are going to focus on text.

This is a course about Generative AI. Generative AI differs from "traditional" AI.  Traditional AI labels data but does not create new data. Examples of "traditional" AI include:
* when the bank approves your credit card transaction or 
* when Amazon / YouTube / Netflix recommend a book / video / movie.

Traditional AI uses patterns in data and algorithms to estimate 
* how much / many  of a thing (regression) or 
* to decide if a thing is in a particular class e.g. is the image that of a dog, a cat, or neither (classification).  


## Large Language Models (LLMs)

A large language model is a type of Generative AI program designed to understand, generate, and interact with human language. It is trained on vast amounts of text data.  An LLM uses statistical analysis and language modelling techniques to repeatedly predict the next word in a sentence to build a response to a prompt.

It does not always choose the _most_ probable next word. This is controlled by a setting named "temperature" If the temperature becomes warmer, the LLM is less likely to choose the most probable word and the output becomes more creative. 

An LLM can answer questions, write essays, and create code. 
Here are a couple of useful terms
* *prompt*  - input to the LLM, usually a sentence or paragraph
* *completion* - the output (or response) from the LLM  

For example, here are three different completions of the next three words of a prompt "A tasty breakfast"
* could vary depending
* may include oatmeal
* includes scrambled eggs

Another example: given the prompt “She walked through”, possible continuations, with made-up probabilities, are:
1. fire (10%)
2. hell with a smile (5%)
3. the  park (3%)
4. the fair (2%)

### Some practical ideas on on how  to use LLMs
LLMs generate text from scratch, starting with a prompt. The prompt could
- _provide an instruction_: summarise, review, plan...
- _ask a question_: Who was Neil Armstrong?
- _complete a text_: Einstein was important to physics because...
- and perform lots of technical/software tasks: e.g. explain an Excel formula, write Python code.

There will be a practical exercise to use LLMs effectively.

## The shortest history of Generative AI

Generative AI seems to have arrived suddenly but in fact it has a long gestation.  Here are a few moments of AI history.
* 1956, Artificial Intelligence (AI) was born with the ambition to create intelligent machines at the [Dartmouth Workshop](https://en.wikipedia.org/wiki/Dartmouth_workshop)
* 1990s, Machine Learning (ML), _statistical_ learning from data and predictions.
* 2000s, commercial use of early single purpose Generative AI: Google Translate (2006), Siri (2011), autocomplete when texting on a phone
* 2017, deep learning, an ML technique inspired by the wiring in our brains takes off. In deep learning, "neurons" are connected into layers and the weights of the connections between neurons can be adjusted so that the neural net can "learn".
* 2021, an extension of the neural net approach using a new "transformer" architecture yields results.

Given that long history, what is the reason for the recent excitement? These LLMs have very recently become **much** more powerful and capable.  For example, in 2023, OpenAI released ChatGPT-4 which can do some very impressive things:
* score more highly on the SAT, a US-based university entrance exam, better than 90% of people,
* pass some university level exams in law, medicine,
* set out arguments in favour and against a certain thing e.g. vaping,
* play an expert role e.g. act a a Python expert and write code,
* write a job description.

Anybody can use ChatGPT and with a few hours training can use it very effectively - no coding proficiency or technical skills are required. 

Because of these factors,  ChatGPT took only 2 months to reach 100m users, compared to 9 months for TikTok and 70 months for Uber.
 
### Multi model models
Models can take in data and respond in several formats (text, audi, images, video).  Current examples:
* text to text
* text to image: such as Open AIs DALL-E, MidJourney
* image to image
* image to text
* text to audio
* audi to text e.g transcription in Microsoft Teams
* Text to Video for example, https://openai.com/sora

Some models are multi-modal.  For example ChatGPT 4 does 
* text to text 
* image to text (it can describe an image)
* text to image (DALL-E)

### Models vs Products
We interact with a LLM through a user interface (UI) or an application.  The UI talks directly to the model.  The UI may provide certain helpful capabilities.  For example, the ChatGPT web user interface and app keep note of the previous prompts and responses in a conversation and resubmit those with the latest prompt so that the LLM always has the entire conversation history.

If needed, we can talk directly with the model, typically using a Python script.  For example, what do you think this Python snippet does?

> completion = client.chat.completions.create(  
>    model="gpt-3.5-turbo",  
>    messages=[  
>      {"role": "system", "content": "You are a poet and an expert in Python."},  
>      {"role": "user", "content": "Compose a poem that explains the list, dics and tuples."} ])  

### How to we make AI do what we want to do 

One framework is the HHH framework
-	Helpful – LLM follows instructions, gives answers,
-	Honest – LLM is factual, provides accurate information, acknowledges when it is unsure
-	Harmless – do not exhibit bias or is offensive.  Does not suggest harmful or dangerous activities.  
More fine tuning is done to make the model be more HHH.

### Problems with LLMs

LLMs are not a perfect technology.  There have a few drawbacks:
* LLMs have read pretty much the entire internet – both the "good" and "bad" stuff. It is not possible to guide them to read just the “good” stuff.
* LLMs will make things up.  A famous example is Google’s Bard mistakenly stating that the James Webb telescope took the first picture of an exo-planet, which when refuted led a a $9bn drop in Google’s market value.
* Generative AI may be used by bad actors: for example, to generate untrue messages and interfere with elections.
* Jobs will be lost (and some will be won) but there will be economic disruption.

### Knowledge Check
Which of the following is true of LLMs?
1. They give exactly the same response every time?
2. They do things perfectly, you can trust results 100%!
3. They are good at initial first drafts - but treat with care and check.