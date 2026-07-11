+++
title = "Proposal: Sonar (Builders Turin 2)"
date = 2026-09-25
draft = true
+++

<!-- Draft companion to GitHub issue — Sonar presentation for Builders Turin 2 -->

## Sonar — private messenger for builders (proposal)

**Presenter:** Vincenzo Palazzo  
**Site:** [sonarprivacy.xyz](https://sonarprivacy.xyz/)  
**Editions:**

| When | Role |
|------|------|
| **Builders Turin 1** (2026-07-11) | **Closing demo** (~7–10 min) — live Sonar + preview BT2 agenda (25 Sep) |
| **Builders Turin 2** (2026-09-25) | **Full session** (~15–20 min) — architecture, Marmot/White Noise bridge, agents |

### What Sonar is

Sonar is a private messenger that combines:

- **Proximity (Bluetooth)** — discover and message people nearby without internet
- **Nostr** — reach anyone on the open relay network with the same identity (npub)
- **E2EE** — keys stay on device; no phone number or corporate account

It sits in the same ecosystem as the BT2 agenda (White Noise, Marmot, MLS/CGKA): **sovereign messaging** for communities that do not want a single vendor in the middle.

### Why Builders Turin 2

Builders Turin 1 focuses on Lightning reliability, OSS infra, and local CLN tooling. **BT2** is explicitly about **Chat Control, E2EE, Nostr, and Marmot/Dark Matter**. Sonar is a practical on-ramp:

- How builders can **dogfood** encrypted DMs for events, coordination, and agent workflows
- How **Hermes-style agents** (tools + memory over Nostr/Sonar) extend “building on Bitcoin” into **human–agent** chat without Telegram phone numbers
- Bridge from **payments (BT1)** to **private coordination (BT2)**

### BT1 closing demo (finale giornata, 11 July)

1. **Hook** (30 s): after Lightning & products — why messaging identity matters next  
2. **Live** (5 min): Sonar nearby + encrypted DM on Nostr  
3. **BT2 preview** (2 min): Chat Control, White Noise, Marmot — save the date **25 Sep**

### BT2 full session shape (~15–20 min)

1. **Problem** (2 min): phone-number messengers vs npub-native identity  
2. **Demo** (8 min): pair nearby + send encrypted DM; optional agent reply on Sonar  
3. **Architecture** (5 min): Bluetooth + Nostr + encryption; relation to Marmot/MLS stack (complementary, not duplicate)  
4. **Q&A** (5 min): builders running their own relays, NIP-05 (`sonarprivacy.xyz`), onboarding guests

### Links

- [Sonar](https://sonarprivacy.xyz/)
- [bitchat-to-sonar / NIP-05 discussion](https://github.com/hedwig-corp/bitchat-to-sonar/issues/101)
- Local continuity: [CLN plugins (BT1)](https://x.com/PalazzoVincenzo/status/2068045408257900705) → **messaging + agents (BT2)**

### Ask

- **BT1:** Closing demo slot confirmed in `builder-01.md` (do not move for open mic).  
- **BT2:** Add to Demos or Local spotlight; expand Marmot/White Noise narrative with Sonar as on-ramp.