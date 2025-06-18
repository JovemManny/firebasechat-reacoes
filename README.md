# ✨ Funcionalidade: Reações a Mensagens (firebasechat)

## 📄 Descrição

Permite que os usuários reajam a mensagens com emojis, tornando a comunicação mais expressiva e visual. As reações são exibidas abaixo da mensagem e atualizadas em tempo real.

---

## 🛠️ Tecnologias Utilizadas

- **React Native (Expo SDK 53)**
- **Firebase Firestore** – armazenamento em tempo real das reações
- **Firebase Auth** – identificação do usuário que reagiu
- **NativeWind** – estilização visual
- **Emoji Picker (emoji-mart-native ou custom picker)**

---

## 💡 Impacto no UI/UX

- Interações mais dinâmicas e parecidas com apps como WhatsApp, Telegram, Messenger.
- Respostas rápidas sem digitar.
- Interface moderna e interativa com reações visíveis nas mensagens.

---

## 🔧 Estrutura no Firestore

- Cada **mensagem** terá uma subcoleção chamada `reactions`.
- Cada documento dentro de `reactions` terá:
  - `emoji`: string (ex: '😂')
  - `userId`: ID do usuário que reagiu
  - `timestamp`: data e hora da reação

Exemplo:
