---
name: tiktok-caption-generator
description: Write TikTok captions built for TikTok search (TikTok SEO), with the keyword up front, useful context, a call to action and up to 5 hashtags, ready to post with the PostOnce TikTok MCP. Use when the user asks for a TikTok caption, a caption generator, TikTok SEO, or a description for a TikTok video or slideshow.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok caption generator

People search TikTok like a search engine. A good caption tells TikTok and the viewer what the video is about in words people actually type.

## Before writing

Get or infer: what the video or slideshow shows, the audience, and the phrase someone would search to find it ("easy meal prep lunches", "how to edit reels on iphone"). If the user shares a script or transcript, pull the keyword from what's actually said. Never add claims the video doesn't make.

## Rules

- Put the main search phrase in the first line, naturally. The first line shows before "more"; make it readable on its own.
- Say the phrase on camera and put it in on-screen text too, if the user can still edit the video. TikTok reads all three.
- Add one line of context or value: what the viewer gets, a step, a detail.
- One call to action at most: save it, follow for part 2, or answer a specific question in the comments.
- Short. 1–3 lines works for most videos. The limit through this server is 2,200 characters; text past that is cut off.
- Hashtags: 3–5, at the end. More than 5 are removed automatically. Mix one broad topic tag with specific niche tags. Use `tiktok-hashtag-generator` for the set.
- Plain words. No "game-changer", no emoji walls, no stacks of generic tags like #fyp #viral that say nothing about the video.

## Slideshows

For photo posts the caption does more work because there's no voiceover. Summarize what the slides deliver in the first line, then add the one detail that makes someone swipe.

## Drafts

If the user will post with `publish_mode: "draft"`, a video arrives in their TikTok inbox without its caption. Give them the caption as a block to paste in the app.

## Output format

Give 3 options, each exactly as it will appear (caption, then hashtags). Under each, one line naming the search phrase it targets. Recommend one.

## Output

Offer to publish or schedule with the `postonce` skill: confirm the TikTok account, the time and any settings (`privacy`, `comments`, `duet` or `stitch` set to `false`) before calling `create_post`.
