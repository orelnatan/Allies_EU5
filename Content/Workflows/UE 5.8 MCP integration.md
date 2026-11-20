```markdown
# Unreal Engine 5.8 — Native MCP Server Setup Guide

Quick reference guide for enabling and configuring Epic's experimental native **Model Context Protocol (MCP)** server embedded directly inside Unreal Engine 5.8.

---

## Step 1: Enable Native MCP & Toolset Plugins

1. Open your project in **Unreal Engine 5.8**.
2. Navigate to the top menu: **Edit > Plugins**.
3. Search for **`Unreal MCP`** and check the **Enabled** box.
4. Search for **`All Toolsets`** (or individual toolsets) and check the **Enabled** box.
   > *Note: Enabling `All Toolsets` automatically enables the dependent `Toolset Registry` plugin, which exposes features like actor spawning, materials, lighting, and automation testing to LLMs.*
5. Click **Restart Now** when prompted by the editor.

---

## Step 2: Configure & Start the MCP Server

1. Open the preferences menu: **Edit > Editor Preferences**.
2. In the search bar at the top, type **`Model Context Protocol`** (or **`MCP`**).
3. Check the **Auto Start Server** option to launch the server automatically upon opening the project.
4. Verify the server configuration parameters:
   * **Server Port Number:** `8000` *(Default)*
   * **Server URL Path:** `/mcp` *(Default)*
5. Open the **Output Log** (`Window > Output Log`).
6. Run the following console command to start the server immediately:
   ```text
   ModelContextProtocol.StartServer

```

7. Verify that the Output Log confirms the server is listening:
```text
LogHttpListener: Created new HttpListener on 127.0.0.1:8000

```


*Your full local MCP endpoint is:* **`http://127.0.0.1:8000/mcp`**

---

## Step 3: Connect Cursor to Unreal Engine

1. In Cursor, open **Settings** (`Ctrl + ,` or `Cmd + ,`).
2. Select the **MCPs** tab (under **Customize**).
3. Click the **+ New** button and select **User** or **Workspaces**.
4. In the configuration JSON, add the following entry:

```json
{
  "mcpServers": {
    "unreal-engine": {
      "url": "[http://127.0.0.1:8000/mcp](http://127.0.0.1:8000/mcp)"
    }
  }
}

```

5. Save the file.
6. Verify under **Cursor Settings > MCPs** that `unreal-engine` displays a **Green Dot (Connected)** status along with active tools (`list_toolsets`, `describe_toolset`, `call_tool`).

```

---

[Model Context Protocol (MCP) Server Support in UE 5.8](https://www.youtube.com/watch?v=F2cWJFcTft4)

This video highlights Epic's official reveal of the embedded MCP server in Unreal Engine 5.8, showing how AI agents can interface directly with editor workflows.

```