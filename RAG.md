## Information Retrieval - LGLSI2 - Assignment 3 - Retrieval Augmented Generation

For this assignment you will build a gpt-like chatbot that will answer your questions based on some specified documents. This is what is called a Retrieval Augmented Generation (RAG).

  

**Part I: Web-based RAG**

The assignment will be based on the following tutorial:

[https://www.youtube.com/watch?v=wd7TZ4w1mSw&list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x](https://www.youtube.com/watch?v=wd7TZ4w1mSw&list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x)

Watch the first video of the tutorial (part 1 - Overview) to get an idea about what RAG is

**Loading notebook to colab**

In the video description, there is a link to the code used in the tutorial. The code is hosted on GitHub. You will load the code to colab and use it. To do this, in colab go to file>open notebook>gitHub then enter the url to the github notebook: [https://github.com/langchain-ai/rag-from-scratch/blob/main/rag_from_scratch_1_to_4.ipynb](https://github.com/langchain-ai/rag-from-scratch/blob/main/rag_from_scratch_1_to_4.ipynb)

**Getting API keys**

To run the code you will need 2 API keys, one for langchain and one for gemini.

*1- LangChain API key*

Create an account on the following website: smith.langchain.com

Go to setting then create API key

Include the key that you generated in the colab code in the line:

    os.environ['LANGCHAIN_API_KEY']

*2- Gemini API key*

The tutorial uses an openAI interface which is not free. So we will change the code to use the free google Gemini instead. To get a Gemini key, go to the following page:

[https://ai.google.dev/tutorials/setup](https://ai.google.dev/tutorials/setup)

Click on the “Get an API key” button and create a Key on Google AI Studio.

**Adapting the code**

In this part, we will adapt the code so that it uses the gpt4all embedding and the gemini chat interface instead of the openAI interface.

You should first start by adding the following line to install gemini:

    pip install langchain-google-genai

Now replace the openai_api_key with the gemini key you created

    os.environ['GOOGLE_API_KEY'] = 'your_gemeni_key’

  

Instead of the langchain_openai embedding we will use the chat of gpt4all embeddings. To do the import use the following code

    from langchain_community.embeddings import GPT4AllEmbeddings

  

Now we will use the embedding from gpt4all, for this, use the following code under the #Embed:

    vectorstore = Chroma.from_documents(documents=splits, embedding=GPT4AllEmbeddings())

  

Instead of the langchain_openai chat we will use the chat of google. To do the import use the following code

    from langchain_google_genai import ChatGoogleGenerativeAI,

To use the gemini-pro, replace the code under #LLM with the following code

    llm = ChatGoogleGenerativeAI(model="gemini-pro", temperature=0.3)

Now try running the code and see what you get

**Part II: PDF-based RAG**

Your task now is to develop a RAG system that searches within a pdf document. To avoid slow programs, do not use a long pdf. A pdf of 2-3 pages should suffice.

**Part III: Improved RAG**

Add your special touch to the project. Use your creativity to add/improve something in the project.






