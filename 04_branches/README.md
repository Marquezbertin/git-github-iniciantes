# Módulo 04 — Branches

## 📖 O que você vai aprender

Criar, alternar e mesclar branches. Entender conflitos e como resolvê-los. Branches são o coração do trabalho colaborativo!

---

## 🤔 O que é uma Branch?

Uma branch é uma **linha de desenvolvimento independente**. Pense como uma "cópia" do projeto onde você pode trabalhar sem afetar o código principal.

```
main:     A --- B --- C --- D
                       \
feature:                E --- F
```

- **main** (ou master): branch principal, sempre estável
- **feature**: branch para desenvolver novas funcionalidades
- **bugfix**: branch para corrigir bugs
- **hotfix**: branch para correções urgentes em produção

---

## 🌿 Comandos de Branch

### Criar branch
```bash
git branch nova-feature        # Cria a branch (sem mudar para ela)
git checkout -b nova-feature   # Cria e já muda para ela
git switch -c nova-feature     # Forma moderna (Git 2.23+)
```

### Listar branches
```bash
git branch               # Lista branches locais
git branch -a            # Lista todas (locais e remotas)
git branch -v            # Lista com último commit
```

### Mudar de branch
```bash
git checkout nome-branch      # Forma antiga
git switch nome-branch        # Forma moderna
```

### Renomear branch
```bash
git branch -m antigo-nome novo-nome
```

### Deletar branch
```bash
git branch -d nome-branch     # Deleta com segurança
git branch -D nome-branch     # Força deleção
```

---

## 🔀 Merge — Mesclar Branches

```bash
# Na branch main, mesclar a feature:
git switch main
git merge nova-feature

# Merge com commit de merge:
git merge --no-ff nova-feature
```

### Tipos de merge

| Tipo | Comando | Quando usar |
|------|---------|-------------|
| Fast-forward | `git merge` | Branch não tem commits próprios |
| Merge commit | `git merge --no-ff` | Cria um commit de merge explícito |
| Squash merge | `git merge --squash` | Juntar vários commits em um só |

---

## ⚠️ Conflitos de Merge

Quando duas branches modificam a mesma linha, o Git não sabe qual usar:

```diff
<<<<<<< HEAD
Código da branch main
=======
Código da branch feature
>>>>>>> nova-feature
```

### Como resolver:
1. Abrir o arquivo e decidir qual versão manter
2. Remover os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Salvar o arquivo
4. `git add arquivo.txt`
5. `git commit`

### Abortar merge em conflito
```bash
git merge --abort
```

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git branch` | Lista ou cria branches |
| `git checkout/switch` | Muda de branch |
| `git merge` | Mescla branches |
| `git branch -d/-D` | Deleta branch |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Criar e listar branches](exercicios/01_criar_listar_branches.txt) | Fácil |
| 2 | [Mudar de branch](exercicios/02_mudar_de_branch.txt) | Fácil |
| 3 | [Merge fast-forward](exercicios/03_merge_fast_forward.txt) | Médio |
| 4 | [Merge com conflito](exercicios/04_merge_com_conflito.txt) | Médio |
| 5 | [Estratégias de merge](exercicios/05_estrategias_merge.txt) | Difícil |
| 6 | [Cenário realista](exercicios/06_cenario_realista.txt) | Difícil |

---

**Módulo anterior:** [← Trabalhando com Mudanças](../03_trabalhando_com_mudancas/)
**Próximo módulo:** [Remotes e Push →](../05_remotes_e_push/)
