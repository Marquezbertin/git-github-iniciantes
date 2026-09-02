# Módulo 10 — Git Avançado

## 📖 O que você vai aprender

Técnicas avançadas do Git: rebase interativo, cherry-pick, tags, bisect e mais.

---

## 🔄 Rebase

Rebase reaplica seus commits "em cima" de outro branch, criando um histórico linear.

```bash
git checkout feature
git rebase main           # Reaplica feature sobre main
git rebase -i HEAD~3      # Rebase interativo (últimos 3 commits)
```

### Rebase interativo — opções:
| Comando | Significado |
|---------|-------------|
| `pick` | Manter o commit |
| `reword` | Manter e editar mensagem |
| `edit` | Parar para editar o commit |
| `squash` | Juntar com o commit anterior |
| `fixup` | Juntar sem mensagem |
| `drop` | Remover o commit |

### ⚠️ Regra de ouro:
NUNCA faça rebase em branches que estão sendo compartilhadas!

---

## 🍒 Cherry-pick

Seleciona commits específicos de outro branch:

```bash
git cherry-pick abc1234           # Um commit
git cherry-pick abc1234 def5678  # Múltiplos
git cherry-pick --no-commit abc1234  # Sem commitar (só staging)
```

### Quando usar?
- Correção urgente precisa ir para outra branch
- Quer trazer apenas um commit específico

---

## 🏷️ Tags

Tags marcam pontos específicos no histórico (geralmente versões):

```bash
git tag v1.0                    # Tag leve
git tag -a v1.0 -m "Versão 1.0"  # Tag anotada
git tag -a v1.0 abc1234          # Tag em commit específico
git tag                          # Lista tags
git push origin v1.0             # Envia tag
git push origin --tags           # Envia todas
```

### Tipos:
- **Leve**: apenas um ponteiro para o commit
- **Anotada**: contém mensagem, autor e data

---

## 🔍 Bisect

Usa busca binária para encontrar o commit que introduziu um bug:

```bash
git bisect start
git bisect bad                  # Commit atual tem bug
git bisect good v1.0            # Esta versão não tinha bug

# O Git testa commits intermediários
# Para cada commit:
git bisect good    # se funciona
git bisect bad     # se tem bug

# Quando encontrar:
git bisect reset
```

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git rebase` | Reaplica commits sobre outro branch |
| `git rebase -i` | Rebase interativo |
| `git cherry-pick` | Seleciona commits específicos |
| `git tag` | Cria/mostra tags |
| `git bisect` | Busca binária por bugs |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Rebase básico](exercicios/01_rebase_basico.txt) | Médio |
| 2 | [Rebase interativo](exercicios/02_rebase_interativo.txt) | Médio |
| 3 | [Cherry-pick](exercicios/03_cherry_pick.txt) | Médio |
| 4 | [Tags](exercicios/04_tags.txt) | Médio |
| 5 | [Bisect](exercicios/05_bisect.txt) | Difícil |
| 6 | [Combinação avançada](exercicios/06_combinacao_avancada.txt) | Difícil |

---

**Módulo anterior:** [← GitHub Pages](../09_github_pages/)
**Próximo módulo:** [Trabalho em Equipe →](../11_trabalho_em_equipe/)
