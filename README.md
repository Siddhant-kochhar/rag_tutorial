# My RAG Pipeline Project for PDF Q&A

This is my project where I built a complete Retrieval-Augmented Generation (RAG) pipeline from scratch. As a student, I'm always looking for exciting projects to learn and grow, and this was a fantastic opportunity to dive into the world of LLMs and vector databases.

I developed this project by following a tutorial from one of my favorite YouTubers, Krish Naik. The goal was to build a system that could take a bunch of PDF documents, understand them, and answer questions based on their content.

## What I Learned and Implemented

- **PDF Data Ingestion**: I wrote code to automatically read and process any PDF files I put into a folder.
- **Text Processing**: I learned how to split the documents into smaller, more manageable chunks for the AI to work with.
- **Embeddings**: I used `SentenceTransformer` models to turn the text chunks into vector embeddings, which is a crucial step for semantic search.
- **Vector Store**: I set up a `ChromaDB` vector store to save and efficiently search through the document embeddings.
- **Retriever**: I built a retriever that can find the most relevant document chunks for any question I ask.
- **LLM Integration**: I connected everything to the Groq API to use powerful models like Llama 3.1 for generating answers based on the retrieved information.
- **Jupyter Notebook Workflow**: The whole process is laid out in a Jupyter Notebook, which made it easy for me to experiment and see the results at each step.

## Project Structure

```
.
├── data/
│   ├── pdf_files/          # This is where I put my PDF files
│   └── vector_store/       # The ChromaDB database is stored here
├── notebook/
│   └── pdf_loader.ipynb    # My main notebook with all the code
├── src/
│   └── __init__.py
├── main.py
├── requirements.txt
└── README.md
```

## How to Get it Running

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd rag_tutorial
    ```

2.  **Set up a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the necessary packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up the Groq API Key:**
    I created a `.env` file in the project folder and added my Groq API key like this:
    ```
    GROQ_API_KEY="your-groq-api-key"
    ```

## How I Use It

1.  **Add PDFs**: I drop all the PDFs I want to use into the `data/pdf_files/` folder.

2.  **Run the Notebook**: I open `notebook/pdf_loader.ipynb` and run the cells one by one. The notebook takes care of everything from processing the files to setting up the retriever.

3.  **Ask Questions**: At the end of the notebook, I can use the `rag_simple` or `rag_advanced` functions to ask questions.

    ```python
    # This is how I ask a question
    answer = rag_simple("What is machine learning?", rag_retriever, llm)
    print(answer)
    ```

## Learning Journey & Acknowledgements

This project was a great learning experience for me. I built it by following the tutorial from Krish Naik's YouTube channel. I'm grateful for his clear explanation, which helped me understand and implement this RAG pipeline from scratch.

- **Inspiration and Guidance**: [Build Your Own RAG From Scratch](https://www.youtube.com/watch?v=o126p1QN_RI) by Krish Naik.

A huge thank you to Krish for his amazing tutorials that empower students like me to learn and build cool projects.
