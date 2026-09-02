# Módulo 05 — Remotes e Push

## 📖 O que você vai aprender

Conectar repositórios locais ao GitHub, enviar e receber código. É aqui que o Git se torna poderoso!

---

## 🤔 O que é um Remote?

Um remote é uma versão do seu repositório que está em outro lugar (geralmente no GitHub). O remote padrão se chama **origin**.

```
Seu computador (local)          GitHub (remote/origin)
┌──────────────┐               ┌──────────────┐
│  Repositório │  ── push ──▶  │  Repositório │
│    local     │  ◀── pull ──  │    remoto    │
└──────────────┘               └──────────────┘
```

---

## 🔗 Comandos de Remote

### Ver remotes
```bash
git remote                    # Lista remotes
git remote -v                 # Lista com URLs
```

### Adicionar remote
```bash
git remote add origin https://github.com/usuario/repo.git
```

### Mudar URL do remote
```bash
git remote set-url origin https://github.com/usuario/novo-repo.git
```

### Remover remote
```bash
git remote remove origin
```

---

## 📤 Push — Enviar código

```bash
git push origin main               # Enviar main para origin
git push -u origin main            # Enviar e fazer tracking
git push origin feature:feature    # Enviar branch específica
git push --force                   # Forçar push (PERIGOSO!)
```

### Tracking (-u)
```bash
git push -u origin main
# Depois disso, pode usar apenas:
git push
```

---

## 📥 Pull — Receber código

```bash
git pull origin main               # Baixar e mesclar
git pull --rebase origin main      # Baixar e rebasear
```

### Pull vs. Fetch
```bash
git pull = git fetch + git merge
git fetch origin                  # Baixa sem mesclar
git diff main origin/main         # Compara com o remote
git merge origin/main             # Mescla manualmente
```

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git remote add` | Adiciona um remote |
| `git remote -v` | Lista remotes |
| `git push` | Envia código para o remote |
| `git pull` | Baixa e mescla código do remote |
| `git fetch` | Baixa código sem mesclar |
| `git clone` | Copia um repositório remoto |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Configurar remote](exercicios/01_configurar_remote.txt) | Fácil |
| 2 | [Primeiro push](exercicios/02_primeiro_push.txt) | Fácil |
| 3 | [Pull e fetch](exercicios/03_pull_e_fetch.txt) | Médio |
| 4 | [Trabalhar com branches remotas](exercicios/04_branches_remotas.txt) | Médio |
| 5 | [Rebase com remote](exercicios/05_rebase_remote.txt) | Difícil |
| 6 | [Fluxo completo](exercicios/06_fluxo_completo.txt) | Difícil |

---

**Módulo anterior:** [← Branches](../04_branches/)
**Próximo módulo:** [GitHub →](../06_github/)
