# Indian-Law-LLM

## Overview
This project utilizes an open-source language model, Llama3, to assist in the classification of crimes under the Indian Penal Code (IPC). The application processes crime descriptions and identifies relevant IPC sections, procedures, and recommendations. The legal information is extracted from a collection of PDF documents containing all relevant legal acts.

![Project Image](indian_law_llm.png)

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

## Example Usage

**Input:** Theft of a mobile phone from a shop.

**LLM Output:**
Based on the input "Theft of a mobile phone from a shop", I analyze the situation and determine that it falls under the category of theft, which is covered under Chapter XVI of the Indian Penal Code (IPC), titled "Offences Against Property".

**IPC Section:** Section 379 of the Indian Penal Code deals with "Theft".

**FIR Registration:** The FIR (First Information Report) should be registered under Section 379 of the IPC, which is a non-cognizable offense, requiring a police officer to register a written report.

**Outline Procedure:**
1. The police officer will register the FIR and take the statement of the complainant.
2. The police will conduct an investigation to gather evidence and identify the accused.
3. If the accused is identified, the police will arrest them and take them to the police station.
4. The accused will be interrogated, and their statement will be recorded.
5. The police will collect evidence from the crime scene, including any witnesses or surveillance footage.
6. The investigation will be completed, and the police will submit a charge sheet to the court.

**Additional Recommendations:**
- The police should ensure that the complainant is provided with a copy of the FIR and a case diary.
- The police should take photographs of the crime scene and the stolen mobile phone to use as evidence.
- The police should interview any witnesses who may have seen or heard something suspicious.
- The police should check for any security footage that may have captured the theft.

*Please note that the above procedure and additional recommendations are general guidelines and may vary depending on the specific circumstances of the case and the jurisdiction in which it is being investigated.*
