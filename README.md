# Indian-Law-LLM

## Overview
This project utilizes an open-source language model, Llama3, to assist in the classification of crimes under the Indian Penal Code (IPC). The application processes crime descriptions and identifies relevant IPC sections, procedures, and recommendations. The legal information is extracted from a collection of PDF documents containing all relevant legal acts.

## Project Structure
- **data**: Contains synthetic or anonymized sample data used for testing and demonstration.
- **notebooks**: Jupyter notebooks with project walkthroughs and explanations.
- **src**: Source code for various components of the project, including data preprocessing, document embedding, and the main application.
- **docs**: Documentation and reports related to the project, including technical documentation and summarized reports.
- **presentations**: Slide decks used to present the project.
- **demos**: Links to demo videos or interactive demos showcasing the project.
- **blog_posts**: Articles and blog posts discussing the project in detail.

## Project Details
### Objective
The main objective of this project is to develop an AI-based tool that can:
1. Classify crimes based on their descriptions.
2. Identify the relevant sections of the Indian Penal Code (IPC) that apply to the crime.
3. Provide procedures and recommendations based on the IPC.

### Methodology
#### Data Collection and Preprocessing
- **Data Collection**: The data used for this project consists of PDF documents containing all legal acts related to the Indian Penal Code (IPC). These documents are loaded and processed to extract relevant legal information.
- **Preprocessing**: The preprocessing phase involves loading the documents, splitting them into manageable chunks, and creating vector embeddings for efficient retrieval.

#### Model and Tools
- **Language Model**: The project uses the open-source Llama3 model via the ChatGroq API to analyze and classify the crime descriptions.
- **Document Embedding**: GoogleGenerativeAIEmbeddings are used to create embeddings for the legal documents, enabling efficient similarity search and retrieval of relevant legal sections.
- **Vector Store**: FAISS (Facebook AI Similarity Search) is used to store and retrieve document vectors.

#### Application Workflow
1. **Document Loading and Embedding**: PDF documents are loaded and processed to create vector embeddings.
2. **Question Input**: Users can input questions related to legal contexts or situations.
3. **Retrieval and Response**: The system retrieves relevant document sections based on the input question and generates a response using the Llama3 model.

## Installation and Usage
### Prerequisites
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/LLM-Indian-Law-IPC.git
    ```
2. Navigate to the project directory:
    ```sh
    cd LLM-Indian-Law-IPC
    ```
3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

### Environment Setup
1. Create a `.env` file in the root directory with the following content:
    ```
    GROQ_API_KEY=your_groq_api_key
    GOOGLE_API_KEY=your_google_api_key
    ```
2. Ensure the PDF documents containing legal acts are placed in the specified directory.

### Running the Application
To run the application:
1. Execute the main application script:
    ```sh
    streamlit run src/app.py
    ```

2. Use the application interface to input questions and view the responses based on the provided legal context.

## Documentation and Reports
Detailed documentation and reports are available in the `docs` directory. These documents provide an in-depth explanation of the project's methodologies, design decisions, and results.

## Project Walkthrough
A step-by-step walkthrough of the project is available in the `notebooks/project_walkthrough.ipynb`. This notebook includes explanations, visualizations, and insights into how the model processes crime descriptions and identifies relevant IPC sections.

## Presentations and Demos
Slide decks and demo videos showcasing the project are available in the `presentations` and `demos` directories, respectively. These resources provide a visual overview of the project's objectives, methodology, and outcomes.

## Blog Posts
Articles and blog posts discussing the project in detail are available in the `blog_posts` directory. These posts cover various aspects of the project, including challenges faced and solutions implemented.

## License
This project is licensed under the MIT License.
