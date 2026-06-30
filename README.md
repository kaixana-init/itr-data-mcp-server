# itr-data-mcp-server
A Module Context Protocol (MCP) Server to serve ITR Documents to ITR Assistant

## Steps to run the application:
1. Clone the below repositories:
    - [itr-assistant](https://github.com/kaixana-init/itr-assistant)
    - [itr-data-mcp-server](https://github.com/kaixana-init/itr-data-mcp-server)

**itr-data-mcp-server**
1. Install python and pip if not already installed.
2. Create and activate virtual environment for the python project (itr-data-mcp-server).
3. Install the required dependencies for the itr-data-mcp-server by running the following command in the terminal:
    ```
    pip install -r requirements.txt
    ```
4. Try running the mcp server using the command:
    ```
    npx @modelcontextprotocol/inspector python -u tax_doc_server.py
    ```
5. If the server runs successfully, stop the server, and now you can start configuring itr-assistant.

**itr-assistant**
1. Open application.yml in itr-assistant and update the following properties:
    - `GOOGLE_GEMINI_API_KEY` - Can be generated from Google AI Studio (https://aistudio.google.com/). Incase if you want to use any other model update the respective dependency in the pom.xml file and update the llm provider related configurations in application.yml.
    - `${/path/to/your/python-executable-inside-venv}` - This is the path to the python executable inside the virtual environment created for itr-data-mcp-server.
    - `${/path/to/your/mcp_server.py}` - This is the path to the tax_doc_server.py file inside the itr-data-mcp-server repository.
2. Run the application