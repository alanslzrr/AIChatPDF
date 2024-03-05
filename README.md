

# MultiPDF Chat App

## - **Introduction** *LLM - OpenAI - VectorDatabase* 
The **MultiPDF Chat App** is a Python application designed for interacting with multiple PDF documents through a chat interface. It enables users to ask questions in natural language, and provides answers based on the content of the PDFs. The app leverages a language model for generating accurate responses to user queries. It is important to note that the application responds solely to questions pertinent to the loaded PDF documents.

## How It Works
The application's operation is delineated in the steps below, facilitating the extraction of information and generation of responses:

![MultiPDF Chat App Diagram](./docs/PDF-LangChain.jpg)

1. **PDF Loading:** The app initiates its process by reading multiple PDF documents and extracting their textual content.
2. **Text Chunking:** The extracted text is then segmented into smaller chunks, enabling more effective processing.
3. **Language Model Processing:** A language model is employed to create vector representations (embeddings) of the text chunks.
4. **Similarity Matching:** Upon posing a question, the app conducts a comparison between the query and the text chunks to find the most semantically similar ones.
5. **Response Generation:** The relevant chunks identified are then processed by the language model, which crafts a response based on the PDFs' content.

## Dependencies and Installation
Follow these instructions to install the MultiPDF Chat App:

1. **Repository Cloning:** Clone the repository to your local machine using the appropriate Git command.
2. **Dependencies Installation:** Install the required dependencies by executing the following command in your terminal:
    ```
    pip install -r requirements.txt
    ```
3. **API Key Configuration:** Acquire an API key from OpenAI and add it to the `.env` file within the project directory:
    ```
    OPENAI_API_KEY=your_secret_api_key
    ```

## Usage
To utilize the MultiPDF Chat App, adhere to the steps outlined below:

1. Confirm the installation of the necessary dependencies and the addition of the OpenAI API key to the `.env` file.
2. Launch the application by running `app.py` through the Streamlit command-line interface with the following command:
    ```
    streamlit run app.py
    ```
3. Upon execution, the application will be accessible in your default web browser, presenting the user interface.
4. Follow the instructions provided within the app to load multiple PDF documents.
5. Utilize the chat interface to ask questions in natural language regarding the content of the loaded PDFs.
