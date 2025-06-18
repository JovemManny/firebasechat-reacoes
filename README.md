# ✨ Funcionalidade: Reações a Mensagens (firebasechat)

## 📄 Descrição

Esta funcionalidade permite que os usuários reajam a mensagens com emojis dentro do app de chat `firebasechat`. O objetivo é tornar a comunicação mais expressiva e divertida, sem a necessidade de escrever uma nova mensagem para demonstrar uma reação. A reação aparece logo abaixo da mensagem correspondente e é atualizada em tempo real.

---

## 🛠️ Tecnologias Utilizadas

- **React Native (Expo SDK 53)**
- **Firebase Firestore** – armazenamento em tempo real das reações
- **Firebase Auth** – identificação do usuário que reagiu
- **NativeWind** – estilização visual
- **Emoji Picker** – menu de emojis para selecionar reações (biblioteca `emoji-mart-native` ou componente customizado)

---

## 🎯 Objetivos e Benefícios

- Interações rápidas com emojis (👍 😂 ❤️ 🤔 😮 etc).
- Interface semelhante a aplicativos modernos como WhatsApp, Telegram e Messenger.
- UX mais fluida e divertida.
- Feedback emocional sem interromper o fluxo da conversa.

---

## 💡 Impacto no UI/UX

- As mensagens terão uma área para reações visíveis abaixo do texto.
- O usuário poderá segurar/pressionar uma mensagem para abrir um menu de emojis.
- As reações são salvas em tempo real e exibidas para todos que estão no mesmo chat.
- A contagem de reações é exibida (ex: ❤️ x2, 😂 x1).

---

## 🔧 Estrutura no Firestore

Cada mensagem no chat terá uma subcoleção chamada `reactions`.

chats/
{chatId}/
messages/
{messageId}/
reactions/
{userId}: {
emoji: '😂',
timestamp: <firebase.firestore.Timestamp>
}


- Um usuário só pode ter uma reação por mensagem (substitui a anterior).
- O documento tem como ID o `userId`, o que facilita sobrescrever.

---

## ✅ Etapas de Implementação

1. [ ] Criar subcoleção `reactions` nas mensagens no Firestore.
2. [ ] Criar componente visual da bolha de mensagem com espaço para reações.
3. [ ] Criar componente de Emoji Picker (customizado ou com biblioteca).
4. [ ] Ao selecionar um emoji, salvar a reação no Firestore.
5. [ ] Exibir reações abaixo da mensagem, agrupadas por emoji e quantidade.
6. [ ] Usar listener do Firestore para atualizações em tempo real.
7. [ ] Estilizar interface com NativeWind.

---

👨‍💻 Desenvolvedores
Emanuel Nunes
Kaio Rodrigo

---

## ✅ Como usar

1. Copie esse conteúdo e substitua o atual `README.md` do seu repositório GitHub.
2. Faça o commit e push:

git add README.md
git commit -m "docs: adiciona planejamento completo da funcionalidade de reações"
git push origin main

---

## 📁 Estrutura do Projeto

```bash
firebasechat-reacoes/
├── assets/
├── components/
│   └── MessageBubble.tsx
│   └── EmojiReactionPicker.tsx
├── screens/
│   └── ChatScreen.tsx
├── services/
│   └── firebase.ts
├── README.md
└── ...
