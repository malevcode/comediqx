comediqx — Master Product Document
Version 4.20.26 | Built by Adam Malev + Grok (xAI)
what this is
comediqx is the clean-slate, 100% xAI-only version of comediq.hear.
It replaces the old AssemblyAI + Claude pipeline with Grok STT + Grok 4.1 Fast. Same one-tap record → automatic set processing, but dramatically better, cheaper, and faster.
one-sentence pitch
Press record, press stop — xAI transcribes with word-level timestamps, Grok 4.1 Fast breaks it into bits (setup + punchline + underlined funny moment), gives real coaching, and you get a rich performance report with exact audio playback per bit.
why this version is better than the original Claude/AssemblyAI build

Cheaper — STT at ~$0.10/hour (batch) vs AssemblyAI. Analysis on Grok 4.1 Fast ($0.20/$0.50 per M tokens). Overall 50-70% lower cost.
Faster — Grok 4.1 Fast has massive rate limits (1,800 RPM / 10M TPM). Processing is snappier.
Richer analysis — Full timestamped transcript fed to Grok → better bit splitting, explicit funny_moment for underlining, specific coaching on “why it landed and how to replicate/improve”.
Better performer UX:
See exact words you said (full transcript)
Per-bit cards: setup, punchline, underlined funny moment, coaching
One-tap “Play this bit” — audio seeks to exact second
Set totality view: laughs per minute, pause proxies, overall stats
Permanent joke identities + performance history (Dice coefficient kept)

Simpler stack — One API key (xAI), one vendor, easier billing & maintenance.
Future-proof — Same company for STT + LLM. Easy to add voice notes, video, real-time later.

core improvements over previous version
You now get performance history, not just joke history.
You see why a bit worked (or didn’t) via Grok’s coaching.
Every set has totality + granular playback. No more “I can only see bit names”.
tech stack (xAI-only)

Transcription: xAI Grok STT (/v1/stt) — word-level timestamps + pauses for laugh proxy
Analysis: Grok 4.1 Fast (grok-4-1-fast-reasoning)
Backend: Node.js + Express + Supabase (same project or new)
Frontend: Single index.html (mobile-first, dark editorial aesthetic)