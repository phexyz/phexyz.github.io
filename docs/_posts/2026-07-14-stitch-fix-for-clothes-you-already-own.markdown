---
layout: post
title: "Stitch Fix, but for the clothes you already own"
date: 2026-07-14 00:00:00 -0400
tags: [idea]
---

Stitch Fix sells you *new* clothes. But most people don't need more clothes — they need to know what to wear with what they already have. The bottleneck isn't supply, it's decision.

So: a subscription that styles your *existing* wardrobe, every day.

You scan your closet once. Every morning the app pushes an outfit — these pants, that shirt, those shoes. Weather-aware, calendar-aware (gym day vs. client dinner), laundry-aware (don't re-suggest what you wore Tuesday).

Inspiration: [this app](https://x.com/cdngdev/status/2076812846793650485).

## Why now

Multimodal models can actually *see* clothes — cut, colour, fabric, formality. Wardrobe digitisation used to be the wall. It isn't anymore. And once the wardrobe is digitised, the taste problem collapses into a ranking problem, and ranking improves with data.

## The business model

Subscription for the daily outfit — $5–15/mo. That's the honest product, and it has to stand on its own.

The upsell is where it gets interesting. The model knows your *gaps*: "your wardrobe has no versatile mid-layer — six new outfits unlock if you own one grey crewneck." That is a commerce recommendation with far more intent behind it than any Stitch Fix box. You earn the right to sell clothes by first being useful without selling them.

## The hard parts

**Onboarding friction.** Photographing sixty garments is a chore, and it sits between the user and any value at all. This kills most users before they experience the product. Mitigations: bulk photo with auto-segmentation, import from order history, or progressive onboarding that starts with ten items.

**Taste is personal.** A generically "correct" outfit that isn't *you* feels worse than no suggestion at all. Needs a fast feedback loop (wore it / didn't) and probably an explicit style archetype at signup.

**Retention.** A daily push is a daily chance to churn. Once users learn their own five good combinations, do they still need this? The counter-argument is novelty, occasions, seasonality, and the fact that wardrobes change.

**Cold start per user**, not just per platform. Every new signup is a fresh cold start.

## The wedge

Pick one user who feels the pain acutely and has money. Probably: people who dislike shopping and dislike deciding, or people onboarding into a new job, city, or climate. Don't launch as "for everyone."

## Open questions

- Standalone subscription, or a feature inside an existing commerce app — which would simply eat it?
- Does it need social? Outfit ratings, friend feeds, "what people with your wardrobe wear." Could be the retention engine or a distraction.
- Physical adjunct: partner with dry cleaners to scan the wardrobe at pickup?
