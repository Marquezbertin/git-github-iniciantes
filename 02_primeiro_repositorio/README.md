# Módulo 02 — Primeiro Repositório

## 📖 O que você vai aprender

Criar seu primeiro repositório Git, adicionar arquivos e fazer commits. É aqui que a mágica começa!

---

## 🤔 O que é um repositório Git?

Um repositório (repo) é uma pasta que o Git está monitorando. Dentro dela, cada mudança é registrada como um **commit** — uma "fotografia" do estado do projeto naquele momento.

### Ciclo de vida de um arquivo no Git

```
Arquivo não rastreado (untracked)
       ↓ git add
Arquivo preparado (staged)
       ↓ git commit
Commit realizado (committed)
       ↓ git push (opcional)
Enviado para o remote
```

---

## 🚀 Criando um repositório

### Método 1: Criar do zero
```bash
# Criar uma pasta para o projeto
mkdir meu-primeiro-projeto
cd meu-primeiro-projeto

# Inicializar o repositório Git
git init
# Saída: Initialized empty Git repository in /caminho/.git/
```

### Método 2: Clonar um existente
```bash
git clone https://github.com/usuario/repositorio.git
```

---

## 📝 Comandos fundamentais

### Verificar status
```bash
git status
# Mostra o estado atual do repositório
```

### Adicionar arquivos
```bash
git add arquivo.txt          # Adicionar um arquivo
git add .                    # Adicionar todos os arquivos
git add *.txt                # Adicionar todos os .txt
git add pasta/               # Adicionar uma pasta
```

### Fazer commit
```bash
git commit -m "Minha mensagem"
# -m permite escrever a mensagem direto no comando
```

### Boas práticas para mensagens de commit
```
✅ "Adicionar página de login"
✅ "Corrigir erro no formulário de cadastro"
✅ "Remover código não utilizado"

❌ "asdfgh"
❌ "mudanças"
❌ "update"
```

### Ver histórico de commits
```bash
git log                     # Histórico completo
git log --oneline           # Um commit por linha
git log --oneline --graph   # Com visualização de branch
git log -5                  # Últimos 5 commits
```

### Comparar mudanças
```bash
git diff                    # Mudanças não staged
git diff --staged           # Mudanças staged
```

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git init` | Inicializa um novo repositório |
| `git status` | Mostra o estado do repositório |
| `git add` | Adiciona arquivos à área de staging |
| `git commit` | Registra as mudanças no histórico |
| `git log` | Exibe o histórico de commits |
| `git diff` | Mostra diferenças entre versões |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Criar primeiro repositório](exercicios/01_criar_repositorio.txt) | Fácil |
| 2 | [Primeiro commit](exercicios/02_primeiro_commit.txt) | Fácil |
| 3 | [Múltiplos arquivos](exercicios/03_multiplos_arquivos.txt) | Fácil |
| 4 | [Mensagens de commit](exercicios/04_mensagens_commit.txt) | Médio |
| 5 | [Explorar histórico](exercicios/05_explorar_historico.txt) | Médio |
| 6 | [Desafio completo](exercicios/06_desafio_completo.txt) | Difícil |

---

**Módulo anterior:** [← O que é Git](../01_o_que_e_git/)
**Próximo módulo:** [Trabalhando com Mudanças →](../03_trabalhando_com_mudancas/)
