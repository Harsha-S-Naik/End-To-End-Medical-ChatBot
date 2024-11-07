# End-to-End Medical Chat Bot using Llama2 and Chainlit

## Objective
The purpose of this project is to build an advanced medical chatbot capable of answering a wide range of queries related to medicine. The chatbot leverages the Llama2 model for natural language understanding and uses **Chainlit** to create an interactive chat interface. Additionally, the project includes functionality to extract data from PDF documents, store it in a vector database (using **FAISS**), and retrieve relevant information to respond accurately to user queries.

## Methodology

### Key Components
1. **Llama2 Model**:
   - Utilized as the core language model to provide accurate, context-aware responses to medical queries.
   - Fine-tuned (optional) for medical-specific data to enhance domain understanding.

2. **Chainlit Framework**:
   - Provides an easy-to-use interface for developing and deploying chat applications.
   - Integrated with the Llama2 model to deliver real-time, interactive responses.

3. **PDF Data Extraction**:
   - Extracts text from medical PDF documents using tools like **PyPDF2** or **pdfplumber**.
   - Cleans and preprocesses extracted text for effective embedding.

4. **FAISS Vector Database**:
   - The extracted text is embedded using sentence embedding models (e.g., **Sentence Transformers**) and stored in **FAISS** (Facebook AI Similarity Search) for efficient similarity search.
   - Allows the chatbot to retrieve contextually relevant data when users ask medical queries.

### Process Flow
1. **Data Ingestion**:
   - PDF documents containing medical literature, articles, or guidelines are loaded and processed.
   - Text is extracted, cleaned, and converted into embeddings using a suitable embedding model.

2. **Embedding and Storage**:
   - Embeddings are created and stored in the **FAISS vector database** to facilitate quick and accurate retrieval.

3. **Query Handling**:
   - User queries are processed by the chatbot interface built with **Chainlit**.
   - If a query involves information stored in the database, the system retrieves the relevant data using similarity search in **FAISS** and combines it with Llama2’s responses for comprehensive answers.

4. **Response Generation**:
   - The Llama2 model generates responses enriched with retrieved data to ensure accurate and informative medical advice.

5. **User Interaction**:
   - The user interacts with the chatbot via the **Chainlit** interface, receiving real-time responses to their medical-related queries.

## Key Results
- **Accurate and context-aware answers** to medical queries with a response generation system powered by Llama2.
- **Seamless data extraction** and storage from PDF files, ensuring that valuable medical data can be referenced and retrieved efficiently.
- Integration with **FAISS vector database** provides a scalable solution for storing and retrieving large volumes of medical data.

## Tools & Libraries
- **Llama2** (Language model)
- **Chainlit** (Interface for chat applications)
- **FAISS** (Vector database for efficient similarity search)
- **PyPDF2/pdfplumber** (PDF data extraction)
- **Sentence Transformers** (For embedding generation)
- **Python** (Programming language)

## How to Run
1. Clone the repository:  
   `git clone https://github.com/Harsha-S-Naik/End-To-End-Medical-ChatBot.git`
   
2. Install the required libraries:  
   `pip install -r requirements.txt`
   
3. Run the Chainlit interface:  
   `chainlit run model.py -w`

5. Start interacting with the chatbot through the **Chainlit** interface.

## Preview
![medical](https://github.com/user-attachments/assets/2a20a474-ac2b-4072-b3ab-b07990f1188c)



# Download the model:(7.16 GB)
https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/blob/main/llama-2-7b-chat.ggmlv3.q8_0.bin

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
