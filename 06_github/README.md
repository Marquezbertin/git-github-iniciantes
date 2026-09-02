# Módulo 06 — GitHub

## 📖 O que você vai aprender

Criar conta no GitHub, configurar repositórios, criar READMEs profissionais e configurar SSH keys.

---

## 🤔 O que é o GitHub?

GitHub é uma plataforma de hospedagem de código-fonte que usa o Git. É onde:

- Você armazena seus repositórios na nuvem
- Colabora com outras pessoas
- Gerencia projetos com Issues e Projects
- Compartilha código open source

### GitHub vs. Git

| Git | GitHub |
|-----|--------|
| Ferramenta local | Plataforma online |
| Funciona no terminal | Interface web |
| Controle de versão | Colaboração |
| Não precisa de conta | Precisa de conta |

---

## 👤 Criar Conta no GitHub

1. Acesse https://github.com
2. Clique em "Sign up"
3. Preencha: email, senha, nome de usuário
4. Verifique o email
5. Pronto! Sua conta está criada

---

## 📁 Criar Repositório

### Pela web:
1. Clique no ícone "+" (canto superior direito)
2. "New repository"
3. Preencha:
   - Nome: `meu-projeto`
   - Descrição: `Descrição do projeto`
   - Público ou Privado
   - Adicionar README (recomendado!)
4. "Create repository"

### Pelo terminal:
```bash
# Criar repo vazio no GitHub (precisa do GitHub CLI)
gh repo create meu-projeto --public

# Ou criar local e enviar
mkdir meu-projeto && cd meu-projeto
git init
echo "# Meu Projeto" > README.md
git add . && git commit -m "Commit inicial"
git remote add origin https://github.com/USUARIO/meu-projeto.git
git push -u origin main
```

---

## 📝 Criar README Profissional

```markdown
# Nome do Projeto

![Badge](https://img.shields.io/badge/status-ativo-green)

> Breve descrição do projeto

## Sobre
O que o projeto faz

## Funcionalidades
- Funcionalidade 1
- Funcionalidade 2

## Como Usar
1. Clone o repositório
2. Instale as dependências
3. Execute o projeto

## Tecnologias
- Linguagem X
- Framework Y

## Contribuindo
Consulte CONTRIBUTING.md

## Licença
MIT License
```

---

## 🔐 SSH Keys

SSH keys permitem autenticar sem digitar senha toda vez.

### Gerar chave SSH
```bash
ssh-keygen -t ed25519 -C "seu@email.com"
# Pressione Enter para aceitar o padrão
```

### Adicionar ao agente SSH
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### Copiar chave pública
```bash
# Linux
cat ~/.ssh/id_ed25519.pub | clip

# macOS
pbcopy < ~/.ssh/id_ed25519.pub

# Windows (PowerShell)
Get-Content ~/.ssh/id_ed25519.pub | Set-Clipboard
```

### Adicionar no GitHub
1. Acesse https://github.com/settings/keys
2. "New SSH key"
3. Cole a chave
4. "Add SSH key"

### Testar conexão
```bash
ssh -T git@github.com
# Saída: "Hi usuario! You've successfully authenticated..."
```

### Usar SSH no repositório
```bash
git remote set-url origin git@github.com:USUARIO/repo.git
```

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `gh repo create` | Cria repositório no GitHub |
| `ssh-keygen` | Gera chaves SSH |
| `ssh -T` | Testa conexão SSH |
| `git remote set-url` | Muda URL do remote |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Criar repositório](exercicios/01_criar_repositorio_github.txt) | Fácil |
| 2 | [Escrever README](exercicios/02_escrever_readme.txt) | Fácil |
| 3 | [Configurar SSH](exercicios/03_configurar_ssh.txt) | Médio |
| 4 | [README avançado](exercicios/04_readme_avancado.txt) | Médio |
| 5 | [Perfil do GitHub](exercicios/05_perfil_github.txt) | Difícil |
| 6 | [Organização GitHub](exercicios/06_organizacao_github.txt) | Difícil |

---

**Módulo anterior:** [← Remotes e Push](../05_remotes_e_push/)
**Próximo módulo:** [Pull Requests →](../07_pull_requests/)
