# Módulo 07 — Pull Requests

## 📖 O que você vai aprender

Contribuir para repositórios usando fork, branches, Pull Requests e Code Review.

---

## 🤔 O que é um Pull Request?

Um Pull Request (PR) é uma proposta de mudança em um repositório. É assim que equipes colaboram:

```
Seu fork     Branch feature    Pull Request    Repositório Original
   │               │                │                    │
   ├── fork ───────┤                │                    │
   │               ├── commit ──────┤                    │
   │               │                ├── review + merge ──┤
   │               │                │                    │
```

### Fluxo completo:
1. **Fork** — Copie o repositório para sua conta
2. **Clone** — Baixe seu fork localmente
3. **Branch** — Crie uma branch para sua mudança
4. **Commit** — Faça suas alterações
5. **Push** — Envie para seu fork
6. **Pull Request** — Proponha a mudança no repositório original
7. **Review** — Outros revisam seu código
8. **Merge** — Sua mudança é aceita e integrada

---

## 🍴 Fork

```bash
# Pelo GitHub: clique em "Fork"
# Pelo terminal:
gh repo fork USUARIO/repositorio --clone
```

---

## 🔀 Criar Pull Request

### Pelo GitHub:
1. Vá ao repositório original
2. Clique "New Pull Request"
3. Selecione: base (main) ← compare (sua branch)
4. Título e descrição claros
5. "Create Pull Request"

### Boas práticas de PR:
- Título claro e descritivo
- Descreva o que mudou e por quê
- Link para Issue relacionada
- Adicione screenshots se aplicável
- Peça review de colegas

---

## 👀 Code Review

Ao revisar um PR:
1. Leia o código linha por linha
2. Deixe comentários constructivos
3. Aprove, solicite mudanças, ou comente
4. Use emojis para indicar: 👍 (aprovado), 💡 (sugestão), ⚠️ (atenção)

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `gh repo fork` | Faz fork de um repositório |
| `gh pr create` | Cria um Pull Request |
| `gh pr list` | Lista PRs abertos |
| `gh pr merge` | Mescla um PR |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Fork e clone](exercicios/01_fork_e_clone.txt) | Fácil |
| 2 | [Criar PR](exercicios/02_criar_pr.txt) | Fácil |
| 3 | [Descrição de PR](exercicios/03_descricao_pr.txt) | Médio |
| 4 | [Code review](exercicios/04_code_review.txt) | Médio |
| 5 | [PR com conflito](exercicios/05_pr_com_conflito.txt) | Difícil |
| 6 | [Fluxo completo de contribuição](exercicios/06_fluxo_contribuicao.txt) | Difícil |

---

**Módulo anterior:** [← GitHub](../06_github/)
**Próximo módulo:** [Issues e Projetos →](../08_issues_e_projetos/)
