# AI Tool Compatibility and Operational Limits

This toolkit consists of ordinary Markdown and text files. It does not require a custom plugin, agent installation, or execution runtime.

| Context | Recommended use | Verify first |
| --- | --- | --- |
| ChatGPT chats | Attach the standard and paste a selected prompt | The exact file is actually available in this chat |
| ChatGPT Projects | Put the standard in accessible Project sources and use project instructions | The assistant can read the source in the current session |
| ChatGPT Work | Use source files and available connected tooling for permitted reviews | Actual filesystem, runtime, GitHub and approval boundaries |
| Claude / Claude Code | Supply the standard in a supported file/context mechanism | File accessibility, tool permissions, and whether commands can run |
| Cursor and other coding agents | Include relevant files in agent context | Repository selection, file boundaries, approval and agent defaults |

**No automatic security coverage:** Reading the standard is not equal to scanner execution. AI agents can be incorrect, have partial file access, or propose unsafe code. Require actual commands, logs and independent manual review for claims of completed testing.

**Version drift:** Interfaces, context features and entitlements change; consult each product's current official documentation before writing tool-specific operational steps. Avoid giving agents blanket permission to install dependencies, access credentials, test third-party systems or publish code.
