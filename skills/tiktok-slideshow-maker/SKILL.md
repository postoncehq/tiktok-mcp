---
name: tiktok-slideshow-maker
description: Plan, write and build a TikTok photo-mode slideshow (carousel of up to 35 images at 1080×1920 or 1080×1440) with its caption, then publish it with the PostOnce TikTok MCP. Use when the user asks for a TikTok slideshow, photo mode post, TikTok carousel, slideshow maker, or to turn a list, guide, thread or article into TikTok slides.
metadata:
  author: PostOnce
  version: "0.1.0"
---

# TikTok slideshow maker

TikTok photo posts show images the viewer swipes through. This server publishes 1 to 35 images per post, JPEG or WEBP, up to 20 MB each. It can't mix photos and video in one post, and it can't choose the sound: TikTok adds music to photo posts automatically. If the user wants a specific sound, post with `publish_mode: "draft"` and pick it in the app.

## Sizes

- 1080×1920 (9:16): fills the screen. Default.
- 1080×1440 (3:4): leaves room around the image; good for photos and screenshots.

Use one size for every slide. Keep text in the middle of the frame, clear of the top edge and the bottom fifth, where the caption and buttons sit.

## Plan the slides

Most slideshows work at 5–10 slides. Write the plan before any design:

| Slide | Job | Words |
| --- | --- | --- |
| 1. Cover | The hook. Names the viewer, a number or the result. Must make someone swipe. | 10 or fewer |
| 2–N. Body | One point per slide, numbered if it's a list. | 8–25 each |
| Last | The takeaway, or one ask (save it, follow for more). | 12 or fewer |

Rules that hold up:
- Big, high-contrast text. It must be readable on a phone without zooming.
- Same layout, font and color on every slide so it reads as one piece.
- Real photos, screenshots and examples beat stock images.
- Put the payoff on the slides, not only in the caption.

## Making the images

If the environment can render HTML to images (headless Chrome or Playwright), build each slide as a fixed-size HTML page at 1080×1920 (or 1080×1440) and screenshot it as JPEG, since TikTok photo posts don't accept PNG. Otherwise, hand the user the slide text and layout notes for their design tool, with the export size and format.

If the user already has images, check the count (35 max), format (JPEG or WEBP) and order.

Upload each image with `create_upload_url` and pass the public URLs in slide order as `media` (all `type: "image"`) in `create_post`. The first image is the cover.

## Caption

Write it with `tiktok-caption-generator`: the search phrase in the first line, one line on what the slides deliver, 3–5 hashtags. Keep it under 2,200 characters. For a draft, `platform_options.title` (up to 90 characters) sets the photo post title.

## Output

Return the slide plan (number, headline, supporting text, visual note), the size, then the caption. Once the images exist, offer to publish or schedule with the `postonce` skill; confirm the TikTok account, the time and `privacy` before calling `create_post`.
