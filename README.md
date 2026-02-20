# CCB Caieiras – Sistema de Fichas 📋✝️

App PWA para cadastro de fichas de apresentação para cargos e reuniões familiares.

---

## 📱 Como usar no Android

### Opção 1 – Firebase Hosting (Recomendado, gratuito)
1. Acesse [console.firebase.google.com](https://console.firebase.google.com)
2. Crie um projeto (ex: `ccb-caieiras`)
3. Vá em **Hosting** → Ative
4. Instale o Firebase CLI: `npm install -g firebase-tools`
5. Execute: `firebase login && firebase init hosting`
6. Copie os arquivos desta pasta para a pasta `public`
7. Execute: `firebase deploy`
8. Acesse a URL gerada no Android Chrome → menu "Adicionar à tela inicial"

### Opção 2 – GitHub Pages (também gratuito)
1. Crie repositório no GitHub
2. Faça upload de todos os arquivos
3. Vá em Settings → Pages → Source: main branch
4. Acesse a URL no Android Chrome → "Adicionar à tela inicial"

---

## 🔥 Configurar sincronização Firebase

Após publicar o app:
1. No Firebase Console, ative:
   - **Authentication** (Email/Password)
   - **Firestore Database**
   - **Storage**
2. Em Project Settings → General → Your apps → Add web app
3. Copie o objeto `firebaseConfig`
4. No app, vá na aba **⚙️ Config**
5. Preencha cada campo com os valores do seu projeto
6. Toque em **Salvar e Reconectar**

---

## 📋 Campos do formulário
- Data da reunião ministerial + aprovação (Sim/Não/Pendente)
- Tipo: Inclusão / Exclusão
- Localidade
- Cargos/Funções (10 checkboxes)
- Nome, Idade, Tempo de Batismo
- Endereço, Telefone, Referências
- Observações
- 📷 Foto da ficha original (câmera ou galeria)

---

## 💾 Armazenamento
- **Sem Firebase**: dados salvos localmente no dispositivo
- **Com Firebase**: sincronização na nuvem, acesso em múltiplos dispositivos

---

## 📁 Arquivos
```
index.html    ← App principal
manifest.json ← Configuração PWA
sw.js         ← Service Worker (offline)
README.md     ← Este arquivo
```
