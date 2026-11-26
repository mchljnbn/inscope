# Inscope

**Free Instagram data viewer for Android and web.** Public profiles, posts,
comments and search work without login. Follower/following lists need a
logged-in session — and that session always stays on your device.

> Status: **pre-launch**. Releases will be published in this repository.
> The source code lives in a separate private repository.

## Download

- [Android releases](releases) (APK, sideload — not on Google Play)
- [Website / landing page](index.html)
- Support: open an issue in this repository

## What you can do

- View public profile data, posts, reels, comments and keyword search
- Look up followers/following and check whether someone is in a list
- Track new follows over time with dated snapshots and merge them for better coverage

Instagram removed chronological follow order in 2026. Inscope records *when a
follow was detected*, not the exact time it happened. Instagram also serves
only a ranked subset (roughly 85–90% coverage per merged snapshot), and
verified accounts may return no list at all.

## Backend

The app connects to Inscope's hosted backend by default, so you don't need to
run any server yourself. If you prefer full control, you can change **Settings →
Backend URL** to your own Inscope-compatible server.

## Your privacy

- **No shared or "helper" Instagram account.** Your access is exactly what your own account can see.
- Your session is sent **per request** in an `X-IG-Session` header. The backend uses it in memory only — it is never written to its database or disk, and no other user can use it.
- With the default hosted backend, that transient header passes through Inscope's server. Self-hosting is available if you prefer not to trust a third party.
- If a private profile isn't visible to you, the app says so. It never borrows someone else's access.
- You choose the backend URL in Settings. Only point the app at a server you control.
- Private profiles you cannot see are reported as unavailable — by design.

## Optional monetization (off by default)

Inscope is free either way. In a private build, users may be offered an
**opt-in** Honeygain integration:

- You see an explicit explanation before anything starts, and Honeygain's own consent screen must be accepted.
- Your device may become an exit node for **encrypted bandwidth sharing**.
- Honeygain does not access your personal data, files, messages, or browsing history.
- You can withdraw consent at any time in **Settings**.
- Bandwidth sharing may increase Instagram rate limits on the same device, so it is off by default.
- Declining changes nothing — the app remains fully usable.

Read the [Honeygain SDK privacy policy](https://www.honeygain.com/sdk-privacy-policy/),
[terms of service](https://www.honeygain.com/sdk-tos/) and
[trust center](https://sdk.honeygain.com/trust-center/).

Inscope is **not distributed on Google Play** — Honeygain's SDK rules do not
permit Google Play apps. Releases here are sideloaded APKs.

## Requirements

Android 5.0 (API 21) or newer for the APK. Web builds are served from the
landing page when published.
