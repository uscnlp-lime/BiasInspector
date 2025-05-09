# Bias Agent Project

## Introduction

This project builds a **Bias Agent**, which assists users in detecting and analyzing potential bias present in structured datasets.

### Features:
- Detect and analyze bias in structured datasets.

### Structure:
The project mainly consists of:
- **Primary_Assistant node**
- **Advisor_Assistant node**
- **Execution_Tools node**

Below is a graphical representation of the project structure:

![Agent Graph](generated_files/agent_graph.png)


## File Descriptions

- **main.py**:
- **agent.py**: Manages the core execution flow of the Bias Agent
- **agent_node_factory.py**: Defines the structure and behavior of the agent's nodes
- **tools.py**: Contains various utility tools for data loading, preprocessing, analysis, and result presentation
- **json_to_markdown.py**:
- **tool_test.py**: Provides a test environment to verify the functionality of tools used in the project
- **prompts.yaml**: Contains the system message that defines the behavior and instructions for the Bias Agent
- **requirements.txt**: Contains the required dependencies for running the project.
- **source_files**: Stores files that the agent needs prior to running.
- **generated_files**: Stores files generated by the agent during the execution of the project.
- **logs**:
- **markdown_logs**:


## Usage

### Setup (Windows only)

To ensure that the execution tool for dynamically generated code always loads the necessary modules correctly, it is essential to run the program within a virtual environment after installing the dependencies from `requirements.txt`.

1. Open a terminal and navigate to your project directory.
2. Run the following commands to create and activate a virtual environment:

```bash
# Create a virtual environment (replace 'venv' with your desired name)
python -m venv venv

# Activate the virtual environment
.\venv\Scripts\activate
```

Once the virtual environment is activated, proceed with the steps below.

Run the following command to install all required dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

Next, create a `.env` file in the root directory by running the following command:

```bash
echo. > .env
```

Then, open the `.env` file and include the following environment variables:

```bash
OPENAI_API_KEY=your_openai_key_here
LANGCHAIN_API_KEY=your_langchain_key_here
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=Multi-agent Collaboration
```

Make sure to always run your program within the activated virtual environment to ensure that all dependencies are loaded correctly.


### Running the Agent

To run this program, use the following command:

```bash
python main.py
```

### For Developers

If you want to test whether the tools are functioning correctly, modify the `tool_test.py` file as needed and run:

```bash
python tool_test.py
```