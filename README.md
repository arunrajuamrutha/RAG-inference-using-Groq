
# LLM RAG Inference using Groq and Langchain Streaming

This project demonstrates Retrieval-Augmented Generation (RAG) for question answering using Groq, Langchain, and a pre-trained Large Language Model (LLM).

## Functionality

- Fetches documents from a list of URLs.
- Splits the documents into chunks for efficient processing.
- Generates embeddings for the document chunks using a Hugging Face model.
- Creates a vectorstore to index the embeddings for retrieval.
- Uses Groq to interact with the LLM for retrieving relevant passages from the vectorstore and generating a response based on a user query.

## Requirements

- Python 3.x
- Langchain libraries: `langchain`, `langchain_community`, `langchain_groq`
- Hugging Face Transformers
- Chroma vectorstore

## Setup

1. Install the required libraries:
   ```bash
   pip install langchain langchain-community langchain-groq transformers chroma
   ```

2. Obtain API keys for:
   - Hugging Face Transformers (`HF_TOKEN`)
   - Groq (`GROQ_API`)

## Project Structure

- `main.py`: Script containing the core logic for data loading, processing, and RAG inference.
- `requirements.txt`: File listing the required Python libraries.

## Running the Script

1. Update `HF_TOKEN` and `GROQ_API` with your respective API keys in `main.py`.
2. Modify `URLS` in `main.py` to include the desired websites for document retrieval.
3. Run the script:
   ```bash
   python main.py
   ```

## Example Usage

The script takes user queries as input and provides answers based on the retrieved passages from the indexed documents. For example:

```
Query: what is RAG?

Assistant: 
Retrieval-Augmented Generation (RAG) is a technique for improving the performance of large language models (LLMs) on question answering tasks. It combines retrieval and generation techniques to leverage the strengths of both approaches. Retrieval helps the LLM to focus on relevant passages of text that are likely to contain the answer to the user's query. Generation allows the LLM to use its knowledge and reasoning abilities to synthesize a concise and informative response.

(Source: https://medium.com/@tejpal.abhyuday/retrieval-augmented-generation-rag-from-basics-to-advanced-a2b068fd576c)
```

## Further Considerations

- This is a basic example. You can customize the prompt template, retriever configuration, and LLM parameters for specific use cases.
- Consider error handling and logging for a robust application.

## Disclaimer

This project is for educational purposes only. The pre-trained LLM might contain biases or generate inaccurate information. Use it with caution and verify the factual accuracy of the responses.

---

Feel free to adjust or expand any section based on additional details or instructions you'd like to provide!
