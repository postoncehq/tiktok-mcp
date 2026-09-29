---
name: tiktok-script-generator
description: Write short-form TikTok video scripts with a hook, beats, on-screen text, B-roll and an ending, ready to film and post with the PostOnce TikTok MCP. Use when the user asks for a TikTok script, a script generator, a video script for TikTok, or to turn an idea, article, product or transcript into a TikTok.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok script generator

Write one TikTok script someone can film today. Hand the finished video to the `postonce` skill when the user wants it published or scheduled.

## Before writing

Get or infer: who is on camera (face, voiceover, hands only, screen recording), the audience, the one thing a viewer should learn or feel, and the target length. If the user gives a long source, pick the single most useful idea. One video, one idea. Never invent numbers, results or testimonials.

Length: 15–45 seconds suits most tips and stories. Go longer only when the content earns it (a tutorial, a story with a payoff). TikTok accepts videos up to 10 minutes through this server.

## Structure

| Part | Time | Job |
| --- | --- | --- |
| Hook | 0–3 s | Spoken line, on-screen text and an opening shot that all say the same promise. Use the `tiktok-hook-generator` patterns. |
| Setup | 3–8 s | Why this matters to the viewer. One line. |
| Beats | the middle | 3–5 beats, one point each, a visual change on every beat (new angle, cut, zoom, B-roll, screen). |
| Payoff | last 5 s | Deliver what the hook promised. Then one ending: a takeaway, a follow for part 2, or a question that's easy to answer in the comments. |

Rules that hold up on TikTok:
- Start mid-action. No "Hey guys", no intro, no logo.
- Write for the ear: short sentences, contractions, one idea per sentence.
- Put key words on screen. Many people watch with the sound off.
- Keep on-screen text out of the bottom fifth and the right edge, where TikTok's caption and buttons sit.
- Film vertical, 9:16, 1080×1920.
- Show, don't describe: if you say "this app", show the app.
- Cut dead air. Every pause over a beat is a reason to swipe.

Avoid: long setups, reading a list with nothing changing on screen, ending on "link in bio" as the only point, and stuffing the script with trend phrases that don't fit the speaker.

## Output format

Return a table the user can shoot from:

| Time | Spoken (voiceover) | On-screen text | Shot / B-roll |
| --- | --- | --- | --- |

Then: total estimated length, a filming checklist (shots and props), and a draft caption (use `tiktok-caption-generator`).

## Output

Offer to publish or schedule the finished video with the `postonce` skill: upload it with `create_upload_url`, confirm the TikTok account and the time, then call `create_post`. Mention the useful options: `publish_mode: "draft"` to finish it in the TikTok app (add a sound there; the video arrives without its caption), `video_cover_timestamp_ms` to pick the cover frame, and `ai_generated: true` if the video uses AI-generated visuals or voice.
