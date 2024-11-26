<body>
    <h1>Ask Questions From PDF with LangChain and FAISS</h1>
    <p>
        This repository implements a pipeline for extracting, processing, and querying information from PDF documents using 
        LangChain, FAISS, and Llama-based models. The pipeline supports querying document content with similarity-based 
        retrieval and a retrieval-augmented generation (RAG) approach.
    </p>
    <h2>Features</h2>
    <ul>
        <li><strong>Load and Process PDFs</strong>: Automatically extracts content from PDFs and splits it into manageable chunks.</li>
        <li><strong>Embeddings Generation</strong>: Utilizes Ollama-based embeddings for efficient and accurate document representation.</li>
        <li><strong>Vector Store Integration</strong>: Uses FAISS for similarity search and Maximum Marginal Relevance (MMR)-based retrieval.</li>
        <li><strong>Customizable RAG Pipeline</strong>: Combines document retrieval with Llama-based models for accurate question-answering.</li>
        <li><strong>Dynamic Prompting</strong>: Adopts a flexible and concise chat prompt for generating context-aware answers.</li>
    </ul>
    <h2>Setup Instructions</h2>
    <h3>Prerequisites</h3>
    <p>Ensure you have Python installed on your system. Install the required Python libraries:</p>
    <pre><code>pip install -r requirements.txt
</code></pre>
    <h3>Environment Configuration</h3>
    <ol>
        <li>Clone the repository:
            <pre><code>https://github.com/Sawanmahna/Ask-Questions-from-PDF-using-LLM.git
cd Ask-Questions-from-PDF-using-LLM</code></pre>
        </li>
        <li>Create a <code>.env</code> file in the project root and set environment variables:
            <pre><code>LANGCHAIN_API_KEY="your_api_key"
LANGCHAIN_PROJECT = "pdfchatnow"
LANGCHAIN_ENDPOINT = "https://api.smith.langchain.com"
LANGCHAIN_TRACING_V2=true</code></pre>
        </li>
        <li>Suppress warnings (optional):
            <pre><code>import warnings
warnings.filterwarnings("ignore")</code></pre>
        </li>
    </ol>
    <h2>Usage</h2>
    <h3>1. Load PDFs</h3>
    <p>Place your PDF files in the <code>Data/</code> directory. The script will automatically load and process them.</p>
    <h3>2. Process Documents</h3>
    <p>Run the script to extract and split the PDF content into manageable chunks for querying.</p>
    <h3>3. Ask Questions</h3>
    <p>You can query the processed PDFs by asking specific questions. For example:</p>
    <pre><code>question = "What is the invoice number?"
output = rag_chain.invoke(question)
print("Answer:", output)</code></pre>
    <h3>4. Sample Questions</h3>
    <ul>
        <li>"What is the price of Web Design?"</li>
        <li>"What is in the PDF?"</li>
        <li>"What is the invoice date?"</li>
    </ul>
    <h2>Acknowledgments</h2>
    <ul>
        <li><strong>LangChain</strong>: For building the framework for language model-based pipelines.</li>
        <li><strong>FAISS</strong>: For efficient similarity search and retrieval.</li>
        <li><strong>Ollama</strong>: For embedding and question-answering models.</li>
        <li><strong>PyMuPDF</strong>: For efficient PDF processing.</li>
    </ul>
</body>
