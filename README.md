# [Chat with India's Budget 2024 using your local CPU chatbot](https://www.aimplabs.org/blogs/chatbot-budget2024/)

![The Parliament](assets/parliament_pencil_drawing.jpeg "The Parliament")

## Motivation

We have implemented a custom chatbot using **Llamafile** to interact with India's Budget 2024 speech in local CPU. Developed by Mozilla, Llamafile converts AI models into executables that can run on any machine, bypassing the need for high-cost servers like AWS and the constraints of frameworks like Langchain. This tutorial is written in raw Python, allowing for a streamlined setup without requiring GPU resources.

## Implementation

We have implemented the follwing steps in the `chatbot-budget2024` notebook.

1. Download and installation of the prerequisites.
2. Reading the budget speech document from `.docx` format.
3. Splitting of the document into smaller chunks.
4. Create embeddings using `TF-IDF` and use of `FAISS` vector store to create embedding index.
5. Execute FAISS's similarity search to find *k* nearest relevant contexts w.r.t the user query.
6. Constuction of prompt using a q&a instruction, relevant contexts and the query.
7. Run Llamafile as a server and chat with the local chatbot.