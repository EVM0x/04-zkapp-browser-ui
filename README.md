# 🧪 zkApp Browser UI

**Compile, verify & deploy Mina zkApp circuits — entirely in the browser. No local toolchain needed.**

[![Stars](https://img.shields.io/github/stars/EVM0x/04-zkapp-browser-ui?style=social)](https://github.com/EVM0x/04-zkapp-browser-ui)
[![Mina](https://img.shields.io/badge/Mina-o1js-0AC18E)](https://minaprotocol.com)
[![Next.js](https://img.shields.io/badge/Next.js-14-black)](https://nextjs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)](https://typescriptlang.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue)](LICENSE)

A zero-knowledge developer tool that brings the **full zkApp circuit workflow into the browser** — write or load contracts, compile circuits, run tests, and deploy to Mina — without ever leaving the UI.

> ⭐ 9 stars · one of the most-starred repos for in-browser zkApp tooling.

---

## ✨ Why this matters

Mina zkApp development normally requires a **local o1js toolchain** — Node, TypeScript, snarkyjs, build steps. That's a wall for beginners and a slowdown for pros.

**This project removes the wall.** The entire compile → verify → deploy loop runs client-side, which means:

- 🔌 **Zero setup** — no npm install, no local node
- 🌐 **Runs anywhere** — any browser, any machine
- 🧑‍💻 **Great for education** — on-ramp people into zk without toolchain hell
- ⚙️ **Demo-ready** — perfect for hackathon pitches and live zk demos

---

## 🧱 Architecture

```
├── contracts/          # o1js (Mina) smart contract circuits
│   ├── src/            # zkApp source code
│   ├── config.json     # contract configuration
│   └── test/           # Jest circuit tests
└── ui/                 # Next.js + TypeScript frontend
    ├── pages/          # Browser UI pages
    └── styles/         # styling
```

**Stack:** TypeScript · o1js (Mina) · Next.js · Jest · coi-serviceworker (COOP/COEP for WASM)

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm

### Run the UI
```bash
cd ui
npm install
npm run dev
# open http://localhost:3000
```

### Test & build contracts
```bash
cd contracts
npm install
npm test          # run Jest circuit tests
npm run build     # compile TypeScript
```

### Deploy UI to GitHub Pages
```bash
cd ui && npm run deploy
```

---

## ✅ What it demonstrates

| Feature | Status |
|---------|--------|
| In-browser zkApp circuit compilation | ✅ |
| Contract load & configuration (config.json) | ✅ |
| Jest test suite for circuits | ✅ |
| Deployable Next.js UI (gh-pages) | ✅ |
| WASM via coi-serviceworker | ✅ |

---

## 🛠 Tech notes

- Circuits use **o1js** (Mina's TypeScript zk framework)
- Browser WASM requires **COOP/COEP headers** — handled by `coi-serviceworker`
- Clean separation between `contracts/` (logic) and `ui/` (presentation)

---

## 📄 License

Apache 2.0 — see [LICENSE](contracts/LICENSE).

## 🤝 Connect

Built by **EVM0x** — [portfolio](https://evm0x.com) · [Telegram @evm0xstark](https://t.me/evm0xstark)

*Open to zk collaborations, bounties & hackathon teams.*
