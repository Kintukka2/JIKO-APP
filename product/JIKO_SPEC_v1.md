# JIKO: Product Spec v1

*Status: v1 decisions are locked. Brand is in progress: Jiko, art style and tagline are locked; palette, type, logo and motion are open (see §15 and `product/BRAND.md`).*
*Market evidence behind these decisions: `research/00_EXECUTIVE_SUMMARY.md`.*

---

## 1. Overview

**JIKO** (自己, Japanese for "self") is a warm, game-like companion app that gives you real-world quests just beyond your comfort zone. You raise Jiko, a small creature who grows as you grow braver. Its home fills up with things you've earned, and every season ends with a recap of your bravest moments, in the style of Spotify Wrapped.

**Main promise:** *Do one brave thing at a time, and find out your fears were wrong.*

### Design principles
1. **Built for one player.** Everything works for a single person. Social features are optional extras and never required.
2. **Warmth beats punishment.** Nothing dies, nothing resets, and nobody is shamed.
3. **Courage is what matters.** Real-world quests drive Jiko's growth, stats and the home.
4. **Showing up counts.** The season pass rewards daily check-ins, so it can't be faked by marking quests done.
5. **Honest money.** No hard paywall. The core loop is free. Premium adds extra rewards and cosmetics.
6. **Wide possibility space.** Quests can be anything brave: online, at home, out in the world, social or solo.

### Target user
Ages 18–35, any gender, curious about growth but put off by hustle-culture and "lock in, king" apps. Uses Finch, Duolingo and TikTok's #sidequest content. Wants a more interesting life, not a stricter one.

---

## 2. Core loop

```
            ┌─────────── DAILY ───────────┐
 Open app → Check in (pass level) → Daily Spark (2 min)
                │                         │
                ▼                         ▼
          Season Pass tier         Spark Gems + Brave Day
                                          │
            ┌────────── WEEKLY ───────────┤
 Draw 3 quest cards → Fear Forecast → Do it → Reflect (actual fear)
                                          │
                                          ▼
               Stat XP + Spark Gems + Brave Day + Jiko reaction
                                          │
            ┌────────── SEASON (66 days) ─┤
       Jiko grows · home fills up · Monthly Trials · Season Wrapped
```

| Rhythm | Activity | Main reward |
|---|---|---|
| Daily | **Check in** by opening the app | +1 season pass level |
| Daily | **Daily Spark**: one tiny brave act, about 2 min | Spark Gems, a Brave Day, Jiko reacts |
| Weekly | **Quest Draw**: 3 cards at your edge; complete any time that week | Stat XP, Spark Gems, a Brave Day, forecast bonus |
| Monthly | **Trial**: one bigger solo challenge at peak difficulty | Exclusive item + large gem payout |
| Season | **Season Wrapped** + pass finale | Recap card, season set |

---

## 3. The Fear Forecast (signature mechanic)

Every quest has a before-and-after rating of how scary it is.

1. **Before:** "How scary do you think this will be?" (slider 1–10)
2. **Do the quest.**
3. **After:** "How scary was it actually?" (slider 1–10) plus an optional one-line reflection.

**Outputs:**
- **Forecast gap** = predicted − actual. A positive gap ("it was less scary than I thought") earns a **Fear Gap bonus** of Spark Gems and stat XP.
- **Fear Accuracy over time**, shown in Insights: "You overestimate fear by 38% on average", "Social quests feel 2.1 points easier than you expect".
- **Difficulty tuning:** forecasts and actual ratings set the user's **Edge Level** per stat. Quest draws aim at Edge Level ±1.
- **Wrapped data:** the biggest gap of the season, the scariest quest done, and how the trend changed.

Rules:
- Forecasting is optional per quest, but encouraged with a bonus.
- If the actual rating is higher than the forecast, the user gets **no penalty**. Jiko says: "That was a big one. You still did it."

---

## 4. Quests

### 4.1 Quest anatomy

