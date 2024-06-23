# Exercise - Advanced Tasks

In this exercise, we will split the class into four teams.  Each team focusses an a different type of advanced task.  Each team will look how how AI can do more advanced tasks than in the previous starter exercise. 

## Thinkers
As AI tools have become more powerful, they have shown emergent abilites: 
* the ability to crack jokes, 
* provide step-by-step instructions, 
* perform chain of thought reasoning,
* act in a role,
* write poetry,
* solve algebraic equations and
* provide strategic advice to directors of large organisations!

### Tasks
Here is a picture (of a ball connected by string to the ceiling).  What happens if we cut the string?

If 3x + 4 = 19, what is x?  Explain your reasoning.

Write a poem, in rhyming couplets, about the stresses and strains - and highlights - of working in the NHS.

Act as a morose, unhappy, pessimistic,and sarcastic football expert _(other sports are available and can be substituted here)_ and answer the following questions I will give you...

Explain ... to me as if I am a | 10 year old child | 10 year old child | professor of...

## Imagers
AI tools can understand and interpret images.

### Tasks
* Download [this image](./Resources/NHS_Staff_Nurses_Doctors_Group.webp) to your computer. The image comes from [this page](https://www.nhsemployers.org/news/latest-nhs-workforce-and-vacancy-statistics) on the NHS Employers website.  Upload to the AI tool and then prompt the AI to describe the attached image.

* Download [this image](./Resources/NHS%20ART.jpg.webp) to your computer. The image comes from [this page](https://ifs.org.uk/articles/state-nhs) on the Institute for Fiscal Studies (IFS) website.  This is a more complex image: more people, police and healthcase workers, engaged in an protest / demonstration activity and a city background. Upload to the AI tool and then prompt the AI to describe the attached image.  See if the AI reads the messages on the banners.  If not, prompt it to do so.


## Customisers

Customisers adapt the AI tool so it provides more relevant responses based on the organisation's needs.

### Tasks
Customise the AI in some way. Here are some suggestions. Some or all if these options may or may not be available to you depending on the particular AI tool and your subscription.

Use prompt engineering, for example following the RICE framework.

Configure the AI tool.  For example, you can customise ChatGPT to tell it something about yourself (location, interests, goals,..) and how it should respond (formal or casual, brief or verbose, neutral or opinionated,...)

Look at examples of customised AIs.  For example, ChatGPT offers several including:
* an educator (Khanmigo)
* a Python helper
Then create your own custom custom AI.  

Create an assistant with a low code approach.  Here is an example using OpenAI.
1. Go to the [Open AI Playground](https://platform.openai.com/playground/) 
1. Create an assistant
1. Configure  the assistant 
    * name it
    * provide instructions into the text box
    * choose a model
    * (important), add documents e.g. PDF filess containing the information or data that you want the assistant to search when providing responses,
    * Test out your assistant
    * Publish your assistant.

Use Azure Copilot Stdio (low code approach)

Use Azure AI studio (high code, Pythonic approach)

## Retrievers
Organisations would like the AI tool to provide responses based on their own internal documents or data rather than on general information culled from external sources.

In the starter tasks, we provided some smallish documents to the AI tools and asked it to summarise these.  This task extends that to much larger documents.  Often a techinque known as Retrieval Augmented Generation (RAG) is used.

### Tasks
[This PDF](./Resources/WITN01020100.pdf) contains a long legal document - the witness statement of the CEO of the Post Office to the Horizon IT Inquiry.  It is 861 pages long with over 1,880 sections.  Download this file to your PC, then upload to the AI with a prompt like this.  
_Please summarise the information in this PDF into 10 paragraphs.  Give a title to each paragraph._

This prompt asks the AI to search several related webpages, a pages specified in the URL and the linked web pages.  
_Read this page https://www.nhs.uk/better-health/ and the pages that it links to, and summarise NHS advice for better health in 5 short paragraphs._

This page https://digital-transformation.hee.nhs.uk/building-a-digital-workforce/phillips-ives-review and the pages that it links to, explain The Phillips Ives Nursing and Midwifery Review. Summarise the content of these pages in 5 short paragraphs.

Download a document from a public web page and then prompt the AI to summarise and review the document.  Example prompts are:
* Please summarise in fewer than 300 words
* How could this article be improved to make more clear and compelling?
* The article discusses ... (e.g. rise of vaping in the UK and suggests it is a good thing).  Provide three arguments to support this conclusion and three argument against it.


