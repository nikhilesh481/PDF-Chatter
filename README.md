# PDF Chatter

A powerful AI-powered application that enables intelligent conversations with multiple PDF documents using advanced language models and vector search technology.

## Overview

PDF Chatter transforms your static PDF documents into an interactive knowledge base. Simply upload multiple PDF files, and the application will process them to create an intelligent chatbot that can answer questions based on the content of your documents. Built with Streamlit, LangChain, and Google's Gemini AI, this tool makes document analysis and information retrieval effortless.

## Key Features

### Intelligent Document Processing
- **Multi-PDF Support**: Upload and process multiple PDF documents simultaneously
- **Smart Text Chunking**: Advanced sliding window technique that adapts to document complexity
- **Vector Embeddings**: Converts text into searchable vector representations using Google's Gemini AI

### Advanced Query Capabilities
- **Multi-Document Search**: Ask questions that span across multiple documents
- **Contextual Understanding**: Maintains conversation context for follow-up questions
- **Semantic Search**: Finds relevant information even when using different wording than the source text

### Flexible AI Integration
- **Multiple LLM Support**: Compatible with Google Gemini Pro, OpenAI GPT, Anthropic Claude, and Llama2
- **Real-time Processing**: Get instant responses to your queries
- **Conversational Interface**: Natural language interaction with your documents

## How It Works

The application follows a sophisticated pipeline to enable intelligent document interaction:

1. **Document Ingestion**: PDFs are uploaded and their text content is extracted
2. **Text Segmentation**: Content is intelligently split into optimal chunks for processing
3. **Vectorization**: Text chunks are converted to high-dimensional vectors using AI embeddings
4. **Indexing**: Vectors are stored in a FAISS database for fast similarity search
5. **Query Processing**: User questions are vectorized and matched against document chunks
6. **Response Generation**: Relevant chunks are fed to the language model to generate accurate answers

## Technical Architecture

### Core Technologies
- **Streamlit**: Web application framework for the user interface
- **LangChain**: Orchestration framework for AI applications
- **Google Gemini AI**: Large language model for text understanding and generation
- **FAISS**: Facebook's library for efficient similarity search and clustering
- **PyPDF2**: PDF text extraction and manipulation

### Dependencies
- **streamlit**: Interactive web application framework
- **google-generativeai**: Google's generative AI SDK
- **langchain**: AI application development framework
- **langchain_google_genai**: LangChain integration for Google AI
- **faiss-cpu**: Vector similarity search library
- **PyPDF2**: PDF processing library
- **python-dotenv**: Environment variable management

## Installation Guide

### Prerequisites
- Python 3.8 or higher
- Google AI API key (obtain from Google AI Studio)

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/nikhilesh481/PDF-Chatter.git
   cd PDF-Chatter
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure API Key**
   Create a `.env` file in the project root:
   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

4. **Launch the Application**
   ```bash
   streamlit run chatapp.py
   ```

## Usage Instructions

### Getting Started
1. **Launch the App**: Run the Streamlit application using the command above
2. **Upload Documents**: Use the sidebar to upload one or more PDF files
3. **Process Documents**: Click "Submit & Process" to analyze your documents
4. **Start Chatting**: Type questions in the chat interface to interact with your documents

### Best Practices
- **Upload Related Documents**: For best results, upload documents that are related to each other
- **Ask Specific Questions**: More specific questions yield better, more focused answers
- **Use Follow-up Questions**: The system maintains context, so you can ask follow-up questions
- **Try Different Phrasings**: If you don't get the expected answer, try rephrasing your question

### Example Queries
- "What are the main findings in the research papers?"
- "Compare the methodologies used in document A and document B"
- "Summarize the key points from the uploaded documents"
- "What are the recommendations mentioned in the reports?"

## Project Structure

```
PDF_Chatter/
├── chatapp.py              # Main Streamlit application
├── requirements.txt        # Python dependencies
├── .env                    # Environment variables (create this)
├── docs/                   # Sample PDF documents
├── img/                    # Application screenshots
├── README.md              # This file
└── LICENSE                # MIT License
```

## Configuration

### Environment Variables
- `GOOGLE_API_KEY`: Required for Google Gemini AI integration

### Customization Options
- Modify chunk size and overlap in the text splitting configuration
- Adjust similarity search parameters for different use cases
- Switch between different language models as needed

## Troubleshooting

### Common Issues
- **API Key Error**: Ensure your Google API key is correctly set in the `.env` file
- **Memory Issues**: For large documents, consider reducing chunk size
- **Slow Processing**: Large PDFs may take time to process; this is normal

### Performance Tips
- Use smaller PDF files for faster processing
- Limit the number of documents uploaded simultaneously
- Clear the chat history if the application becomes slow

## Contributing

We welcome contributions to improve PDF Chatter! Please feel free to:
- Report bugs and issues
- Suggest new features
- Submit pull requests
- Improve documentation

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Support

If you find this project helpful, please consider giving it a star! For questions or support, please open an issue in the repository.

---

**Transform your PDF documents into an intelligent knowledge base with PDF Chatter!**
