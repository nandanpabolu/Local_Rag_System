
# Local LLM with Retrieval-Augmented Generation (RAG) 📚

This project is a Streamlit-based web application that leverages local Large Language Models (LLMs) with Retrieval-Augmented Generation (RAG) capabilities. The app allows users to interact with local LLMs, choose from various models, and index documents to enhance the question-answering process using research-based context.

## Features

- **Interactive Interface**: Streamlit app with a sidebar for model selection and document indexing.
- **Local Model Management**: Use models available locally or download them as needed.
- **Retrieval-Augmented Generation (RAG)**: Efficiently integrates document retrieval with generative capabilities for enhanced answers.
- **Session Management**: Maintains chat history and selected model state across sessions.

## Requirements

- Python 3.12 or higher
- Streamlit
- Ollama (for managing LLM models)
- Chroma (for document database management)
- Additional Python libraries: `httpx`, `langchain`, `langchain-community`, `pypdf`, `tqdm`, `watchdog`

## Installation

To run the app locally, follow these steps:

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/nandanpabolu/Local_Rag_System.git
    cd Local_Rag_System
    ```

2. **Set Up Virtual Environment**:

    ```bash
    python3.12 -m venv venv
    source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Required Packages**:

    ```bash
    pip install -r requirements.txt
    ```

   Ensure your `requirements.txt` includes:

    ```text
    streamlit
    httpx
    langchain
    langchain-community
    pypdf
    tqdm
    ollama
    watchdog
    ```

4. **Run the Streamlit App**:

    ```bash
    streamlit run ui.py
    ```

## Usage

1. **Select a Model**: Use the sidebar to choose from available LLM models. If the selected model is not available locally, the app will attempt to download it from the Ollama repository.

2. **Enter Folder Path**: Provide the folder path containing documents to be indexed. The documents will be loaded into a Chroma database, and embeddings will be created using the specified embedding model.

3. **Ask Questions**: Use the chat input to ask questions. The app retrieves relevant documents, processes them using the selected LLM model, and provides contextually enriched answers.

4. **View Responses**: The assistant's responses, along with the context used for generation, are displayed in the chat interface.

## Customization

- **Model Management**: Update the list of available models by modifying the `get_list_of_models` function in `models.py`.
- **Document Loaders**: Adjust document loaders in `document_loader.py` to support additional document formats or preprocessing steps.
- **Prompt Templates**: Modify prompt templates in `llm.py` to customize the question generation and answering styles.

## Troubleshooting

- **Connection Issues**: Ensure a stable internet connection if models need to be downloaded from the Ollama repository.
- **Model Availability**: Confirm that the selected models are compatible with your local setup.
- **Python Errors**: Ensure all required packages are installed and up-to-date. Reinstall them if necessary.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your enhancements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- Built with [Streamlit](https://streamlit.io/), [LangChain](https://langchain.com/), and [Ollama](https://ollama.com/).
- Special thanks to the open-source community for their invaluable tools and resources.