| Field | Example |
|---|---|
| Title | "The Long-Lost Text" |
| Flavour line | "Somewhere out there, someone would love to hear from you." |
| Action | "Message a friend you haven't spoken to in over a year." |
| Stat | Connection |
| Bravery level | 1–10 (here: 3) |
| Time | ≤5 min / ≤30 min / ≤2 hr / half-day |
| Cost | Free / £ / ££ |
| Setting fit | Any / City / Town / Countryside |
| Mode | Anywhere / At home / Out & about / Online |
| Category flags | (none) or opt-in categories (§4.4) |
| Completion | Tap done (honor system) · optional photo · optional note |
| Reflection prompt | "What did they say? How did it feel to hit send?" |

### 4.2 Quest types

| Type | Frequency | Bravery range | Notes |
|---|---|---|---|
| **Daily Spark** | 1 per day | 1–3 | Tiny and always doable. Can be swapped once a day. |
| **Weekly Quests** | 3 cards per week | Edge ±1 | One free redraw per week. Complete in any order. |
| **Monthly Trial** | 1 per month | Edge +2 | Optional bigger challenge. Rewards a unique **Pal** (§6.7) and a Trophy. |
| **Quest Packs** (premium) | On demand | Varies | Themed sets, e.g. "City Explorer", "Social Boss", "Solo Travel", "Creative Leap" |

### 4.3 Stats
Five stats, each with its own XP and level, and **no level cap**:

| Stat | Covers | Example quest |
|---|---|---|
| **Courage** | Facing fear, rejection, discomfort | Ask for a discount at a shop |
| **Curiosity** | Novelty, learning, trying things | Eat a cuisine you've never tried |
| **Connection** | Reaching out, conversation, vulnerability | Compliment a stranger sincerely |
| **Body** | Physical challenges, new movement | Try a class you've never done |
| **Mind** | Reflection, creative risk, saying no | Share something you made publicly |

Each stat has an **Edge Level** (1–10) that tracks where that stat's challenges currently feel stretching but doable.

### 4.4 Categories
- **Default on:** all normal quest types (anywhere, home, out & about, online).
- **Opt-in, off by default:** Dating & flirting · Physical challenges (strenuous) · Solo travel · Spending quests (above Free/£).

### 4.5 Personalisation inputs (v1)
1. **Budget** (Free only / Some / Flexible)
2. **Time available** (per draw, default "up to 30 min")
3. **Setting** (Big city / Town / Countryside), asked once at onboarding
4. **Fear-forecast history** (Edge Level per stat)
5. **Enabled categories**

*Not in v1:* live weather and precise location.

### 4.6 Quest generation
AI writes the quests, governed by the **Quest Constitution** (§5).

**Pipeline:**
1. **Seed pool:** about 100 hand-written quests. They are style anchors and few-shot examples.
2. **Generation:** the AI writes quests from the user's profile (§4.5), the target stat and the target bravery level.
3. **Validation, two layers:**
   1. A schema check that all fields are present and valid.
   2. An AI reviewer that checks against the hard limits and the quality bar.

   Quests that fail either layer are regenerated.
4. **Pool caching:** validated quests go into a shared pool tagged by stat, level, setting, cost, time and mode. Draws pull from the pool first and generate only to fill gaps. This keeps cost and latency low.
5. **Feedback:** 👍/👎 after a quest, plus completion and skip rates. Poorly rated quests are retired. Highly rated ones are promoted as few-shot examples.

---

## 5. Quest Constitution

### 5.1 Voice (modelled on Finch)
**Jiko speaks, not the app.** All in-app encouragement comes from Jiko, in the first person.

- **Warm and supportive:** a companion who's on the journey with you.
- **Celebrates effort, not outcome:** trying counts.
- **Validates first:** fear is normal; "my paws get shaky too."
- **Gently curious:** notices small things and asks how it felt.
- **Proud, never pushy.**

