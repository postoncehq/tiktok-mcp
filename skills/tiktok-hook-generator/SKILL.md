---
name: tiktok-hook-generator
description: Generate 10 first-3-second TikTok hooks for a topic, each with the spoken line, the on-screen text and the opening shot. Use when the user asks for TikTok hooks, a hook generator, video openers, "how should I start this TikTok", or better first lines for a short-form video.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok hook generator

The first three seconds decide whether someone keeps watching. A hook on TikTok has three layers that should agree: what you say, what the screen says, and what the viewer sees.

## Before writing

Get or infer: the topic, the audience, the payoff the video actually delivers, and the format (talking head, voiceover, screen recording, B-roll). A hook must promise only what the video pays off. Never invent results or numbers.

## Patterns

Write 10 hooks across at least 6 of these patterns:

| Pattern | Example shape |
| --- | --- |
| Call out the viewer | "If you [specific situation], watch this." |
| Result first | Show the end result, then "Here's how I got here." |
| Mistake | "Stop [common habit]. Do this instead." |
| Contrarian | "[Popular advice] is wrong for [who]." |
| Curiosity gap | "I didn't expect [thing] to change [outcome]." |
| Number | "[N] [things] I wish I knew before [event]." |
| Before / after | Split screen or a hard cut from before to after. |
| Point of view | "POV: you [relatable moment]." |
| Question with stakes | "Why does [annoying thing] keep happening?" Only when the answer is specific. |
| Visual pattern break | An unexpected object, motion or location in frame 1. |

## Rules

- Spoken line: under 12 words, said in the first second. No greeting.
- On-screen text: 3–7 words, readable in one glance, placed in the top two-thirds of the frame, clear of TikTok's caption and buttons at the bottom and right.
- Opening shot: movement or a clear subject in frame 1. Not a logo, not a blank wall.
- Name the specific audience or problem. "Freelance designers" beats "everyone".
- Plain words. No clickbait the video can't back up; viewers leave and TikTok notices early drop-off.

## Output format

Return a numbered list. For each hook:

1. **Pattern:** name
   - **Say:** the spoken line
   - **Text:** on-screen text
   - **Shot:** what's on screen in the first second

Mark your top 3 picks and say why in one line each.

## Output

Offer to write the full script with `tiktok-script-generator`, or, if the video is done, a caption with `tiktok-caption-generator`, then publish or schedule it with the `postonce` skill (confirm the TikTok account and time before `create_post`).
