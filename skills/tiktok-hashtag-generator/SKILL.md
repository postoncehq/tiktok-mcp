---
name: tiktok-hashtag-generator
description: Pick 3 to 5 relevant TikTok hashtags for a video or slideshow, mixing a broad topic tag with specific niche tags that match what people search. Use when the user asks for TikTok hashtags, a TikTok hashtag generator, which tags to use, or to fix a caption's hashtags.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok hashtag generator

Hashtags on TikTok work as labels. They help TikTok understand who the video is for; they don't make a weak video spread. Posts through this server keep at most 5 hashtags. Any beyond 5 are removed automatically, so choose on purpose.

## Before choosing

Get or infer: what the video shows, the niche and audience, and the search phrase the caption targets. If the user has a caption already, read it first. Only use tags that describe the actual content.

## How to build the set

Pick 3–5 from these layers:

| Layer | Purpose | Example (a meal prep video) |
| --- | --- | --- |
| Topic | What the video is about | #mealprep |
| Specific | The exact angle or format | #mealpreplunch, #budgetmeals |
| Audience or community | Who it's for, as that group tags itself | #studentmeals |
| Keyword echo | The caption's search phrase as a tag, when people actually use it | #easylunchideas |

Rules:
- Specific beats huge. A tag with a clear audience helps more than a giant generic one.
- Skip #fyp, #foryou, #viral and similar. They describe nothing.
- Don't repeat near-duplicates (#mealprep, #mealprepping, #mealpreps).
- Lowercase, no spaces, no punctuation. Use camel case only if it helps readability for long tags.
- Brand or series tag: include one only if the user already uses it consistently.
- Never use a tag that misrepresents the video.

You can't check live tag volumes through this server. If the user wants to validate, suggest they type each tag in TikTok search and look at the related suggestions and recent videos.

## Output format

Return the recommended set on one line, ready to paste at the end of the caption. Under it, one line per tag saying which layer it covers. Offer one alternate set with a different angle.

## Output

Offer to add the tags to the caption and publish or schedule with the `postonce` skill. Confirm the TikTok account and the time before calling `create_post`.