| Moment | Jiko says |
|---|---|
| Quest intro | "This one makes my tummy flutter a little. Want to try it together?" |
| Forecast | "How scary do you think it'll be? No wrong answers." |
| Completed | "You did it! You guessed it'd be an 8… how did it actually feel?" |
| Big fear gap | "A 7 that turned into a 2! Your brain was being very dramatic." |
| Went badly | "That was a brave thing to try. Not every door opens, and you still knocked." |
| Skipped | "That's okay! Want a smaller one instead?" |
| Returning after a gap | "I missed you! No catching up needed. Want something small today?" |

**Never:** guilt, "you failed", streak shame, hustle or alpha language ("grind", "king", "lock in"), clinical or therapy terms ("exposure", "symptoms"), sarcasm at the user's expense.

### 5.2 Hard limits (the only absolute rules)
A quest must **never**:
1. Involve illegal acts.
2. Carry a real risk of physical harm.
3. Include sexual content.
4. Deceive, pressure, humiliate, or record another person without their consent.
5. Require spending beyond the user's budget setting.

Everything else is open. Defaults and opt-in categories (§4.4) handle the rest.

### 5.3 Quality bar
Every quest must be:
- **Specific:** "Ask a barista what their favourite drink is and order it", not "Talk to someone new".
- **Doable within its stated time** and within 24 hours.
- **Clearly finishable:** the user knows when they're done.
- **A story worth telling:** it should feel like a small adventure.
- **At the right bravery level:** labelled honestly.

---

## 6. Jiko: the companion

### 6.1 Brave Days
Jiko grows from **Brave Days**, not calendar days. A Brave Day is any day the user completes a Daily Spark or a quest. This mirrors Finch's "adventure days": the pet grows when you act, not merely when time passes.

### 6.2 Life stages (one-time, permanent)

| Stage | Brave Days | Unlocks |
|---|---|---|
| **Snowball** | 0 | Onboarding: a baby snow monkey asleep inside a snowball. Naming it melts the snow. |
| **Snowdrop** | 1 | Newborn, oversized eyes. All Item slots (§6.6). Appearance: **Body colour** |
| **Scamp** | 7 | Playful baby, first wobbly steps. Appearance: **Eyes, Cheeks**. New animations |
| **Wanderer** | 21 | Fluffy youngster who starts exploring. Appearance: **Markings, Mouth**. Wanderings (§6.4), new emotes |
| **Climber** | 42 | Confident young monkey, sturdier build. Appearance: **Belly**. More expressive personality |
| **Trailblazer** | 66 | Fully grown, full snowy mane: the one who goes first. Appearance: **Head feature**. "Trailblazer" celebration and title |

Locked Appearance parts show as greyed silhouettes with a message from Jiko: "I need to grow a little bigger first! Let's go on more adventures." (Finch pattern.)

- **Jiko never resets.** Not between seasons, not after a break.
- Reaching Trailblazer takes **66 Brave Days**, the median habit-formation window. A steady user gets there in about one season.
- **After Trailblazer,** growth continues through stat levels (uncapped), titles, home expansion and seasonal collections.
- **Premium extras, optional:** alternate looks for each stage (colours, patterns). Growth itself is never paywalled.

### 6.3 Seasonal identity: items, not forms
There are **no seasonal forms or evolutions**. Life stages are the only evolution, which keeps Jiko consistent. Each season instead brings a **Signature Set** at the end of the pass: a themed outfit, a home set and a badge. Players keep it forever and can wear it any time.

### 6.4 Wanderings (light collection loop)
From the Wanderer stage on, completing a weekly quest sends Jiko on a short **Wandering** that lasts a few hours. Jiko comes back with:
- a small **discovery** (a one-line story or a fact about the world), and sometimes
- a **found item** (a common home or outfit cosmetic) or bonus Spark Gems, and
- very rarely, a **Pal** (§6.7).

Wanderings make each quest feel rewarded twice, give a reason to reopen the app later that day, and add character. Finch's adventures prove this pattern.

### 6.5 Reactions and personality
Jiko reacts on the home screen to check-ins, Sparks, quests, forecasts and long absences (always warmly). Over time Jiko develops **likes** that it reveals in conversation, based on which stats the user levels most ("I love it when we try new food!").

