+++
title = "Builders Turin 2"
date = 2026-09-25
+++

## Agenda
- 16:30–16:45 — Networking
- 16:45–17:00 — Presentation
- 17:00–17:45 — Socratic Seminar
- 17:45–18:00 — Demos & Startup Showcase

A participatory afternoon: bring questions, jump into the discussion, and share what you're building — or what you're stuck on. Plenty of Q&A throughout.

## Intro
- [Chatham House Rules](https://grok.com/share/bGVnYWN5LWNvcHk_0ddfe410-0f5a-466a-a2b4-835edd791e30) — no photos/video
- Intros: name · what you do · what you want out of it

## Socratic Seminar

### The threat: EU Chat Control & the war on private messages
- [The Backdoor Battle — *My Friend Bitcoiner* podcast](https://open.spotify.com/episode/5IYsspcXELmSeD78upEmWR) — the CSAR saga from Parliament tricks to "nothing to hide"
- [What is Chat Control? — EDRi](https://edri.org/our-work/chat-control/) — ubiquitous surveillance dressed up as child-safety policy
- [Signal: we will exit the EU before we break encryption](https://signal.org/bigbrother/) — the "existential risk" of mandated client-side scanning
- [EFF: Chat Control issue page](https://www.eff.org/issues/chat-control) — technical analysis and advocacy updates
- Discussion: Can you scan E2EE messages without breaking E2EE? (Spoiler: no.)

### Building the answer: White Noise & the Nostr-native messenger
- [White Noise](https://www.whitenoise.chat/) — a secure, identity-free messenger on Nostr
- [MLS (Messaging Layer Security) — RFC 9420](https://datatracker.ietf.org/doc/html/rfc9420) — the IETF standard for group E2EE at scale
- How White Noise combines **Nostr relays** (decentralized, self-hostable, censorship-resistant) with **MLS** (forward secrecy + post-compromise security, logarithmic group scaling)
- Why relay-level architecture matters: no single point of failure, instant relay switching, metadata-only interception
- Discussion: If Chat Control passes, does a Nostr + MLS stack make enforcement structurally impossible?

### Deep dive: Dark Matter — the next-gen CGKA engine
- [Dark Matter — Marmot Protocol](https://github.com/marmot-protocol/darkmatter) — candidate Marmot v2 protocol draft & CGKA engine
- **CGKA** (Continuous Group Key Agreement) as the evolution of MLS for decentralized group messaging
- The [OpenMLS](https://github.com/openmls/openmls)-backed engine + [Tamarin](https://tamarin-prover.github.io/) formal proofs for convergence guarantees
- Testing strategy: simulator, vector fixtures, property tests, generated chaos — how you prove a distributed group-key protocol actually converges
- Discussion: Why formal verification matters when the threat model includes state actors, not just bugs

### Quick hits: the privacy infrastructure stack
- [Self-hosting Nostr relays](https://github.com/nostr-protocol/nostr) — communities running their own infrastructure
- MLS crypto-agility: quantum-resistant algorithms without app overhauls
- The intersection of Lightning + private messaging: payments that don't leak metadata

### Local spotlight
- [Vincenzo: work on the Marmot Protocol — White Noise & Dark Matter](https://github.com/marmot-protocol)
- From Core Lightning plugins (Builders Turin 1) to decentralized encrypted messaging infrastructure

## Demos & Startup Showcase
- Open mic: show what you're building — or what you're stuck on
- Suggested: live demo of [White Noise](https://www.whitenoise.chat/) + walkthrough of the [Dark Matter](https://github.com/marmot-protocol/darkmatter) CGKA engine and test harness
- **Proposed (issue [#15](https://github.com/dev-crew-it/BitcoinBuilderTurin/issues/15)):** [Sonar](https://sonarprivacy.xyz/) — full demo + Marmot/White Noise bridge ([proposal](../proposals/sonar-builders-2.md)). *Teaser at **BT1 closing demo** (11 Jul).*

## Wrap
- What landed? What should change next month?
