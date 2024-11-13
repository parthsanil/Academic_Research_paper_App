# Academic Research Paper Assistant

An academic research paper assistant developed using Streamlit and various NLP tools, designed to assist with academic research tasks such as searching, summarizing, querying, and extracting future research directions from academic papers.

## Features

1. **Search Papers**: Searches for relevant academic papers on a topic from the arXiv API, downloads PDFs, and stores metadata in a local database.
2. **Query Papers**: Retrieves and displays information about stored research papers based on a selected topic.
3. **Summarize Research**: Extracts and summarizes text from PDF files associated with a research topic using NLP models.
4. **Q/A Chatbot**: Real-time Q&A chatbot using PDF content to answer user questions about a given research topic.
5. **Future Work**: Generates future research direction suggestions based on recent papers on a topic.

## Installation

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Set up your environment:
    - Create a `.env` file to store the API key for Google Gemini.
    - Example `.env` file:
      ```
      GENIUS_API_KEY=<Your-API-Key>
      ```
4. Run the application:
    ```bash
    streamlit run main.py
    ```

## Dependencies

- `Streamlit`: For creating a web-based user interface.
- `transformers`: Used for text generation.
- `sentence-transformers`: For creating text embeddings.
- `faiss`: To perform fast similarity search on text embeddings.
- `pdfplumber`: To extract text from PDF files.
- `requests`, `dotenv`, `json`, `xml.etree.ElementTree`: For API interactions, handling data, and environment variables.

## Usage

1. **Home**: Overview of the assistant.
2. **Search Papers**: Enter a topic and select a range of years. The app fetches relevant papers and downloads PDFs for local storage.
3. **Query Papers**: View metadata and summaries of stored papers, including PDF download options.
4. **Summarize Research**: Generates summaries of stored PDFs for a selected research topic.
5. **Q/A Chatbot**: Ask questions based on PDF content, and the chatbot provides answers derived from the available text.
6. **Future Work**: Generates suggestions for future research directions based on recent papers.

## Project Structure

- `main.py`: The main Streamlit app file with all functionality.
- `requirements.txt`: Lists dependencies.
- `database.json`: Local storage of paper metadata.
- `downloaded_papers/`: Directory for downloaded PDFs categorized by topic and year.

## Limitations

- Currently configured to fetch papers only from arXiv.
- Limited summarization length due to token restrictions in generative models.

## License

This project is licensed under the MIT License.