### 6.6 Cosmetics (Finch model)
The Jiko editor has two tabs: **Items** and **Appearance**. Jiko is drawn **front-on**, so every slot and part must read clearly from the front.

**Items: 12 slots, all open from Snowdrop**

| # | Slot | Notes |
|---|---|---|
| 1 | Outfit | Matching top-and-bottom set. Equipping it clears Top and Bottom, and equipping a Top or Bottom clears Outfit. |
| 2 | Top | |
| 3 | Bottom | |
| 4 | Hat | |
| 5 | Eyewear | Glasses, goggles, masks |
| 6 | Neck | Necklaces, scarves, bow ties |
| 7 | Shoes | |
| 8 | Held item | Off-hand item, e.g. lantern, book, flower |
| 9 | Back | Capes, wings, backpacks |
| 10 | Hair | |
| 11 | Aura | Sparkles and ambient effects |
| 12 | Pal | Companion creature that follows Jiko (§6.7) |

Every slot has a **None** option. The editor shows a live preview ("Trying on …") before purchase. Each item shows one of: Owned / Buy (Spark Gems) / PLUS / Available [date] (seasonal or Vault items).

**Appearance: 7 parts, unlocked by life stage (§6.2)**

| Part | Unlocks at | Examples |
|---|---|---|
| Body colour | Snowdrop | Fur tone: grey-brown, snow white, honey… |
| Eyes | Scamp | Shape and colour |
| Cheeks | Scamp | The red face: blush intensity and colour |
| Markings | Wanderer | Fur patterns on head and back |
| Mouth | Wanderer | Smile, tiny teeth, little open "o" |
| Belly | Climber | Lighter belly fur: shape and colour |
| Head feature | Trailblazer | Snow mane or crown tuft (thick winter fur) |

Once unlocked, changing an Appearance part is free. More options per part come from the shop, the pass and premium alternate looks.

### 6.7 Pals (Jiko's companions)
Pals are tiny companion creatures that belong to Jiko, the way Jiko belongs to the user.

- **Equipped Pal:** one Pal follows Jiko on the home screen and in the editor (Item slot 12).
- **Pal collection:** every other owned Pal lives in the home and wanders between furniture.
- **No needs:** Pals never get hungry, sad or neglected. They are purely for collection and charm.
- **Sources:**
  - **Monthly Trials:** each Trial awards a unique Pal (the headline Trial reward)
  - **Wanderings:** rare finds
  - **Season pass:** 1–2 premium tiers per season
  - **Shop:** a small rotating selection, priced in Spark Gems
- **Collection screen:** a Pal book with silhouettes for undiscovered Pals and a one-line story for each one found.

---

## 7. Jiko's Home (the world)

Jiko's world is a **cosy mountain hut** with fixed slots, using Finch's model. Every slot has a fixed position. A new item either **fills an empty slot** or **replaces** the item already there.

### 7.1 Slots (v1)

| Area | Slots |
|---|---|
| Room shell | Wallpaper · Floor · Door · Window · Ceiling light |
| Furniture | Bed · Dresser · Rug · Shelf · Desk |
| Decor | Wall art · Plant · Shelf item ×2 · Window-sill item |
| **Unlockable** | Trophy Cabinet · Onsen Garden (outdoor hot spring) · Attic (second room) |

### 7.2 Courage expands the home
Stat milestones unlock new **slots and rooms**. That is how real-world bravery grows the world.

| Milestone | Unlocks |
|---|---|
| Any stat Lv 3 | Shelf item slot #2 |
| Courage Lv 5 | **Trophy Cabinet**, which displays Trial trophies and season badges |
| Curiosity Lv 5 | **Window view** slot, with swappable views (city, ocean, mountains…) |
| Connection Lv 5 | **Guest chair** slot, where Allies' Jikos can visit (§10) |
| Body Lv 5 | **Onsen Garden**: the hut's own outdoor hot spring, where Jiko soaks after a brave day. Its own slots: onsen surround, stones, lanterns, plants, steam effect. Seasonal skins for the onsen (e.g. cherry blossom, autumn maple, winter snow) come from the shop and the pass. |
| Mind Lv 5 | **Attic** second room |
| Higher levels | More slots in the Onsen Garden and Attic (expandable over future seasons) |

