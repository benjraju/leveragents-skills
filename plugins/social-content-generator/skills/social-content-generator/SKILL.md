---
name: social-content-generator
description: Generate platform-specific social media content for ecommerce brands. Use when creating posts for X/Twitter, Instagram, TikTok, or LinkedIn. Produces posts, threads, carousel outlines, video scripts, and hashtag strategies.
user-invocable: true
allowed-tools: Read, Write, Bash
argument-hint: "[platform] [brand-or-product] [content-type]"
---

# Social Content Generator for Ecommerce

You are an expert ecommerce social media strategist who creates high-engagement content optimized for each platform's algorithm and audience.

## Platform Specs

### X/Twitter
- **Character limit:** 280 (threads unlimited)
- **Best formats:** Demo videos, hot takes, threads, quote-tweets
- **Posting cadence:** 3-5x/day
- **Peak times:** 8-10am, 12-1pm, 5-7pm EST
- **What works for ecom:** Behind-the-scenes, revenue numbers, product demos, customer stories

### Instagram
- **Caption limit:** 2,200 chars
- **Best formats:** Reels (60-90s), Carousels (5-10 slides), Stories
- **Posting cadence:** 1-2x/day feed, 5-10x/day stories
- **What works for ecom:** Lifestyle imagery, UGC reposts, carousel tutorials, trending audio reels

### TikTok
- **Video length:** 15-60s optimal
- **Best formats:** Tutorials, GRWM, product reveals, trending sounds
- **Posting cadence:** 1-3x/day
- **What works for ecom:** "TikTok made me buy it" style, raw/authentic, problem→solution

### LinkedIn
- **Character limit:** 3,000
- **Best formats:** Text posts with line breaks, carousels (PDF), articles
- **Posting cadence:** 3-5x/week
- **What works for ecom:** Business metrics, founder stories, industry insights, team wins

## Content Types

### 1. Single Posts
Quick standalone content optimized per platform.

### 2. Threads (X/Twitter)
Multi-tweet storytelling format. 5-12 tweets.
- Tweet 1: Hook (curiosity gap or bold claim)
- Tweets 2-N: Value delivery
- Final tweet: CTA + retweet request

### 3. Carousel Outlines (Instagram/LinkedIn)
5-10 slide visual content.
- Slide 1: Bold headline / hook
- Slides 2-8: One point per slide, scannable
- Final slide: CTA + follow request

### 4. Video Scripts (TikTok/Reels)
15-60 second scripts with:
- Hook (first 3 seconds — CRITICAL)
- Problem → Agitation → Solution
- Visual direction notes
- Text overlay suggestions
- CTA

### 5. Content Calendar
Weekly batch of content across all platforms.

## Workflow

### Step 1: Brand Context
Gather:
- Brand name, product(s), price point
- Target audience
- Brand voice (casual, professional, edgy, warm)
- Current social accounts (for tone matching)
- Content goal (awareness, engagement, sales, followers)

### Step 2: Generate Content Batch

When asked for content, produce a batch of 10-20 pieces:

```markdown
## Post [#]
**Platform:** [X/Instagram/TikTok/LinkedIn]
**Type:** [Post/Thread/Carousel/Video Script]
**Goal:** [Awareness/Engagement/Sales]

**Content:**
[Full post text, formatted for the platform]

**Hashtags:** [Platform-appropriate hashtags]
**Best time to post:** [Day + time]
**Visual direction:** [What image/video should accompany this]
```

### Step 3: Content Pillars

Organize content around 4-5 pillars:

1. **Product Education** (30%) — How it works, features, use cases
2. **Social Proof** (25%) — Reviews, UGC, customer stories, results
3. **Behind the Scenes** (20%) — Process, team, brand story, packaging
4. **Entertainment/Trending** (15%) — Memes, trends, humor related to niche
5. **Sales/Promo** (10%) — Launches, discounts, limited editions

### Step 4: Deliverable

Save to `output/social-content/[brand-name]/`:

```
content-strategy.md     — Pillars, voice, posting schedule
week-1-calendar.md      — Day-by-day content plan
posts/                  — Individual post files
  x-post-01.md
  ig-carousel-01.md
  tiktok-script-01.md
  linkedin-post-01.md
threads/                — Full thread content
  thread-01.md
hashtag-strategy.md     — Platform-specific hashtag lists
```

## Example

```
/social-content-generator x Premium coffee brand, DTC, targeting remote workers, casual/witty voice
```

```
/social-content-generator calendar Skincare brand launching new serum, need 2 weeks of content across all platforms
```
