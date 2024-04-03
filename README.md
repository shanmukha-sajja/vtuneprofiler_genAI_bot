# vtuneprofiler_genAI_bot
Chatbot powered by GenAI to provide targeted assistance to developers seeking information about Intel Vtune Profiler and its components

# Problem statement:
Develop a chatbot powered by GenAI to provide targeted assistance to developers seeking information about Intel Vtune Profiler and its components. The chatbot should specialize in addressing queries specifically related to Intel technologies and their application within the oneAPI ecosystem.

# Technologies used:
1.	Python standard library 
2.	Third-party libraries
  •	Chromadb
  •	PyPDF2
  •	Transformers
3.	Langchain
  •	CharacterTextSplitter
  •	RecursiveCharacterTextSplitter
  •	HuggingFacePipeline
  •	HuggingFaceEmbeddings
  •	RetrievalQA
  •	Document
  •	Chroma
4.	Transformers
  •	AutoTokenizer
  •	AutoModelForQuestionAnswering
  •	AutoModelForCausalLM
  •	pipeline

# Implementation:

**Input Processing:**

Utilization of PyPDF2 library to convert the input PDF file into text within a document.
Employing RecursiveCharacterTextSplitter to segment the text into smaller chunks based on specific criteria based on our requirment.

**Text Encoding:**

Utilized the Hugging Face embeddings i.e "hkunlp/instructor-large" model, to encode the text.
Transformation of text into a numerical representation capturing semantic meaning and context which signifies the Embedding.

**Database Storage:**

Utilization of Chroma for storing processed text data into a structured storage system.
Efficient data management and retrieval capabilities provided by Chroma.

**Hugging Face Model Initialization:**

Initialization of specified Hugging Face model ("< zephyr-7b-beta or Xwin-LM-13B-V0.1 >") along with autotokenizer.
Autotokenizer automatically configures appropriate tokenizer based on the model for optimal text processing.

**Data Retrieval with RAG (Retrieval Augmented Generation):**

Integration of retrieval-based and generation-based techniques in NLP.
Utilization of retrievalQA method to fetch relevant data from knowledge base or corpus using a retriever.
Employing keyword matching models to identify and retrieve most relevant information.

**Input Augmentation:**

Incorporation of retrieved data as input augmentation to enhance context and completeness.
Augmented input passed through generative model ("< zephyr-7b-beta or Xwin-LM-13B-V0.1 >") for generating responses, answers, or summaries based on task requirements.
