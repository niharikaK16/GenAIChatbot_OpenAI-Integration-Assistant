# GenAIChatbot_OpenAI-Integration-Assistant
The GenAI-OpenAI Chatbot is an innovative solution that leverages the power of general artificial intelligence (GenAI) and the OpenAI API to create a personalized and intelligent conversational assistant. This chatbot enables users to interact with a sophisticated AI model capable of answering a wide range of questions based on uploaded documents.
# Chatbot Project

This project utilizes the OpenAI API to create a personalized chatbot. Let's break down what's happening in the code:

## Python Libraries Used

- **Streamlit**: Streamlit is a Python library used for building interactive web applications for data science and machine learning. It's employed here to create a user-friendly interface for interacting with the chatbot.

- **PyPDF2**: PyPDF2 is a Python library for working with PDF files. It's used to extract text from uploaded PDF documents.

- **Langchain**: Langchain is a library for natural language processing tasks, including text splitting, embeddings, vector stores, and question answering.

- **FAISS**: FAISS is a library for efficient similarity search and clustering of dense vectors. Here, it's utilized to create a vector store for the text chunks extracted from the PDF document.

## OpenAI API Integration

The OpenAI API is integrated into the chatbot in the following steps:

1. **Initialization**: The API key for OpenAI is provided at the beginning of the script (`OPENAI_API_KEY = "sk-PHzh89333124kjfd38493jjfdk84035i5Z"`).

2. **User Interaction**: Users upload a PDF document through the Streamlit interface and input their questions into a text input field.

3. **PDF Text Extraction**: PyPDF2 is used to extract text from the uploaded PDF document.

4. **Text Splitting**: The extracted text is split into smaller chunks using Langchain's `RecursiveCharacterTextSplitter`. This step is necessary to process large documents efficiently.

5. **Embeddings Generation**: Langchain's `OpenAIEmbeddings` class is used to generate embeddings for the text chunks. These embeddings are representations of the textual content that capture semantic information.

6. **Vector Store Creation**: FAISS is employed to create a vector store from the generated embeddings. This vector store enables efficient similarity search based on the user's input question.

7. **Question Answering**: When the user inputs a question, the chatbot performs a similarity search using the vector store to find relevant chunks of text. The relevant chunks are then passed to the OpenAI language model (LLM) via Langchain's `ChatOpenAI` class.

8. **Response Generation**: The OpenAI language model generates a response based on the input question and the relevant text chunks. This response is displayed to the user through the Streamlit interface.

## Usage

1. Upload a PDF document.
2. Type your question in the provided input box.
3. Get answers based on the content of the uploaded document.

## Installation

1. Install required Python libraries:


2. Run the application:

