# Chat with a Website from URL - LangChain Chatbot with Streamlit GUI

#### **Introduction** 
This project documents my experience building a chatbot using LangChain and Streamlit. The chatbot interacts with websites, extracts information, and communicates effectively through a user-friendly interface.

#### **Key Features**
**Website Interaction:** Utilizes LangChain to extract real-time data from websites, ensuring responses are relevant and contextually accurate.

**Large Language Model Integration:** Compatible with models like GPT-4, Mistral, Llama2, and Ollama. GPT-4 is used by default, but the system can easily switch to other models.

**Streamlit GUI:** Provides a clean, intuitive interface designed for users with varying technical expertise, enabling real-time query input and response generation.

**Python-Based Implementation:** Entirely coded in Python, leveraging its extensive libraries for natural language processing, web interaction, and development.

## Retrieval-Augmented Generation (RAG) Overview
RAG enhances language models by integrating external knowledge into their responses. Here's how it works:

- **Vectorization:** Converts text sources into vector representations (embeddings) that capture semantic meaning.

- **Retrieval:** User queries are vectorized and compared against the knowledge base to find the most relevant texts.

- **Augmentation:** The retrieved texts are included as additional context in the prompt.

- **Generation:**The language model generates a response using the augmented information, resulting in more accurate and context-rich answers.

### **How It Works in This Project**
![](doc/HTML-rag-diagram.jpg)

1. **Web Scraping:** Scrape and extract text from the target website using BeautifulSoup.
2. **Text Splitting:** Divide the extracted text into smaller chunks for manageable processing.
3. **Vectorization:** Convert text chunks into vector representations (embeddings).
4. **Storage in Chroma:** Store the vectorized text chunks in Chroma, the vector database.
5. **Semantic Search:** Embed user queries into vectors and compare them against the stored vectors in Chroma to find the most relevant text chunks.
6. **Augmentation:** Retrieve and use the most relevant text chunks to augment the query.
7. **Response Generation:** Pass the augmented query to the LLM, which generates a contextually enriched response.