# 🔗 Guia de Configuração - Sincronização com GitHub

Este guia explica como configurar a sincronização automática dos dados da Competição Fitness com o GitHub, permitindo que todos os dispositivos compartilhem os mesmos dados em tempo real.

## 📋 Pré-requisitos

1. Ter o projeto publicado no GitHub Pages
2. Ter acesso ao repositório do projeto
3. Criar um Personal Access Token (PAT) do GitHub

---

## 🔑 Passo 1: Criar Personal Access Token (PAT)

O PAT é necessário para que o site possa atualizar os arquivos JSON no seu repositório.

### Como criar:

1. Acesse: https://github.com/settings/tokens/new
2. Preencha:
   - **Note**: `Fitness Competition Sync`
   - **Expiration**: Escolha a duração (recomendado: 90 dias ou 1 ano)
   - **Scopes**: Marque apenas ✅ **repo** (acesso completo aos repositórios)

3. Clique em **Generate token**
4. ⚠️ **IMPORTANTE**: Copie o token gerado (começa com `ghp_...`) 
   - Você só verá este token UMA VEZ
   - Guarde em local seguro (gerenciador de senhas)

---

## ⚙️ Passo 2: Configurar no Site

1. Abra seu site da competição fitness
2. Role até a seção **💾 Gerenciar Dados**
3. Clique em **⚙️ Configurar GitHub**

### Preencha os campos:

- **Usuário GitHub**: Seu nome de usuário (ex: `joaosilva`)
- **Nome do Repositório**: Nome do repo (ex: `fitness-competition`)
- **Branch**: Normalmente `main` ou `master`
- **Token de Acesso (PAT)**: Cole o token que você criou (`ghp_...`)
- **Sincronização Automática**: ✅ Marque para sync automático após cada evento

4. Clique em **🔍 Testar Conexão** para verificar se está tudo certo
5. Se der ✅, clique em **💾 Salvar Configuração**

---

## 🚀 Como Funciona

### 📥 Armazenamento Local
- Dados são salvos no **localStorage** do navegador (funciona offline)
- Cada dispositivo mantém uma cópia local

### 🔄 Sincronização com GitHub
- **Manual**: Clique em "🔄 Sincronizar Agora" quando quiser
- **Automática**: Se habilitado, sincroniza após cada evento registrado

### 📤 O que é sincronizado
- `data/players.json` - Nomes e pontuações dos jogadores
- `data/history.json` - Histórico completo de eventos

### 🌐 Acesso Compartilhado
1. Você registra academia no celular: +1 ponto
2. Sistema salva no localStorage E no GitHub (se auto-sync ativo)
3. Outra pessoa acessa o site no computador
4. Ao carregar, puxa os dados atualizados do GitHub
5. Ambos veem os mesmos dados! 🎉

---

## 💡 Casos de Uso

### Cenário 1: Dois Competidores
- Leticia acessa no celular dela
- Lidio acessa no computador dele
- Ambos configuram o GitHub com o mesmo repositório
- Cada um registra seus eventos independentemente
- Dados são compartilhados em tempo real via GitHub

### Cenário 2: Múltiplos Dispositivos
- Configure o GitHub em cada dispositivo que você usa
- Acesse de qualquer lugar: celular, tablet, computador
- Dados sempre sincronizados

---

## 🔒 Segurança

### ⚠️ O Token é Sensível!
- **NÃO** compartilhe seu token com ninguém
- **NÃO** publique em redes sociais ou fóruns
- O token dá acesso de escrita ao repositório

### 💾 Onde está armazenado?
- O token fica salvo no **localStorage** do navegador
- Apenas você tem acesso (não vai para o GitHub)
- É salvo criptografado em base64

### 🔐 Dicas de Segurança:
1. Use um token com apenas permissão `repo`
2. Defina uma data de expiração
3. Se o token vazar, revogue imediatamente em: https://github.com/settings/tokens
4. Gere um novo token e reconfigure

---

## 🛠️ Solução de Problemas

### ❌ "Repositório não encontrado"
- Verifique se o nome do usuário e repositório estão corretos
- Certifique-se que o repositório é público ou que o token tem acesso

### ❌ "Token inválido"
- Verifique se copiou o token completo
- Confirme se o token tem permissão `repo`
- Token pode ter expirado - crie um novo

### ❌ "Erro ao sincronizar"
- Verifique sua conexão com internet
- Confirme que o GitHub está acessível
- Veja o console do navegador (F12) para mais detalhes

### 🔄 Conflitos de Dados
- Se dois dispositivos modificarem ao mesmo tempo, o último a sincronizar prevalece
- Recomendamos: apenas um dispositivo por pessoa
- Ou use "Sincronizar Agora" manualmente para controlar

---

## 📊 Status de Sincronização

### Indicadores no site:

- **💾 Local** - Dados apenas no dispositivo, GitHub não configurado
- **🔗 GitHub conectado** - Configurado, sincronização manual
- **🔄 Auto-sync ativo** - Sincronização automática habilitada
- **⏳ Sincronizando...** - Upload em andamento
- **✅ Sincronizado** - Dados atualizados com sucesso
- **❌ Erro ao sincronizar** - Falha na sincronização

---

## 🎯 Melhores Práticas

1. **Configure uma vez**: Salve o token em um local seguro para reconfigurar se necessário
2. **Auto-sync**: Ative para máxima praticidade
3. **Backup manual**: Use "📤 Exportar Dados" periodicamente como backup adicional
4. **Teste primeiro**: Clique em "Testar Conexão" antes de salvar
5. **Monitore**: Fique de olho no indicador de status no topo da página

---

## ❓ FAQ

**P: Preciso configurar em todos os dispositivos?**
R: Sim, cada dispositivo precisa ter seu próprio token configurado.

**P: Posso usar o mesmo token em vários dispositivos?**
R: Sim, mas recomendamos criar tokens diferentes para cada dispositivo por segurança.

**P: E se eu desabilitar o auto-sync?**
R: Você precisará clicar manualmente em "🔄 Sincronizar Agora" quando quiser atualizar.

**P: Os dados sincronizam instantaneamente?**
R: Sim, se o auto-sync estiver ativo. Caso contrário, sincronize manualmente.

**P: Posso voltar a usar só localStorage?**
R: Sim! Basta não configurar o GitHub ou desabilitar nas configurações.

**P: O que acontece se o GitHub estiver fora do ar?**
R: O site continua funcionando normalmente com localStorage. Sincronizará quando voltar.

---

## 🎉 Pronto!

Agora vocês têm um sistema de competição fitness totalmente funcional com sincronização em tempo real via GitHub!

**Boa competição! 💪🏋️🍎**
