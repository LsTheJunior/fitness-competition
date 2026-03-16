# 🏆 Sistema de Competição Fitness

Sistema web simples para acompanhar uma aposta fitness entre duas pessoas, desenvolvido para funcionar 100% no navegador sem necessidade de backend.

> 📚 **Novo aqui?** Veja o [INDEX.md](INDEX.md) para guias organizados por nível de experiência

---

## ✨ Funcionalidades

- ⚙️ **Configuração inicial** - Configure os nomes dos dois jogadores
- 🏋️ **Registro de atividades** - Academia (+1 ponto) e Junk Food (-1 ponto)
- 📊 **Placar em tempo real** - Acompanhe quem está ganhando
- 📈 **Gráfico de evolução** - Visualize o progresso ao longo do tempo
- 📜 **Histórico completo** - Veja todos os eventos registrados
- 💾 **Persistência de dados** - Dados salvos no localStorage do navegador
- � **Sincronização GitHub** - Compartilhe dados automaticamente entre dispositivos via GitHub API
- �🚫 **Validação** - Impede registrar o mesmo evento duas vezes no mesmo dia
- 📱 **Design responsivo** - Funciona perfeitamente em celular e desktop

## 🚀 Como usar localmente

1. Abra o arquivo `index.html` no seu navegador
2. Configure os nomes dos dois jogadores
3. Clique em "Iniciar Competição"
4. Use os botões para registrar eventos diariamente
5. Acompanhe o placar e veja quem está ganhando!

## 📦 Deploy no GitHub Pages

### 🚀 Guia Completo de Deploy

📖 **Veja o guia passo a passo com imagens e explicações detalhadas:**
👉 [DEPLOY_GITHUB_PAGES.md](DEPLOY_GITHUB_PAGES.md)

### ⚡ Resumo Rápido

1. **Criar repositório no GitHub** (público)
2. **Fazer upload dos arquivos** (index.html + pasta data/)
3. **Ativar GitHub Pages** (Settings → Pages → Branch: main)
4. **Aguardar 1-3 minutos** 
5. **Acessar:** `https://seu-usuario.github.io/nome-do-repo/`

✅ **Pronto! Site no ar!**

## 🎮 Como funciona

### Regras
- **Academia**: +1 ponto por dia
- **Junk Food**: -1 ponto por dia
- **Limite**: Um evento de cada tipo por dia, por jogador

### Dados armazenados
Todos os dados são salvos no localStorage do navegador:
- Nomes dos jogadores
- Pontuação total
- Histórico de eventos (data, jogador, tipo, pontos)

### Reset
Para recomeçar a competição:
1. Clique no botão "Resetar Tudo"
2. Confirme a ação
3. Configure novamente os nomes dos jogadores

## 🛠️ Tecnologias utilizadas

- **HTML5** - Estrutura
- **Tailwind CSS** - Estilização (via CDN)
- **Chart.js** - Gráficos (via CDN)
- **Marked.js** - Renderização de markdown (via CDN)
- **JavaScript** - Lógica e interatividade
- **localStorage API** - Persistência de dados local
- **GitHub API** - Sincronização de dados entre dispositivos (opcional)

## 📱 Compatibilidade

Compatível com todos os navegadores modernos:
- ✅ Chrome
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Opera

## 🎨 Cores do sistema

- 🔵 Azul - Jogador 1
- 🟣 Roxo - Jogador 2
- 🟢 Verde - Academia/Pontos positivos
- 🔴 Vermelho - Junk Food/Pontos negativos

## 📄 Estrutura do arquivo

O arquivo `index.html` contém tudo em um único arquivo:
- HTML (estrutura)
- CSS inline (estilos customizados)
- JavaScript (toda a lógica)
- Links CDN (Tailwind CSS e Chart.js)

## 🔒 Privacidade

- Todos os dados ficam salvos apenas no navegador do usuário
- Nenhum dado é enviado para servidores externos
- Para compartilhar dados entre dispositivos, é necessário exportar/importar manualmente

## 🔄 Sincronização com GitHub (NOVO!)

### O que é?
Agora você pode sincronizar automaticamente os dados da competição com seu repositório GitHub, permitindo que **todos os dispositivos compartilhem os mesmos dados em tempo real**!

### Como funciona?
1. Configure um Personal Access Token (PAT) do GitHub
2. Ative a sincronização no site
3. Cada evento registrado é automaticamente salvo no GitHub
4. Qualquer dispositivo que acessar o site verá os dados atualizados

### Vantagens
✅ **Compartilhamento real**: Ambos os competidores veem os mesmos dados  
✅ **Multi-dispositivo**: Acesse de celular, tablet ou computador  
✅ **Backup automático**: Dados salvos no GitHub  
✅ **Tempo real**: Sincronização automática ou manual  
✅ **Offline-first**: Funciona offline, sincroniza quando possível  

### Como configurar?

📖 **Guia completo**: Veja [GITHUB_SYNC_SETUP.md](GITHUB_SYNC_SETUP.md)

**Resumo rápido:**
1. Crie um Personal Access Token em: https://github.com/settings/tokens/new
   - Permissão necessária: ✅ `repo`
2. No site, vá em "💾 Gerenciar Dados"
3. Clique em "⚙️ Configurar GitHub"
4. Preencha: usuário, repositório, branch e token
5. Ative "Sincronização Automática" (opcional)
6. Salve e pronto!

## 💡 Dicas

- Abra o site em diferentes dispositivos para cada jogador acompanhar
- Use o botão de resetar apenas ao final da competição de 2 meses
- O histórico mostra data e hora de cada evento
- O gráfico atualiza automaticamente conforme eventos são registrados
- **NOVO**: Configure a sincronização GitHub para dados compartilhados em tempo real!

## 🎯 Modos de Uso

### Modo 1: Solo (localStorage)
- Dados salvos apenas no navegador
- Ideal para uso individual
- Não requer configuração adicional

### Modo 2: GitHub Sync (Recomendado para competições)
- Dados sincronizados entre todos os dispositivos
- Ideal para competições entre duas pessoas
- Requer configuração do GitHub PAT (5 minutos)
- **Todos veem os mesmos dados em tempo real**

## 📞 Suporte

Para problemas ou dúvidas, verifique se:
- JavaScript está habilitado no navegador
- Você está usando um navegador moderno
- O localStorage não está bloqueado nas configurações

---

Desenvolvido para competições fitness entre amigos! 💪
