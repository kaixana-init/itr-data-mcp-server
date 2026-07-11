# itr-data-mcp-server
A Module Context Protocol (MCP) Server to serve ITR Documents to ITR Assistant

## Steps to run the application:
1. Clone the below repositories:
    - [itr-assistant](https://github.com/kaixana-init/itr-assistant)
    - [itr-data-mcp-server](https://github.com/kaixana-init/itr-data-mcp-server)

**itr-data-mcp-server**
1. Install python and pip if not already installed.
2. Create and activate virtual environment for the python project (itr-data-mcp-server).
   ```
   -- Create Virtual Environment
   python -m venv <virtual environment name> [Eg: python -m venv .venv]

   -- Activate Virtual Environment:
   .venv\Scripts\activate
   
   -- Deactivate Virtual Environment after use:
   deactivate
   ```
3. Install the required dependencies for the itr-data-mcp-server by running the following command in the terminal:
    ```
    pip install -r requirements.txt
    ```
4. Install Node.js as it's required for testing mcp server in the next point.
5. Try running the mcp server using the command:
    ```
    npx @modelcontextprotocol/inspector python -u tax_doc_server.py
    ```
6. If the server runs successfully, stop the server, and now you can start configuring itr-assistant.

**itr-assistant**
1. Find the setup information in itr-assistant README.md