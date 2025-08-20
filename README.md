## Project Overview

This project leverages cutting-edge tools to make fine-tuning accessible and efficient:

-   **Base Model**: Phi-3-mini-4k-instruct-bnb-4bit (a powerful and efficient small LLM)
-   **Fine-tuning Frameworks**: `unsloth` (for blazing-fast and memory-efficient training) and `trl` (Transformers Reinforcement Learning for supervised fine-tuning)
-   **Example Task**: Extracting structured JSON data from unstructured text.
-   **Example Dataset**: `json_extraction_dataset_500.json` (a sample dataset for JSON extraction, easily swappable with your own data).
-   **Output**: A fine-tuned model saved in the universal GGUF format, ready for deployment with local inference engines like Ollama.

## Getting Started

### Prerequisites

-   Python 3.x
-   `pip` package manager
-   A CUDA-enabled GPU (highly recommended for optimal training speed)

### Installation

1.  Clone this repository to your local machine:
    ```bash
    git clone https://github.com/Fidelek84/fine_tune_llm.git
    cd fine_tune_llm
    ```

2.  The `Fine Tuning.ipynb` notebook will guide you through installing all necessary Python packages directly within the notebook environment.

### Running the Fine-tuning Process

The entire fine-tuning workflow is encapsulated within the `Fine Tuning.ipynb` Jupyter notebook.

1.  Launch Jupyter Notebook from your project directory:
    ```bash
    jupyter notebook "Fine Tuning.ipynb"
    ```
2.  Execute all cells in the notebook sequentially. The notebook will:
    -   Load your chosen dataset (e.g., `json_extraction_dataset_500.json`).
    -   Initialize the base LLM (`Phi-3-mini-4k-instruct-bnb-4bit`).
    -   Configure LoRA (Low-Rank Adaptation) adapters for efficient and effective fine-tuning.
    -   Train the model.
    -   Demonstrate how to test the newly fine-tuned model.
    -   Save the fine-tuned model in the highly compatible GGUF format.

## Repository Structure

-   `Fine Tuning.ipynb`: The Jupyter notebook containing the complete fine-tuning and testing workflow.
-   `json_extraction_dataset_500.json`: A sample dataset illustrating the format required for JSON extraction. **Replace this with your own dataset for different tasks!**
-   `Modelfile`: (Likely for Ollama setup, defining how to serve the GGUF model).
-   `ollama_llm/`: Contains files related to Ollama deployment, including the `Modelfile` and the resulting `unsloth.Q4_K_M.gguf` model.
-   `PyTorch/`: A directory for general PyTorch-related notebooks and experiments.

## Using Your Fine-tuned Model

Once fine-tuned, your GGUF model is ready for local inference! You can easily integrate it with local LLM serving solutions like Ollama. Check the `ollama_llm/` directory for examples on how to set up and run your custom model.

## Contribution

Feel free to fork this repository, experiment with your own datasets, and contribute improvements!
