  Available Tools

  ┌────────────────────────────┬──────────────────────────────────────────────────────┐
  │            Tool            │                       Purpose                        │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ get_design_context         │ Read design styling (React + Tailwind by default)    │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ get_screenshot             │ Capture visual snapshots of selections               │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ get_metadata               │ Get layer structure (IDs, names, types, positions)   │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ get_variable_defs          │ Retrieve design tokens (colors, spacing, typography) │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ generate_figma_design      │ Capture live UI from a web app and send it to Figma  │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ generate_diagram           │ Create FigJam diagrams from Mermaid syntax           │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ create_design_system_rules │ Generate design system rule files                    │
  ├────────────────────────────┼──────────────────────────────────────────────────────┤
  │ Code Connect tools         │ Map Figma components to codebase components          │
  └────────────────────────────┴──────────────────────────────────────────────────────┘

  Key Limitation

  The remote MCP server cannot create designs from scratch in Figma. The generate_figma_design tool only captures existing live UI  
  (from localhost, staging, or production) and converts it into Figma layers.

  For Full Design Creation

  Your local figma-mcp-bridge is what you want for creating and manipulating designs programmatically — it has ~62 tools including  
  mutations for creating frames, shapes, text, components, setting styles, etc. The remote server complements it by providing:      

  - Better design reading (styled code output, screenshots)
  - Design token extraction
  - Code Connect mappings
  - FigJam diagram generation

  TL;DR: Use figma-mcp-bridge (your local plugin) to create/edit designs, and figma-remote-mcp to read designs and generate code    
  from them.

  Sources:
  - https://developers.figma.com/docs/figma-mcp-server/
  - https://developers.figma.com/docs/figma-mcp-server/tools-and-prompts/
  - https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Figma-MCP-server