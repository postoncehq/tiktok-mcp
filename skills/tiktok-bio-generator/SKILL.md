---
name: tiktok-bio-generator
description: Write TikTok bio options that fit TikTok's 80-character limit and tell a visitor who you are, what you post and why to follow. Use when the user asks for a TikTok bio, bio ideas, a TikTok bio generator, or to rewrite their TikTok profile bio.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok bio generator

A TikTok bio has 80 characters to turn a profile visit into a follow. This skill writes the text; the user pastes it into their TikTok profile themselves. The PostOnce MCP publishes posts and can't edit TikTok profiles.

## Before writing

Get or infer: the creator or brand name, the niche, who the content is for, what they post and how often, one proof point if they have a real one (a job title, a result, a credential), and where the link in bio goes, if they have one. Never invent follower counts, awards or results.

## What a good bio does

Answer, in this order of priority:
1. What you post, in the words your audience uses ("Budget meal prep", "iPhone editing tips").
2. Who it's for or what they get ("for busy students", "weekly lunches under $5").
3. One reason to trust you or a reason to follow now ("Chef, 10 yrs in kitchens", "New recipe every Sunday").
4. A pointer to the link, only if there is one ("Free meal plan ↓").

Rules:
- 80 characters maximum, counting spaces and emoji. Count every option.
- Line breaks are allowed and often read better: one idea per line.
- One or two emoji at most, used as bullets or pointers, not decoration.
- Put the niche keyword in the bio. It helps people who find the profile understand it at a glance.
- Plain, specific words. Skip "Living my best life", "Dreamer", quotes and vague slogans.
- A brand account can still sound like a person.

## Output format

Give 5 options in different styles (straightforward, benefit-led, proof-led, playful, series-led), each in a code block exactly as it should be pasted, with its character count. Recommend one and say why in a line.

## Output

Tell the user to paste the chosen bio in TikTok under Edit profile. Offer next steps that the MCP can do: plan the posts the bio promises with `tiktok-content-calendar`, or publish one now with the `postonce` skill.
