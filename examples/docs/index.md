# web-docs

Teste do webdocs

```kroki-mermaid
sequenceDiagram
GitLab->>Kroki: Request render
Kroki->>Mermaid: Request render
Mermaid-->>Kroki: Image
Kroki-->>GitLab: Image
```
