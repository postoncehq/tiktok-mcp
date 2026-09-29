---
name: tiktok-content-calendar
description: Plan 1 to 4 weeks of TikTok videos and slideshows from the user's goals and content pillars, or by repurposing a blog post, YouTube video or transcript, then draft every slot and schedule them with the PostOnce TikTok MCP. Use when the user asks for a TikTok content calendar, content plan, posting schedule, TikTok video ideas, or to turn one piece of content into a month of TikToks.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok content calendar

Plan native TikToks, not reposted captions. Every slot is either a video or a photo slideshow, because TikTok posts through this server need media; there are no text-only TikToks.

## Inputs

Get or infer:
- Goal: followers, traffic, sales, community, or proof of expertise.
- Audience and niche.
- 2–4 content pillars (for example: tips, behind the scenes, results, answers to common questions). Or a source to repurpose: a blog URL, a YouTube video, a podcast transcript, notes.
- Capacity: how many videos they can actually film per week, and whether they prefer talking head, voiceover, screen recording or slideshows.
- Timezone, the weeks to cover, and preferred posting times.

Never invent results, customers or numbers for the posts.

## Build the plan

- Frequency: match capacity. Consistent beats occasional bursts. If filming is the bottleneck, fill gaps with slideshows (`tiktok-slideshow-maker`), which need no camera.
- Rotate pillars so no two adjacent posts feel the same.
- Repurposing: split the source into single ideas. One idea per TikTok. A 1,500-word article usually yields several posts: each tip, the main mistake, a before/after, a myth, a quick how-to.
- Series: when an idea has parts, number them ("Part 1 of 3") so viewers come back.
- Posting times: use the user's audience timezone. If they have no data, spread times across the day and suggest they compare results in TikTok's analytics.

## Draft every slot

For each slot, write:
- Date, time and timezone.
- Format: video or slideshow.
- Hook (see `tiktok-hook-generator`).
- Script outline or slide plan (see `tiktok-script-generator`, `tiktok-slideshow-maker`).
- Caption with 3–5 hashtags (see `tiktok-caption-generator`), under 2,200 characters.
- Settings if any: `privacy`, `comments`/`duet`/`stitch` off, `publish_mode`.

Return the plan as a table (date, time, pillar, format, hook, status), then the full drafts.

## Schedule it

Scheduling needs the finished media. On approval:
1. Confirm the TikTok account (`list_accounts`) and the timezone.
2. For each slot with media ready: upload with `create_upload_url`, then `create_post` with `media` and `publish_at` as an ISO timestamp with offset.
3. For slots still being filmed, save the caption and notes with `create_draft` so they're ready when the video is.
4. Report each post ID and status with `get_post`. Scheduled is not published; say which is which.

Offer `publish_mode: "draft"` for creators who want to add a TikTok sound or edit in the app before it goes live. Note that video drafts arrive without the caption.
