# Módulo 03 — Trabalhando com Mudanças

## 📖 O que você vai aprender

Gerenciar mudanças no seu código: comparar versões, pausar trabalho, desfazer alterações e restaurar arquivos.

---

## 🔍 Diff — Comparar Mudanças

O `git diff` mostra exatamente o que mudou entre versões.

```bash
git diff                    # Mudanças não staged vs. último commit
git diff --staged           # Mudanças staged vs. último commit
git diff --stat             # Resumo das mudanças
git diff HEAD               # Todas as mudanças vs. último commit
git diff HEAD~1             # Comparar com o commit anterior
git diff arquivo.txt        # Apenas um arquivo específico
git diff branch1 branch2    # Comparar entre branches
```

### Exemplo de saída
```diff
- Linha antiga do código
+ Nova linha do código
```
- 🔴 `-` = linha removida
- 🟢 `+` = linha adicionada

---

## 📦 Stash — Pausar Trabalho

Quando você precisa mudar de tarefa sem commitar:

```bash
git stash                   # Guarda mudanças e volta ao último commit
git stash list              # Lista todos os stashes guardados
git stash pop               # Restaura o stash mais recente e remove da lista
git stash apply             # Restaura sem remover da lista
git stash drop              # Deleta o stash mais recente
git stash clear             # Deleta todos os stashes
```

### Quando usar stash?
- Está no meio de uma feature e precisa urgentemente corrigir um bug
- Fez mudanças experimentais e quer voltar ao estado anterior
- Precisa trocar de branch rapidamente

---

## ⏪ Checkout e Restore — Desfazer Mudanças

### Para arquivos específicos (Git 2.23+)
```bash
git restore arquivo.txt              # Desfaz mudanças não staged
git restore --staged arquivo.txt    # Remove do staging (mantém mudanças)
git restore --staged --worktree arquivo.txt  # Desfaz tudo no arquivo
```

### Para o último commit (CUIDADO!)
```bash
git reset --soft HEAD~1    # Desfaz commit, mantém staged
git reset HEAD~1           # Desfaz commit e staged
git reset --hard HEAD~1    # Desfaz TUDO (perde mudanças!)
```

### Atalho (compatibilidade)
```bash
git checkout -- arquivo.txt     # Restaurar arquivo (forma antiga)
git checkout .                  # Restaurar todos os arquivos
```

---

## ⚠️ Perigo: Comandos que podem perder trabalho

| Comando | Risco | O que faz |
|---------|-------|-----------|
| `git reset --hard` | 🔴 ALTO | Apaga todas as mudanças não commitadas |
| `git clean -fd` | 🔴 ALTO | Deleta arquivos não rastreados |
| `git stash drop` | 🟡 MÉDIO | Remove um stash permanentemente |

**Regra de ouro:** Se não tem certeza, faça um commit ou stash antes!

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git diff` | Compara mudanças |
| `git stash` | Guarda mudanças temporariamente |
| `git stash pop` | Restaura stash |
| `git restore` | Desfaz mudanças em arquivos |
| `git reset` | Desfaz commits |
| `git clean` | Remove arquivos não rastreados |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Usar git diff](exercicios/01_usar_git_diff.txt) | Fácil |
| 2 | [Usar git stash](exercicios/02_usar_git_stash.txt) | Fácil |
| 3 | [Restaurar arquivos](exercicios/03_restaurar_arquivos.txt) | Médio |
| 4 | [Stash avançado](exercicios/04_stash_avancado.txt) | Médio |
| 5 | [Desfazer commits](exercicios/05_desfazer_commits.txt) | Difícil |
| 6 | [Cenário de emergência](exercicios/06_cenario_emergencia.txt) | Difícil |

---

**Módulo anterior:** [← Primeiro Repositório](../02_primeiro_repositorio/)
**Próximo módulo:** [Branches →](../04_branches/)
