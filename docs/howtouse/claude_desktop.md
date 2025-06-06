

## Why Use Claude Desktop?

* Claude Desktop can communicate directly with the `BP_MD_LLM` server running inside Unreal Editor.
* This enables Claude Desktop to control the Unreal Editor directly.
* Communication between Claude.ai and the editor via a web browser will be implemented in the future.

### Most Important Note

* Once a Blueprint is converted into JSON, the LLM can understand it.
* Therefore, start by either converting a Blueprint to JSON or loading an existing JSON file.
* After that, you can analyze and modify the Blueprint within Claude Desktop.
* Modifying a Blueprint means editing its JSON representation.
* After completing all modifications, you must convert the JSON back into a Blueprint and save it.
* When saving as a Blueprint, it uses the name and path specified in the JSON file. If you wish to change them, do so before saving.

## Example Conversations

1. "Convert the Blueprint named 'Test' to JSON."

   * You can search for Blueprints by type or name.

2. "Render the Event Graph as a Mermaid diagram."

   * You can specify the Event Graph or a particular function name.
   * "Also render nodes that are not connected."
   * "Change the diagram colors to high contrast."
     
3. Proceed with any tasks you wish to perform.

   * For example: "Explain the current Blueprint's functionality."

4. When modifying JSON, include the following instruction:

   * "Only modify the JSON. I will generate the Blueprint later."  
     (This instruction must be provided at the beginning; otherwise, a Blueprint will be generated each time.)  
     (If the JSON is modified, the Mermaid diagram will be re-rendered. If not, you can manually request a re-render.)  

5. "Generate a Blueprint from the modified JSON."

   * The Blueprint will be saved using the name and path specified in the JSON.
   * If an asset with the same name already exists, the existing asset will be renamed to `original_name_Old` before saving.

6. "Please tell me how to use BP_MD_LLM"
   
