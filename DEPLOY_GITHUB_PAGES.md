# 🚀 Como Fazer Deploy no GitHub Pages

Guia passo a passo para publicar seu site de Competição Fitness no GitHub Pages.

---

## 📋 O que você precisa

- ✅ Conta no GitHub (gratuita)
- ✅ Os arquivos do projeto no seu computador
- ✅ 10 minutos

---

## 🎯 Passo a Passo Completo

### **PASSO 1: Criar Conta no GitHub** (se não tiver)

1. Acesse: https://github.com
2. Clique em **Sign up** (Cadastrar)
3. Preencha: email, senha, nome de usuário
4. Confirme email
5. ✅ Pronto!

---

### **PASSO 2: Criar Novo Repositório**

1. Faça login no GitHub
2. No canto superior direito, clique no **+** (mais)
3. Selecione **New repository** (Novo repositório)

**OU** acesse direto: https://github.com/new

#### Configure o repositório:

```
┌─────────────────────────────────────────┐
│ Repository name:                        │
│ ┌─────────────────────────────────────┐ │
│ │ fitness-competition                 │ │ ← Escolha um nome
│ └─────────────────────────────────────┘ │
│                                         │
│ Description: (opcional)                 │
│ ┌─────────────────────────────────────┐ │
│ │ Competição Fitness entre amigos     │ │
│ └─────────────────────────────────────┘ │
│                                         │
│ ○ Private                               │
│ ● Public  ← IMPORTANTE: Marque Public  │
│                                         │
│ □ Add a README file                     │
│ □ Add .gitignore                        │
│ □ Choose a license                      │
│                                         │
│         [Create repository]             │
└─────────────────────────────────────────┘
```

4. Clique em **Create repository** (Criar repositório)

---

### **PASSO 3: Fazer Upload dos Arquivos**

Você verá uma página com várias opções. Escolha: **uploading an existing file**

**OU** clique em **Add file** → **Upload files**

#### Arraste os arquivos:

```
Arraste para a área ou clique para selecionar:

📄 index.html              ← OBRIGATÓRIO
📄 README.md
📄 FITNESS_README.md
📄 GITHUB_SYNC_SETUP.md
📄 QUICK_START.md
📄 DEPLOY_GITHUB_PAGES.md
📁 data/
   ├── 📄 competition.json
   ├── 📄 history.json
   ├── 📄 players.json
   ├── 📄 posts-index.json
   └── 📁 posts/
       ├── 📄 post1.md
       └── 📄 post2.md
```

**⚠️ IMPORTANTE:**
- Selecione a **pasta data** inteira para manter a estrutura
- Ou arraste todos os arquivos de uma vez

#### Commit:

```
┌─────────────────────────────────────────┐
│ Commit changes                          │
│ ┌─────────────────────────────────────┐ │
│ │ Add files via upload                │ │
│ └─────────────────────────────────────┘ │
│                                         │
│          [Commit changes]               │
└─────────────────────────────────────────┘
```

Clique em **Commit changes**

---

### **PASSO 4: Ativar GitHub Pages**

1. No seu repositório, clique em **Settings** (Configurações)
   - Ícone de engrenagem no menu superior

2. No menu lateral esquerdo, role até encontrar **Pages**
   - Está na seção "Code and automation"

3. Configure o GitHub Pages:

```
┌─────────────────────────────────────────┐
│ GitHub Pages                            │
│                                         │
│ Source                                  │
│ ┌─────────────────────────────────────┐ │
│ │ Deploy from a branch            ▼   │ │
│ └─────────────────────────────────────┘ │
│                                         │
│ Branch                                  │
│ ┌──────────────┐  ┌──────────────────┐ │
│ │ main      ▼  │  │ / (root)      ▼  │ │
│ └──────────────┘  └──────────────────┘ │
│                                         │
│            [Save]                       │
└─────────────────────────────────────────┘
```

4. Selecione:
   - **Branch:** `main` (ou `master`)
   - **Folder:** `/ (root)`

5. Clique em **Save**

---

### **PASSO 5: Aguardar Deploy** ⏳

Aguarde **1-3 minutos** enquanto o GitHub processa seu site.

Você verá uma mensagem:
```
✅ Your site is live at https://seu-usuario.github.io/fitness-competition/
```

---

### **PASSO 6: Acessar Seu Site** 🎉

Seu site estará disponível em:

```
https://SEU-USUARIO.github.io/NOME-DO-REPO/
```

**Exemplo:**
- Usuário: `lidio-junior`
- Repositório: `fitness-competition`
- Site: `https://lidio-junior.github.io/fitness-competition/`

---

## 🔄 Como Atualizar o Site

### Método 1: Via Interface Web (Simples)

1. Acesse seu repositório no GitHub
2. Navegue até o arquivo que quer editar
3. Clique no ícone do lápis ✏️ (Edit)
4. Faça as alterações
5. Role até o final
6. Clique em **Commit changes**
7. Aguarde 1-2 minutos
8. ✅ Site atualizado!

