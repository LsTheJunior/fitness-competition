# 🏆 Competição Fitness - Guia de Uso

## 📁 Estrutura de Arquivos Criada

```
C:\Users\Lidio-Junior\
├── index.html              # Aplicação principal (atualizada)
├── data/
│   ├── players.json        # Dados dos jogadores
│   ├── competition.json    # Configurações da competição
│   ├── history.json        # Histórico de eventos
│   ├── posts-index.json    # Índice de posts do blog
│   └── posts/
│       ├── post1.md        # Post: Bem-vindo
│       └── post2.md        # Post: Dicas de Motivação
└── FITNESS_README.md       # Este guia
```

## 🚀 Como Testar Localmente

1. **Abra o arquivo**: Clique duas vezes em `index.html`
2. **Configure a competição**: Insira os nomes dos jogadores
3. **Experimente as funcionalidades**:
   - Registre idas à academia
   - Registre junk food
   - Veja o histórico e gráficos
   - Clique em "Mostrar/Ocultar" no Blog para ver os posts

## 📊 Gerenciamento de Dados

### Botões Disponíveis

1. **📥 Carregar do JSON**: Importa dados de `data/players.json` e `data/history.json`
2. **💾 Salvar no JSON**: Mostra os dados atuais para copiar
3. **📤 Exportar Dados**: Baixa arquivos JSON para substituir em `data/`

### Fluxo de Trabalho

```
[Usuário usa app] → [Dados no localStorage]
                           ↓
                  [Exportar Dados]
                           ↓
           [Baixa players.json + history.json]
                           ↓
         [Substitui arquivos em data/]
                           ↓
              [Faz commit no GitHub]
                           ↓
           [GitHub Pages atualiza site]
```

## 🌐 Deploy no GitHub Pages

### Passo 1: Criar Repositório

```bash
# Na pasta C:\Users\Lidio-Junior\
git init
git add .
git commit -m "Initial commit - Fitness Competition"
```

### Passo 2: Push para GitHub

```bash
# Crie um repositório no GitHub first
git remote add origin https://github.com/seu-usuario/fitness-competition.git
git branch -M main
git push -u origin main
```

### Passo 3: Ativar GitHub Pages

1. Vá para o repositório no GitHub
2. Clique em **Settings**
3. No menu lateral, clique em **Pages**
4. Em "Source", selecione **main branch**
5. Clique em **Save**
6. Aguarde alguns minutos
7. Acesse: `https://seu-usuario.github.io/fitness-competition/`

## 📝 Editando Posts do Blog

### Criar Novo Post

1. Crie arquivo em `data/posts/post3.md`:
   ```markdown
   # Meu Novo Post
   
   Conteúdo aqui com **negrito** e *itálico*.
   
   ## Seções
   
   - Item 1
   - Item 2
   ```

2. Adicione ao `data/posts-index.json`:
   ```json
   [
     {
       "id": 3,
       "title": "Meu Novo Post",
       "date": "2026-03-17",
       "file": "post3.md",
       "author": "Seu Nome"
     }
   ]
   ```

3. Faça commit:
   ```bash
   git add data/posts/
   git commit -m "Adicionar novo post"
   git push
   ```

## 🔄 Atualizar Dados da Competição

### Método Rápido (Recomendado)

1. Use a aplicação normalmente
2. Quando quiser salvar:
   - Clique em "📤 Exportar Dados"
   - Dois arquivos serão baixados
3. Substitua os arquivos em `C:\Users\Lidio-Junior\data\`
4. Commit via git:
   ```bash
   git add data/players.json data/history.json
   git commit -m "Update competition data"
   git push
   ```

### Método Manual

1. Abra `data/players.json`
2. Edite manualmente os dados
3. Salve o arquivo
4. Faça commit

## 📊 Estrutura dos Dados

### players.json
Armazena informações dos jogadores:
- `name`: Nome do jogador
- `score`: Pontuação total
- `gymCount`: Número de vezes na academia
- `junkCount`: Número de vezes comendo besteira

### history.json
Lista de todos os eventos:
- `playerId`: 1 ou 2
- `type`: "gym" ou "junk"
- `points`: 1 ou -1
- `date`: Data do evento
- `timestamp`: Data/hora completa

### competition.json
Configurações gerais (não utilizado atualmente pela UI)

## ⚠️ Importante

### Limitações do GitHub Pages

- ❌ **Não permite escrita direta**: Usuários não podem salvar dados automaticamente
- ✅ **Permite leitura**: Todos podem ver os dados atualizados
- ⏱️ **Delay de 1-5 minutos**: Tempo para o site atualizar após commit

### Solução

- Use **localStorage** para dados locais do usuário
- Use **arquivos JSON** para compartilhar dados entre usuários
- **Export/Import** manual para sincronização

## 💡 Casos de Uso

### Caso 1: Competição Solo
- Use apenas localStorage
- Não precisa de GitHub Pages
- Dados ficam no navegador

### Caso 2: Competição com Amigos
- Cada um usa seu próprio navegador
- Um "administrador" faz export periódico
- Todos carregam dados atualizados do GitHub Pages

### Caso 3: Leaderboard Público
- Mantenha JSON atualizado no GitHub
- Compartilhe link do GitHub Pages
- Visitantes veem ranking em tempo real (com delay)

## 🛠️ Troubleshooting

### "Erro ao carregar JSON"
- Verifique se os arquivos existem em `data/`
- Verifique se o JSON está válido (use JSONLint.com)
- Limpe o cache do navegador

### "Dados não atualizaram"
- Aguarde 5 minutos após o commit
- Force refresh: Ctrl + Shift + R
- Verifique se o commit foi para a branch correta

### "Blog não carrega"
- Verifique se `posts-index.json` está válido
- Verifique se os arquivos .md existem
- Veja o console do navegador (F12) para erros

## 📞 Próximos Passos

1. ✅ Testar aplicação localmente
2. ✅ Fazer primeiro deploy no GitHub Pages
3. ⬜ Adicionar mais posts ao blog
4. ⬜ Personalizar cores e estilos
5. ⬜ Configurar automação com GitHub Actions (avançado)

---

**Divirta-se com sua competição! 💪🏆**
