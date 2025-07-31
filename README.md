# 🎰 Solana Meme coin Casino Platform 🚀  
*A Fully Decentralized, Token-Integrated Casino Ecosystem on Solana-
Solana Casino Platform** is a next-generation, fully decentralized gambling platform built on the Solana blockchain. Designed for speed, transparency, and modular scalability, the platform empowers anyone to turn their SPL token into a complete, secure, and engaging casino environment with provably fair games, real-time analytics, and institutional-grade infrastructure.*

![Solana Casino Platform](https://raw.githubusercontent.com/osmanx8/Solana-Casino/refs/heads/main/public/slots.png)

---

## 🧭 Overview

**Solana Casino Platform** is a next-generation, fully decentralized gambling platform built on the Solana blockchain. Designed for speed, transparency, and modular scalability, the platform empowers anyone to turn their SPL token into a complete, secure, and engaging casino environment with provably fair games, real-time analytics, and institutional-grade infrastructure.

---

## 🆕 Latest Updates – v1.3.2

### 🚀 Dashboard Optimization
- ✅ **Flash-Free Interface**: Removed legacy marketing page to prevent flicker on refresh.
- 📉 **Component Minimization**: Reduced dashboard code by 75% for better maintainability.
- 🎮 **Direct Access to Games**: Instantly land on playable games with improved UX.

### 🧼 Codebase Cleanup
- 🧹 Removed outdated components and unused files.
- ⚡ Eliminated React `StrictMode` to stop double renders and speed up performance.
- 🎨 Applied anti-flash CSS techniques for seamless visual loading.

### 🛠️ Navigation Fixes
- 🧩 Fixed Z-index and clickability issues with game cards.
- 🔧 Optimized layout spacing and pointer event handling.

---

## 🌟 Key Features

### 🎮 Provably Fair Casino Games
- **Coin Flip** – 1.95x multiplier, physics-based animation.
- **Dice Roll** – Variable odds and payouts with animated rolls.
- **Slots** – Up to 25x win, immersive visuals and sound.
- **Chat Roulette (Coming Soon)** – Social betting via Telegram.

### 🪙 Token Support
- 🎯 Integrate any SPL token instantly.
- 💰 Create liquidity pools and manage limits.
- 📊 Dynamic odds, multipliers, and payouts based on pool health.

### 🤖 Telegram Bot Integration
- 💬 Play games directly in Telegram groups.
- 📲 Wallet commands: balance, deposit, withdraw.
- 🏆 Live leaderboards, win tracking, and instant payouts.

### 🧑‍💼 Token Creator Tools
- 🎨 Custom branding and color theming.
- 📈 Dashboard with player insights and profit tracking.
- 🧮 House edge, risk controls, and exposure management.

---

## 🎲 Game Mechanics

### 🪙 Coin Flip
- 50/50 odds with a 1.95x payout
- Realistic animated coin flip
- Provably fair outcome via client/server seed hashing
- Instant results and recorded game history

### 🎲 Dice Roll
- Roll under/over with configurable targets
- Transparent win probabilities
- Smooth dice animations and results visualization
- Dynamic multipliers and result logs

### 🎰 Slots
- Classic 3-symbol match format
- Up to **25x payout**
- High-fidelity slot reel animations and effects
- Sound effects and jackpot celebration visuals

### 🔁 Chat Roulette *(Coming Soon)*
- Real-time in-chat games within Telegram groups
- Group pools and collaborative bets
- Visual results and winner announcements

---

## 🔐 Provably Fair RNG System

```ts
const generateResult = () => {
  const serverSeed = SHA256(Date.now().toString());
  const clientSeed = SHA256(Math.random().toString());
  const combinedHash = SHA256(serverSeed + clientSeed);
  return parseInt(combinedHash.substring(0, 8), 16);
};
