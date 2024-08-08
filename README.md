## Semantic Search System for Policy Documents

### Overview: 
This project focuses on creating a semantic search system tailored for policy documents, integrating advanced techniques for document processing, vector embeddings, and coherent answer generation. The system comprises three key layers: embedding, searching, and generation, each optimized for enhanced performance.

### System Design
This is a 3 layer model.

<img width="625" alt="image" src="https://github.com/user-attachments/assets/41860252-4889-4106-a1ad-ac9dff9a7ba7">

#### Embedding layer 
Explore various PDF document processing and chunking strategies.   Choose between OpenAI's embedding model or SentenceTransformers for vector representations.
<img width="599" alt="image" src="https://github.com/user-attachments/assets/17ffeb43-bf2a-4940-a9a9-156da4e34bf4">

- Extracted text and tables from PDFs were formatted into data frames.
-	OpenAI's text-embedding model produced vector representations, which were stored in Chroma DB.
-	Documents underwent processing and chunking to enhance retrieval efficiency.

#### Search and re-rank layer
- Semantic searches were conducted on queries to fetch the top K relevant documents or chunks.
-	A re-ranking module used cross-encoders to enhance search precision.

<img width="609" alt="image" src="https://github.com/user-attachments/assets/5b6cfae9-881b-4a63-aab3-54037b25cc4a">

#### Generation layer
A carefully crafted prompt, which incorporated the original query along with the retrieved documents, was employed by the language model to produce coherent responses.

<img width="582" alt="image" src="https://github.com/user-attachments/assets/0bdff731-6b45-47c9-8754-e707505ccc0f">


