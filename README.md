# 🦅 DOCUHAWK - Insurance Document Analyzer

![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/streamlit-v1.28+-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![OCR](https://img.shields.io/badge/OCR-Tesseract-green.svg)
![AI](https://img.shields.io/badge/AI-Groq%20LLM-purple.svg)

An intelligent document analysis tool that leverages OCR (Optical Character Recognition) and Large Language Models to extract, analyze, and process information from insurance PDF documents.

## 🌟 Features

### 📄 Document Processing
- **PDF to Image Conversion**: High-quality conversion with 300 DPI resolution
- **Advanced OCR**: Tesseract-based text extraction with preprocessing
- **Multi-page Support**: Process documents with multiple pages

### 🤖 AI-Powered Analysis
- **Smart Metadata Extraction**: Automatically extract key information like policy numbers, dates, names
- **Document Segmentation**: Intelligently identify and segment document sections
- **Header Detection**: Hierarchical structure recognition
- **Q&A System**: Natural language queries about document content

### 🎯 Key Information Extraction
- Policy Number
- Policy Holder Name
- Policy Start/End Dates
- Nominee Information
- Mobile Numbers
- Addresses
- Policy Types
- Custom field extraction

### 🖼️ Visual Features
- **Text Highlighting**: Visual highlighting of extracted information on original document
- **Interactive Preview**: Page-by-page document preview
- **Smart Matching**: Fuzzy matching to locate relevant text sections

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **OCR Engine**: Tesseract OCR
- **Image Processing**: OpenCV, PIL
- **PDF Processing**: pdf2image
- **AI/LLM**: Groq API (Meta LLaMA)
- **Text Matching**: FuzzyWuzzy
- **Language**: Python 3.8+

## 🚀 Quick Start

### Prerequisites

1. **Python 3.8 or higher**
2. **Tesseract OCR** installed on your system:
   - **Ubuntu/Debian**: `sudo apt-get install tesseract-ocr`
   - **macOS**: `brew install tesseract`
   - **Windows**: Download from [GitHub](https://github.com/UB-Mannheim/tesseract/wiki)

3. **Poppler** (for PDF processing):
   - **Ubuntu/Debian**: `sudo apt-get install poppler-utils`
   - **macOS**: `brew install poppler`
   - **Windows**: Download from [releases](http://blog.alivate.com.au/poppler-windows/)

4. **Groq API Key**: Get your free API key from [Groq Console](https://console.groq.com/)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/insurance-document-analyzer.git
   cd insurance-document-analyzer
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

1. **Start the Streamlit app**:
   ```bash
   streamlit run app.py
   ```

2. **Open your browser** and go to `http://localhost:8501`

3. **Enter your Groq API key** in the sidebar

4. **Upload a PDF document** and start analyzing!

## 📱 Usage Guide

### Step 1: Configuration
- Enter your Groq API key in the sidebar
- The key is required for AI-powered analysis features

### Step 2: Upload Document
- Click "Choose a PDF file" 
- Select your insurance document
- Click "🔄 Process PDF"

### Step 3: Analyze Document
Choose from various analysis options:

- **🖼️ Preview Pages**: View all processed pages
- **📑 Segments**: See document sections and structure  
- **📊 Metadata**: View extracted key information
- **📋 Headers**: Document outline and hierarchy
- **❓ Q&A Analysis**: Ask questions about the document

### Step 4: Ask Questions
- Select from predefined questions or ask custom queries
- Get highlighted answers with visual location on document
- View confidence scores and matching accuracy

## 🔧 Configuration

### Environment Variables
Create a `.env` file for API keys:
```
GROQ_API_KEY=your_groq_api_key_here
```

### Streamlit Secrets
For deployment, use `.streamlit/secrets.toml`:
```toml
GROQ_API_KEY = "your_groq_api_key_here"
```

## 📊 Supported Document Types

- ✅ Insurance Policy Documents
- ✅ Policy Certificates
- ✅ Insurance Applications
- ✅ Claims Documents
- ✅ Multi-page PDFs
- ✅ Text-based PDFs (not scanned images)

## 🎯 Example Queries

- "What is the policy number?"
- "When does this policy expire?"
- "Who is the nominee?"
- "Extract all personal details"
- "What type of insurance is this?"
- "Find the premium amount"

## 🔒 Privacy & Security

- **No Data Storage**: Documents are processed in memory only
- **Temporary Files**: Automatically cleaned up after processing
- **API Keys**: Securely handled through environment variables
- **Local Processing**: OCR runs locally on your machine

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) for optical character recognition
- [Streamlit](https://streamlit.io/) for the web framework
- [Groq](https://groq.com/) for LLM API services
- [OpenCV](https://opencv.org/) for image processing

## 🐛 Issues & Support

If you encounter any issues or need support:

1. Check the [Issues](https://github.com/yourusername/insurance-document-analyzer/issues) page
2. Create a new issue with detailed information
3. Include error messages and document types

## 🚀 Future Enhancements

- [ ] Support for more document types
- [ ] Batch processing capabilities
- [ ] Export results to CSV/JSON
- [ ] Advanced analytics dashboard
- [ ] Multi-language support
- [ ] Integration with cloud storage
- [ ] API endpoints for programmatic access

## 📈 Performance Tips

- Use high-quality PDFs for better OCR results
- Ensure documents have clear, readable text
- For large documents, processing may take 30-60 seconds
- Internet connection required for AI analysis features

---


