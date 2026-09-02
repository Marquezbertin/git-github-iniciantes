# Módulo 09 — GitHub Pages

## 📖 O que você vai aprender

Criar sites estáticos gratuitamente usando GitHub Pages. Deploy automático a cada push!

---

## 🌐 O que é GitHub Pages?

GitHub Pages é um serviço gratuito que hospeda sites estáticos diretamente do repositório. Perfeito para:

- Portfólios pessoais
- Documentação de projetos
- Blogs
- Páginas de apresentação

### Tipos de site:
- **User site**: `https://seu-usuario.github.io`
- **Project site**: `https://seu-usuario.github.io/nome-repo`
- **Custom domain**: `https://seudominio.com`

---

## 🚀 Criar Site com GitHub Pages

### Método 1: Branch main
1. Crie um arquivo `index.html` na branch main
2. Vá em Settings → Pages
3. Source: "Deploy from a branch"
4. Branch: main, pasta: / (root)
5. Salve

### Método 2: GitHub Actions (recomendado)
1. Vá em Settings → Pages
2. Source: "GitHub Actions"
3. Crie um workflow na pasta `.github/workflows/`

### Método 3: Usar Jekyll
1. Crie arquivos Markdown
2. O GitHub converte automaticamente

---

## 📁 Estrutura de um site

```
meu-site/
├── index.html          # Página principal
├── styles.css          # Estilos
├── script.js           # JavaScript
├── images/             # Imagens
│   ├── logo.png
│   └── foto.jpg
└── pages/              # Páginas extras
    ├── sobre.html
    └── contato.html
```

---

## ⚙️ Configurações

### Configurar Source
1. Settings → Pages
2. Escolha a branch e pasta
3. Salve

### Ver status
Após alguns minutos, seu site estará em:
`https://seu-usuario.github.io/nome-repo`

### Custom Domain
1. Compre um domínio
2. Adicione arquivo `CNAME` com seu domínio
3. Configure DNS no provedor

---

## 📋 Comandos deste módulo

| Comando | Função |
|---------|--------|
| `git checkout -b gh-pages` | Cria branch de deploy |
| `git push origin gh-pages` | Publica na branch gh-pages |

---

## 🏋️ Exercícios

| # | Exercício | Dificuldade |
|---|-----------|-------------|
| 1 | [Criar site básico](exercicios/01_criar_site_basico.txt) | Fácil |
| 2 | [Ativar GitHub Pages](exercicios/02_ativar_github_pages.txt) | Fácil |
| 3 | [Site multi-página](exercicios/03_site_multipagina.txt) | Médio |
| 4 | [Template responsivo](exercicios/04_template_responsivo.txt) | Médio |
| 5 | [Deploy com Actions](exercicios/05_deploy_actions.txt) | Difícil |
| 6 | [Custom domain](exercicios/06_custom_domain.txt) | Difícil |

---

**Módulo anterior:** [← Issues e Projetos](../08_issues_e_projetos/)
**Próximo módulo:** [Git Avançado →](../10_git_avancado/)
