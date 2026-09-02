# Módulo 08 — Issues e Projetos

## 📖 O que você vai aprender

Usar GitHub Issues para rastrear bugs e tarefas, e GitHub Projects para organizar o trabalho.

---

## 🐛 O que são Issues?

Issues são **tarefas, bugs ou funcionalidades** que precisam ser trabalhadas no projeto. É como um sistema de tarefas integrado ao repositório.

### Tipos de Issues:
- 🐛 **Bug report** — Reportar um erro
- ✨ **Feature request** — Sugerir nova funcionalidade
- 📖 **Documentação** — Melhorar docs
- ❓ **Pergunta** — Tirar dúvida sobre o projeto

---

## 📝 Criar uma Issue

### Pela web:
1. Aba "Issues" do repositório
2. "New issue"
3. Título claro
4. Descrição detalhada
5. Labels, assignees, milestone

### Pelo terminal:
```bash
gh issue create --title "Título" --body "Descrição"
gh issue create --title "Bug no login" --label "bug" --assignee @me
```

---

## 🏷️ Labels

Labels categorizam Issues:

| Label | Cor | Uso |
|-------|-----|-----|
| bug | Vermelho | Erros |
| enhancement | Verde | Novas funcionalidades |
| documentation | Azul | Documentação |
| good first issue | Verde claro | Boas para iniciantes |
| help wanted | Laranja | Precisa de ajuda |
| question | Roxo | Perguntas |

---

## 📅 Milestones

Milestones agrupam Issues em versões ou entregas:
- `v1.0` — Primeira versão
- `Sprint 1` — Trabalho de 2 semanas
- `Backlog` — Itens para futuro

---

## 📋 GitHub Projects

Projects são quadros Kanban para gerenciar trabalho:

### Colunas típicas:
1. **To Do** — A fazer
2. **In Progress** — Em andamento
3. **In Review** — Em revisão
4. **Done** — Concluído

### Criar Project:
1. Aba "Projects" do repositório
2. "New project"
3. Escolher modelo (Kanban ou Table)
4. Adicionar Issues e Pull Requests

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `gh issue list` | Lista Issues |
| `gh issue create` | Cria Issue |
| `gh issue close` | Fecha Issue |
| `gh project` | Gerencia Projects |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Criar Issue](exercicios/01_criar_issue.txt) | Fácil |
| 2 | [Usar labels](exercicios/02_usar_labels.txt) | Fácil |
| 3 | [Milestone](exercicios/03_milestone.txt) | Médio |
| 4 | [Project board](exercicios/04_project_board.txt) | Médio |
| 5 | [Issue template](exercicios/05_issue_template.txt) | Difícil |
| 6 | [Gerenciar sprint](exercicios/06_gerenciar_sprint.txt) | Difícil |

---

**Módulo anterior:** [← Pull Requests](../07_pull_requests/)
**Próximo módulo:** [GitHub Pages →](../09_github_pages/)
