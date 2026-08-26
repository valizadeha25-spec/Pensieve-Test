# PamAI — Pensieve context mirror

This repository is a **read-only mirror** of a curated context layer in
[Pensieve](https://app.pensieve.uk/dashboard/contexts/506). It is generated and published automatically: any
file edited on this branch by hand is overwritten on the next sync.

- Every page is a directory, and its content is that directory's `page.md`.
- `page.md` at the root is the context overview; its child pages are the
  directories beside it, and so on down the tree.
- A page keeps its path when it gains or loses child pages, so links into this
  repository stay valid as the tree is reorganised.
- Links between pages are ordinary relative Markdown links.
- Source citations link back to the original document and keep a `data:ID`
  handle, which resolves through the Pensieve MCP server.

To change the content, edit the page in Pensieve — the change appears here on
the next sync.
