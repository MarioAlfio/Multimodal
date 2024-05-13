# RAG

RAG is an acronym for Retrieval Augmented Generation and in the RAG technique we divide our data into small segments, allowing the LLM to use them, within the limits of its context window.
So with the RAG technique, we will divide our data, into small segments. Then it will convert the small segments into numbers.
And finally it will load these numbers into a vector database.
That these numbers are called embeddings.
Embeddings are the result to convert small segments of text into numbers.
Embeddings are more than numbers, they are vectors of numbers.



## Multimodal RAG explained

1. ```bash
    pip install langchain openai
   ```
2. ```bash
    pip install pydantic lxml chromadb tiktoken
   ```
3. ```bash
    pip install "unstructured[all-docs]"
   ```
     
* Summarize text with the LLM model.
* Summarize table with the LLM model.
* Summarize images with the new Multimodal LLM model (GPT4V).
* Convert summaries into numbers (embeddings) and store the embeddings in a multivector retriever (vector database).
* Store the raw documents (the text and the summary of the images) in a DocumentStore.
* When a question is asked, do similarity search to retrieve the most relevant docs and send the response to the LLM Model to format it properly using natural language.
* The unstructured module is the key here. We will use it to extract all the relevant parts of the document (text, tables and images).
* Chromadb will be our vector store.
