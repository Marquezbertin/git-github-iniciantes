# Módulo 11 — Trabalho em Equipe

## 📖 O que você vai aprender

Fluxos de trabalho em equipe, estratégias de branching, CODEOWNERS e boas práticas de colaboração.

---

## 🤝 Por que trabalhar em equipe?

Projetos reais têm múltiplos desenvolvedores. O Git facilita:

- Muitas pessoas no mesmo código
- Revisão antes de integrar
- Histórico de quem fez o quê
- Experimentação sem risco

---

## 🌿 Estratégias de Branch

### Git Flow
```
main ─────────────────────────────▶
  │                                 
  └── develop ────────────────────▶
        │         │         │
        └─ feat1 ─┘  feat2 ─┘
              │
              └── release ──▶ main
```

| Branch | Quando criar | Quando mergear |
|--------|-------------|----------------|
| main | Sempre existe | Deploy |
| develop | Projeto inicia | Integra features |
| feature/* | Nova func | develop |
| release/* | Preparar versão | main + develop |
| hotfix/* | Bug urgente | main + develop |

### GitHub Flow (simplificado)
```
main ──────────────────────▶
  │        │         │
  └─ feat1 ┘  feat2 ─┘
```

- Cria branch da main
- Faz mudanças
- Abre PR
- Após review, merge na main

### Trunk-Based (avançado)
```
main ────────▶
  │  │  │  │
  └──┘  └──┘
```
- Todo mundo trabalha na main
- Features são pequenas e frequentes

---

## 👥 CODEOWNERS

Arquivo `.github/CODEOWNERS` define quem revisa o quê:

```
# Donos do projeto
* @dono-do-projeto

# Documentação
docs/ @equipe-docs

# Backend
src/api/ @equipe-backend

# Frontend
src/ui/ @equipe-frontend
```

---

## 📏 Boas Práticas

1. **Branch por feature** — nunca trabalhe direto na main
2. **Commits pequenos** — commits atômicos e descritivos
3. **PRs descritos** — inclua contexto, screenshots, testes
4. **Reviews rápidos** — responda em até 24h
5. **Rebase antes de merge** — mantenha histórico limpo
6. **Delete branches após merge** — limpe o repositório

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git flow init` | Inicializa Git Flow |
| `git flow feature start` | Inicia feature |
| `git flow feature finish` | Finaliza feature |
| `gh pr review` | Review via CLI |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Git Flow básico](exercicios/01_git_flow_basico.txt) | Médio |
| 2 | [GitHub Flow](exercicios/02_github_flow.txt) | Médio |
| 3 | [CODEOWNERS](exercicios/03_codeowners.txt) | Médio |
| 4 | [Review de PR](exercicios/04_review_pr.txt) | Médio |
| 5 | [Conflito em equipe](exercicios/05_conflito_equipe.txt) | Difícil |
| 6 | [Workflow completo](exercicios/06_workflow_completo.txt) | Difícil |

---

**Módulo anterior:** [← Git Avançado](../10_git_avancado/)
**Próximo módulo:** [CI/CD Básico →](../12_ci_cd_basico/)
