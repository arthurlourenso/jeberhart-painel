# J Eberhart — Painel de Faturamento

Painel visual da evolução de faturamento da clínica (jan/2025 – set/2026).
Mostra o impacto do período de ausência e a recuperação subsequente, com
marcos de crescimento e comparativo trimestral ano a ano.

## ⚠️ Sobre os dados

Este repositório é **público**. Por isso, os **números reais não são versionados**.

- `dados.json` — números reais da clínica. Fica **apenas localmente** (listado no `.gitignore`). Nunca é enviado ao GitHub.
- `dados.exemplo.json` — dados fictícios, só para o painel renderizar como demonstração (inclusive no GitHub Pages).

O `index.html` tenta carregar `dados.json` primeiro; se não existir (como no GitHub Pages),
usa `dados.exemplo.json` e exibe um aviso de demonstração.

## Como ver os números reais (local)

1. Garanta que o arquivo `dados.json` real está nesta pasta (ele não vem do Git).
2. Rode um servidor local simples (o `fetch` não funciona abrindo o arquivo direto):

```bash
python3 -m http.server 8000
```

3. Abra http://localhost:8000 no navegador.

## GitHub Pages

O painel publicado no Pages mostra **apenas os dados de demonstração** — os
números reais nunca saem da máquina local. Serve como esqueleto visual.

## Estrutura

```
index.html            painel (sem dados embutidos)
dados.exemplo.json    dados fictícios (versionado)
dados.json            dados reais (NÃO versionado)
.gitignore
README.md
```
