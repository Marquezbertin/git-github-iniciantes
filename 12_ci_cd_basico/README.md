# Módulo 12 — CI/CD Básico

## 📖 O que você vai aprender

Automação com GitHub Actions: testes, linting, build e deploy automáticos.

---

## 🤔 O que é CI/CD?

**CI** (Integração Contínua): automatizar testes a cada commit
**CD** (Entrega Contínua): automatizar deploy após testes passarem

```
Push → CI (testes) → CD (deploy) → Produção
  │        │              │
  └─ code ─┴─ test ───────┴─ release
```

### Por que automatizar?
- Detectar erros cedo
- Consistência no deploy
- Economizar tempo humano
- Reduzir erros manuais

---

## ⚡ GitHub Actions

GitHub Actions é o sistema de CI/CD do GitHub.

### Conceitos-chave:
- **Workflow**: arquivo YAML que define a automação
- **Job**: conjunto de passos
- **Step**: cada instrução dentro de um job
- **Action**: ação reutilizável (ex: checkout, setup-node)
- **Runner**: servidor que executa o workflow

### Estrutura de um workflow:
```yaml
name: Nome do Workflow

on:                    # Quando rodar
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Meu passo
        run: echo "Olá!"
```

---

## 📁 Estrutura de pastas

```
.github/
└── workflows/
    ├── ci.yml
    ├── deploy.yml
    └── lint.yml
```

---

## 🔧 Exemplos de Actions Comuns

```yaml
# Checkout do código
- uses: actions/checkout@v4

# Setup Node.js
- uses: actions/setup-node@v4
  with:
    node-version: '20'

# Instalar dependências
- run: npm install

# Rodar testes
- run: npm test

# Rodar linter
- run: npm run lint

# Build
- run: npm run build

# Deploy (GitHub Pages)
- uses: actions/deploy-pages@v4
```

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `gh workflow list` | Lista workflows |
| `gh run list` | Lista execuções |
| `gh run view` | Ver detalhes |
| `gh workflow run` | Roda manualmente |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Primeiro workflow](exercicios/01_primeiro_workflow.txt) | Médio |
| 2 | [CI com testes](exercicios/02_ci_com_testes.txt) | Médio |
| 3 | [Lint automático](exercicios/03_lint_automatico.txt) | Médio |
| 4 | [Deploy Pages](exercicios/04_deploy_pages.txt) | Difícil |
| 5 | [Matrix build](exercicios/05_matrix_build.txt) | Difícil |
| 6 | [Pipeline completa](exercicios/06_pipeline_completa.txt) | Difícil |

---

**Módulo anterior:** [← Trabalho em Equipe](../11_trabalho_em_equipe/)
**Próximo módulo:** [Open Source →](../13_open_source/)
