# Privacy Policy

**Last updated: 2026-07-29**

All Languages Learner (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

All Languages Learner has no backend server of its own, no user accounts, and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your reading subject, generated texts, or API keys.

## Your API keys

In Settings, you enter your own Claude (Anthropic) API key, which is required to generate reading practice. You can optionally add an ElevenLabs API key for higher-quality narration. Each key is:
- Stored only on your device, in the system Keychain — never synced via iCloud, never sent to us.
- Sent only directly to that provider's own API (`api.anthropic.com` or `api.elevenlabs.io`), never to us or any other server.

Usage of each key is billed directly by that provider to your own account.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)

## Reading subject and generated text

Whatever optional subject you type in, and the resulting generated text, is sent to Claude to generate the passage and its translation, and — if you've entered an ElevenLabs key and haven't muted narration — the passage text is also sent to ElevenLabs to generate spoken audio. This content is never sent anywhere else.

## Your reading history

Your reading history (every passage you've generated) and bookmarks (passages you've starred) are stored locally on your device using Apple's CloudKit framework, so they're available across app launches and, if you're signed into iCloud, synced to your other devices through your own iCloud account. This data is only ever accessible to you, through your own Apple ID; we have no access to it. Your API keys are deliberately excluded from this sync (see above). You can permanently delete this history at any time from Settings → Clear History.

## Subscriptions

All Languages Learner offers an optional auto-renewing subscription, sold and processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing, receipts, and renewal directly. See Apple's own [Privacy Policy](https://www.apple.com/legal/privacy/) and the Terms of Use linked in the app for how Apple handles subscription and payment data.

## Third parties

The only third parties involved are:
- **Anthropic** (`api.anthropic.com`) — generates each reading passage and its translation from your chosen languages and optional subject.
- **ElevenLabs** (`api.elevenlabs.io`) — only if you enable narration with an ElevenLabs key, to generate spoken audio from passage text.
- **Apple** — iCloud (for history/bookmark sync) and StoreKit (for the subscription), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/alllanguageslearner-support/issues).
