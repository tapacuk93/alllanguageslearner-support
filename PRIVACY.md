# Privacy Policy

**Last updated: 2026-08-20**

All Languages Learner (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

All Languages Learner has no user accounts and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your reading subject or generated texts beyond what's needed to relay them, described below.

## How AI requests work (no personal API keys)

The app does **not** ask you for your own AI provider API key. Every request to generate a reading passage, its translation, or narration audio is sent to our own relay server, **aicoin-proxy**, at `proxy.aicoin.oeaio.com`. aicoin-proxy adds its own paid Anthropic/ElevenLabs credential, forwards your request unchanged, and returns the response — you never handle or expose a provider credential, and we never see one of yours because there isn't one.

**1 AICoin = 1 AI API call.** Each passage generation or narration clip costs exactly 1 AICoin, debited from your AICoin wallet at the moment of the call.

## AICoin wallet

Your wallet is identified by a keypair generated and stored on your device (Keychain) — we never see your private key. There are two ways to get AICoin:
- **Buy it**, via an in-app purchase processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing and receipts directly. A successful purchase credits your wallet by contacting `proxy.aicoin.oeaio.com` with Apple's own signed proof of purchase.
- **Receive a transfer** from another AICoin wallet (yours on another device, or someone else's).

Your wallet address and balance are stored server-side at `proxy.aicoin.oeaio.com` (see the [aicoin.oeaio.com](https://aicoin.oeaio.com) site for how the ledger works) — this is necessary for the wallet to function across devices and to debit calls, and is not linked to your name, email, or Apple ID.

## Reading subject and generated text

Whatever optional subject you type in, and the resulting generated text, is relayed (via aicoin-proxy) to Claude to generate the passage and its translation, and — if narration isn't muted — the passage text is also relayed to ElevenLabs to generate spoken audio. This content is never sent anywhere else.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)

## Your reading history

Your reading history (every passage you've generated) and bookmarks (passages you've starred) are stored locally on your device using Apple's CloudKit framework, so they're available across app launches and, if you're signed into iCloud, synced to your other devices through your own iCloud account. This data is only ever accessible to you, through your own Apple ID; we have no access to it. You can permanently delete this history at any time from Settings → Clear History.

## Third parties

The only third parties involved are:
- **aicoin-proxy** (`proxy.aicoin.oeaio.com`, operated by us) — relays every AI request below with its own paid credentials and debits your wallet; see [aicoin.oeaio.com](https://aicoin.oeaio.com) for how it works. The same single set of credentials is used for every user of the app: the AI providers below are never given a per-user account, key, or identifier, so what reaches them is one stream of requests with nothing in it that distinguishes you from anyone else. Your wallet address is used by the proxy to debit the call and is not forwarded to them.
- **Anthropic** — generates each reading passage and its translation from your chosen languages and optional subject.
- **ElevenLabs** — generates spoken audio from passage text, unless narration is muted.
- **Apple** — iCloud (for history/bookmark sync) and StoreKit (for AICoin purchases), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/alllanguageslearner-support/issues).
