# 🚀 Guia Rápido - GitHub Sync

## 📋 Antes de Começar

**Já fez o deploy no GitHub Pages?**
- ✅ Sim → Continue aqui para configurar o sync
- ❌ Não → Veja primeiro: [DEPLOY_GITHUB_PAGES.md](DEPLOY_GITHUB_PAGES.md)

---

## ⚡ Setup Rápido (5 minutos)

### 1️⃣ Criar Token (2 min)
```
1. Acesse: https://github.com/settings/tokens/new
2. Note: "Fitness Competition"
3. Marque: ✅ repo
4. Clique: Generate token
5. Copie o token (ghp_...)
```

### 2️⃣ Configurar no Site (2 min)
```
1. Abra o site da competição
2. Vá em "💾 Gerenciar Dados"
3. Clique "⚙️ Configurar GitHub"
4. Preencha:
   - Usuário: seu-usuario
   - Repo: fitness-competition
   - Branch: main
   - Token: ghp_... (cole aqui)
   - ✅ Sincronização Automática
5. Clique "🔍 Testar Conexão"
6. Se ✅, clique "💾 Salvar"
```

### 3️⃣ Configurar no Outro Dispositivo (1 min)
```
Repita o Passo 2 em cada dispositivo:
- Celular do Jogador 1
- Celular do Jogador 2
- Computador, etc.

⚠️ Use o MESMO token em todos os dispositivos!
```

---

## 🎮 Como Usar

### Registrar Evento
1. Clique no botão correspondente
2. Se auto-sync ativo: sincroniza automaticamente
3. Veja "⏳ Sincronizando..." no topo
4. Quando terminar: "✅ Sincronizado"

### Sincronização Manual
1. Faça alterações offline
2. Quando voltar online, clique "🔄 Sincronizar Agora"
3. Aguarde confirmação

---

## 🔍 Indicadores de Status

| Ícone | Significado |
|-------|-------------|
| 💾 Local | Apenas localStorage, GitHub não configurado |
| 🔗 GitHub conectado | Configurado, sync manual |
| 🔄 Auto-sync ativo | Sincronização automática ativa |
| ⏳ Sincronizando... | Upload em andamento |
| ✅ Sincronizado | Dados atualizados no GitHub |
| ❌ Erro | Falha na sincronização |

---

## 💡 Exemplo de Uso

### Cenário: Leticia vs Lidio

**Segunda-feira, 10h:**
- Leticia abre o celular
- Registra "🏋️ Academia" (+1)
- Auto-sync: dados vão pro GitHub
- Celular mostra: "✅ Sincronizado"

**Segunda-feira, 15h:**
- Lidio abre o computador
- Site carrega dados do GitHub
- Vê que Leticia já registrou academia
- Placar mostra: Leticia 1 x 0 Lidio

**Segunda-feira, 19h:**
- Lidio registra "🏋️ Academia" (+1)
- Auto-sync: dados atualizados no GitHub
- Placar agora: Leticia 1 x 1 Lidio

**Terça-feira, 8h:**
- Leticia abre o app novamente
- Vê que Lidio empatou! 
- Ambos têm 1 ponto

✨ **Tudo sincronizado automaticamente!**

---

## ⚠️ Troubleshooting

### "Token inválido"
- Verifique se copiou o token completo
- Token deve ter permissão `repo`
- Token pode ter expirado

**Solução:**
1. Crie novo token
2. Reconfigure no site

### "Repositório não encontrado"
- Confirme nome do usuário e repo
- Repositório deve existir no GitHub
- Deve ter os arquivos data/players.json e data/history.json

**Solução:**
1. Verifique o nome no GitHub
2. Crie a pasta `data/` se não existir
3. Faça o primeiro upload manual dos JSONs

### Dados não sincronizam
- Verifique conexão com internet
- Confirme que auto-sync está ativo
- Tente sincronização manual

**Solução:**
1. Clique "🔄 Sincronizar Agora"
2. Veja console (F12) para erros
3. Teste conexão novamente

---

## 🎯 Checklist de Configuração

- [ ] Token criado com permissão `repo`
- [ ] Token copiado e guardado
- [ ] Site configurado com usuário/repo corretos
- [ ] Teste de conexão bem-sucedido ✅
- [ ] Auto-sync habilitado (opcional)
- [ ] Configurado em todos os dispositivos
- [ ] Primeiro evento sincronizado com sucesso

---

## 📞 Precisa de Ajuda?

Veja a documentação completa: [GITHUB_SYNC_SETUP.md](GITHUB_SYNC_SETUP.md)

**Problemas comuns e soluções detalhadas estão lá!**

---

🎉 **Boa competição com dados sincronizados!** 💪
