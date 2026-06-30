# Glossário Estrateg[IA]

Glossário visual standalone de Claude Code e Vibe Coding, explicado com analogias hospitalares pra gestores e coordenadores da saúde.

**197 termos** organizados em 8 categorias:
- 🩺 **Claude Code** (23): .env, Agent SDK, Claude Code, Hooks, MCP, Memory, Skills...
- 🔧 **Ferramentas** (29): terminal, IDEs, plugins, deploy, debug
- 🌿 **Git** (25): commit, branch, merge, rebase, stash, PR
- 🤖 **IA & LLM** (25): tokens, prompt, fine-tuning, hallucination, embeddings
- ⚡ **Node & JS** (22): npm, npx, package.json, ESM, CommonJS
- 🖥️ **Terminal** (26): bash, cd, grep, pipe, environment
- 💡 **Vibe Coding** (20): pair programming, prompt-first, agent loop
- 🌐 **Web** (27): HTML, CSS, DOM, API, REST, GraphQL, HTTP

## Como rodar local

O glossário precisa de servidor estático (não funciona direto com `file://` por causa do fetch):

```bash
cd "C:/Claude Code"
node server.js
```

Abre: `http://localhost:5678/projetos/ia-saude/Modo%20IA%20Saude/Glossario/`

## Como publicar (GitHub Pages)

O workflow `.github/workflows/deploy.yml` já está pronto. Para publicar:

1. Crie o repo: https://github.com/new — nome `estrategia-glossario`, **public**
2. Faça push (instruções abaixo)
3. Settings → Pages → Source: **GitHub Actions**
4. Em ~1min está no ar

## Estrutura

```
Glossario/
├── index.html      ← glossário (logo tipográfica Estrateg[IA] inline)
├── termos.json     ← 197 termos em JSON
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

## Licença

Uso interno do Estrateg[IA] — Inteligência que move a gestão em saúde.
