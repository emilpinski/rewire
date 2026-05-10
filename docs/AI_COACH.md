# AI Coach - Design and Safety

## Overview

The AI Coach in Rewire is a conversational assistant designed around CBT (Cognitive Behavioral Therapy) and ACT (Acceptance and Commitment Therapy) principles. It provides motivational nudges, session check-ins, and reflective prompts - not therapy.

## Model

Claude Haiku 4.5 via OpenRouter. Chosen for low latency (sub-1s responses) and cost efficiency for short conversational turns.

## Coaching methodology

The system prompt grounds coach responses in:
- CBT: identifying and reframing unhelpful thought patterns around productivity and focus
- ACT: values clarification, defusion from self-critical thoughts, committed action
- ADHD-aware design: validates executive dysfunction, avoids shame-based language, celebrates small wins

## What the coach does not do

- Provide medical advice or diagnosis
- Prescribe or recommend medication changes
- Substitute for a licensed therapist or psychiatrist
- Store conversation history beyond the current session (episodic memory is a planned feature)

## Safety and crisis routing

If a user message contains keywords or patterns associated with self-harm, suicidal ideation, or acute crisis, the coach response:
1. Acknowledges the user with warmth (no clinical coldness)
2. Does not attempt to counsel - immediately surfaces emergency contacts
3. Shows: Telefon Zaufania dla Doroslych: 116 123 (free, 24/7), Emergency services: 112, Crisis text resources

This routing is handled at the system-prompt level and cannot be overridden by user messages.

## Prompt structure

The system prompt (paraphrased, not reproduced verbatim):
- Role: supportive focus coach, not therapist
- Methodology: CBT/ACT-informed, ADHD-aware
- Tone: warm, direct, non-judgmental
- Length: short responses (2-4 sentences) unless user asks for more
- Refusals: medical advice, diagnosis, comparison to other users
- Crisis routing: as above

## Limitations

- No persistent memory between sessions (planned: episodic memory with user consent)
- English and Polish supported; other languages receive best-effort responses
- Effectiveness depends on user engagement; passive use yields limited benefit