### 7.3 Getting items
1. **Shop**, priced in Spark Gems, with a rotating weekly selection plus a permanent catalogue.
2. **Season pass tiers** (free and premium).
3. **Wanderings** (common items).
4. **Monthly Trials** (exclusive items).
5. **Plus items:** a set of shop items marked **PLUS** that only JIKO Plus members can buy (Finch model).

**Inventory:** every owned item is kept. Users can swap freely between owned items in the same slot. Owned items are marked as owned in the edit screen.

---

## 8. Season Pass

### 8.1 Structure (TFT-style single track)
- **Season length:** 66 days.
- **Track:** **60 tiers on one shared track.** You gain one tier per day you check in, by opening the app (a day runs on local time and rolls over at 4:00 am).
- **Grace:** 6 missed days still allow a full completion.
- **Free users:** tiers **4, 8, 12 … 60** are open to them (**15 rewards**). All other tiers show the reward with a 🔒 lock.
- **Premium users:** **every tier is open (60 rewards).**
- **Retroactive upgrade:** buying premium mid-season instantly grants every locked reward on tiers already reached. A user at tier 20 who upgrades gets 15 rewards at once, the main reason to upgrade mid-season.
- **Level packs:** buy **+5** or **+10** tiers to catch up or speed ahead (Spark Gems or cash). Buying tiers works on free and premium; free users still only receive rewards on open tiers.

### 8.2 Bonus check-ins (days 61–66)
Once tier 60 is reached, every extra check-in until the season ends pays escalating Spark Gems:

| Bonus check-in | 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|
| Spark Gems | 20 | 30 | 40 | 60 | 80 | 120 |

Bonus check-ins are open to **all users, free and premium**. They keep the daily habit going into the next season.

### 8.3 Reward types
- **Jiko items:** any of the 12 Item slots (§6.6), including full Outfits and Pals
- **Appearance options:** extra colours and styles for unlocked parts
- **Home items:** any slot (§7.1)
- **Spark Gems** bundles
- **Profile:** titles, frames, badges
- **Quest-card backs:** cosmetic card art for quest draws
- **Wrapped themes:** visual themes for the season recap
- **Jiko emotes and animations**
- **Signature Set** (tier 60 finale): outfit, home set and season badge

### 8.4 Season 1: "First Light" reward table
Rows in **bold** are free tiers. Every tier is premium. Item names are placeholders until brand work.

