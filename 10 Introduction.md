# Introduction to Generative AI

## Generative AI vs Traditional (discriminative) AI

AI (Artificial Intelligence) can be defined as when a computer does something that a person would normally do.  Generative AI creates _new_ content.  This content can be audio, video (images and movies) or text.  We are going to focus on text.

This is a course about Generative AI. Generative AI differs from "traditional" AI.  Traditional AI labels data but does not create new data. 

Traditional AI uses patterns in data and algorithms to estimate 
* how much / many  of a thing (_regression_) 
* to decide if a thing is in a particular class e.g. is the image that of a dog, a cat, or neither (_classification_)
* grouping items with similar attributes into sets (_clustering_)  

Examples of "traditional" AI in daily life  include:
* when the bank approves your credit card transaction or 
* when Amazon / YouTube / Netflix recommend a book / video / movie.
* facial reconition at passport e-gates
* choice of adverts presented to us on search engines and sites like YouTube

Examples of Generative AI in daily life include:
* customer service chatbots
* Amazon's Alexa, Apple's Siri

## Examples of how AI tools can make us more productive at work
AI tools can help us with the following types of task:
* provide step by steo instructions to complete a task 
* ask a question e.g. Who was Neil Armstrong?
* plan a task: plan activities for a day out in ...
* brainstorm ideas: suggest a name of a pub quiz team 
* review and suggest improvements an some text or a document 
* and perform lots of technical/software tasks: e.g. explain an Excel formula, write SQL or Python code.

## Multi modal models
Models can take in data and respond in several formats (text, audi, images, video).  Current examples include:
* text to image: such as Open AIs DALL-E, MidJourney
* audio to text e.g transcription in Microsoft Teams
* text to video for example, https://openai.com/sora  or Google's Veo

More and more AIs are becoming multi-modal.  For example, ChatGPT 4o transforms text to text, image to text (it can describe an image), text to image, and text to video.   OpenAI demos GPT 4o as able to understand facial expressions and respond with a voice  expressing emotion.

## Problems with AI Tools

AI tools and large language models (LLMs) are not a perfect technology.  There have a few drawbacks:
* LLMs have read pretty much the entire internet – both the "good" and "bad" stuff. It is not possible to guide them to read just the “good” stuff.
* LLMs will make things up.  A famous example is Google’s Bard mistakenly stating that the James Webb telescope took the first picture of an exo-planet, which when refuted led a a $9bn drop in Google’s market value.
* Generative AI may be used by bad actors: for example, to generate untrue messages and interfere with elections.
* Jobs will be lost (and some will be won) but there will be economic disruption.

## How to we make AI do what we want to do 

One framework is the HHH framework
-	Helpful – LLM follows instructions, gives answers,
-	Honest – LLM is factual, provides accurate information, acknowledges when it is unsure
-	Harmless – do not exhibit bias or is offensive.  Does not suggest harmful or dangerous activities.  

## Models vs Products
We interact with a LLM through a user interface (UI) or an application.  The UI talks directly to the model.  The UI may provide certain helpful capabilities.  For example, the ChatGPT web user interface keeps note of the previous prompts and responses in a conversation and resubmits those with the latest prompt so that the LLM always has the entire conversation history.

If needed, we can talk directly with the model, typically using a Python script.  For example, what do you think this Python snippet does?

> completion = client.chat.completions.create(  
>    model="gpt-3.5-turbo",  
>    messages=[  
>      {"role": "system", "content": "You are a poet and an expert in Python."},  
>      {"role": "user", "content": "Compose a poem that explains the list, dics and tuples."} ])  

## Knowledge Check
Which of the following is true of LLMs?
1. They give exactly the same response every time?
2. They do things perfectly, you can trust results 100%!
3. They are good at initial first drafts - but treat with care and check.