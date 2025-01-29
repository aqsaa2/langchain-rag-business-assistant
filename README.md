# Langchain RAG-based Business Assistant with CSV Output

This project implements a Streamlit application that utilizes Langchain and Retrieval-Augmented Generation (RAG) to create a business assistant. The application allows users to:

*   Upload documents and URLs to provide context for the assistant.
*   Interact with the assistant through a chat interface.
*   Generate personas, user stories, and Gherkin scenarios based on the provided information.
*   Download the generated artifacts as a CSV file.

## Technologies Used

*   Streamlit: A Python library for building web apps.
*   Langchain: A library for building AI pipelines that combine retrieval and generative techniques.
*   Chat Google Generative AI: A Google AI API for generating text.
*   Chroma: A vector database for storing and retrieving document embeddings.

## Running the Application

1.  Clone this repository.
2.  Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3.  Set your Google API Key as an environment variable:

    ```bash
    export GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
    ```

4.  Run the application:

    ```bash
    streamlit run app.py
    ```

## How it Works

The application follows these steps:

1.  Users can upload documents (PDF, TXT, DOCX, MD) or provide URLs to add relevant information to the knowledge base.
2.  The application interacts with the user through a chat interface. User responses are stored in a Chroma vector database.
3.  When the user provides enough input (determined by a threshold), the application leverages Langchain and the Chat Google Generative AI API to:
    *   Generate personas based on the stored data and user responses.
    *   Generate user stories for each persona.
    *   Generate Gherkin scenarios for each user story.
4.  Users can download the generated artifacts as a CSV file.


Test the app on this link: https://langchain-rag-business-assistant-y8cnnhb2zfcvmjpw6nkxoc.streamlit.app/
