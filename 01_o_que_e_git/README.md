# Módulo 01 — O que é Git

## 📖 O que você vai aprender

Neste módulo, você vai entender o que é Git, por que ele existe, como instalar e configurar no seu computador. É a base para todo o resto!

---

## 🤔 O que é Git?

Git é um **sistema de controle de versão distribuído**. Em termos simples:

- É um "salvador de progresso" para o seu código
- Permite voltar a qualquer ponto do seu projeto
- Registra quem mudou o quê, quando e por quê
- Funciona mesmo sem conexão com a internet

### Por que usar Git?

| Sem Git | Com Git |
|---------|---------|
| `projeto_final_v2_FINAL_DO_FINAL.py` | Um histórico organizado de mudanças |
| Copiar e colar trechos de código | Branches para experimentar sem medo |
| Trabalhar um de cada vez | Múltiplas pessoas no mesmo projeto |
| Perder dias de trabalho | Recuperar qualquer versão |

### Como o Git funciona (conceito)

```
Você edita arquivo
       ↓
   git add (prepara)
       ↓
   git commit (salva um snapshot)
       ↓
   Histórico cresce → v1 → v2 → v3 ...
```

---

## ⚙️ Instalação

### Windows
1. Acesse https://git-scm.com/downloads
2. Baixe o instalador para Windows
3. Execute e aceite os padrões (funciona bem para iniciantes)
4. Para verificar: abra o terminal e digite:

```bash
git --version
# Saída esperada: git version 2.x.x
```

### macOS
```bash
# Via Homebrew (recomendado)
brew install git

# Ou instale o Xcode Command Line Tools
xcode-select --install
```

### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install git
```

---

## 🔧 Configuração

Após instalar, configure sua identidade. Essas informações aparecem nos seus commits:

```bash
# Configurar nome (aparece nos commits)
git config --global user.name "Seu Nome"

# Configurar email (deve ser o mesmo do GitHub)
git config --global user.email "seu@email.com"

# Configurar editor padrão (opcional)
git config --global core.editor "code --wait"  # Para VS Code

# Verificar configurações
git config --list
```

### Verificar instalação
```bash
git --version
git config --global user.name
git config --global user.email
```

---

## 📚 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git --version` | Verifica a versão do Git instalada |
| `git config --global user.name` | Define o nome do usuário |
| `git config --global user.email` | Define o email do usuário |
| `git config --list` | Lista todas as configurações |

---

## 🏋️ Exercícios

Após instalar e configurar o Git, realize os exercícios abaixo na ordem:

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Verificar instalação](exercicios/01_verificar_instalacao.txt) | Fácil |
| 2 | [Configurar identidade](exercicios/02_configurar_identidade.txt) | Fácil |
| 3 | [Explorar configurações](exercicios/03_explorar_configuracoes.txt) | Fácil |
| 4 | [Configurar editor](exercicios/04_configurar_editor.txt) | Médio |
| 5 | [Múltiplos perfis](exercicios/05_multiplos_perfis.txt) | Médio |
| 6 | [Diagnóstico completo](exercicios/06_diagnostico_completo.txt) | Difícil |

---

## 💡 Dicas

- Use `git config --global` para configurar para todos os repositórios
- Use `git config` (sem --global) para configurar apenas o repositório atual
- O email do Git deve ser o mesmo que você usa no GitHub
- No Windows, o terminal推荐ado é o **Git Bash** (vem com o Git)

---

**Próximo módulo:** [Primeiro Repositório →](../02_primeiro_repositorio/)
