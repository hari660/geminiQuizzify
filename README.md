# Gemini Quizzify

## Mission
Create a quiz generator using Google Gemini, Langchain, Chroma, and Streamlit to explore LLMs and vector embeddings. 

## Requirments:

- Python version 3.11 or above
- [Streamlit Documentation](https://docs.streamlit.io/)
- Google Cloud account
- [Vertexai Documentation](https://cloud.google.com/vertex-ai)

## Task 1: Enabling Google Cloud

- Go to the [Google Cloud Platform](console.cloud.google.com) and select "Get Started for free".
- Sign in using your Google Account and complete the billing requirements.
- Create a new project.
- Navigation -> Artificial Intelligence -> Vertex AI -> Enable All Recommended APIs


## Task 2: Google Cloud Initialization

- Install the Google SDK using this [link](https://cloud.google.com/sdk/docs/install).
- Run the following command to initialize the SDK:
  ```
  gcloud init
- Sign in using your Google Account credentials.
- Select an existing project or Create a new project


## Task 3: Setting up Google Gemini

- Install the streamlit framework
  ```
  pip install streamlit
- In the project, we are using Gemini Pro as the LLM.
- Use the project ID instead of the project name, like this: `project = "project_id"`. This helps avoid encountering a 403 permission denied error.



## Task 11: Preparing Submission

 - A GitHub repository for the project containing all the project files.
 - Loom Video to show the approach. [Loom Link](https://www.loom.com/share/27cbe9a2df964cc6be0be9d745df0d03?sid=69ccce98-14cf-43a9-b03e-cbf601615b38)

## Acknowledgements
Special thanks to the [Radical AI](https://lab.radicalai.app/) team for allowing me to work on this AI Mission.
