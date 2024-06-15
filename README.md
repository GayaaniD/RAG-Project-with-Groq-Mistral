# RAG-Project-with-Groq-Mistral
![image](https://github.com/GayaaniD/RAG-Project-with-Groq-Mistral/assets/125920863/ad43bdeb-be1e-45e6-9279-ed420e05b90c)
This project is about leveraging Groq, a powerful open-source inference engine, to create a Retrieval-Augmented Generation (RAG) based Q&A system. Utilise open-source Large Language Models (LLMs) to process and answer user queries.

**Why Groq? Exceptional Performance for LLMs** 🤔

Groq is the AI infrastructure company pioneering the world’s fastest AI inference technology. Their LPU™ (Language Processing Unit™) inference engine is a hardware and software platform designed for exceptional compute speed, quality, and energy efficiency. Here’s what sets Groq apart:

  - Unmatched Speed for LLMs: The LPU tackles the two key LLM bottlenecks: compute density and memory bandwidth. It boasts superior compute capacity compared to GPUs and CPUs when handling LLMs. This translates to faster processing of individual words, leading to significantly quicker generation of text sequences.
  - Eliminating Memory Bottlenecks: Traditional GPUs rely on external memory, creating a bottleneck for LLMs. The LPU eliminates this issue, enabling orders of magnitude better performance compared to GPUs.
    
**What is the LPU™ Inference Engine?** 🤔

The LPU™ inference engine is a hardware and software platform designed specifically for language processing tasks. Unlike GPUs, which excel at parallel computations, the LPU priorities sequential processing, making it ideal for tasks like LLM inference where sequence generation is paramount.

**Available LLM Models in Groq Engine** 👉
  - Gemma-7b-It: A large LLM with 7 billion parameters, trained on a massive dataset of text and code.
  - Llama3–70b-8192: A factual LLM with 70 billion parameters, focused on providing informative and comprehensive answers.
  - Llama3–8b-8192: A smaller version of Llama3 with 8 billion parameters, offering a balance between performance and resource efficiency.
  - Mixtral-8x7b-32768: An LLM specifically designed for question answering tasks, with 8.7 billion parameters. (This is the model used in the code example)

## Project Flow
1. **Data Loading and Pre-processing :**

This section focuses on loading documents from a website using WebBaseLoader. Then, it splits the documents into smaller chunks for processing and creates vector embedding to efficiently compare documents based on their meaning.

2. **LLM Integration and Prompt Design :**

  - Create an LLM instance using the ChatGroq class and Groq API key. The specified model name (“mixtral-8x7b-32768”) is one of the options available in the Groq engine.
  
  - Define a prompt using the ChatPromptTemplate class. This prompt instructs the LLM to consider the provided context (documents) and answer the user’s question based on that information.
  
  - Create two essential chains:

      1. document_chain: This chain prepares the documents and the prompt for the LLM.
      2. retrieval_chain: This chain combines the document retrieval step (using the vector embedding)

## How to Run the Project
1. Clone the GitHub repository.
2. Rename the `.env.example` file to `.env` and add your API keys.
3. Install the project dependencies by running the `requirements.txt` file. You can do this by opening your terminal and typing:
    ```
    pip install -r requirements.txt
    ```
4. After the dependencies are installed, you can run the project using :
   ```
   streamlit run app.py
   ```
   
## Outcome
![image](https://github.com/GayaaniD/RAG-Project-with-Groq-Mistral/assets/125920863/2cb9c8f4-e707-4b77-93c0-a96b009eeac1)

## Response time : 0.09375, here response time is less due to Groq engine.
