# RAG LLM Assistant for E-Commerce data using Snowflake Cortex  

## Overview  
This project uses a **Retrieval Augmented Generation (RAG)** framework to create an AI-powered chat assistant tailored for a health drink e-commerce use case. The assistant is built using **Streamlit** and **Snowflake Cortex Search** to provide intelligent responses grounded in product manuals, e-commerce data, and sales/operations metrics.  

## Workflow  
1. **Document Organization & Pre-Processing**  
   - Organize and preprocess user manuals and metric documents.  
   - Use Cortex LLM serverless capabilities to label documents with metadata for filtered searches.  

2. **Cortex Search Service**  
   - Utilize Cortex Search for automatic embeddings and efficient document retrieval.  

3. **Chat UI Development**  
   - Build a Streamlit chat interface with retrieval and generation logic.  
   - UI with retrieved document chucks alongside LLM-generated responses.  
   - Implement conversation history summarization for better context handling.  

---

## Folder Structure  

### `app/`  
- Contains Python code for the Streamlit app:  
  - **`rag_llm_assistant_with_history.py`**: Chat assistant with conversation history.  
  - **`rag_llm_assistant_basic.py`**: Basic chat assistant without conversation history.  

### `sql/`  
- Contains SQL scripts for setting up e-commerce tables and queries:  
  - **`ecommerce_data_setup.sql`**: Queries for creating databases, schemas, temporary tables and Cortex Search Service.

### `assets/`  
- Stores data and reference materials:  
  - **`documents/`**: Product instruction manuals, sales reports, and metrics documents in PDF format.  
  - **`screenshots/`** : This folder contains screenshots of the application, showcasing its UI, features, and a comparison of outcomes when using the provided documents data with the LLM versus without it.

---
## Features  
- **RAG Framework:** Reduces hallucinations by grounding responses in relevant documents.  
- **Document Traceability:** Displays retrieved document chunks used to generate answers.  
- **Enhanced Context:** Includes a chat UI with conversation history and sliding window summarization for contextual responses.  
- **Product Expertise:** Answers queries related to health drink products, sales, and operations metrics.  
- **Instructional Support:** Provides detailed instructions for using health drink mix machines and mix proportions.  

---

## Additional Notes  

- **Conversation History:** The app includes a sliding window approach to manage past interactions and summarize conversations effectively.  
- **Secure Sharing:** Streamlit in Snowflake ensures secure data handling and sharing within role-based access policies.  
- **Deploying the App:** Find out more here - [**"Build a Retrieval Augmented Generation (RAG) based LLM assistant using Streamlit and Snowflake Cortex Search Quickstart Guide"**](https://quickstarts.snowflake.com/guide/ask_questions_to_your_own_documents_with_snowflake_cortex_search/index.html).
-  The application categorizes documents using two tags: `instructions` and `metrics`. These tags help organize and retrieve the right type of content effectively during responses.
- For the underlying language model (LLM), different models were tested to evaluate cost and performance. In this specific case, **Llama3-70B** was selected for its superior results (concise) and cost efficiency.
---

## Data Disclaimer  

The data in instruction manuals and metrics documents are **AI-generated (ChatGPT)** and used for **demo purposes only**.   
