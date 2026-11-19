# Voice Agent Testing

A single, self-contained page that shows what a real-time voice agent actually does — not what a brochure says it does.

**Open `index.html` in a browser.** No build step, no dependencies, no network calls, no analytics.

## What is on the page

| Section | What it demonstrates |
|---|---|
| Hero | A canvas waveform. Press **use your microphone** and it switches from a simulated signal to a live analyser on your actual mic (audio never leaves the browser). |
| Capabilities | Nine concrete behaviours — streaming ASR, barge-in, intent over keywords, tool calling, code-switching, sub-second turn-taking, handoff, grounded answers, per-call measurement. |
| Live call | A scripted transcript that plays as you scroll: caller speech, agent thinking, a `billing.get_invoice(...)` tool call, then the spoken resolution. |
| Numbers | Animated counters for latency, containment, languages and uptime — targets to beat, not vendor claims. |
| How it works | The four-hop loop: listen → understand → act → speak. |

## Design notes

- Aurora background, glass cards with gradient borders, scroll-reveal with staggered delays, parallax orb, animated counters.
- Everything respects `prefers-reduced-motion` — animations switch off entirely.
- Canvas redraws at device pixel ratio so the waveform is sharp on retina screens.
- Colour is carried by a violet → teal → rose gradient used consistently for the waveform, the avatar and the headline.

## Making it public

This repo is Pages-ready as-is: enable GitHub Pages on the `main` branch with the root folder, and the site serves from `index.html` with no changes.

## Caveats

The transcript, the metrics and the tool call are illustrative. The microphone visualisation is real; nothing else is connected to a live agent.
