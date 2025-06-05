## Requirements

python3

## Install Plugin

1. Look at the release next to the screen.  
   There is a zipped file of the Unreal plugin.  
   Unzip that file to the root directory of your Unreal project.  
   In Unreal, all plugins should be structured like this. It's nothing unusual.  
   Detailed for beginners.
   
2. Open your project in the editor.
   then open the Plugins window and activate the plugin called BP_MD_LLM.

## Install MCP Server for Claude Desktop (This is not required. Install only if you use claude desktop.)

1. Go into the plugins folder. (In the shell window of each operating system (cmd for Windows))
   {Your Project}/Plugins/BP_MD_LLM/Resources/MCPBridge
   
2. Run python install 
   pip install -r ./requirements.txt
   
3. add json data into
   ```
   macOS: ~/Library/Application Support/Claude/claude_desktop_config.json
   Windows: %APPDATA%\Claude\claude_desktop_config.json
   ```

   Change Your Project Path. See here https://modelcontextprotocol.io/quickstart/user#windows
   ```json
    {
      "mcpServers": {
        "bml_v2_server": {
          "command": "python",
          "args": [
            "Your Project Path\\Plugins\\BP_MD_LLM\\Resources\\MCPBridge\\mcp-bridge-simple.py"
            ],
          "env": {}
        }
      }
    }
    ```

4. Run test.
   ```
   python3 .\test-python-bridge.py
   ```
      
