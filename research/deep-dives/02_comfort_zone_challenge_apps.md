# 02 — Comfort-Zone, Courage & Real-World Challenge Apps: Competitive Landscape

*Research date: 22 Nov 2026. Scope: apps that push people out of their comfort zone through daily challenges, dares, quests, rejection therapy, social exposure, novelty and adventure prompts. Adjacent categories are included where they compete for the same user motive: gamified exploration, IRL social, bucket lists, clinical exposure tools, life-RPGs, cold exposure and kindness challenges.*

---

## 0. Method, sources and caveats

- **App Store data** comes from the iTunes Search API (about 95 search terms) and the Lookup API, both US storefront, pulled 22 Nov 2026. I also sampled recent reviews from the public customer-reviews RSS feed for about 24 apps and fetched App Store pages for in-app-purchase prices. Each figure is given as **"iOS ★ rating (number of ratings)"**. These are the *current-version-weighted* US counts the API reports.
- **Google Play data** comes from `google_play_scraper` (search plus `app()` detail, US/en): score, number of ratings and the install bucket, plus `realInstalls` (GP's internal exact count) where it was returned. Written as **"GP ★ (installs)"**.
- **Web sources** (TechCrunch, NPR, CBC, CNBC, Axios, Bustle, Wikipedia, company sites) are named inline. When a figure is a third-party *estimate* (AppGoblin, Screensdesign, a Substack, Dealroom) I say so.
- **Reddit was not directly accessible.** Reddit blocks this environment's user agent and the search tool refuses reddit.com. User sentiment therefore comes from App Store and Play reviews plus secondary write-ups. Treat "Reddit says…" claims elsewhere with caution. I have not invented any.
- **"Delisted"** means an App Store ID that appears in search-engine indexes or older listings no longer resolves through the Lookup API in the US, GB or PY storefronts. That most likely means the app was removed.
- I found **no app** for these seed names: "Uncomfy", "Get Out There", "Dared", "Kiddo" (anxiety), "Brrr" (cold exposure: the name belongs to an unrelated push-notification utility) or a "Yes Theory / Seek Discomfort" app. Yes Theory runs a WhatsApp challenge community and sells "Challenge Accepted" merch, not an app (yestheorycommunity.substack.com). "Bravely" is a workplace-coaching company (Bravely Inc.), not a courage app.

---

## 1. Landscape at a glance

| # | App | Developer / country | Launch | iOS ★ (ratings) | GP ★ (installs) | Model | Status (Nov 2026) |
|---|---|---|---|---|---|---|---|
| 1 | Rejection Therapy (card game) → **Rejection+** app | Jason Comely (CA) → Jia Jiang / Rejection Therapy Inc. (US) | game 2009–10; app 31 Dec 2025 | 5.0 (1) | — (iOS only) | $29.99/mo, $99.99/yr | Alive but almost no traction |
| 2 | **Rejectionmax** | Aidan Riehl (US) | Jul 2026 | 4.89 (27) | — | $7.99/wk, $79.99/yr | Alive, actively shipping |
| 3 | **Freewill: Social Confidence** | Freewill Labs LLC (TN, US) | Jul 2026 | 4.95 (21) | — | $5.99/mo, $39.99/yr | Alive, shipping weekly |
| 4 | Get Rejected (1000 Rejections) | Eugene Hennie | Mar 2026 | 5.0 (3) | — | freemium packs | Alive, early |
| 5 | 100 Rejections: Overcome Fear | Axel Sars Groener | Nov 2025 | 5.0 (2) | — | freemium, AI challenges | Stalled (last update Dec 2025) |
| 6 | Rejection Therapy: Confidence | Stijn Braams (NL) | Oct 2025 | 3.0 (2) | — | subscription | Low traction |
| 7 | **IDareTo – Comfort Zone Crusher** | Addmec AB (SE) | Mar 2016 | not found in US iOS | 4.0 (10k+; 14,386) | **$3.99 paid** | Long-lived, small |
| 8 | YesChallenges – seek discomfort | Kenja | Apr 2021 | — | 4.33 (1k+; 3,630) | free | Dormant |
| 9 | Boldly: Comfort Zone Challenge | Savyo Brenner Barboza Santos | Jun 2026 | 0 ratings | — | freemium + Pro | Alive, no traction |
| 10 | DISCOMFRT | Robert Makar | Nov 2026 | 5.0 (1) | — | free | Brand new |
| 11 | Push: Comfort Zone Missions | Benayaho Nissanian | Mar 2026 | 0 | — | free | Single release, abandoned |
| 12 | Diss Comfort | PragmaTec (FI) | May 2026 | 0 | — | free | Single release, abandoned |
| 13 | Sidequest – Social challenges | Jonah Kalkman | Apr 2025 | 0 | — | free | Single release, abandoned |
| 14 | Sidequest Everyday | Jakub Sejkora (CZ) | Jan 2026 | 5.0 (5) | — | — | Alive |
| 15 | **Leap: Daily Social Challenge** | Inesh Pulugurtha (US) | Jun 2026 | 5.0 (17) | — | free | Stalled since 14 Jun 2026 |
| 16 | DareDash – Daily Social Dares | Roger You | Jun 2025 | 4.71 (14) | — | free | Stalled since Jul 2025 |
| 17 | Gontlet: Daily Dare Challenge | Ryan August Abraham | Jun 2026 | 5.0 (2) | — | free | Early |
| 18 | unrue: Daily Real World Quests | Joshua de Souza | Jul 2026 | 0 | — | free | Early |
| 19 | Dare Zone (Yope Challenges) | Salo App, Inc. (yope) | Jun 2023 | 3.29 (7) | — | free | Dead (last update Sep 2023) |
| 20 | DARE – Photo challenge | Livehouse Ltd (LiveIn) | Mar 2023 | 2.8 (5) | — | free | Dead (last update Mar 2023) |
| 21 | Challenge Accepted | Challenge Accepted Ltd (UK) | Jul 2020 | 4.67 (3) | 4.0 (10k+; 45,987) | free | Alive, low engagement |
| 22 | **SideQuest: Tiny Adventures** | OMG Career, LLC | Sep 2026 | 5.0 (9) | — | $7.99/wk, $9.99/mo, $29.99–34.99/yr, packs | Alive, shipping fast |
| 23 | Sidequests HQ | Blinq Software LLC | Oct 2025 | 4.86 (7) | — (1k+; 2,106) | — | Alive |
| 24 | **Sidequest: Explore Your City** | Riley Palattao (knowaspot) | Mar 2026 | 4.37 (222) | — | $9.99/mo, $17.99–29.99/yr | Alive, paywall backlash |
| 25 | **SideQuest: Nearby Activities** | Adhish Paranjothi / SideQuest Inc | Mar 2026 | 4.68 (19) | 4.88 (10k+; 20,048) | IAP $4.99–99.99 | Alive |
| 26 | SideQuest: Explore & Challenge | Colden Bjorn Johnson | Oct 2025 | 5.0 (5) | — | free | Alive, tiny |
| 27 | 2026 "side quest" long tail (Syde, Venture, Kuji, Opia, SideQ, WeirdQuest, 5ideQuest, Wander, Firsts, Branch Out, Flypp, nudge., BeThere, Twistday, QuestDay, Daily Side Quests, Mapside, Quester…) | various solo devs | 2025–26 | mostly 0–6 ratings | mostly <1k | mostly freemium | Flood of micro-launches |
| 28 | **outernet: go outside & explore** | Outernet Explorer Inc. (US) | Mar 2026 | 4.90 (288) | — | free | Alive, waitlist, TechCrunch-covered |
| 29 | Wim – An Adventure Awaits | WimNow, Inc. | Aug 2026 | 5.0 (6) | — | free | Early |
| 30 | DoSomething – Daily Challenges | Entermaurs Inc. | Feb 2025 | 0 | — | free | Dead (last update Apr 2025) |
| 31 | **Randonautica** | Randonauts LLC/Co. (US) | Feb 2020 | 3.57 (13,499) | 4.65 (10M+; 21.4M) | points + Pro sub | Alive, past peak, "trialslop" complaints |
| 32 | **Pokémon GO** | Niantic → Scopely (2025) | Jul 2016 | 4.0 (657k) | 3.46 (500M+; 568M) | F2P IAP | Alive, giant |
| 33 | **Pikmin Bloom** | Niantic/Nintendo → Scopely | Oct 2021 | 4.81 (71k) | 4.76 (5M+; 9.4M) | F2P IAP | Alive |
| 34 | **Geocaching®** + Adventure Lab | Groundspeak (Seattle) | 2009 (app) | 4.83 (66.6k) | 4.58 (10M+; 23.3M); Lab 4.77 (761k) | Premium sub | Alive, durable |
| 35 | Seek by iNaturalist | iNaturalist (non-profit) | 2018 | 4.75 (30.9k) | 3.40 (1M+; 4.36M) | free | Alive |
| 36 | Fog of World | Ollix (TW) | 2012 | 4.81 (3,138) | 3.58 (10k+; 16.6k) | $30 one-time | Alive, cult |
| 37 | Let's Roam: Scavenger Hunts | Lets Roam LLC (US) | 2018 | 4.74 (18,005) | — | per-hunt / sub | Alive |
| 38 | Questo | Questo Global SRL (RO) | 2017 | 4.78 (2,974) | 4.44 (100k+) | per-quest | Alive |
| 39 | Atlas Obscura | Atlas Obscura Inc. (US) | 2021 (app) | 4.85 (9,955) | 4.84 (100k+) | free / membership | Alive |
| 40 | 1000 Hours Outside | Team Yurich LLC | 2021 | 4.77 (7,822) | 4.56 (10k+) | freemium | Alive |
| 41 | SideQuest – Walk & Level Up | Gaurav Vyas | Jan 2026 | 4.94 (220) | 4.9 (1k+; 1,745) | IAP | Alive, well loved |
| 42 | The Bucket List App | The Bucket List Studios (Bucket List Family) | Nov 2024 | 4.94 (924) | 4.85 (10k+; 19.9k) | IAP $4.99–239.99 | Alive |
| 43 | BucketListers | Bucket Listers Inc. | 2022 | 4.66 (3,311) | — | ticket commerce | Alive (events marketplace) |
| 44 | Bucket List – The Bucket App / iBucket / Bucketlist (B.C.) | Trent Wann / PuurPuur / 0952915 B.C. | 2020 / 2015 / 2018 | 4.65 (715) / 4.55 (83) / 2.45 (11) | iBucket 10k+ | freemium | Alive / Alive / Neglected |
| 45 | The Adventure Challenge (books) | The Adventure Challenge (US) | ~2019 | no standalone app found | — | $40–50 physical books | Alive (physical product) |
| 46 | **Timeleft** | Timeleft SAS (FR) | Dec 2023 (app) | 4.62 (9,141) | 4.28 (1M+; 1.25M) | $19.99–62.99 sub/tickets | Alive, scaled |
| 47 | **222** | TwoTwoTwo Inc. (YC, US) | Feb 2024 | 4.68 (7,845) | not found on GP | ~$22/mo membership + fees | Alive, funded |
| 48 | Meetup | Meetup LLC (Bending Spoons-owned) | 2010 | 4.72 (272.7k) | 3.85 (10M+; 22.5M) | organizer subs, Meetup+ | Alive |
| 49 | Bumble BFF | Bumble | 2020 (standalone) | 4.21 (9,063) | — | freemium | Relaunched Sep 2025 on Geneva |
| 50 | Pie | Pie Labs, PBC | 2021 | 4.77 (1,533) | — | free | Alive |
| 51 | Wakie | Wakie Inc. | 2014 | 4.53 (18.8k) | 4.37 (10M+; 10.2M) | IAP | Alive |
| 52 | BeReal | BeReal → Voodoo (2024) | 2020 | 4.77 (1.16M) | 4.55 (10M+; 38M) | free | Alive, post-hype |
| 53 | MindShift CBT | Anxiety Canada (built by 247 Labs) | 2013 | 4.35 (579) | 3.74 (500k+; 828k) | free | Alive |
| 54 | Joyable | Joyable (US) | 2014 | — | — | employer B2B | Acquired by AbleTo, 2019 |
| 55 | DARE: Anxiety & Panic Relief | BMD Publishing (IE; Barry McDonagh) | 2015 | 4.84 (6,939) | — | sub | Alive |
| 56 | Exposure – Face Your Fears / FearTools | Inquiry Health LLC | 2016 | 4.14 (7) / 4.84 (145) | FearTools 4.3 (50k+) | free | Abandoned (2017 / 2021) |
| 57 | FearLadder – Face Fears | 丽佳 施 | Aug 2026 | 0 | — | free | New |
| 58 | Social-anxiety exposure cluster: UNSHY, PebbleStep, Social Anxiety Quest, FACING IT, SocialEase, Beat Social Anxiety Challenge, Hatchr, iNTRPT, Bold AF | various | 2022–26 | 0–42 ratings each | SocialEase 15.6k; FACING IT 7.2k | subs, weekly plans | Mostly small; FACING IT abandoned |
| 59 | AI social-skill coaches: **Gleam**, Magneta, Social Wizard, Make Me Social, EdgeLab, Cringe, Socially, Solis Quest, Social XP, CharmXP | various | 2024–26 | Gleam 4.74 (12,255); Magneta 4.92 (47k); Social Wizard 4.84 (6.7k) | Gleam 100k+ | $10–13/mo, $40–90/yr | Booming, heavy paywalls |
| 60 | SuperBetter | SuperBetter LLC (Jane McGonigal) | 2012 | 4.65 (7,883) | 4.04 (100k+) | $24.99/yr Hero | Pivoted to education |
| 61 | Habitica / Finch / Lion XP / Earth Online | HabitRPG / Finch Care PBC / POXI AS / Pei-Tzu Huang | 2013 / 2021 / 2024 / 2026 | 4.33 (3.7k) / 4.95 (778k) / 4.49 (313) / 4.78 (85) | 5M+ / 10M+ / — / — | freemium | Alive |
| 62 | Cold exposure: Wim Hof Method, GoPolar, IceBuddy, Brisk, PlungePalz, ColdStreak… | WHM Services / various | 2014–26 | WHM 4.86 (13.8k); GoPolar 4.67 (317) | tiny | sub | Alive, niche |
| 63 | Kindness: BeKind, The Great Kindness Challenge, ~10 2026 micro-apps | TeamEXtension / ExaMobile / various | 2014–26 | BeKind 4.70 (114) | BeKind 4.67 (5k+; 8.8k) | free | BeKind alive; GKC dead (2018) |
| 64 | Gloop / Challenger / Dare: AI Photo | Gloop LLC / William Leaf / Bounty Studio | 2026 / 2020 / 2026 | 4.73 (15) / 5.0 (6) / 5.0 (12) | — | free | Small |
| — | **Delisted** comfort-zone apps: Daily Dare, EaseUp, Challenge: Your Best Version, Roadmap (social-anxiety "miles" game), Discomfort Zone, Fearless Life, Sidequest – Social Adventures | various | 2014–25 | IDs no longer resolve | — | — | **Dead / removed** |

---

## 2. Direct competitors: rejection therapy, dares and comfort-zone challenge apps

### 2.1 Rejection Therapy (Jason Comely's card game) → Rejection+ (Jia Jiang's official app)
- **Developer and history.** Jason Comely, a freelance IT consultant from Cambridge, Ontario, invented the game around 2009–2010 during a lonely stretch after a breakup. He printed 30-card decks, each card describing a way to get rejected that day, and sold them online for about $10. NPR (Jan 2015, Dec 2015) called it "a small cult phenomenon", and CBC profiled it in 2015. Jia Jiang's "100 Days of Rejection" (2012–13) went viral; his TEDx talk passed 10M views and his book *Rejection Proof* followed in 2015. Jiang **acquired Rejection Therapy in 2016**, and rejectiontherapy.com now sells Classic, Blue Pill and Entrepreneur editions plus PDFs (Wikipedia; rejectiontherapy.com; NPR). A 2014 article described an earlier beta app (Business101), and one source names an older iOS app "DareMe". Neither became a product of any size.
- **App.** "Rejection Therapy™" (branded Rejection+), developer Rejection Therapy Inc., iOS only, Education category, v1.0 released **31 Dec 2025**, last update v1.6 on 26 Mar 2026.
- **Core loop.** "Make bold, respectful asks — and learn from the answers," with a "Classic challenge" mode that mirrors the cards. The listing gives few details.
- **Challenge generation.** Curated: the existing card corpus plus Jia's system.
- **Difficulty, proof, social.** Not specified. Proof appears to be the honor system.
- **Monetization.** Free download with a trial. **$29.99/month or $99.99/year**, the most expensive subscription in the niche.
- **Traction.** iOS ★5.0 from **1 rating**. Not on Google Play.
- **Press.** The concept has huge press (NPR, TED, the book); the app itself has had essentially none.
- **What users love.** The concept is legendary. Jia's "51 yes / 49 no" story is the best-known proof that asking works (BYU Magazine).
- **Complaints and status.** No app reviews exist yet. The app is alive but looks dormant after March 2026. **Lesson: the strongest brand in the niche failed to turn into app usage.** A premium price, no visible game loop, iOS only and no distribution push.

### 2.2 Rejectionmax
- **Developer.** Aidan Riehl (indie, US). iOS. First version Jul 2026; v2.1.9 on 11 Nov 2026, with frequent releases.
- **Concept.** "The Duolingo of Social Confidence."
- **Core loop.** Users get **8 challenges a week and must complete 5 to "beat the week."** Examples include complimenting a stranger or asking for a discount. A short lesson on social anxiety and rejection follows each challenge, and the program runs for 50 days.
- **Difficulty progression.** At the end of each week users rate how hard it was. Harder challenges unlock "only once your current ones become so easy they bore you." This is user-paced exposure titration.
- **Proof.** Honor system. **Social:** "progress tracking with friends," plus a home-screen widget.
- **Monetization.** Weekly $7.99 or annual $79.99, discounted to $39.99–49.99. Subscriptions arrived in v2.1.2 (Sep 2026).
- **Ratings.** iOS ★4.89 (27). Reviews are uniformly 5★: "made three new friends in two days," "fear of rejection used to rule my life." One reviewer says a friend built the app and asked for the review, so treat early ratings as partly friends-and-family.
- **Status.** Alive.

### 2.3 Freewill: Social Confidence
- **Developer.** Freewill Labs LLC (Tennessee). iOS. v1.0 on 24 Jul 2026, then 11 releases in four months.
- **Core loop.** **One small real-world challenge a day**, taking about 5 minutes: "say hi to the barista," "speak up once in class." Users accept it in the morning and **predict how hard it will be**, then rate how it actually went afterwards. That prediction-versus-outcome gap, borrowed from CBT behavioural experiments, is the core mechanic. The app describes itself as "built on exposure therapy and CBT, turned into a daily habit."
- **Game mechanics.** A **hermit-crab pet** that comes out of its shell across 7 levels, streaks, Streak Restores (2 a month on Pro), friend streaks, weekly quests with a friend, nudges, invite rewards and share cards.
- **Social.** "The Cove," a pseudonymous community with topic rooms (Small Talk, Dating, Work) where users post outcomes and send "Snaps" when someone does something brave.
- **Challenge generation.** Curated. "Free roam after Day 21 with 90 new challenges."
- **Proof.** Honor system.
- **Monetization.** First 3 challenges free, a "Lite" tier, then **$5.99/month or $39.99/year** with a 3-day trial.
- **Ratings.** iOS ★4.95 (21). "Saw this app on Instagram… 8 days in and I already feel a difference," "a little hermit crab telling you to get out there is all you need."
- **Status.** Alive, and the most thoughtfully designed product in the direct niche: a Finch-style pet combined with CBT prediction logging and community. It is very early.

### 2.4 Get Rejected (1000 Rejections Challenge)
- **Developer.** Eugene Hennie, with the site 1000rejections.app. iOS, Mar 2026.
- **Content.** **500 challenges in 50 themed packs**, 3 tiers (Warm-Up, The Push, No Fear) and 6 categories (sales, dating, career, social, creative, custom). Two packs are free and no sign-up is needed. Users can log any rejection in three taps.
- **Game mechanics.** Streaks with a grace period, an emotional log and milestones at 50, 100 and 1000 rejections.
- **Positioning.** "Exposure therapy disguised as a game."
- **Ratings and status.** iOS ★5.0 (3). Alive, and runs SEO content ("Rejection Therapy Results…").

### 2.5 100 Rejections: Overcome Fear
- Axel Sars Groener. iOS, Nov 2025; last update 1 Dec 2025.
- One "brave ask" a day with **Easy / Medium / Spicy** difficulty and arenas (Social, Work, Fitness, Dating, Online), **or AI-generated personalized challenges**. Users log outcome, notes and an optional **photo as evidence**, and the app "celebrates effort over perfection."
- ★5.0 (2). **Stalled.**

### 2.6 Rejection Therapy: Confidence (by Stijn Braams)
- iOS, Oct 2025. Uses the "Rejection Therapy" name but is a general social-skills coach: an ACT-based conversation-reflection coach, daily social prompts and "Speak Up Streaks." The copy still mentions "Thrive," a sign it was rebranded.
- ★3.0 (2). Low traction. **It shows how freely the rejection-therapy name is used and how weak the trademark is.**

### 2.7 IDareTo – Comfort Zone Crusher
- **Developer.** Addmec AB (Sweden). Released **Mar 2016**. Google Play, **paid at $3.99**; not found in the US iOS store today.
- **Concept.** A library of comfort-zone challenges aimed at social ease: speaking up, connecting, handling the spotlight. "Courage isn't something you're born with… one small challenge at a time."
- **Traction.** GP ★4.0 (85 ratings), **10k+ installs (14,386)** over about 10 years.
- **Status.** Alive and long-lived, but small. **This is the oldest surviving dedicated comfort-zone app I found, and its numbers set the realistic ceiling for an undifferentiated challenge list.**

### 2.8 YesChallenges – seek discomfort
- Developer Kenja. Google Play, Apr 2021. "Inspired from Yes Theory": day-to-day and weekly challenges.
- GP ★4.33 (18), 1k+ installs (3,630). **Dormant.** It shows Yes Theory's audience is not automatically reachable through app stores.

### 2.9 Boldly: Comfort Zone Challenge
- Savyo Brenner Barboza Santos, boldlynow.app. iOS, Jun 2026, v1.4.1 in Oct 2026.
- **Onboarding** asks 3 questions (what you want more of, what holds you back, how much time you have), then sends **one challenge a day at a time the user picks**. Categories are Social, Adventure, Creative, Presence, Bold and Spontaneous. Each challenge has clear steps and an estimated time.
- **Proof.** Photo plus a feeling note. **"Retro"**: a weekly or monthly collage and shareable video (Pro). Streaks and stats. "Better with a friend" lets two people take the same challenge.
- **Traction.** 0 US ratings.

### 2.10 DISCOMFRT
- Robert Makar, dailydiscomfort.app. iOS, released 9 Nov 2026.
- One personalized quest a day across social, adventure, spontaneity, independence, creativity and courage. **It deliberately has no streaks or leaderboards**, and photos and reflections stay private. ★5.0 (1).

### 2.11 Push: Comfort Zone Missions
- Benayaho Nissanian. iOS, single release on 6 Mar 2026.
- A "mission engine generates daily challenges tailored to your progress." Users log anxiety before and after, and an "Anxiety Map" shrinks over time. **XP and ranks from "Observer" to "Vanguard,"** streaks, and 5 categories (Social, Visibility, Discipline…).
- 0 ratings. Abandoned after launch, even though the design is decent on paper.

### 2.12 Diss Comfort
- PragmaTec (Finland). iOS, single release May 2026.
- A daily dare across Physical, Social, Mental and Discipline, with **SOFT / HARD / SAVAGE** difficulty, 3 shuffles a day and streaks. 0 ratings.

### 2.13 Sidequest – Social challenges (Jonah Kalkman, sidequest.quest)
- iOS, single release Apr 2025. A daily social challenge "to step outside your comfort zone." 0 ratings. Abandoned.

### 2.14 Sidequest Everyday
- Jakub Sejkora (CZ), sidequesteveryday.com. iOS, Jan 2026, many updates (v2.12.24).
- One tiny daily sidequest ("talk to a stranger, explore a street you've never walked, send a message you've been postponing"), with no feed. ★5.0 (5).

### 2.15 Leap: Daily Social Challenge
- **Developer.** Inesh Pulugurtha (taketheleap.app; reads like a student or very young founder). iOS, Jun 2026, last update 14 Jun 2026.
- **Core loop.** One **daily challenge for everyone; users post a video** and climb the **"Leaperboard."** "No follower counts, no filters." The **feed is gated until you post**, which reviewers singled out: "its barrier to entry… Forcing users to 'take the Leap.'" A 4 pm nudge shows how many people have already leaped. Posts go through moderation ("pending review"). Age rating 13+.
- **Proof.** Video. **Social.** Friends, likes and comments.
- ★5.0 (17). **Stalled after 2 weeks of updates.** BeReal-style mechanics but no growth engine.

### 2.16 DareDash – Daily Social Dares
- Roger You. iOS, Jun 2025, last update Jul 2025. "**The BeReal for Dares.** Overcome social anxiety step by step… while laughing at your friends doing the same."
- ★4.71 (14). One reviewer: "I haven't done any of the dares yet… I'm just unemployed and don't live in a place where people are actively outside." That points to a real constraint on context and density. **Stalled.**

### 2.17 Gontlet: Daily Dare Challenge
- Ryan August Abraham. iOS, Jun 2026.
- One dare each morning ("stand on one leg in a grocery store," "ask a stranger to rate your outfit"). Users **film it and submit to unlock the feed**. **One reroll a day, and a skipped challenge is gone for good.** Leaderboard and bonus "Roll Again" challenges.
- ★5.0 (2).

### 2.18 unrue: Daily Real World Quests
- Joshua de Souza. iOS, Jul 2026. **One quest a day, and everyone gets the same one.** Photo proof is required and the feed stays locked until you post. Explicitly "no decision fatigue." 0 ratings.

### 2.19 Dare Zone (yope Challenges)
- Salo App, Inc., the company behind yope (friends-only photos, 11k iOS ratings). iOS, Jun 2023 to Sep 2023.
- A "biggest collection of challenges." Users dare their squad, record proof that posts to yope, create their own challenges and compete on a leaderboard. ★3.29 (7).
- **Dead.** Even a funded social-app team with an existing friend graph couldn't make dares stick as a spin-off.

### 2.20 DARE – Photo challenge (Livehouse / LiveIn)
- Livehouse Ltd, makers of LiveIn (30k ratings). iOS, Mar 2023.
- One dare prompt pushed to every US user daily. Users post a photo, friends vote, and the winning photo goes to everyone's home screen. ★2.8 (5). **Dead within a month.**
- **Lesson:** the BeReal-for-dares format was tried by experienced Gen-Z social-app teams in 2023 and failed twice.

### 2.21 Challenge Accepted (UK)
- Challenge Accepted Ltd. iOS and Android, Jul 2020, still updated in Oct 2026.
- Discover, track and complete challenges: 30-day fitness, reading and travel wish lists, habit challenges. Hundreds of preset challenges, user-created ones and friend challenges.
- GP ★4.0 (10k+; 45,987). iOS ★4.67 (3).
- This is a generic challenge tracker, not courage-specific. **Alive but has low engagement** (3 written GP reviews).

### 2.22 Social-anxiety exposure cluster
| App | Dev / launch | Mechanic | Price | Traction / status |
|---|---|---|---|---|
| **UNSHY: Beat Social Anxiety** | Filippo Cecchi (IT), Oct 2025, unshy.app | "Gradual real-world challenges… one small action at a time"; progress/rating system, "daily confessions," meditation, community, achievements (v2.0) | Bewildering paywall: weekly $3.99–9.99, yearly $19.99–39.99, lifetime $24.99–59.99 | iOS ★4.5 (12); alive |
| **PebbleStep** | Steve Scott / Evil Sidekick Games, Jan 2026 | 40+ challenges in Social, Crowds and Mindfulness; anxiety logged before and after; "no therapist required" | — | ★3.0 (1) |
| **Social Anxiety Quest** | Tobias Lochau, Jul 2026 | A tiny daily dare with a fox mascot; skip or reroll; 20+ themed sets (dating, boundaries, being seen); "Guided Courage Journeys" | — | 0 ratings |
| **FACING IT** | FACING IT International AB (SE), Feb 2022 | "AI coach"; small daily actions; CBT, ACT and exposure built with PhD psychologists | $3.99–24.99 | iOS ★4.62 (42); GP ★3.79 (7.2k installs); **abandoned** (last update Dec 2022/Feb 2023) |
| **SocialEase** | WellCompass, Feb 2025 | ACT/CBT exercises plus community | $4.99–39.99 | GP ★4.4 (10k+; 15,610); iOS 0 ratings |
| **Beat Social Anxiety Challenge** | TaBi, Nov 2025 | A 30-day micro-challenge program | $0.99 | GP 100+ |
| **Hatchr: Social Anxiety Coach** | Hbrothers, Apr 2025 | Coach | — | iOS ★4.19 (27); last update Jun 2025 |
| **iNTRPT: Approach Anxiety App** | B. E. Eze, Jun 2026 | Approach anxiety (dating-coded) | — | ★5.0 (12) |
| **Bold AF** | Vertical AI SRLS, Oct 2025 | AI companion plus challenges | — | ★3.44 (9) |
| **Rizzup – Confidence Challenges** | Lambda Soft, Aug 2026 | "Street approach challenges" | — | GP 25 installs |

*Pattern:* exposure therapy is the explicitly cited science in almost every one. All are solo-dev, iOS-first, subscription-gated, and none has passed about 50 ratings.

### 2.23 AI social-skills coaches (the money is here, mostly not in real-world challenges)
| App | Dev | Launch | iOS ★ (ratings) | GP | Price | Real-world component |
|---|---|---|---|---|---|---|
| **Gleam: Social Intelligence** | C137, LLC (listed elsewhere as Gleam Labs) | May 2025 | 4.74 (12,255) | 4.60 (100k+) | $12.99/mo; $39.99–89.99/yr | "Something to practice today" after each lesson; mostly simulations. arr.club headline: "**Gleam passed $1M ARR with 500M views**" (TikTok-driven). AppGoblin vs Screensdesign revenue estimates conflict ($10k vs $80–100k/mo). |
| **Magneta – Confidence & Clarity** | Tenacity Labs | Sep 2025 | **4.92 (47,263)** | — | — | AI chat "bestie" about confidence and relationships; no IRL challenges |
| **Social Wizard** | Kelechi Onyeama | Jan 2024 | 4.84 (6,664) | — | ~$10/week | AI rizz reply generator; reviews: "$10 a week… greed," "3-day trial charged $23"; last update Apr 2025 |
| **Make Me Social** | Intflo LLC | Jan 2026 | 4.67 (114) | 4.64 (5k+) | $9.99–39.99 | "Daily Connection and Confidence challenges tailored to difficulty." Reviews: "you cannot use the app at all unless you pay." |
| **EdgeLab: Social Confidence** | Luka Ivancevic | Dec 2025 | 4.59 (93) | — | sub | AI scenario practice; "everything is blocked behind a paywall" |
| **Cringe: Social & Dating Skills** | Cringe Labs Inc. | Feb 2026 | 4.82 (22) | — | sub | Lessons plus "Cringe Sims" |
| **Socially** | Soniya Panjwani | Mar 2026 | 4.85 (27) | — | sub | Lessons plus AI feedback plus "micro-actions" |
| **Solis Quest** | ZSTACK Capital | Nov 2025 | 3.77 (13) | — | sub | Lessons plus "Daily Quests: real-world missions" |
| **Social XP** | Kidus Kumbi | Aug 2025 | 5.0 (5) | — | sub | Daily missions in Romance/Mindset/Social, XP, levels, streaks, badges, "guys like you" community; stalled Sep 2025 |
| CharmXP, Volo, Quippy, PatterAI, Wellspoken, Speeko, Orai | various | 2017–26 | 98–6,794 ratings | — | sub | Speech and charisma drills |

*Takeaway:* **the category's revenue goes to AI-chat and lesson apps marketed on TikTok** (Gleam, Magneta). Their reviews are full of the same complaints: hard paywalls straight after onboarding, trials that convert to annual plans without warning, and "AI slop." **The real-world challenge part is a footnote in all of them.**

---

## 3. "Side quest" and novelty apps (the 2025–26 TikTok trend)

**Context.** Bustle reported that TikTok called 2025 "the year of the side quest," and The Every Girl and others covered the #sidequesting hashtag. The idea is small spontaneous adventures outside routine: getting off at a random train stop, fostering a dog, side-quest bucket lists by creators like @diaryoflo_ and @hyphygrandma. A tool site claims "side quest ideas" searches rose 900% year on year in 2025; I could not verify that. The App Store response was a **flood: a US search for "side quest(s)" returns 35+ apps, about 30 of them launched between Aug 2025 and Nov 2026, most with 0–10 ratings.**

### 3.1 SideQuest: Tiny Adventures
- **Developer.** OMG Career, LLC (tinysidequest.com). iOS, 8 Sep 2026, v3.5.2 on 21 Nov 2026 (fast cadence).
- **Core loop.** Pick a pack, choose a quest, go do it, **take a photo**, log it, and it becomes a **Polaroid in a Journal**. Users earn XP, levels and badges.
- **Bravery rating.** Every quest shows **time, cost and "how brave you'll need to be"** before you start. That makes it the most explicit difficulty labelling in the niche.
- **Content.** 10 "Originals" packs with 121 quests: *Talk to Humans, Make It Weird, Rejection Therapy, Main Character Energy, City After Dark, Familiar Faces* (27 low-pressure ways to meet people, such as run clubs and board-game nights) and others. "City Editions" are scavenger-hunt packs for **160+ cities**; "Better Together" date and group plans unlock when users invite friends. Example quests: "Borrow a Stranger's Soundtrack," "Neighborhood Cat Census."
- **Generation.** Curated and hand-written with a whimsical voice. A personalized plan is built from onboarding questions.
- **Monetization.** $7.99/week, $9.99/month, $29.99–34.99/year (annual includes 2 cities), plus pack keys at $9.99–34.99 and a 7-day trial.
- **Ratings.** ★5.0 (9).
- **Status.** Alive. The **closest existing product to a "comfort-zone quest app done well"**: pack structure, bravery labels and a memory journal. It is subscription-heavy and very early.

### 3.2 Sidequests HQ
- **Developer.** Blinq Software LLC. iOS Oct 2025, Android Jan 2026 (GP 1k+; 2,106).
- **Content.** "300+ real-world side quests." Challenge categories by mood: *Social Spark, Weekend Warrior, Kindness Conspiracy, Creative Chaos, City Explorer*. Quests range from minutes to long-term.
- **Mechanics.** XP, stories, bragging rights, and "progress without drowning in charts."
- iOS ★4.86 (7). Alive.

### 3.3 Sidequest: Explore Your City (knowaspot)
- **Developer.** Riley Palattao. iOS, Mar 2026, v1.3.11 in Nov 2026.
- **Concept.** "Turns your city into a real-world game."
- **Mechanics.** **Dice-roll "Random Quest"** to a place you've never been, by mood (Nature, Food, Adventure, Hidden Gems) and distance, with turn-by-turn directions and rerolls. **Fog-of-war map clears as you move.** Group and solo quests with a friends-only photo feed. "The Immortal Snail" multiplayer chase (Aug 2026). CarPlay and Watch support, 9 languages.
- **Monetization.** $9.99/month, $17.99–29.99/year. A free tier was added only in Aug 2026 after backlash.
- **Ratings.** ★4.37 (222). **The most-reviewed new side-quest app, and its reviews are dominated by paywall anger:** "They do a whole interview just to make it a paid trial app. 0/10," "Forced paywall… clearly vibe coded," "How long is this interview??… stop pretending it's a psych therapy app when it's a simple map tracking app," "Uses live activity to display a promotion in the Dynamic Island." The positive review: "Finally a reason to get out of my rut."
- **Status.** Alive.

### 3.4 SideQuest: Nearby Activities (Sidequest Local Inc. / SideQuest Inc.)
- **Developer.** Adhish Paranjothi; the iOS copyright reads "Sidequest Local, Inc." The Product Hunt maker describes it as "a **Strava for real-life adventures**, experiences & skills" (May 2026). iOS Mar 2026; **Android 15 Mar 2026, GP ★4.88 (137 ratings), 10k+ installs (20,048)**, IAP $4.99–99.99.
- **Concept.** A discovery feed of user-generated SideQuests: things to do alone, with friends or with new people. Trending, New and Top-rated tabs. "Find a SideQuest. Make a plan. Go do it."
- **Generation.** Community and UGC. iOS ★4.68 (19).
- **Status.** Alive. **The best Android traction among the 2026 side-quest apps.**

### 3.5 SideQuest: Explore & Challenge (Colden Bjorn Johnson; formerly "geode")
- iOS Oct 2025. **Anyone can create a SideQuest and anyone can complete it.** Users see how others did it, in a friends-only social feed ("share it with people who actually know you"). ★5.0 (5).

### 3.6 The 2026 micro-launch long tail (all iOS, mostly 0–6 ratings)
- **Syde: Side Quests** (Mirai Studio, Jul 2026). One quest each morning (visit a museum, enter a shop you always walk past), captured as a short video, with a feed of others doing the same quest.
- **Venture: Real-Life Side Quests** (Jabar Studios, UK, May 2026). **Three quests a day; pick one, commit, put the phone down**, then reflect and add one photo to a private archive.
- **Kuji: Real-Life Side Quests** (Aleksandra Klinkovskaia, Jun 2026). Shake to draw a "kuji" lot (Japanese capsule-toy aesthetic). Moods: outdoor, cozy, social, solo, creative. Mark it "Lived."
- **Opia – Real World Quests** (Jun 2026). Spin a compass for a random quest.
- **SideQ: Real Life Quests** (Patrik Cesnek, May 2026). "Some will make you question your decisions."
- **WeirdQuest** (Rizwan Ahmed, Nov 2026). Party mode: friends in different places get the same "slightly unhinged" 15-minute quest generated from their real streets ("Find the least confident shop sign on this street"). **AI and location generation.**
- **5ideQuest: Micro-Adventures** (Yan Budman, Jul 2026). One verified real place within a short walk.
- **Wander: Daily Adventures** (Les Nants, Jul 2026). A daily side quest ("find a unicorn," "get lost on purpose"), proof photo with a film-look "development."
- **Firsts: Try Something New** (Nov 2026). One "first" a day that you tap to log.
- **Branch Out: Try New Things** (Nov 2026). A skill-tree galaxy: doing one star opens connected ones, filterable by cost and time.
- **Flypp: Real-Life Ideas** (Esaro, UK). A few ideas at a time with built-in pauses and no infinite feed.
- **nudge. – weekly challenges** (Michael Kowalczyk). One a week, "Chill" or "Bold."
- **BeThere – Daily Challenges** (Jun 2026). Prosocial challenges with proof, streaks and points among friends.
- **Twistday, QuestDay, Daily Side Quests, Side-Quest Daily, Quester, Mapside, Break! Side Quests, Side Quests Today: Touch Grass, Side Quest Life** (GP, Oct 2026). Map-based quests by Nature, Adventure, Social or Relax, e.g. "Sign up for something you are not ready for."
- **Side-Quest** (Benjamin Snook, ★3.92, 12 ratings). "Personalized quests that spark curiosity."
- **Status:** a classic gold-rush pattern. Near-zero distribution, many single-release abandonments, interchangeable copy ("less scrolling, more doing") and probably vibe-coded builds (Questo and Sidequest reviewers now use "AI slop / vibe coded" as an insult).

### 3.7 outernet: go outside & explore
- **Developer.** Outernet Explorer Inc., founded by Daniel Egan (ex-LinkedIn BizOps) and Athena Leong (TechCrunch, 3 Aug 2026). iOS Mar 2026. Waitlisted.
- **Concept.** Share TikTok/IG/URL/screenshot saves into the app; AI researches and organizes them into plans; reminders and nudges get you to actually go; **collect stamps when you complete adventures**.
- **Insight from the founders.** Participants in their earlier community adventure campaigns "didn't get involved because they loved scavenger hunts… they just wanted an **excuse to go outside**."
- **Ratings.** ★4.90 (288), glowing: "I'm actually going to all the cool places I had saved on TikTok." One 2★ review complains of months on the waitlist.
- **Funding.** Not disclosed. **Status:** alive and growing.
- **Relevance:** it competes for "do new things IRL" but without the courage framing.

### 3.8 Wim – An Adventure Awaits
- WimNow, Inc. iOS Aug 2026. "Wim makes the call": the user says what they have (car, cash, gear), and Wim picks **one spontaneous activity nearby** and invites friends. ★5.0 (6).

### 3.9 DoSomething – Daily Challenges
- Entermaurs Inc. iOS Feb–Apr 2025. "Tiny daily nudges that snap you out of autopilot… No pressure. No self-improvement." 0 ratings. **Dead.**

### 3.10 Randonautica
- **Developer.** Randonauts LLC/Co.; founders Joshua Lengfelder and Auburn Salcedo. Launched 22 Feb 2020.
- **Concept.** A "quantum random" coordinate generator. Set an intention, go to the random point and look for "synchronicity."
- **History.** It exploded on **TikTok and YouTube in June 2020**: about **10.8M downloads per Sensor Tower** (NYT/Atlantic-sourced figures quoted on Wikipedia), then tapered off (App Annie). Controversies: a group following the app found a suitcase with human remains in West Seattle (2020), trafficking rumours (denied), and trespass concerns.
- **Traction now.** GP ★4.65, **10M+ (21.4M)**. iOS ★3.57 (13,499).
- **Monetization.** Points plus a Pro subscription.
- **Complaints (recent iOS reviews).** "Used it back in 2020… now is a cash grab," "Turned into trialslop," "canceled my subscription then it made me pay 53 dollars," and repeated **safety reports** (in Spanish: "they robbed us and shot a friend in the back"; in Russian: "they threatened me").
- **Lesson.** The biggest viral "go somewhere random" app proves the demand spike is real. It also proves a randomness-only loop has no retention and that **sending strangers to random coordinates is a safety and liability problem**.

---

## 4. Gamified real-world exploration (adjacent giants and durable niches)

### 4.1 Pokémon GO
- Niantic → **Scopely (Savvy Games/Saudi PIF)**, which agreed to pay **$3.5B in Mar 2025** for Niantic's games (Pokémon GO, Pikmin Bloom, Monster Hunter Now). Niantic's games business had **30M+ MAU and over $1B in 2024 revenue**; Pokémon GO has about 20M weekly players (TechCrunch, Investing.com, LA Times). Launched Jul 2016, 1B+ downloads.
- iOS ★4.0 (657k). GP ★3.46 (568M installs).
- **Core loop.** Walk, catch, raid, community days. **Social:** raids, trading, friends. **Proof:** GPS.
- **Relevance.** It proves that **location plus collection plus scheduled community events** gets people outside at huge scale. Courage is not the aim, but its **Community Day events** have been a socially easy way for many shy players to meet strangers.

### 4.2 Pikmin Bloom
- Niantic and Nintendo (now Scopely). Oct 2021. iOS ★4.81 (71k). GP ★4.76 (9.4M installs).
- Walk to grow Pikmin, plant flowers and do "expeditions." Gentle, cosy, no combat, plus a postcard and memory "Lifelog."
- Reviews: "It genuinely motivates you to walk and go to different places," and from a 72-year-old, "gets you going." Complaints: loading hangs, missing badges.
- **Relevance:** the template for **low-pressure, cute, memory-keeping** real-world gamification.

### 4.3 Geocaching® and Adventure Lab
- Groundspeak (Seattle); geocaching since 2000, app since 2009. iOS ★4.83 (66.6k). GP ★4.58 (23.3M installs). **Adventure Lab** (community-created outdoor scavenger hunts): GP ★4.77 (761k installs).
- Scale: **3.47M active caches in 191 countries**, and **1,608,335 people found at least one cache in 2025**, averaging 69 finds each (Geocaching blog and newsroom).
- **Proof.** A physical logbook plus an online log, the strongest verification in the space. **Generation.** Community. **Mechanics.** Find counts, souvenirs (badges), challenge caches, difficulty and terrain ratings (D/T 1–5). Premium subscription.
- **Relevance:** the **most durable** real-world quest community, 25 years old. Its explicit **Difficulty/Terrain grid** is the closest analogue to a "courage rating."

### 4.4 Seek by iNaturalist
- iNaturalist (non-profit). 2018. iOS ★4.75 (30.9k). GP ★3.40 (4.36M).
- Point the camera, identify species, earn **badges and monthly challenges** (often with partners such as WWF or Nat Geo). No login and no ads.
- Complaints: inaccurate IDs, poor camera focus on new iPhones.
- **Relevance:** **camera-as-proof** with badge collection, and safe for kids.

### 4.5 Fog of World
- Ollix (Taiwan). 2012. **$30 one-time.** iOS ★4.81 (3,138). GP ★3.58 (16.6k).
- The map stays fogged until you have physically been there, with levels ("Level 508") and private data sync.
- "I've been using this thing for 15+ years… certainly the longest I've ever consistently used an app." Complaints: GPS dropouts, battery.
- **Relevance:** the **fog-of-war mechanic** is now copied by Sidequest: Explore Your City, FogWalk, FOG and others. One-time pricing plus personal data ownership drives very long retention.

### 4.6 Let's Roam / Questo / Dispatch (paid scavenger hunts)
- **Let's Roam** (US, 2018). iOS ★4.74 (18k). 3,500+ cities. Riddles plus photo challenges. Per-hunt pricing (one review: "$26").
  - Complaints: "walking around but nothing more," closed or missing locations, no-refund policy, internet errors after payment. Praise: "great date night… gets you out of your comfort zone."
- **Questo** (Romania, 2017). iOS ★4.78 (2,974). GP ★4.44 (100k+). "1M+ players, 1,000+ cities." Outdoor escape game plus walking tour.
  - Recent complaints: "**AI slop**, vibe coded," "chock full of AI slop!!! Totally ruined the fun," glitchy maps, clues not tied to the real site.
- **Dispatch: Real-World Quests** (Nicholas Reynolds, Aug 2026). Story-driven hunts using telegrams and coded letters.
- **Relevance:** people **will pay per experience** for structured IRL adventures, and **AI-generated filler content is now actively punished in reviews**.

### 4.7 Atlas Obscura
- Atlas Obscura Inc. App since Oct 2021. iOS ★4.85 (9,955). GP ★4.84 (100k+). A community-sourced map of unusual places. A discovery engine for the "do something new" motive.

### 4.8 1000 Hours Outside
- Team Yurich LLC. 2021. iOS ★4.77 (7,822). GP ★4.56 (10k+). Logs a family's hours outdoors, built on a movement and blog. **A movement-led app: the community came first.**

### 4.9 SideQuest – Walk & Level Up (Gaurav Vyas)
- iOS Jan 2026, ★4.94 (220). GP ★4.9 (1.7k).
- Steps earn XP. Classes (Warrior, Wizard…), co-op expeditions, pets that hatch by walking, guilds. Reviews: "has helped me reach my daily walking goals," "6 of my friends downloaded it," "started a guild… sense of community is amazing."
- **Relevance:** a solo dev reached 4.9★ by building an RPG layer over passive data, with **no challenge friction at all**.

---

## 5. Bucket-list apps

### 5.1 The Bucket List App ("Bucket List – Travel Goals")
- The Bucket List Studios Inc., run by the **Bucket List Family** (Gee and Garrett Gee, a large YouTube/IG audience). iOS Nov 2024, ★4.94 (924). GP ★4.85 (10k+; 19.9k). IAP $4.99–239.99.
- Build and check off bucket lists, passport "stamps," shared lists, and a Q&A community.
- **The creator audience is the moat:** "I've been following for years… my only regret is not downloading this app sooner."

### 5.2 BucketListers
- Bucket Listers Inc. 2022. iOS ★4.66 (3,311). In practice it's a **discounted event-ticket marketplace** (NYC, Chicago…). Complaints focus on refunds and customer service.

### 5.3 Bucket List – The Bucket App (Trent Wann, ★4.65, 715), iBucket (PuurPuur, 2015, ★4.55, 83; GP 10k+), Bucketlist (0952915 B.C. Ltd, 2018, ★2.45, 11; neglected), plus a dozen 2025–26 couple bucket-list apps (Withly, brochi, TwoDo, Sparkz)
- **Pattern:** a list with no prompting and no difficulty is a passive store of intentions with low engagement.

### 5.4 The Adventure Challenge (scratch-off books)
- The Adventure Challenge (US). Physical scratch-off books (Couples, Friends, Family, In Bed editions) sold at Target and DTC. Ratings run 4.7/5 on the company site (962 reviews) versus Trustpilot 3.3–3.5 (about 2,800 reviews).
- **Praised for:** the *surprise* mechanic of scratching to reveal a hidden challenge. **Complaints:** scratch surfaces failing, customer service, "corny" challenges.
- I could not find a standalone app with measurable traction (Influenster links an app download, but none appears in US iOS search).
- Copycat apps exist: **the2: Scratch Adventure** (Maurice Wirth, ★4.68, 565), which pivoted to sex and couple dares.
- **Relevance:** a **mystery reveal plus a commitment to complete before you see it** is a proven physical-product mechanic that digital apps have barely used.

---

## 6. IRL social and "meet strangers" apps (courage-adjacent)

### 6.1 Timeleft
- **Developer.** Timeleft SAS (Paris). Product since about 2021, app Dec 2023.
- **Concept.** **Dinner with 5 strangers**, matched by personality quiz; now also coffee, drinks and walks. "No swiping. No planning. Just show up."
- **Traction.** iOS ★4.62 (9,141). GP ★4.28 (1.25M installs). It claims 3–4M+ users and 250+ cities. A Substack profile reports **€18M ARR and 150k monthly participants (Aug 2025)**; that is a secondary source. Dealroom lists a $2M pre-seed (2021). Covered by Axios in several cities, RTÉ and Brussels Times.
- **Price.** €12.99 per seat or €14.99+/month (France); IAP $19.99–62.99.
- **Complaints.** New paywalls ("$4.99 to show you who you're dining with"), cancelled events, dinners only in the evening.
- **Relevance:** **the most commercially successful "do the scary social thing" product**, because the courage is packaged as a booked event with logistics handled. Media explicitly describe it as "forcing Glaswegians out of [their] comfort zone" (Yahoo UK).

### 6.2 222
- TwoTwoTwo Inc. (YC). Co-founders Keyan Kazemian, Danial Hashemi and Arman Roshannai, started late 2021. A **$2.5M seed (Oct 2024, 1517 Fund, General Catalyst, Best Nights VC)**; later rounds bring reported totals to $13.7M (CB Insights) or $16.8M (Welcome to the Jungle), figures that conflict.
- iOS ★4.68 (7,845). "No profiles, no DMs… an opportunity to **choose chance**." AI-curated small-group experiences.
- **Complaints.** "$22 membership fee, plus whatever the event costs, PLUS a $22 bail fee," "boring and just lots of drinking," AI-generated profiles, no-shows, heavy onboarding.
- **Praise.** "One of the most unexpectedly fun and spontaneous things I've ever done."

### 6.3 Meetup
- Meetup LLC (owned by Bending Spoons since 2024; I didn't re-verify the deal in this session). iOS ★4.72 (272.7k). GP ★3.85 (22.5M installs). 60M members. The incumbent for "try new things with people," but it has no challenge or courage layer.

### 6.4 Bumble BFF
- Bumble. **Relaunched Sep 2025** on Geneva, which Bumble acquired in 2024 and then shut down. Adds a Groups tab with chat, events and a calendar; group discovery slated for Feb 2026. Geneva had made no revenue by June 2025 (TechCrunch, Bumble IR). iOS ★4.21 (9,063).

### 6.5 Pie
- Pie Labs PBC. 2021. iOS ★4.77 (1,533). Free small-group events matched by interests.

### 6.6 Wakie
- Wakie Inc. 2014. GP 10M+ (10.2M), iOS ★4.53 (18.8k). Anonymous voice calls with strangers ("talk to strangers"), the lowest-stakes form of social exposure.

### 6.7 Long tail
Kndrd (★4.75, 3,403), Peeps, BeFriend, Mesh Local, NiceToMeet, Cuculi, Buffet, Bunch, Homii, Frnds, plus "spontaneous hangout" apps (Sponty, Swazz, Sonaara, NoPlan, Jump In, Green Light, Emit). Almost all are tiny and suffer the classic **cold-start / local-density problem**.

---

## 7. BeReal-style challenge social

### 7.1 BeReal
- BeReal (FR) → **acquired by Voodoo in 2024** (widely reported at about €500M; not re-verified here). iOS ★4.77 (1.16M). GP 38M installs. One synchronized daily prompt, front and back camera, and **the feed locks until you post**.
- **Relevance:** Leap, DareDash, Gontlet, unrue and Syde all copy this "**post to unlock the feed**" gate, applied to dares. The two professional attempts at "BeReal for dares" (Livehouse DARE and yope Dare Zone, both 2023) died within months. **The mechanic works for low-effort posts ("show where you are") and fails when each post demands real effort ("go talk to a stranger"), because daily participation collapses and the feed empties.**

---

## 8. Clinical and therapeutic exposure tools

### 8.1 MindShift CBT
- **Anxiety Canada** (non-profit), developed by 247 Labs. 2013, relaunched as "MindShift CBT" in 2019.
- Free CBT tools including **"Face Your Fears" step-by-step exposure ladders**, thought journals and coping cards. iOS ★4.35 (579). GP ★3.74 (500k+; 828k).
- **Status.** Alive. Clinically grounded but **not motivating**: nothing pulls the user back and there are no social mechanics. The GP rating is mediocre.

### 8.2 Joyable
- Joyable (SF), from 2014: a 3-month CBT program for social anxiety with real-world exposure "challenges" and a coach.
- **Laid off half its staff in 2017** when it moved from consumer to employer sales (Fortune). **Acquired by AbleTo in Mar 2019 for "eight figures"** (CNBC). The consumer program was wound down. It is effectively defunct as a standalone product.
- **Lesson:** even a VC-backed, coach-supported exposure program could not make **direct-to-consumer** social-anxiety exposure a business, and B2B absorbed it.

### 8.3 DARE: Anxiety & Panic Relief
- BMD Publishing (Ireland; Barry McDonagh, author of *Dare*). 2015. iOS ★4.84 (6,939), subscription.
- An audio program plus the "DARE response" (lean into anxiety). Users love the voice and the community: "Barry is such a familiar voice."
- **Relevance:** **book plus author voice plus app** can sustain a subscription in the anxiety space, which is relevant to how Rejection+ *could* have worked.

### 8.4 Exposure – Face Your Fears / FearTools / Social Anxiety Test (Inquiry Health LLC)
- Inquiry Health LLC, 2016. Users build a fear hierarchy and log anxiety (SUDS) during exposure.
- Exposure: ★4.14 (7), last updated 2017. FearTools: iOS ★4.84 (145), GP 50k+, last updated 2021. **Abandoned.**

### 8.5 FearLadder – Face Fears (Aug 2026)
- 16 ladder templates, before/peak/after anxiety curves, heat maps and share cards. Everything is free. 0 ratings.

### 8.6 Phobia-specific VR and apps
ZeroPhobia (heights, ★3.85), oVRcome (★3.45), SOAR and Sky Guru (fear of flying), Clear Fear (Stem4, teens), OCD ERP apps (NOCD, unstuck, OCD SensAI). Clinical and narrow.

### 8.7 SuperBetter
- SuperBetter LLC (Jane McGonigal). 2012. iOS ★4.65 (7,883). GP 100k+. Resilience reframed as a game: **quests, power-ups, "bad guys," allies**. Backed by RCT evidence for depression symptoms (2015).
- **Redesigned in 2023 as an educator and youth tool**, which forced new accounts; the old web app closed at the end of 2023. Hero tier $24.99/yr.
- **Status:** alive but pivoted away from consumers. **The vocabulary (quests, allies, power-ups) is now everywhere, but the original consumer product didn't hold up as a business.**

---

## 9. Life-RPGs and gamified self-improvement (mechanics benchmarks)

- **Habitica** (HabitRPG, 2013, Kickstarter). iOS ★4.33 (3.7k), GP 5M+. Tasks become RPG combat; parties and guilds; mature but stagnant UX.
- **Finch** (Finch Care PBC, 2021). **iOS ★4.95 (778k), GP 10M+.** A self-care pet that goes on "adventures" when you complete self-care goals. **The benchmark for an emotionally safe, non-shaming gamified pet**, which Freewill's hermit crab clearly borrows from.
- **Lion XP** (POXI AS, NO, 2024). ★4.49 (313). An "MMORPG for real life": auto-recommended challenges, skills, equipment, and a "Demon King Gatekeeper" that locks features until a habit forms. Its ToS domain is "become-fearless."
- **Earth Online: Real Life RPG** (Pei-Tzu Huang, 2026). ★4.78 (85). A fully custom attribute and skill tree with a custom economy.
- **Arise: Level Up Workout Game** (Digital Lions, 2025). **★4.76 (20,989).** A Solo Leveling-style "System" for fitness.
- Plus about 30 more: Do It Now, LifeUp, Skillion, Levelite, Solo Levelling Daily Quests (GP 50k+), MainQuest and others.
- **Relevance:** the "Solo Leveling / System" aesthetic is a strong 2025–26 Gen-Z hook (Arise is at 21k ratings). Nobody has applied it convincingly to **courage quests** ("The System has assigned you: talk to 3 strangers").

---

## 10. Cold-exposure challenge apps
- **Wim Hof Method** (WHM Services, PT; 2014). iOS ★4.86 (13.8k). Breathing plus cold-shower challenges (a 20-day video course), timers and progress.
- **GoPolar: Cold Plunge & Sauna** (2024). ★4.67 (317).
- IceBuddy, Brisk (GP 100+), PlungePalz (GP 500+), ColdStreak, Coldsmith, Polar Log, Kelvin, and many plunge timers with 0–50 ratings.
- **Pattern:** cold exposure is the one discomfort challenge that is **easy to verify** (a timer, sometimes a wearable temperature reading), solo and safe. It is commoditized as timers and loggers. Nobody combines physical discomfort (cold) with social discomfort into one "courage" score.

---

## 11. Kindness challenge apps
- **BeKind: Acts of Kindness Ideas** (TeamEXtension / Michael Ryan Paclibar, 2020). iOS ★4.70 (114). GP ★4.67 (8.8k). Daily kindness ideas, photo logging, friends and a story feed.
- **The Great Kindness Challenge** (ExaMobile, 2014–2018). ★3.69 (16). **Dead.** It was a school-campaign tie-in.
- The 2026 long tail: One kind act a day, 30 Acts of Kindness, Kindbook, Acts of Kindness: Missions, kind365, Kind Act App, ROK: Ripples of Kindness, be nice, The Kindness Project, liftd, GoodHeart, Good Vibes Only: Kindness Map. All have 0–12 ratings.
- **Relevance:** kindness acts are the **lowest-fear on-ramp to stranger interaction** ("compliment a stranger" is both a kindness and a rejection-therapy rep). That makes them a useful first tier on a courage ladder.

---

## 12. Other challenge-social formats
- **Gloop: Social Challenges** (Gloop LLC, 2026; ★4.73, 15). Video challenges against friends or strangers worldwide, reward tokens.
- **Challenger – Local Challenges** (William Leaf, 2020; ★5.0, 6). A map of **location-tied video challenges**: upload your attempt.
- **Dare: AI Photo & Video** (Bounty Studio). The "Bounty" name: AI generation, not real dares.
- **ChallengeRunner** (★4.53, 8.7k) and **The Conqueror** (★4.83, 12.6k; GP 1M+). Virtual-route fitness challenges with physical medals. **Paid physical rewards for IRL effort work.**
- **75 Hard / 75 Soft** apps (BeHard ★4.82 on 9k iOS ratings, but **GP ★1.45**; Her 75 ★4.82 on 5.4k; several others). Rigid all-or-nothing challenge programs, viral on TikTok. **Strong evidence that Gen Z will adopt a named, finite, hard challenge with an identity attached.**

---

## 13. Dead or delisted (graveyard)
| App | What it was | Evidence |
|---|---|---|
| Joyable | VC-backed social-anxiety CBT and exposure program | Halved staff 2017; sold to AbleTo 2019 |
| Roadmap (id883887354) | "Real-life social anxiety as a game," earn miles for challenges | ID no longer resolves |
| Daily Dare (id6748892806) | Bite-sized dares, time windows by difficulty, "buy a friend a coffee if you miss" penalty | Delisted |
| EaseUp (id6477931386) | Gamified exposure therapy, early access | Delisted |
| Challenge: Your Best Version (id6472225791) | 80+ challenges, group challenges | Delisted |
| Discomfort Zone (id6448200940), Fearless Life (id6459058894) | Comfort-zone challenge apps (2023) | Delisted |
| Sidequest – Social Adventures (id6761319024) | 2026 side-quest app | Delisted |
| DARE – Photo challenge (Livehouse) | BeReal for dares | No update since Mar 2023 |
| Dare Zone (yope) | Squad dares with video proof | No update since Sep 2023 |
| DoSomething – Daily Challenges | Anti-scroll nudges | No update since Apr 2025 |
| DareDash | BeReal for dares | No update since Jul 2025 |
| Push, Diss Comfort, Sidequest – Social challenges | Comfort-zone dares | Single release, 0 ratings |
| FACING IT, Exposure (Inquiry Health), FearTools | Anxiety exposure tools | Abandoned 2017–2023 |
| The Great Kindness Challenge | Kindness challenge app | Abandoned 2018 |
| SuperBetter (consumer) | Resilience game | Pivoted to education in 2023; old accounts closed |
| Geneva | Community app | Bought by Bumble, shut down 2025 |

---

## 14. Patterns, gaps and white space

### 14.1 What the market looks like
1. **The niche is crowded and has no leader.** I catalogued 60+ apps. **No dedicated courage or comfort-zone challenge app has 1,000 US App Store ratings.** The best-performing *dedicated* ones are Sidequest: Explore Your City (222 ratings, a map app with quests attached) and SideQuest: Nearby Activities (about 20k Android installs). The oldest survivor, IDareTo (2016), has about 14k installs after a decade. Meanwhile adjacent products that package the same motive differently are large: Timeleft (1.25M GP installs, reportedly €18M ARR), Gleam (100k+ GP, a reported $1M ARR), Randonautica (21M GP installs), Finch (10M+), Pikmin Bloom (9.4M) and Geocaching (23M).
2. **2025–26 brought a gold rush.** The #sidequest trend plus AI and vibe-coding tools led to dozens of near-identical iOS-only launches ("one quest a day, less scrolling, more doing"). Most have 0–10 ratings. Many shipped once and were abandoned. Reviewers now spot and punish "vibe coded" and "AI slop" apps by name.
3. **Content is mostly curated, sometimes AI-generated.** Libraries range from about 40 challenges (PebbleStep) to 500 (Get Rejected). AI-generated quests show up in 100 Rejections, WeirdQuest and Push. Community-generated quests show up in SideQuest Nearby, SideQuest Explore & Challenge, Challenger, Geocaching and Atlas Obscura. Only the community model has scaled, and only Geocaching has sustained it.
4. **Proof is nearly always the honor system or a photo.** Video appears in Leap, Gontlet and Syde. GPS proof appears only in exploration apps. **No courage app verifies the social part of a challenge**: whether you actually spoke to the person, or what they said.
5. **Monetization pulls toward aggressive weekly subscriptions.** Weekly plans run $3.99–9.99 (Rejectionmax, UNSHY, SideQuest Tiny Adventures, Social Wizard). Hard paywalls appear right after a long onboarding quiz. **This is the single most common source of 1★ reviews across the category**: Sidequest Explore Your City, Make Me Social, EdgeLab, Gleam, Social Wizard and Randonautica all draw complaints like "they do a whole interview just to make it a paid trial app."

### 14.2 Why apps in this niche fail
1. **The core action happens off-app and is effortful and scary.** Effort per check-in is high: a meditation app asks for 5 minutes on the couch, while a courage app asks you to walk up to a stranger. Daily-dare streaks break, and streak loss on a *fear* task feels like personal failure, so users churn from shame. DISCOMFRT drops streaks for exactly this reason, and Freewill adds Streak Restores.
2. **There is no difficulty titration.** Most apps hand out a random or daily-fixed dare. For a socially anxious user that is either trivial or terrifying. Exposure works through a **graded hierarchy at the edge of tolerance** (SUDS 40–60). Only Rejectionmax (weekly self-rating) and Freewill (predicted versus actual difficulty) attempt adaptive difficulty, and both are tiny.
3. **Context mismatch.** A dare like "ask a stranger for a song" fails for someone who is rural, unemployed, working from home, 15 or physically limited. DareDash's reviewer said it outright ("don't live in a place where people are actively outside"). Generic dares ignore time, place, budget, mobility, safety and culture.
4. **Social apps for dares hit cold start, and the effort tax empties the feed.** The "post to unlock the feed" mechanic (BeReal) collapses when posting costs real courage. Two experienced social-app teams (yope, LiveIn) gave up within months in 2023. Leap and DareDash stalled in weeks.
5. **Stigma and identity problems.** "Social anxiety app" is clinical and people hide it. "Rizz app" is gendered and cringe. "Dare app" reads as a party game, and the App Store "dare" category is flooded with truth-or-dare and NSFW couple apps. There is no aspirational, shareable identity like "75 Hard finisher" or "Geocacher."
6. **Distribution.** Almost every entrant is iOS-only and solo-built, with no creator or community engine. The winners each have a non-app moat: Gleam (a TikTok content machine), the Bucket List App (a creator family's audience), Rejection Therapy (book and TED, though it still failed to convert), Timeleft and 222 (city ops and press), Geocaching (a 25-year community).
7. **Safety and liability.** Random locations (Randonautica's reviews describe robbery and threats), strangers and night-time quests. A mainstream courage app needs explicit safety design: public places, daylight defaults, no trespass, age gating, nothing that pressures users into risky behaviour. Leap is rated 13+ with UGC and moderation queues.
8. **Proof can be gamed and the reward is hollow.** An honor-system XP for "talked to a stranger" feels meaningless after week one. The intrinsic reward (the story, the connection) isn't captured or celebrated.
9. **Content quality and voice.** Users can tell hand-written, funny, specific quests ("Neighborhood Cat Census") from generic AI lists ("try a new food"). The latter are commoditized and now attract "AI slop" reviews.
10. **D2C mental-health economics.** Joyable (VC-backed) went B2B. SuperBetter pivoted to education. FACING IT was abandoned. Clinical framing costs more (evidence, compliance) and gets lower willingness to pay than "fun" framing.

### 14.3 Gaps (nobody does these well)
- **An adaptive courage engine.** A personal fear hierarchy across several domains (social, rejection, visibility and performance, novelty and adventure, physical discomfort, creative vulnerability), with difficulty set from *before and after anxiety ratings* (SUDS) and outcomes. Nobody combines exposure-therapy titration with a fun, non-clinical surface.
- **Context-aware quest generation.** Quests that fit right now: location type (city, suburb, campus, rural, home), time of day, budget, weather, energy and whether you're alone or with friends. WeirdQuest, Wim and 5ideQuest do this for *novelty* but not for *courage*.
- **Mixing courage, novelty and kindness.** Today courage apps are pure social anxiety, side-quest apps are pure novelty and kindness apps are pure prosocial. A ladder that starts with kindness and novelty (low threat) and climbs into rejection and visibility (high threat) doesn't exist.
- **Meaningful proof without humiliation.** Proof options that protect the other person: an audio note to yourself, a "story card," an outcome log, a "witness" friend, a GPS check-in at a public place, optional photo or video. Most apps force photo or video (cringe, and a privacy problem with strangers) or rely on bare honor.
- **Courage memories.** Converting reps into an artifact, like the Polaroid journal (SideQuest Tiny Adventures) or Boldly's Retro. **The story is the reward.** A "Year of Yes" recap and a "bravest moments" reel would be shareable and help growth.
- **Squads and accountability without a public feed.** Small private crews (3–6 friends) doing the same weekly quest, with a "witness and cheer" mechanic (Freewill's Snaps hint at this). This is better than a public leaderboard, which shames beginners and rewards stunt content.
- **IRL bridges.** Graduating users from solo dares to real social events: partnering with Timeleft/222-style dinners, run clubs or Meetup groups. SideQuest Tiny Adventures' "Familiar Faces" pack (join a run club, a board-game night) is the only attempt.
- **Physical discomfort as part of the same courage score.** Cold showers, hard workouts and a public-speaking rep are all logged together today only by 75-Hard-style rigid programs.
- **Android.** Almost all 2025–26 courage and side-quest apps are iOS-only. SideQuest: Nearby Activities reached 20k Android installs fast with little competition there.
- **Fair pricing.** A real free core loop and a one-time or lifetime option (Fog of World's $30 one-time keeps users for 15 years) would be a differentiator against category-wide "trialslop."

### 14.4 What a great product in this space would do
1. **Frame it as an adventure and identity, not therapy.** "Become someone who says yes." Keep the exposure science (graded hierarchy, SUDS before and after, behavioural experiments that compare prediction to outcome as Freewill does) under a fun, gender-neutral, aspirational surface. Avoid "anxiety," "rizz" and "dare" as headline words.
2. **Onboard with a short courage profile.** Domains, current comfort level, context (city or rural, student or worker), safety limits and time budget. Show value before any paywall, since the onboarding-into-hard-paywall pattern is the category's top 1★ trigger.
3. **Use an adaptive ladder.** Each quest carries a visible "bravery level" (as SideQuest Tiny Adventures does), plus time and cost (as Branch Out does). The engine targets the user's "stretch zone" from their past before and after ratings, with an option to scale down ("too much today, give me the 60% version") rather than skip. Missing a day keeps progress; a weekly target (Rejectionmax's 5-of-8) beats a fragile daily streak.
4. **Combine hand-written quests with AI context.** Hand-written, funny, specific quest templates set the voice. AI adapts them to the user's real context (street, weather, budget, friends nearby) the way WeirdQuest does, so quests never feel generic. Seasonal and themed packs, plus Geocaching-style community-submitted quests with moderation.
5. **Offer layered, respectful proof.** Choose reflection, photo of the *place*, audio note, GPS check-in or a friend witness. Never require filming strangers. Proof feeds a beautiful journal and a monthly or yearly "courage recap" that people want to share.
6. **Socialize around small crews and witnessing.** Friend crews, co-op weekly quests ("everyone in the crew asks for something this week"), cheering and "I was there" witnessing. Leave out any global feed that shames beginners.
7. **Build in safety.** Public-place and daylight defaults, no trespass or risky-stunt content, age gating, and a "kind to others" rule (no pranks at strangers' expense).
8. **Use progression that means something.** Character, pet or avatar growth (Finch and Freewill-style creatures, or the Solo-Leveling "System" aesthetic for the Gen-Z male segment); domain-specific "courage stats" that visibly climb; named, finite seasons ("30 Days of Yes," "100 Asks") as identity markers, like 75 Hard. Physical milestone rewards (The Conqueror's medals) could work as merch.
9. **Bridge to the real world.** At higher levels, unlock IRL group quests and partner events (dinners, run clubs, classes) so the app graduates users into a richer life instead of keeping them in a feed.
10. **Treat distribution as part of the product.** A creator-led content engine (the Gleam and 75 Hard playbook: before-and-after stories, "I did a side quest every day for 30 days"); shareable quest cards; campus and city ambassador packs. Launch on iOS and Android together.
11. **Earn trust in the business model.** A generous free core loop, transparent trials (no surprise annual charges), affordable monthly and annual plans, optional paid packs (city or themed) and a lifetime option.

**Bottom line.** Demand is proven by the #sidequest trend, Randonautica's 2020 spike, Timeleft and 222's growth, Gleam's revenue, the cult status of Rejection Therapy and Jia Jiang's 10M-view TED talk. **The dedicated "comfort-zone challenge app" category has never produced a winner.** Products fail on difficulty titration, context fit, effort-heavy social mechanics, stigma, paywall greed and lack of distribution, not on the idea. The white space is an **adaptive, context-aware, safe, story-producing courage engine with small-crew social features and a fair business model**, positioned as adventure and identity rather than therapy, with real exposure-therapy mechanics underneath.
