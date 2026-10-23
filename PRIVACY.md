# Privacy Policy

**Last updated: 2026-10-23**

All Languages Learner (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

All Languages Learner has no user accounts and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your reading subject or generated texts beyond what's needed to relay them, described below.

## How AI requests work (no personal API keys)

The app does **not** ask you for your own AI provider API key. Every request to generate a reading passage, its translation, a picture, or narration audio is sent to our own relay server, **aicoin-proxy**, at `proxy.aicoin.oeaio.com`. aicoin-proxy adds its own paid credential for the AI provider the request is for, forwards your request to that provider, and returns the response — you never handle or expose a provider credential, and we never see one of yours because there isn't one.

**AI calls are paid for in AICoin, priced by what they cost to run.** Each passage, picture or narration clip costs from 1 AICoin — a longer one costs more — debited from your AICoin wallet at the moment of the call.

### What the relay keeps, and what the providers keep

- **The relay does not log or store what you send or get back** — no subjects, passages, translations, audio or pictures. For each request it keeps only a line of metadata: the time, the kind of request and the provider's endpoint (without query parameters; for narration this includes the ID of the voice used), which provider, your wallet address, the result status, sizes, timings, and the AICoin charged. Those logs rotate and are capped in size.
- **The AI providers do receive your requests**, and keep them under their own retention policies (linked below).
- **Nothing you send is stored on a provider where other users could reach it.** Every user's requests go through the same provider accounts, so the relay only forwards requests to providers' generation endpoints and refuses the provider features that store things on the account — file uploads, batch jobs, stored responses and conversations, caches, and generation history.
- **The one exception is designed voices.** With "New voice per card" or "Match voice" on (both on by default), the app writes a short voice description from the card or word form and asks ElevenLabs to design a voice from it; that voice is saved in the shared ElevenLabs account, named "All Languages Learner — card …" or after the word form. The relay records which wallet created each voice: only your wallet sees it in voice lists and only your wallet can delete it. The app deletes a card's voice when it designs the next one.

## AICoin wallet

Your wallet is identified by a keypair generated and stored on your device (Keychain) — we never see your private key. There are two ways to get AICoin:
- **Buy it**, via an in-app purchase processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing and receipts directly. A successful purchase credits your wallet by contacting `proxy.aicoin.oeaio.com` with Apple's own signed proof of purchase.
- **Receive a transfer** from another AICoin wallet (yours on another device, or someone else's).

Your wallet address and balance are stored server-side at `proxy.aicoin.oeaio.com` (see the [aicoin.oeaio.com](https://aicoin.oeaio.com) site for how the ledger works) — this is necessary for the wallet to function across devices and to debit calls, and is not linked to your name, email, or Apple ID.

## Reading subject and generated text

Whatever optional subject you type in, and the resulting generated text, is relayed (via aicoin-proxy) to Claude to generate the passage and its translation (if Claude fails, the request may be retried with another provider the relay offers: OpenAI, Google Gemini, Mistral or Kimi by Moonshot AI). If narration isn't muted, the passage text is also relayed to the narration service for that language — ElevenLabs, Google (Gemini or Cloud Text-to-Speech), or OpenAI — to generate spoken audio, and a short description is relayed to ElevenLabs to design a voice (see above). A picture prompt written from the passage is relayed to Stability AI or Google Gemini to draw an illustration. This content is never sent anywhere else.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)
- [Google's privacy policy](https://policies.google.com/privacy)
- [OpenAI's privacy policy](https://openai.com/privacy)
- [Stability AI's privacy policy](https://stability.ai/privacy-policy)
- [Mistral AI's privacy policy](https://mistral.ai/terms#privacy-policy)
- [Moonshot AI's (Kimi) privacy policy](https://platform.moonshot.ai/docs/agreement/userprivacy)

## Your reading history

Your reading history (every passage you've generated) and bookmarks (passages you've starred) are stored locally on your device using Apple's CloudKit framework, so they're available across app launches and, if you're signed into iCloud, synced to your other devices through your own iCloud account. This data is only ever accessible to you, through your own Apple ID; we have no access to it. You can permanently delete this history at any time from Settings → Clear History.

## Third parties

The only third parties involved are:
- **aicoin-proxy** (`proxy.aicoin.oeaio.com`, operated by us) — relays every AI request below with its own paid credentials and debits your wallet; see [aicoin.oeaio.com](https://aicoin.oeaio.com) for how it works. The same single set of credentials is used for every user of the app: the AI providers below are never given a per-user account, key, or identifier, so what reaches them is one stream of requests with nothing in it that distinguishes you from anyone else. Your wallet address is used by the proxy to debit the call and is not forwarded to them.
- **Anthropic** — generates each reading passage and its translation from your chosen languages and optional subject.
- **ElevenLabs** — generates spoken audio from passage text and designs card voices, unless narration is muted.
- **Google** — draws illustrations (Gemini), and narrates languages it is the chosen or fallback voice for.
- **OpenAI** — narrates languages it is the chosen or fallback voice for.
- **Stability AI** — draws illustrations.
- **OpenAI, Google, Mistral, Moonshot AI (Kimi)** — only if Claude fails and the request is retried with one of them.
- **Apple** — iCloud (for history/bookmark sync) and StoreKit (for AICoin purchases), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/alllanguageslearner-support/issues).
