# Módulo 14 — Ferramentas

## 📖 O que você vai aprender

Usar Git com VS Code, GitHub Desktop e GitHub CLI para trabalhar de forma mais produtiva.

---

## 💻 VS Code + Git

O VS Code tem integração nativa com Git.

### Recursos:
- **Source Control** (Ctrl+Shift+G): visualiza mudanças
- **Branch indicator**: mostra branch atual (canto inferior esquerdo)
- **Inline blame**: mostra quem editou cada linha
- **Merge editor**: resolve conflitos visualmente

### Atalhos úteis:
| Atalho | Função |
|--------|--------|
| Ctrl+Shift+G | Abre Source Control |
| Ctrl+Enter | Commit |
| Ctrl+Shift+P → "Git:" | Todos os comandos Git |

### Extensões recomendadas:
- **GitLens**: blame avançado, histórico
- **GitHub Pull Requests**: gerenciar PRs
- **Git Graph**: visualizar histórico como grafo

---

## 🖥️ GitHub Desktop

Interface gráfica para Git + GitHub.

### Recursos:
- Commits visuais
- Branch management por clique
- Diff visual de mudanças
- Review de PRs

### Quando usar:
- Preferência visual
- Aprender Git sem terminal
- Projetos simples

---

## ⌨️ GitHub CLI (gh)

O Git oficial da GitHub no terminal.

### Instalação:
```bash
# Windows
winget install GitHub.cli

# macOS
brew install gh

# Linux
sudo apt install gh
```

### Autenticar:
```bash
gh auth login
```

### Comandos úteis:
```bash
gh repo create           # Criar repositório
gh repo clone            # Clonar repositório
gh issue create          # Criar Issue
gh issue list            # Listar Issues
gh pr create            # Criar PR
gh pr list              # Listar PRs
gh pr checkout          # Checkout de um PR
gh pr merge             # Merge de um PR
gh pr review            # Review de um PR
gh api                  # Chamar API do GitHub
gh gist create          # Criar Gist
```

---

## 📋 Comandos deste módulo

| Ferramenta | Instalação | Uso principal |
|-----------|------------|---------------|
| VS Code | code.visualstudio.com | Edição + Git visual |
| GitHub Desktop | desktop.github.com | Git visual completo |
| GitHub CLI | gh auth login | GitHub no terminal |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [VS Code + Git](exercicios/01_vscode_git.txt) | Fácil |
| 2 | [GitHub Desktop](exercicios/02_github_desktop.txt) | Fácil |
| 3 | [GitHub CLI básico](exercicios/03_gh_cli_basico.txt) | Médio |
| 4 | [CLI avançado](exercicios/04_cli_avancado.txt) | Médio |
| 5 | [Extensões VS Code](exercicios/05_extensoes_vscode.txt) | Médio |
| 6 | [Comparação de ferramentas](exercicios/06_comparacao_ferramentas.txt) | Difícil |

---

**Módulo anterior:** [← Open Source](../13_open_source/)
**Próximo módulo:** [Projeto Prático →](../15_projeto_pratico/)