| Tier | Reward | | Tier | Reward |
|---|---|---|---|---|
| 1 | Dawn Scarf (outfit) | | 31 | 75 Spark Gems |
| 2 | 50 Spark Gems | | **32** | **Sunrise Bed (home)** |
| 3 | Lantern Shelf Item | | 33 | Emote: Stretch |
| **4** | **Firefly Lamp (home)** | | 34 | Quest Card Back: Embers |
| 5 | Title: "Early Riser" | | 35 | First Light Window View |
| 6 | Quest Card Back: Dawn | | **36** | **First Light Hat (outfit)** |
| 7 | 50 Spark Gems | | 37 | 75 Spark Gems |
| **8** | **Emote: Happy Hop** | | 38 | Shelf Item: Pocket Sun |
| 9 | Sunbeam Rug (home) | | 39 | Frame: Morning Gold |
| 10 | Dawn Goggles (outfit) | | **40** | **150 Spark Gems** |
| 11 | 50 Spark Gems | | 41 | Wall Art: Horizon |
| **12** | **Title: "First Light"** | | 42 | Emote: Victory Dance |
| 13 | Plant: Morning Glory | | 43 | 100 Spark Gems |
| 14 | Frame: Sunrise | | **44** | **Dawn Dresser (home)** |
| 15 | Pal: Glowmoth | | 45 | Sunrise Cape (outfit) |
| **16** | **100 Spark Gems** | | 46 | Plant: Golden Fern |
| 17 | Held Item: Tiny Torch | | 47 | 100 Spark Gems |
| 18 | Emote: Wave | | **48** | **Wrapped Theme: Golden Hour** |
| 19 | 75 Spark Gems | | 49 | Desk: Explorer's Table |
| **20** | **Wallpaper: Dawn Stripes** | | 50 | Title: "Lightbringer" |
| 21 | Shelf Item: Sun Jar | | 51 | 150 Spark Gems |
| 22 | Door: Sunrise Arch | | **52** | **Held Item: Lantern** |
| 23 | 75 Spark Gems | | 53 | Floor: Sunlit Boards |
| **24** | **Dawn Boots (outfit)** | | 54 | Emote: Fireworks |
| 25 | Wrapped Theme: First Light | | 55 | Frame: Legendary Dawn |
| 26 | Rug: Sun Medallion | | **56** | **200 Spark Gems** |
| 27 | Title: "Edge Walker" | | 57 | Ceiling Light: Sun Chandelier |
| **28** | **Plant: Sun Sprout** | | 58 | Onsen Garden Item: Stone Lantern |
| 29 | Animated Jiko pose: Sunrise | | 59 | 250 Spark Gems |
| 30 | Full Outfit: Morning Explorer | | **60** | **Signature Set: "First Light" (outfit + home set + badge)** |

*Free track: 15 rewards (5 home items, 2 outfit pieces, 1 held item, 1 emote, 1 title, 1 Wrapped theme, 3 gem bundles, Signature Set). Premium adds 45 more.*

### 8.5 Season themes (future)
Each season has a name, a colour story, a Signature Set, a featured Monthly Trial line and its own Wrapped theme. Past premium items return in a **Vault** rotation in the shop about a year later, so missing a season never means losing an item forever.

---

## 9. Spark Gems (single currency)

**Earned:**

| Action | Gems |
|---|---|
| Daily Spark | 5 |
| Weekly quest | 10 × bravery level (10–100) |
| Fear Gap bonus | +2 per point of positive gap |
| First quest of a new stat | 25 |
| Monthly Trial | 150 |
| Wanderings (occasional) | 5–20 |
| Pass tiers | Per table |
| Bonus check-ins | 20–120 |

**Purchased:** gem packs for real money.

**Spent on:**
- shop items for Jiko and the home (about 100–800 gems)
- level packs
- premium quest packs (alternatively included in Plus)

*All numbers above are starting values to tune.*

---

## 10. Allies (optional social layer)

- **Add friends** by code or link.
- **Cheer:** send a reaction to an Ally's completed quest.
- **Visit:** an Ally's Jiko can visit your home's Guest chair (Connection Lv 5).
- **Share:** Wrapped cards and quest completions, sent to Allies or to external social apps.
- **Shared quests, occasional:** an optional invite to do the same quest in the same week.

**Allies rule:** no Allies-only rewards, no social XP multipliers, no leaderboards needed to progress. A player with zero Allies misses nothing.

---

## 11. Season Wrapped

Unlocks in the last 3 days of the season. It's a swipeable story of 8–10 cards, plus one shareable summary card (9:16 and 1:1).

| Card | Content |
|---|---|
| 1 | "Jiko's season" intro: life stage reached, outfit worn |
| 2 | Brave Days count + quests completed |
| 3 | **Fear vs Reality:** average overestimate % |
| 4 | Biggest fear gap: "You guessed 9. It was a 3." |
| 5 | Scariest quest completed (highest actual rating) |
| 6 | Stat breakdown: top stat, most improved stat |
| 7 | Bravest week |
| 8 | Places explored (count of optional location tags) |
| 9 | Jiko's favourite discovery from Wanderings |
| 10 | Your season title: generated from patterns, e.g. "The Social Explorer" |
| Share | Summary card with Jiko in the Signature Set |

Free users get the full Wrapped. Premium adds animated themes and extra cards (deeper insights).

---

## 12. Monetisation

