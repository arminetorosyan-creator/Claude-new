---
name: meeting-notes-summarizer
description: Turn a raw meeting transcript (Zoom/Meet/Otter-style, with speaker labels and filler words) or rough typed notes into a short, clean summary paragraph. Use this skill whenever the user pastes meeting notes or a transcript and asks to summarize it or write it up — even if they just say "here's the notes from today, can you clean this up" or "what happened in this call." Also use it when a Product Owner needs to bring someone up to speed on a meeting they missed.
---

# Meeting Notes Summarizer

Raw meeting input is noisy — transcripts have speaker labels, crosstalk, filler words, and tangents; typed notes are shorthand fragments. Your job is to distill it into a short summary that gives someone who wasn't there enough context to understand what happened, without making them read the whole transcript.

## Handling transcript input

Transcripts (Zoom/Meet/Otter-style) typically look like repeated `Speaker Name: text` lines with timestamps, filler ("um," "yeah so," "I think"), and people talking over each other or restating things. Read through the whole thing before summarizing — the substance (decisions, direction, outcomes) is often buried mid-tangent, not announced clearly. Strip the filler and crosstalk; keep the substance.

## Handling typed shorthand notes

Rough notes are usually already compressed, so the job shifts from *filtering noise* to *turning fragments into readable prose* — connecting related bullets into a coherent narrative rather than just reformatting a list.

## Output

Write **one short paragraph** (roughly 2-5 sentences, more only if the meeting genuinely covered several distinct substantial topics). It should cover:

- What the meeting was about / what was discussed
- Where things landed — any decisions, direction, or outcomes that emerged
- Anything left clearly unresolved, if that's a significant part of how the meeting ended

Don't try to capture every topic discussed or reproduce the meeting chronologically — that's what the transcript is for. Skip small talk, scheduling logistics ("let's move next week's meeting"), and restatements where someone just repeats what another person said. If the same point gets discussed multiple times before landing, summarize the final outcome once rather than narrating the back-and-forth.

Write it as plain prose, not bullet points — a paragraph someone can read in a few seconds, not a structured report. If the user asks for action items, decisions broken out separately, or a longer/more structured writeup, do that instead of forcing everything into one paragraph — this default is for the common case of "just tell me what happened."