### Método 2: Upload de Novo Arquivo

1. No repositório, clique em **Add file** → **Upload files**
2. Arraste o arquivo atualizado
3. Marque **Replace the file with the same name**
4. Clique em **Commit changes**
5. Aguarde 1-2 minutos
6. ✅ Arquivo atualizado!

### Método 3: GitHub Sync Automático ⭐

Se você configurou a sincronização GitHub (veja GITHUB_SYNC_SETUP.md):
- Todos os dados são atualizados automaticamente!
- Não precisa fazer upload manual
- Funciona em tempo real

---

## 🎯 Checklist Completo

- [ ] Conta criada no GitHub
- [ ] Repositório criado (público)
- [ ] Todos os arquivos enviados
- [ ] Pasta `data/` com estrutura completa
- [ ] GitHub Pages ativado (Settings → Pages)
- [ ] Branch `main` e folder `/root` selecionados
- [ ] Aguardado 1-3 minutos
- [ ] Site acessível via URL
- [ ] Testado no navegador
- [ ] Configurado GitHub Sync (opcional)

---

## ⚠️ Problemas Comuns

### ❌ "404 - Page not found"

**Causas:**
- Site ainda não está pronto (aguarde 3-5 minutos)
- Repositório está privado (mude para público)
- GitHub Pages não foi ativado

**Solução:**
1. Vá em Settings → Pages
2. Confirme que está configurado
3. Aguarde publicação

### ❌ "index.html não carrega"

**Causa:** Arquivo não está na raiz do repositório

**Solução:**
1. Verifique que `index.html` está na raiz (não dentro de pasta)
2. Se estiver em pasta, mova para a raiz

### ❌ "data/players.json não encontrado"

**Causa:** Estrutura de pastas incorreta

**Solução:**
1. Verifique que existe a pasta `data/`
2. Dentro dela devem estar os arquivos JSON
3. Se não estiver, crie a pasta e faça upload novamente

### ❌ "Site não atualiza"

**Causa:** Cache do navegador

**Solução:**
1. Pressione `Ctrl + Shift + R` (Windows/Linux)
2. Ou `Cmd + Shift + R` (Mac)
3. Ou limpe o cache do navegador

---

## 🌐 Estrutura Final no GitHub

Seu repositório deve ficar assim:

```
seu-usuario/fitness-competition/
│
├── 📄 index.html                    ← Página principal
├── 📄 README.md
├── 📄 FITNESS_README.md
├── 📄 GITHUB_SYNC_SETUP.md
├── 📄 QUICK_START.md
├── 📄 DEPLOY_GITHUB_PAGES.md
│
└── 📁 data/
    ├── 📄 competition.json
    ├── 📄 history.json
    ├── 📄 players.json
    ├── 📄 posts-index.json
    │
    └── 📁 posts/
        ├── 📄 post1.md
        └── 📄 post2.md
```

---

## 🎊 Próximos Passos

Após o deploy bem-sucedido:

1. ✅ **Compartilhe a URL** com o outro competidor
2. ✅ **Configure GitHub Sync** (veja GITHUB_SYNC_SETUP.md)
3. ✅ **Teste registrar eventos**
4. ✅ **Comece a competição!** 💪

---

## 💡 Dicas Pro

### Personalizar URL (Opcional)

Se você quer uma URL mais curta, pode:
1. Criar repositório com nome: `seu-usuario.github.io`
2. URL será apenas: `https://seu-usuario.github.io/`

### Domínio Customizado (Avançado)

Você pode usar seu próprio domínio:
1. Compre um domínio (ex: fitness-competition.com)
2. Em Settings → Pages → Custom domain
3. Configure DNS do domínio
4. Adicione o domínio

### Proteção com Senha (Não Disponível)

⚠️ GitHub Pages não suporta proteção com senha nativamente.
Para isso, seria necessário:
- Usar serviço externo (Netlify, Vercel)
- Ou implementar autenticação via Firebase

---

## 📱 Acesso Mobile

Seu site funcionará perfeitamente em:
- ✅ iPhone/iPad (Safari, Chrome)
- ✅ Android (Chrome, Firefox, Samsung Internet)
- ✅ Tablets
- ✅ Desktop

O design é totalmente responsivo!

---

## 🎉 Pronto!

Agora você tem um site de competição fitness profissional e totalmente funcional no GitHub Pages!

**URL de exemplo:**
```
https://lidio-junior.github.io/fitness-competition/
```

**Compartilhe com seus amigos e comece a competição! 🏆**

---

**Dúvidas?** Veja também:
- [README.md](README.md) - Visão geral do projeto
- [GITHUB_SYNC_SETUP.md](GITHUB_SYNC_SETUP.md) - Configurar sincronização
- [QUICK_START.md](QUICK_START.md) - Início rápido

**Boa sorte na competição! 💪🏋️**