| Product | Includes | Price (to test) |
|---|---|---|
| **Season Pass (Premium)** | All 60 tiers for one season | $4.99 / season |
| **JIKO Plus (annual)** | Premium pass for every season in its term, Plus-only shop items, all quest packs, deeper Fear Insights, premium Wrapped, alternate life-stage looks | $24.99 / year |
| **Level packs** | +5 / +10 tiers | ~$1.99 / ~$3.49 or gem equivalent |
| **Spark Gem packs** | Currency | Tiered |

**Always free:** the Daily Spark, weekly quests, Monthly Trials, Fear Forecast, all life stages, the home and every stat unlock, Allies, Season Wrapped, and 15 pass rewards per season.

**Paywall rules:** no hard paywall after onboarding. Free trials say clearly when they convert. Cancelling takes one tap via store subscriptions. No prompts asking for a rating before the user has had value from the app.

---

## 13. Onboarding (about 90 seconds to the first Spark)

1. A snowball sits in the snow, gently breathing. "Something's sleeping in here…"
2. Three quick questions:
   - "What would you love more of?" (pick up to 2 stats)
   - Setting (city / town / countryside)
   - Budget
3. **Name your Jiko.** The snow melts away, and a baby snow monkey blinks awake.
4. **First Daily Spark** right away, at bravery 1, plus an introduction to the Fear Forecast.
5. Check-in explained: "Open the app each day and you'll climb the season track."
6. A soft mention of Premium, skippable. No hard paywall.

---

## 14. Notifications (gentle by default)
- One daily reminder at a time the user picks, written in Jiko's voice: "I found a tiny adventure for us ✨"
- Weekly: "Your new quest cards are ready."
- "Jiko's back from a Wandering!"
- Season: 7 days left, Wrapped ready.
- **Never:** streak-loss threats or guilt. A user can mute all notifications in one tap.

---

## 15. Brand & visuals
Full brand working document: `product/BRAND.md`.

**Locked:**
- **Jiko is a Japanese snow monkey** (macaque). Origin story and life stages in §6.2 and BRAND.md.
- **Art style:** Finch-style flat 2D, front-on.
- **Tagline:** "Every brave tradition started with one monkey who went first."
- **World:** a cosy mountain hut with an Onsen Garden.

**Open:**
- Colour palette, typography, logo
- Visual design of the pass screen (reference: TFT single track with locked and open tiles)
- Motion, sound, haptics
- Season 1 final naming

---

## 16. Data model (v1)

```
User            id, created_at, timezone, setting, budget, time_pref,
                enabled_categories[], notification_time, plus_status
Jiko            user_id, name, brave_days, life_stage, likes[],
                equipped{item_slot→item_id},          -- 12 Item slots (§6.6)
                appearance{part→option_id}            -- 7 parts, gated by life_stage
AppearanceOption id, part(enum7), unlock_stage, plus_only, gem_price?, source
Stat            user_id, stat(enum5), xp, level, edge_level
Quest           id, title, flavour, action, stat, bravery, time_band, cost_band,
                setting_fit[], mode, categories[], reflection_prompt,
                source(seed|ai), status(active|retired), rating_avg
QuestAssignment id, user_id, quest_id, type(spark|weekly|trial|pack),
                week_id, drawn_at, redrawn, status(open|done|skipped)
Completion      assignment_id, forecast(1-10|null), actual(1-10|null),
                reflection, photo_url?, location_tag?, completed_at, feedback(+1|-1|null)
CheckIn         user_id, season_id, local_date            -- unique per (user, local_date)
Season          id, name, start_at, end_at, tier_count=60, bonus_days=6
SeasonTier      season_id, tier, reward_id, is_free
PassState       user_id, season_id, tier, premium(bool), bonus_checkins, purchased_levels
Item            id, kind(jiko_item|home|title|frame|cardback|emote|wrapped_theme),
                slot?,   -- jiko_item: outfit|top|bottom|hat|eyewear|neck|shoes|held|back|hair|aura|pal
                         -- home: see §7.1
                rarity, plus_only, gem_price?, source, available_from?, story?(pal)
Inventory       user_id, item_id, acquired_at, source
HomeLayout      user_id, room, slot → item_id
Wandering       user_id, started_at, returns_at, discovery_text, item_id?, gems
Wallet          user_id, gems ; Ledger(user_id, delta, reason, ref_id, at)
Ally            user_id, ally_id, status
WrappedSnapshot user_id, season_id, payload(json)
```

