# Gemini Quizzify

## Mission
Create a quiz generator using Google Gemini, Langchain, Chroma, and Streamlit to explore LLMs and vector embeddings. 

## Requirements:

- Python version 3.11 or above
- [Streamlit Documentation](https://docs.streamlit.io/)
- Google Cloud account
- [Vertexai Documentation](https://cloud.google.com/vertex-ai)


## Usage

To run the Quiz Builder:

1. Install the necessary dependencies listed in `requirements.txt`.
2. Run the Streamlit application by executing `streamlit run xxx.py` in the terminal where xxx is the name of the py file you want to run.
3. Follow the instructions provided in the user interface to interact with the Quiz Builder.


## Tasks

## Task 1: 🔑 Google Cloud, Vertex AI, & SDK Authentication

- Go to the [Google Cloud Platform](console.cloud.google.com) and select "Get Started for free".
- Sign in using your Google Account and complete the billing requirements.
- Create a new project.
- Navigation -> Artificial Intelligence -> Vertex AI -> Enable All Recommended APIs


## Task 2: 💻 Dev Environment Setup

- Install the Google SDK using this [link](https://cloud.google.com/sdk/docs/install).
- Run the following command to initialize the SDK:
  ```
  gcloud init
- Sign in using your Google Account credentials.
- Select an existing project or Create a new project
- Add your Gemini authentication.json to the gitignore file


## Task 3: 📥 Document Ingestion

- Install the streamlit framework
  ```
  pip install streamlit
- Create a file uploader using ```st.file_uploader()``` that only accepts PDF's
- Process the file using a [PyPDFLoader](https://python.langchain.com/docs/modules/data_connection/document_loaders/pdf#using-pypdf)
  ![quizzifytask3](https://github.com/hari660/geminiQuizzify/assets/55326522/e1366955-19f7-4fa4-85f7-b10020ec6e4d)



## Task 4: 🔗 Embedding with VertexAI & Langchain
- Install the Langchain Vertex framework
  ```
  pip install langchain_google_vertexai
- Initialize VertexAIEmbeddings Client
- Create a function to retrieve embeddings for a single query
- Create a function to retrieve embeddings for multiple documents


## Task 5: 🛠️ Data Pipeline to Chroma DB
- Create a Chroma collection from the documents processed by the DocumentProcessor (from previous tasks)
  - Split documents into chunks using Langchain's [CharacterTextSplitter](https://python.langchain.com/docs/modules/data_connection/document_transformers/character_text_splitter)
  - Create the [Chroma](https://docs.trychroma.com/) collection
  ![quizzifytask5](https://github.com/hari660/geminiQuizzify/assets/55326522/377606c6-c695-411a-b30a-5c88183033f6)



## Task 6: 📡 Streamlit UI for Data Ingestion
- Initialize DocumentProcessor, EmbeddingClient, and ChromaCollectionCreator from previous tasks
- Use Streamlit to capture user's inputs regarding quiz topic and desired number of questions
- Create a chroma collection from the processed documents

## Task 7: 🧠 Quiz Generator Class
- Create a QuizGenerator Class
  - Create a question template
  - Enable a retriever using the vectorstore object
  - Create chain with the retriever, template, and llm as to generate a question based off of the various ingested documents



## Task 8: 🔮 Generate Quiz Algorithm
- Loop the QuizGenerator and validate the questions uniqueness



## Task 9: 🎓 Generate Quiz UI
- Create a Streamlit UI to visualize a question
  ![quizzifytask9](https://github.com/hari660/geminiQuizzify/assets/55326522/a95aa6ea-b7d5-4ccb-9368-96fe64aa7590)





## Task 10: 🔄 Screen State Handling
- Enable the interface to handle all the quiz questions, move back and forth in the quiz, and display the correct answer and an explanation
  ![quizzifytask10](https://github.com/hari660/geminiQuizzify/assets/55326522/6c89bc3e-16da-49d9-aab1-73e7498cd5e7)




## Task 11: Preparing Submission

 - A GitHub repository for the project containing all the project files.
 - Loom Video to show the approach. [Loom Link](https://www.loom.com/share/0d3477b7b1564b648903a67f07756414?sid=f9a28bf1-1fb8-469e-b8e3-06b0ff630ebb)


## License

This project is licensed under the MIT License - see the LICENSE file for details.



## Acknowledgements
Special thanks to the [Radical AI](https://lab.radicalai.app/) team for allowing me to work on this AI Mission.
