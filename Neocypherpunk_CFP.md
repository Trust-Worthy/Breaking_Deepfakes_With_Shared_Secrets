# The Doppelgänger Protocol
### Memory-Anchored Cryptography Against Deepfake Identity Attacks

> *This isn't theoretical. This is cryptography deployed against the most urgent identity threat of our time.*

---

## Abstract

Voice clones fool CEOs into wiring millions. AI-generated video calls scam elderly parents. Traditional authentication, passwords, 2FA, and biometrics, can all be faked or phished. And as Signalgate demonstrated, even an end-to-end encrypted channel is only as secure as your ability to verify who you're adding to it.

How do we verify identity when audio, video, and even biometrics are no longer trustworthy?

This talk introduces **The Doppelgänger Protocol**: a cryptographic approach that transforms shared human memories into unforgeable authentication keys. Memory-based verification combines challenge-response protocols, local-first cryptography, and zero-knowledge principles to create a new layer of human authentication that AI cannot replicate.

We'll walk through the full technical architecture: how each party generates an ECDH keypair locally in the browser using the Web Crypto API, how Alice's memory answer is embedded as a 384-dimensional semantic vector (`all-MiniLM-L6-v2`), and how cosine similarity scoring gates the key exchange itself. Alice's public key is never released to an unverified Bob. Sessions are ephemeral by design: 256-bit session IDs, 5-minute Redis TTL, no accounts, no PII persisted.

Beyond the architecture, this talk addresses the harder design problem: **building cryptographic trust for non-technical users.** Most people facing grandparent scams, executive impersonation, and romantic catfishing have no mental model for public key infrastructure, and they shouldn't need one. The Doppelgänger Protocol uses human memory as the trust anchor precisely because it maps to something everyone already understands: **shared experience is proof of shared identity.**

This is also an accessible entry point into foundational public-key cryptography concepts. Attendees will leave with an intuitive understanding of why bootstrapping trust is the central unsolved problem in PKI––illustrated through a protocol they just used themselves.

---

## What You'll Learn

1. Why traditional authentication fails against sophisticated deepfake attacks
2. How memory-based challenges create cryptographic proof of shared human experience
3. The technical architecture: local key generation, ECDH exchange, semantic embedding, and privacy-preserving session design
4. Real-world threat models: grandparent scams, executive impersonation, romantic catfishing, synthetic identity fraud, and privacy-critical contexts (journalist verification, activist networks, whistleblower communication)

---

## What You'll Do

After the technical walkthrough, you'll pair up with another attendee and run the live protocol yourselves. Using the browser-based demo at [doppelgangerprotocol.app/verify](https://doppelgangerprotocol.app/verify), you'll:

- Generate ECDH keypairs directly in your browser via the Web Crypto API
- Create and answer memory challenges with your partner
- Watch a real encrypted channel open between two people who just met

The built-in debug panel logs every cryptographic event in real time (keypair generation, embedding vector preview, cosine similarity score, shared secret derivation) so you can follow the protocol at whatever depth you choose.

The source code is MIT-licensed and publicly available at [doppelgangerprotocol/doppelganger-web](https://github.com/doppelgangerprotocol/doppelganger-web). Fork it, audit it, build on it.

---

## Walk Away With

- A new mental model for human-layer authentication
- Hands-on experience running a live cryptographic protocol
- Insight into deploying cryptographic solutions for non-technical users facing AI threats
- Working code you can examine and build upon

---

## Speaker
([@Trust-Worthy](https://github.com/Trust-Worthy)) — Founder, [realxreal.ai](https://realxreal.ai)