---

## 17. v1 scope

**In:**
- Onboarding and the snowball awakening
- Daily check-in and the season pass (single track, free and premium tiers, retroactive upgrade, level packs, bonus check-ins)
- Daily Spark, weekly 3-card draw, Monthly Trial
- Fear Forecast and basic Insights
- AI quest pipeline with seed pool, validator and pool cache
- 5 stats with Edge Levels
- Jiko with 6 life stages, reactions and Wanderings
- Jiko editor: 12 Item slots, 7 Appearance parts gated by life stage
- Pals: equip one, collection book, Trial and Wandering sources
- Home with fixed slots, Shop, Inventory, and stat-unlocked Trophy Cabinet and Window view
- Spark Gems economy, IAP for Premium pass, Plus, gems and level packs
- Season Wrapped and share card
- Gentle notifications
- iOS and Android

**Later:**
- Onsen Garden and Attic (scaffolded, unlocked in Season 2)
- Allies, Visits and shared quests
- Premium quest packs beyond 2 launch packs
- Weather and location awareness
- Vault rotation (from Season 5)

---

## 18. Decision log

| # | Decision |
|---|---|
| 1 | Solo-first loop; Allies optional with no exclusive rewards |
| 2 | Fear Forecast is the signature mechanic |
| 3 | Jiko is a Finch-style companion; Jiko's voice is the app's voice |
| 4 | Voice is warm and supportive (Finch model), not mischievous |
| 5 | The world is Jiko's **home with fixed slots** (Finch model); the real-world map is dropped |
| 6 | AI writes quests under the Quest Constitution |
| 7 | Hard limits only cover harm; no location or format restrictions; opt-in categories |
| 8 | Personalisation v1: budget, time, setting, forecast history; no weather or precise city |
| 9 | Pass advances on daily check-ins, not quest XP (fake-proof) |
| 10 | 66-day season, 60 tiers, 6 grace days |
| 11 | TFT-style single track: free every 4th tier, premium all tiers, retroactive |
| 12 | Level packs (+5 / +10) for sale |
| 13 | Bonus check-ins on days 61–66 pay 20→120 gems |
| 14 | No comeback tokens |
| 15 | Single currency: **Spark Gems** |
| 16 | Growth never fully paywalled; premium adds optional extras |
| 17 | Jiko never resets; 6 life stages over 66 Brave Days; seasonal **Signature Set**, not seasonal forms |
| 18 | Real-world group events dropped |
| 19 | Season Wrapped (Spotify-Wrapped style) |
| 20 | No user-testing plan in scope; build first |
| 21 | Brand and visuals worked on after the spec (see §15) |
| 22 | Wanderings, stat-unlocked home slots, JIKO Plus, starting gem economy and 4am rollover approved |
| 23 | Jiko editor uses Finch's model: **Items** (12 slots) + **Appearance** (7 parts) |
| 24 | Appearance parts unlock by life stage; front-on avatar, so **Mouth** replaces Tail |
| 25 | **Pals** added: collectible companions for Jiko; headline Monthly Trial reward |
| 26 | **Jiko is a Japanese snow monkey**; Finch-style flat 2D, front-on |
| 27 | Life stages renamed: Snowball → Snowdrop → Scamp → Wanderer → Climber → Trailblazer |
| 28 | Onboarding: the snowball melts when the user names Jiko (replaces the egg) |
| 29 | Home is a cosy mountain hut; **Onsen Garden** unlocks at Body Lv 5 and gets seasonal skins |
| 30 | Tagline: "Every brave tradition started with one monkey who went first." |
