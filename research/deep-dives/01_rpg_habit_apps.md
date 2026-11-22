# Competitive landscape 01: RPG-style and gamified habit trackers / "level up your life" apps

Research date: 2026-11-22. Scope: apps that turn habits, self-care, focus, fitness or quitting a vice into a game (XP, avatars, pets, quests, streaks, loot, ranks).

## How the numbers were collected (read first)

- **App Store (US)**: iTunes Search/Lookup API, pulled 2026-11-22. "iOS ratings" = `userRatingCount` (lifetime US ratings unless Apple reset them). IAP price lists were scraped from the public apps.apple.com US page for each app.
- **Google Play (US)**: `google_play_scraper` (`app()`), pulled 2026-11-22. "Installs" = the public bucket; "real installs" = the scraper's `realInstalls` field (Google's internal exact-ish count shown in page data). "Play ratings" = number of ratings.
- **Review mining**: for ~35 apps I pulled the 200–400 *newest* Google Play reviews (US/English) and read every 1–2★ and a sample of 5★ reviews. "1–2★ share" in the tables below = share of 1–2★ in that recent sample. It is a snapshot of current sentiment, not the lifetime average, and the time windows differ by app (busy apps cover ~2 weeks, small apps cover months/years).
- **Revenue/funding**: only from press, company statements or named third-party estimators (Sensor Tower, AppMagic, Appfigures, Adapty, etc.). Estimates are labeled as such. Where I could not find a number, I say so rather than guess.
- Raw data files (TSV) are in `/tmp/claude-0/-home-user-JIKO-APP/991f7682-4e32-5a50-8877-e20cdbe323fc/scratchpad/work/` (`ios_out.tsv`, `ios_out2.tsv`).

---

## Master table (hard numbers, 2026-11-22)

| App | Developer (country) | iOS US rating / # ratings | Play rating / # ratings | Play installs (bucket / real) | Launched | Recent Play 1–2★ share |
|---|---|---|---|---|---|---|
| Finch: Self-Care Pet | Finch Care PBC (US) | 4.95 / 778,291 | 4.88 / 643,552 | 10M+ / 16.8M | 2021 | 10% (n=400) |
| Me+ Lifestyle Routine | Enerjoy Pte (Singapore) | 4.80 / 249,016 | 4.71 / 865,836 | 10M+ / 23.9M | iOS 2022, Play 2023 | 20% |
| Fabulous | TheFabulous | 4.42 / 89,622 | 3.82 / 590,428 | 10M+ / 27.8M | 2013 (Play) | **60.5%** |
| Forest | Seekrtech (Taiwan) | 4.79 / 49,616 | 4.29 / 814,394 | 10M+ / 50.0M | 2014 | 36% |
| Duolingo (benchmark) | Duolingo (US) | 4.72 / 5,612,297 | 4.75 / 52.1M | 1B+ / 1.0B | 2012 | n/a |
| I Am Sober | I Am Sober LLC (US) | 4.88 / 191,746 | 4.75 / 144,565 | 10M+ / 12.9M | 2013 | 8% |
| Structured | unorderly GmbH (Germany) | 4.79 / 169,243 | 4.59 / 33,030 | 1M+ / 2.6M | 2020 | 21% |
| Waterllama | Llama Luna Apps | 4.87 / 165,150 | (no real Play version found) | – | 2019 | – |
| Plant Nanny | SPARKFUL (Taiwan) | 4.72 / 106,736 | 4.65 / 180,946 | 5M+ / 6.3M | 2019 (v2) | 7% |
| Liftoff – Ranked Gym | Liftoff Labs (US) | 4.82 / 103,597 | 4.74 / 103,918 | 1M+ / 2.2M | 2023 | 10% |
| Productive | Mosaic S.r.l. (Italy) | 4.60 / 91,063 | 3.66 / 20,899 | 1M+ / 3.2M | 2015 | 30% |
| Flora – Green Focus | AppFinca (Taiwan) | 4.76 / 83,050 | 4.60 / 3,771 | 100K+ / 0.24M | 2017 | – |
| Pikmin Bloom | Niantic → Scopely | 4.81 / 71,395 | 4.76 / 260,511 | 5M+ / 9.4M | 2021 | – |
| Unchaind (quit porn, faith) | Rocapine (France) | 4.83 / 50,246 | 4.71 / 73,535 | 100K+ / 0.36M | 2025 | 11% |
| Lock In – Reset Your Life | Omega Labs LLC (US) | 4.75 / 27,777 | 4.73 / 5,743 | 50K+ / 54K | 2025 | 10% |
| Streaks | Crunchy Bagel (Australia) | 4.81 / 27,353 (paid $5.99) | iOS only | – | 2015 | – |
| Brainbuddy (quit porn) | AppStudio Australia | 4.68 / 26,062 | 4.67 / 31,325 | 500K+ / 0.85M | 2013 | – |
| Pokémon Sleep | The Pokémon Co. (Japan) | 4.54 / 25,414 | 4.40 / 139,755 | 10M+ / 13.6M | 2023 | – |
| Zombies, Run! | Six to Start (UK) | 4.79 / 24,155 | 3.90 / 27,096 | 1M+ / 3.3M | 2012 | – |
| Tiimo | Tiimo ApS (Denmark) | 4.60 / 21,886 | 4.57 / 4,079 | 100K+ / 0.14M | 2019 | 28% |
| **Arise: Level Up Workout Game** (iOS) | Digital Lions Apps SL (Spain) | 4.76 / 20,989 | – | – | Apr 2025 | – |
| **Arise: Workout & Fitness RPG** (Play) | Golden Gate Media (pkg `llc.sololeveling.Arise`) | – | 4.56 / 275,977 | 1M+ / 2.2M | Apr 2025 | 16% |
| RiseGuide | Celeb Innovations / RiseGuide | 4.60 / 20,198 | 4.23 / 5,233 | 100K+ / 0.38M | 2024 | – |
| Routinery | Routinery Corp (Korea) | 4.71 / 18,228 | 4.41 / 18,864 | 1M+ / 2.26M | 2019 | 19% |
| Do Habits | Kodeon (US) | 4.05 / 16,877 | – | – | 2016 | – |
| Grit: Daily Habit Tracker | GrittyApps | 4.78 / 16,423 | (different "Grit" on Play) | – | 2023 | – |
| Life Reset: 66 Day Habit (formerly "Rise") | Savvy Tech Ltd / "Design and Build" | 4.71 / 13,319 | 4.66 / 22,065 | 500K+ / 0.79M | 2024 | 20% |
| Focus Friend by Hank Green | Honey B Games (US) | 4.84 / 10,638 | 4.89 / 13,522 | 1M+ / 2.14M | Jul–Aug 2025 | 4.5% |
| Habit Rabbit | J. P. Silang / SuperByte | 4.66 / 8,867 | 4.61 / 7,824 | 500K+ / 0.64M | 2021 | – |
| Walkr | SPARKFUL (Taiwan) | 4.53 / 8,087 | 4.19 / 77,045 | 1M+ / 1.2M | 2014 | – |
| SuperBetter | SuperBetter LLC (US) | 4.65 / 7,883 | 4.04 / 6,554 | 100K+ / 0.34M | 2012 | 20% |
| DAWG – Discipline | DWG Labs LLC (US) | 4.75 / 7,243 | 4.54 / 13,341 | 100K+ / 0.39M | 2025 | **52%** |
| Habitify | Unstatic (Vietnam) | 4.59 / 7,210 | 4.20 / 6,679 | 500K+ / 0.69M | 2016 | 26% |
| Tangerine | Bitdreams OÜ (Estonia) | 4.71 / 6,640 | iOS only | – | 2020 | – |
| Joon (kids ADHD) | Joon App Inc (US, YC W22) | 4.68 / 6,569 | parent app 10K+ / 31K; pet game 100K+ / 135K | – | 2020 | – |
| Seed (gamified NoFap) | Nara Capital / Quiet Games | 4.66 / 6,509 | 4.42 / 78,449 | 1M+ / 1.16M | 2024–25 | 10.5% |
| (Not Boring) Habits | Not Boring Software (US) | 4.78 / 6,397 | – | – | 2021 | – |
| Voidpet Garden | Voidpet Inc (US) | 4.86 / 5,725 | 4.53 / 15,666 | 500K+ / 0.99M | 2023 | 22.5% |
| Focus Plant | Shikudo (Taiwan) | 4.72 / 5,473 | 4.16 / 58,148 | 1M+ / 4.19M | 2019 | – |
| Quabble | museLIVE (US/Korea) | 4.80 / 4,607 | 4.64 / 13,887 | 500K+ / 0.86M | 2023 | – |
| **Habitica** | HabitRPG Inc (US) | 4.33 / **3,731** (count appears reset) | 4.63 / 76,522 | 5M+ / 8.45M | 2013 web; 2015 apps | 14% |
| Cub: Self Care Pet | Offbeat Apps (US) | 4.68 / 3,229 | 4.24 / 799 | 50K+ / 61K | 2023 | – |
| Monke – Habit Game | Myles Root / Monke Business Ent. | 4.83 / 2,023 | **2.38** / 114 | 10K+ / 12.6K | Dec 2025 | **67%** |
| Habit Hunter (Goal Hero) | Tien Long Nguyen / Active User Studio | 4.64 / 807 | 4.46 / 3,629 | 100K+ / 0.10M | 2018 | – |
| Brili Routines | Brili GmbH | 4.65 / 605 | 3.95 / 1,131 | 50K+ / 95K | 2021 | 31% |
| SleepTown | Seekrtech (Taiwan) | 4.65 / 1,468 (paid $1.99) | 4.07 / 13,973 | 1M+ / 1.6M | 2017 | 15% |
| Skilltree | Project Skill Tree Ltd (UK) | 4.72 / 285 | 4.48 / 2,851 | 50K+ / 58K | 2023 | 7.5% |
| Levla: Habit Tracker RPG | 1v9 Holding AB / Turbo Labs SE (Sweden) | 4.92 / 148 | 4.81 / 1,333 | 10K+ / 38K | 2026 | 6.5% |
| Dual: Solo Leveling For Life | Pei-Tzu Huang (indie) | 4.66 / 139 | – | – | 2025 | – |
| Do It Now: RPG To Do List | Taras Lozovyi (Ukraine) | (iOS clone by other dev: 1.17 / 6) | 4.14 / 12,739 | 1M+ / 1.30M | 2016 | 20% |
| LifeUp: Gamify Tasks & Habits | LifeUp Apps (indie) | – (Android-first) | 4.67 / 7,191 | 100K+ / 0.32M | 2019 | 7% |
| Solo Leveller: The System | The Leveller Project | – | 3.86 / 1,732 | 500K+ / 0.61M | 2024 | 18% |
| ARISE SOLO – Level Up System | Arise Solo | – | 4.58 / 3,867 | 50K+ / 92K | 2025 | 5.7% |
| Lion XP: Gamify Life | Poxi AS (Norway) | 4.49 / 313 | 3.67 / 188 | 5K+ / 7K | 2024 | – |
| Loop Habit Tracker | Álinson S. Xavier (open source) | (no official iOS) | 4.72 / 63,754 | 5M+ / 8.0M | 2016 | 2.4% |
| HabitNow | HabitNow Apps | – | 4.75 / 93,801 | 5M+ / 7.3M | 2019 | 3.5% |
| HabitKit | Sebastian Röhl (Germany) | 4.84 / 2,619 | 4.54 / 12,265 | 500K+ / 0.78M | 2022 | – |
| Focus Quest (Shikudo) | Shikudo | – | 4.53 / 6,881 | 500K+ / 0.85M | 2021 | 19% |
| LifeRPG | Jayvant Javier Pujara | – | **removed from Google Play (404)** | – | ~2014 | – |
| EpicWin | Supermono Ltd / RexBox (UK) | **removed from App Store 2024-06-20** (AppBrain) | – | – | 2010 | – |

Notable smaller 2024–26 entrants found on the US App Store (ratings count in brackets): Idle Habits RPG [63], Pixel Fantasy – Habit Game [270], Levla [148], HabitForge [8], Habit Legends [8], HeroDay [2], ASCENSION [13], XP Tracker [4], Habit Dragon [4], HabitRealm [3], QuestHabit [0], Orbit RPG Habit Quest [3], Life Rank [1], Questify [1], Forgeborn: Life RPG [3], Sigils: Life RPG & AI Mentor [0], Arete [0], PORTAL Real Life RPG [1], LifeFlow [0], RPG Life [6], RPLife [155], Level Up Life: Arise Leveling [50], Skillion [32], Statos [29], ASCEND AI [70], Evolve [2], Ashborn [4], RP6 [1], Quest Leveling: Arise [36], SYSTEM AI [28], Monarch: Leveling Workout RPG [95], LEVELING: Fitness [870], Solo Hunter [7], The System: RPG Habit Tracker [2], SYSTEM // ZERO [0], Solo Leveling Your Self [5], Disciplinex [8], Rankup [5], Mastermind [53], Mindscape [112], Habit Slayer [14], Habbie [242], Otto [344], Habit-chi [5], Mochi [0], Momo (O7) [2,267], Catzy [1,122], Callie [3,696], Taskoria ADHD Planner RPG [5], ModernSam: The Self-Care RPG [70], Superhabits [401], Dialed In [29]. **Takeaway: the "System/level-up RPG habit app" niche has 50+ live iOS apps, almost all with fewer than 300 ratings. It is a long tail of indie and vibe-coded clones; very few break out.**

---

# Part A: Classic RPG habit trackers (avatar plus user-authored tasks)

## 1. Habitica (formerly HabitRPG)

- **Developer / company**: HabitRPG, Inc. (US). Started by Tyler Renelle as a spreadsheet, then a web app. Kickstarter launched 11 Jan 2013 with a $25K goal and raised ≈$41K from ~2,800 backers. Incorporated 2014 (co-founders include Siena Leslie and Vicky Hsu). Renamed Habitica on 31 Jul 2015. Open source (GitHub HabitRPG/habitica), with a large volunteer contributor community.
- **Platforms**: Web, iOS (2015), Android (Play listing since Dec 2015), plus a basic watch app. Public API used by many community extensions.
- **Core loop and mechanics**: 8-bit pixel avatar. Three task types: **Habits** (+/− buttons), **Dailies** (missed dailies deal HP damage at "cron", the day rollover) and **To-Dos**. Completing tasks earns XP, gold and random **drops** (eggs, hatching potions, food), so you collect and raise **pets and mounts**. **Classes** unlock at level 10 (Warrior, Mage, Healer, Rogue) with skills. **Equipment** shop. **Parties** of up to ~30 players take on **Quests**: boss fights where your completed tasks deal damage and each member's missed dailies hurt the whole party. Collection quests too. **Challenges** with gem prizes, a custom reward shop (spend your own gold on real-life treats), streaks on dailies, seasonal events with limited gear, and **death** (HP reaches 0: lose a level and gold). In August 2023 Habitica shut down the **Tavern and public Guilds** (official FAQ: "a disproportionately small percentage of our player base" used them, plus "new content regulations". Community view: in-house moderation was too heavy). Parties and Challenges remained.
- **Target audience**: Gamers, students, ADHD users, and people who like spreadsheets, systems and nostalgic RPGs. Skews millennial/Gen Z.
- **Monetization**: Free core. **Subscription** $4.99/mo, $14.99/3 mo, $29.99/6 mo, $47.99/yr. Gives monthly Mystic Hourglasses and subscriber items, the ability to buy gems with gold, and longer data history. **Gems IAP**: 4 gems $0.99, 21 gems $4.99, 42 gems $9.99, 84 gems $19.99, used for quests, backgrounds and outfits. No ads.
- **Store data**: iOS 4.33★ with only **3,731 ratings** (the count looks reset, which is odd for a decade-old app). Google Play 4.63★, 76,522 ratings, 5M+ installs (8.45M real installs).
- **Revenue / users**: No reliable public revenue figures. Third-party "4M+ users" claims are unverified.
- **Press**: Lifehacker, The Verge and many "best habit app" lists. A Wikipedia article exists. Frequently the canonical example of gamified productivity in academic papers.
- **What users love**: "It's changed my life so much for the better… I like it more than Finch, feels like I'm making my life more of a game." Loved for being F2P with no paywall and no popups, for the API ("fantastic API access"), for parties with friends or partners, and for losing HP as real stakes.
- **What users complain about** (recent Play sample, 14% 1–2★): **dated, clunky UI** ("looks like it was created around the same time the first computer was"); **stagnation** ("in nine years… it's never had a new feature"); **sync bugs** that count dailies twice and kill the avatar; **no offline mode**; **no onboarding/tutorial**; overwhelming for ADHD users ("all the different tabs"); "more tedious than rewarding"; **punishing damage creates a shame spiral** ("losing at life every time I start my Habitica day"); a weak watch app; privacy concerns. On Reddit and comparison blogs the recurring line is that people "spend more time managing Habitica than doing the habits". The honor system is easy to cheat, and **the game layer is thin**: one reviewer asks for real monsters and loot ("defeating level 2 monsters could drop trousers").
- **Decline signals**: Removing the Tavern and Guilds cost it its town square. Most growth in the space moved to Finch-like cozy apps and paywalled "level up" apps. Habitica is still alive and has a large installed base, but has had little press momentum since 2020.

## 2. LifeRPG

- **Developer**: Jayvant Javier Pujara (indie). Android only. Free.
- **Mechanics**: Missions (tasks) grant XP, user-defined **skills** level up when missions are assigned to them, a character level, a reward store, reminders and repeats. Very bare UI.
- **Status**: **Dead.** The Google Play package `com.jayvant.liferpgmissions` now returns 404. AlternativeTo users report no updates since ~2017. It is still cited in old "best life RPG apps" lists such as Android Authority's.
- **Why it died**: A solo developer with no monetization and no polish. Its ideas (custom skill trees, XP per real-world skill) were absorbed by Do It Now and LifeUp. One Do It Now reviewer: "Used LifeRPG… It was unfinished product. Do It Now is like someone… finished [it]".

## 3. Do It Now: RPG To Do List

- **Developer**: Taras Lozovyi (indie, Ukraine). Package `com.levor.liferpgtasks`, on Play since Jan 2016. Android only. An unrelated iOS app with the same name has 6 ratings and a 1.17★ average.
- **Mechanics**: The user defines **characteristics** (Strength, Intelligence…) and **skills**. Tasks give XP to skills with configurable weights. Character level, achievements, a custom rewards shop, gold, inventory, statistics graphs, widgets, and penalties for failed tasks. Deeply customizable: an "RPG spreadsheet for life".
- **Monetization**: Freemium with IAP from $0.99 to $49.99 (premium subscription plus a lifetime option). Users ask for a one-time payment instead of a subscription.
- **Store**: Play 4.14★, 12,739 ratings, 1M+ installs (1.30M real).
- **Loves**: "Robust features and responsive devs", fine-tuning skills, a sense of long-term growth.
- **Complaints** (20% 1–2★): Updates broke graphs and widgets, slow load times ("five minutes to load"), notification-permission nagging, preset tasks that can't be removed without lowering stats, backfilling missed days is painful, and subscription-only premium.

## 4. LifeUp: Gamify Tasks & Habits

- **Developer**: LifeUp Apps (indie, Android-first; package `net.sarasarasa.lifeup`), on Play since Apr 2019. A cloud/HTTP API companion app and a sister app "ulives" exist.
- **Mechanics**: Self-built gamification toolkit: tasks earn XP across user-defined attributes, coins, a custom **shop**, **loot boxes** ("bags of coins") and synthesis/crafting, achievements, a pomodoro timer and a "feelings" journal. You design the game yourself.
- **Monetization**: One-time Pro purchase, $2.99 (via Play IAP).
- **Store**: Play 4.67★, 7,191 ratings, 100K+ installs (319K real).
- **Loves**: "This app is changing my life… house is cleaner, exercised more" and the depth of customization.
- **Complaints** (7%): **Backlash against added generative-AI features** ("went from something I used every day for years to something I now need to find an alternative to"); "very detailed, very confusing, takes a LOT of work to set up"; not ADHD-friendly; can't change the day-end time for night-shift workers; notifications; "you make up tasks to collect coins… no monetary value".

## 5. HabitRPG clones (2024–2026 wave)

Across the dozens of small apps listed above, the patterns are the same: a pixel or anime hero, XP/gold/levels, a gear shop, bosses damaged by your habits, and sometimes an idle-game layer.

- **Levla: Habit Tracker RPG** (1v9 Holding AB / Turbo Labs SE, Sweden, 2026). Positions itself as "Habitica fixed". Unlimited habits and to-dos with no ads. Every check-in earns XP, coins and **stamina** for a character who **adventures while you work** (focus mode). Explicitly **"A missed day never costs your character health or gear"**: streaks reward "consistency, not perfection". Membership $5.99–9.99/mo, $29.99–69.99/yr, lifetime $99.99–199.99. Play 4.81★ / 1,333 ratings / 38K installs; iOS 4.92★ / 148. Complaints: lockups during character setup, a "convoluted, nested" interface, a "free" label followed by a $70/yr ask, and a card required even for the free tier. One sharp critique: "RPG players aren't looking to do something IRL to get stuff done in their mobile game". The company publishes SEO comparison pages ("best apps to level up your real life like an RPG").
- **Habit Hunter: Gamified Routine** (Goal Hero; Active User Studio / Tien Long Nguyen, 2018). Hero, gold, weapons, armor, skills, monsters you defeat by keeping streaks, and a built-in Pomodoro timer. Play 100K+ / 3,629 ratings; iOS 807.
- **TaskHero: Task & Habit RPG** (Whetware, 2025). Play 4.70★ / 95 ratings / 36K installs.
- **Idle Habits RPG** (2024). "100% free forever, no ads, no IAP". Morning routine powers up the hero, the hero adventures all day, and the evening routine collects rewards. 4.83★ / 63.
- **Pixel Fantasy – Habit Game** (2026). Knight/Mage/Rogue classes, kingdom building, bosses defeated through consistency. 4.67★ / 270, in 10 languages.
- **RPLife** (2019), 4.87★ / 155. **Habit Legends**, **HeroDay**, **HabitForge**, **Habit Dragon**, **HabitRealm**, **QuestHabit**, **Orbit**, **ASCENSION**, **Forgeborn**, **Sigils: Life RPG & AI Mentor**: all have fewer than 20 ratings.
- **"Questlog"**: several apps share the name: Questlog – RPG To-Do List (2026, 5 ratings), Quest Log: Real Life RPG (0), Quest Log: Game TODO (1). There is no meaningful player.
- **"Habit Hero"**: at least 8 different App Store apps with this name, all with 0–1 ratings (kids routine, fitness, AI tracker). On Play, "Habit Tracker – Habit Hero" (10x Engineer) shows 500K+ installs, 4.8★. **The name is commoditized; there is no category leader called Habit Hero.**
- **Lesson**: Cloning Habitica's visual RPG is trivial (many of these look AI-assisted). Distribution is the moat, not mechanics.

## 6. EpicWin (defunct, history)

- **Developer**: Supermono Ltd (London; also made MiniSquadron), published under the RexBox brand and associated with Rex Douglass. iPhone, launched Aug 2010. Paid app (around $2.99 at launch).
- **Mechanics**: A streamlined to-do list with a role-playing spin. Each completed task gives XP and a **tiny animated battle** in which your character beats a monster. Loot, stat points, a journey map and character classes (skeleton, etc.).
- **Reception**: Heavy 2010 tech press (Gameranx, AppAdvice, Wirefly, Gamecola). AppGrooves shows about 1,500 reviews. Early critics already raised the cheating problem: you can check off tasks without doing them.
- **Fate**: Updates stopped years ago, and AppBrain reports it was **removed from the App Store on 2024-06-20**. Supermono was associated with an acquisition by Red Robot Labs.
- **Why it faded**: A paid-upfront business model with no recurring revenue to fund content, no social layer, iOS only, and a shallow loop: the battle animation is the same every time. Habitica (free, social, web plus mobile) took the category in 2013.

---

# Part B: Cozy companion and pet apps (care for a creature by caring for yourself)

## 7. Finch: Self-Care Pet (category leader)

- **Developer**: Finch Care Public Benefit Corporation (US). Founders Stephanie Yuan and Thomas "Nino" Budi (ex-Quora). Launched May 2021. **Bootstrapped, no VC** (its LinkedIn says "profitable"; investor commentator @ArfurRock: "bootstrapped & extremely profitable… best-in-class D30 retention beating Duolingo, Calm, Headspace… declined to raise").
- **Platforms**: iOS, Android.
- **Core loop**: You hatch a baby bird. Each completed self-care goal (drink water, journal, breathe, any custom goal) gives your bird **energy**. With enough energy the bird goes on an **adventure** and comes back with stories, so your progress is told as the pet's journey. Rainbow Stones currency buys clothes and furniture (cosmetics). Micro-journaling and reflections, mood check-ins, breathing exercises, soundscapes, a "Tree Town" with friends who send each other Good Vibes, and streaks. **The bird never dies and is never punished.** Language is relentlessly gentle.
- **Audience**: Gen Z and millennials, many women, many with anxiety, depression or ADHD, some teens. Strong "cottagecore/cozy game" overlap.
- **Monetization**: Free core. **Finch Plus** subscription: US App Store tiers show $5.99, $9.99, $34.99, $39.99, $41.99, $49.99, $59.99, $69.99 (regional and intro variants), plus a Guardian Program at $7.99. Play IAP runs $1.99–$399.99, the top being lifetime/family. Merch store.
- **Store**: **iOS 4.95★ from 778,291 ratings**, the highest rating volume in this whole slice except Duolingo. Play 4.88★ / 643,552 ratings / 10M+ (**16.8M real installs**).
- **Revenue estimates**: Adapty about $1M/month (model-based). ScreensDesign about $1M/month. A Sensor Tower-based write-up (Review Rounds) about $1M/month. One newsletter claims $30–40M ARR (unverified). @ArfurRock tweet about $4M/month (unverified). **Range: $12M–$48M/yr; treat it as "eight-figure annual revenue, bootstrapped".**
- **Loves**: "Makes each task feel like a little side quest"; "pushes my ADHD brain"; supportive for disability and bipolar users; cute; never makes you feel bad.
- **Complaints** (10% 1–2★): **Data-integrity bugs**: friends lists vanish, streaks reset when travelling across time zones ("1,000+ day streak reset"), with advice to back up manually. **Energy cap**: after about 6 tasks the pet is "full", so there is no reason to do more. **Novelty fade** after about 2 months ("I don't care for dressing my bird up"). **Trial billing**: charged about $75 after a "free" trial, limited-time pressure offers. **Devs ignore feedback** (Discord/forms) according to long-time supporters. Cultural-war reviews about pronouns. Damaged merch.
- **Why it works**: It adds **zero punishment and no shame**, gives a cute visible companion, and accepts low-effort inputs (drink water counts). It also carries a narrative (adventures) and a social layer of gentle gifting. This is the single most important comp for any "self-improvement as a game" app.

## 8. Clones and adjacent pet apps

- **Cub: Self Care Pet** (Offbeat Apps; iOS 3,229, Play 61K installs; ADHD focus; $8.49–59.99).
- **Callie: Food Self Care Pet** (Nabi Health; iOS 3,696).
- **Catzy** (China; iOS 1,122; Play 1M+).
- **Momo** (O7; iOS 2,267).
- **Otto** (Zipo Apps iOS 344; a separate "Otto: Habit Tracker Pet" by Loose Pen on Play).
- **Habbie** (242), **Habit-chi**, **Mochi**, **Habimon**, and **Amaru: The Self-Care Pet** (Six Wing Studios, an older entrant).
- **Quabble** (museLIVE; iOS 4,607, Play 0.86M installs): a duck mental-health companion.
- **Voidpet Garden** (Voidpet Inc., an a16z Speedrun company): emotions as collectible creatures, plus CBT/DBT journaling. iOS 4.86★ / 5,725, Play 0.99M installs. Complaints: "cash grab", daily grind/FOMO, a mental-health paywall right after onboarding, an auto-annual charge (≈$200 NZD), and **anger at a generative-AI chatbot** (it reportedly called a user "boring"). A sister game, Voidpet Dungeon, is a full creature battler.
- **Lesson**: Finch's success spawned a pet genre. Most clones copy the cuteness but not the gentleness, the depth or the scale of content.

## 9. Joon (ADHD kids)

- **Developer**: Joon App, Inc. (US; YC W22). CEO Isaac Eaves, who has ADHD himself. Raised **$6.4M** (led by MaC Venture Capital and Dune Ventures, per a YC announcement), and possibly an earlier ~$2.1M seed.
- **Mechanics**: Two apps. Parents assign tasks in the parent app. The child plays **Joon Pet Game**, where they adopt a **"Doter"** to feed, wash and grow, explore a world and play mini-games. **Game access is gated on completing real chores.** Coins, rewards, levels. Built with OTs and psychologists. Targets ages 6–12 with ADHD, ASD, ODD, anxiety or depression.
- **Monetization**: "All Access" subscription $12.99–14.99/mo, $49.99–149.99/yr (iOS), Play $49.99–139.99.
- **Store**: iOS 4.68★ / 6,569. Play: parent app 31K installs, pet game 135K installs.
- **Insight**: This is the "earn screen time / earn game time by doing real tasks" pattern. It works because parents enforce it, which moves the verification problem onto the parent. It is a strong model for a kids or family segment.

---

# Part C: The "Solo Leveling / System / Level up your life" wave (2024–2026)

Context: Netmarble's *Solo Leveling: Arise* game launched May 2024 (AppMagic: $138.9M gross in its first 6 months, 50M+ players), riding the anime's popularity. In the anime the protagonist receives "Daily Quests" from a "System" (push-ups, sit-ups, a run) and is punished for skipping. That spawned a TikTok/YouTube "real-life System" self-improvement meme, overlapping with "The Great Lock-In" TikTok trend (a Sept–Dec self-improvement sprint), looksmaxxing, NoFap and "monk mode" content aimed at young men. App makers rushed in.

## 10. Arise (two different apps sharing the name)

**(a) Arise: Level Up Workout Game (iOS)**

- **Developer**: Digital Lions Apps, S.L. (Spain), Apr 2025.
- **Mechanics**: "World's #1 gamified workout generator". A lifestyle questionnaire builds a custom plan, then **daily quests** follow, with rewards, levels and "aura farm" language. Anime styling and a Discord community.
- **Monetization**: **Subscription required** ("Arise requires a subscription to access workout plans, quests and app features"). US IAP: Arise Pro $4.99–59.99.
- **Store**: iOS **4.76★ / 20,989**.

**(b) Arise: Workout & Fitness RPG (Google Play)**

- **Developer**: Golden Gate Media (package `llc.sololeveling.Arise`, Apr 2025). There is no evidence of a Solo Leveling license.
- **Store**: Play **4.56★ / 275,977 ratings / 1M+ (2.2M real installs)**. An exceptional ratings-to-installs ratio (≈1 rating per 8 installs) suggests aggressive in-app rating prompts during onboarding.
- **Monetization**: $4.99–59.99.
- **Complaints** (16% 1–2★; nearly all about the business model): "went through all the screens… after you answer all the questions, you have to PAY"; "advertised free but you have to pay"; "no trial"; "the character looks like AI"; "data collecting AI slop, spits out the same stuff no matter what you selected"; refunds ignored.
- **Loves**: "Daily quests and leveling system actually keep me accountable because I don't want to break my streak or lose XP".
- **Lesson**: It proves **huge top-of-funnel demand** for the "System" fantasy among young men. It also shows the default monetization (quiz then hard paywall) burns trust.

## 11. Solo Leveller: The System / ARISE SOLO / Level Up: Solo Leveling System / others (Android)

- **Solo Leveller: The System** (The Leveller Project, Sept 2024). Play 3.86★ / 1,732 / **500K+ (610K real)**. Ad-supported, with an ad-removal IAP of $2.99–4.99. Complaints: ad removal doesn't work, unskippable ads 30 seconds in, quests reset on app close (XP exploit), no penalties, levels 6–8 become a grind ("two months and still…"). Users ask for "a real playable game that levels up with continuous exercise like Voidpet".
- **ARISE SOLO – Level Up System** (2025). Play 4.58★ / 3,867 / 92K installs. Has a free tier, ads every 10–15 seconds, and constant premium upsell. Fans: "best Solo Leveling app… so many free options… achieved an aesthetic body, charisma and respect even on free". It also uses a "bro" tone, which some users dislike.
- **Level Up: Solo Leveling System** (Rwired, 2026, 17K), **Solo Level: System**, **Solo Levelling Daily Quests** (StoryCom, 50K+), **Awaken**, **Solo Level Up: System Workout**, **Leveling App: Quest System**, **ARISE: Shadow System**.
- **iOS equivalents**: LEVELING: Fitness (870 ratings), Monarch: Leveling Workout RPG (95), Quest Leveling: Arise (36), SYSTEM AI (28), Dual: Solo Leveling For Life (139), Level Up Life: Arise Leveling (50).
- **Web/SEO players**: HabitForge, Solo X Player ("E-Rank to Monarch across 22 tiers"), MainQuest, RPG Fitness.
- **Mechanics common to all**: a blue holographic **System window** UI, **daily quests** (often the anime's 100 push-ups / 100 sit-ups / 10 km), **stats** (STR/AGI/INT/VIT/PER) and **rank tiers E→S/Monarch**, a **penalty zone** or penalty quest for missed days, a "dungeon" or "gate" as the stretch goal, and titles.

## 12. Lock In – Reset Your Life

- **Developer**: Omega Labs, LLC (US), Jun 2025. Founder story in the listing: "I built Lock In because I needed it myself".
- **Mechanics**: Habits and goals earn XP and raise an **OVR (Overall Rating)**, framed like a sports video game card. Custom tags (Gym, Health, Focus), streaks and heatmaps, **quit-habit timers with relapse tracking**, journaling, breathing, affirmations, quotes, and an **AI coach**. Rides the "Great Lock-In" TikTok trend.
- **Monetization**: Hard paywall after a questionnaire (3-day trial). Pro $17.99–34.99/yr, lifetime $59.99–89.99.
- **Store**: iOS 4.75★ / **27,777**, the largest of the 2025 "reset" apps. Play 4.73★ / 5,743 / 54K installs.
- **Complaints**: "Everything is blocked behind a paywall after a long questionnaire", "make it look like a free app", Google Play charged before setup was finished, double charges.
- **Loves**: "This app has changed me… I am different".

## 13. Life Reset: 66 Day Habit (formerly "Rise")

- **Developer**: Savvy Tech Limited (iOS) / "Design and Build" (Play package `build.designand.riselife`; IAP SKUs still read "Rise: Life reset in 66 days"). Launched 2024. Listing claims "over 1.5 million people have already started their arc".
- **Mechanics**: Personal onboarding with a "science-backed" assessment and a custom 66-day program (based on the Lally et al. habit-automaticity median). Goals become **daily quests, XP and streaks**, with an "arc" narrative.
- **Monetization**: **Subscription required for all features.** $12.99–59.99.
- **Store**: iOS 4.71★ / 13,319. Play 4.66★ / 22,065 / 500K+ (790K real).
- **Complaints** (20% 1–2★, nearly all paywall): "paid subscription hidden until the very end", "no free trial at all", "asks for review before I even start = red flag", "should be noted in the store listing".

## 14. DAWG – Discipline & Motivation

- **Developer**: DWG Labs LLC (US), 2025. Explicitly targets **"young men who want to build discipline, confidence and winning habits"**. Daily challenges (physical, mental, social), XP, leveling and streaks.
- **Monetization**: Premium $19.99/mo, $34.99–79.99/yr. **Pay to enter**: there is no free tier.
- **Store**: iOS 4.75★ / 7,243. Play 4.54★ / 13,341 / 390K installs. **But 52% of the recent Play sample is 1–2★**: "requires a subscription to get in the app", "charging people to improve themselves is predatory", unauthorized triple subscriptions with no support response.
- **Lesson**: The high store average comes from early in-funnel rating prompts. Real sentiment among people who actually tried to use it is poor.

## 15. Monke – Habit Game

- **Developer**: Myles Nicholas Root / Monke Business Enterprises, Dec 2025.
- **Mechanics**: You start as a monke alone on an island. Habits and focus sessions earn **bananas**, which buy trees, tents, campfires and pirate ships. You unlock other monke characters and build new islands. It is a **base-building meta-game** fed by habits (an Animal Crossing / Forest hybrid).
- **Monetization**: Monke Pro $9.99/mo, $39.99/yr, $39.99–79.99 lifetime.
- **Store**: iOS 4.83★ / 2,023, but **Play 2.38★**, and 67% of recent Play reviews are 1–2★: "5 minutes of useless questions → start free trial", purchases can't be restored, and onboarding text uses only "he" (female users felt excluded).
- **Lesson**: Base-building is a good meta-game, and the paywall-first funnel undermines it.

## 16. Skilltree: Self-improvement

- **Developer**: Project Skill Tree LTD (UK), 2023.
- **Mechanics**: A literal **video-game skill tree for real life**, from one-minute goals up to relationships, business, quitting games and social media. XP, levels, achievements, friend competition, and a gamified or minimalist mode toggle. Tokens economy ($0.99–69.99) plus Premium.
- **Store**: iOS 4.72★ / 285. Play 4.48★ / 2,851 / 58K installs.
- **Complaints**: Can't edit the trees to your own goals ("I don't want to meditate and journal"), content is "very alpha male" (users asked for cooking, cleaning and self-sufficiency trees), tutorial lock bug, progress lost without an account.

## 17. Lion XP: Gamify Life

- **Developer**: Poxi AS (Norway), 2024. "An MMORPG for real-life progress". Equipment, character customization, global profile, community and quests.
- **Notable design**: Features stay locked until you **defeat the "Demon King Gatekeeper"** boss, which forces a habit of using the app before revealing everything (progressive disclosure as game).
- **Monetization**: Lion Pro $6.99–189.99.
- **Store**: iOS 4.49★ / 313. Play 3.67★ / 7K installs.

## 18. Other "level up" and "self improvement" entrants (2024–26)

- **RiseGuide**: an expert-lesson microlearning app (Duolingo-for-self-help). iOS 20,198 ratings; Play 377K installs; $9.99–79.99.
- **Mindscape**, **Mastermind**, **Rankup**, **Disciplinex**, **Ascend**, **ASCEND AI: Gamify Life** (70), **Statos** (29), **Skillion** (32), **Evolve**, **Ashborn**, **Webbr: Self-Improvement RPG**, **Forge: Men's Self Improvement**.
- **Liftoff – Ranked Gym Workouts** (Liftoff Labs, 2023): a **ranked-ladder fitness** app with competitive ranks per lift, streaks, friend leaderboards and global challenges, and the claim of "4M+ lifters". iOS 4.82★ / 103,597, Play 2.2M installs. Users say "If you like Duolingo you might like this app" (for better and worse). Complaints: the trial auto-converts to annual (about $85), no verification ("I was sitting and it still gave me rank"), clutter.
- **Takeaway**: Ranks borrowed from competitive gaming (OVR, E→S, Bronze→Diamond) are the 2025 mechanic of choice for male Gen Z.

## 19. Quit-a-vice apps with game layers (QUITTR, Seed, Unchaind, Brainbuddy, I Am Sober)

- **QUITTR** (Alex Slater, UK; founded at age 19 and bootstrapped). Founder-claimed **>$500K/month** revenue and 1.5M downloads (New York magazine, Mar 2026). Earlier: $250K MRR and 350K downloads (LA Weekly). One TikTok video reportedly drove 10M views and $100K revenue. Sensor Tower estimated about 1M MAU. Mechanics: a streak counter, "brain rewiring" progress, a panic button, an AI therapist, community leaderboards, and quiz-based onboarding that "diagnoses" addiction (Inc. questioned its transparency). **404 Media reported that QUITTR exposed user data.** It is **not discoverable via US App Store search** for "QUITTR" (the API returned only clones). It grows through creators and brand search. A Play lookalike, "Quitter: Quit Porn Recovery" (com.keji.quittr), has only 11.7K installs.
- **Seed: Gamify No Nut / Quit Temptation** (Nara Capital / Quiet Games, 2024–25). **Interactive 3D orbs** evolve with your streak, alongside levels, hypnosis audio, an AI coach and community. Play 4.42★ / 78,449 ratings / 1.16M installs; iOS 6,509. Complaints: paywall before seeing the UI, a rating prompt before use ("its five star rating is fake… asks you to rate it before you even get to use it"), and achievements removed in a redesign.
- **Unchaind** (Rocapine, France; faith-based Christian). iOS 4.83★ / **50,246**; Play 73,535 ratings / 365K installs. $6.99–17.99/week, up to $49.99/yr. Complaints: "$7.99 a week", "if the Bible app can be free…", a 60% discount offered right after claiming not to discount, lost data followed by a re-bill, and pushed to high-schoolers by a speaker.
- **Brainbuddy** (Australia, 2013): the veteran. Play 852K installs.
- **CURE** (MWM), **Overcomer** (10.5K iOS), **CLNSR**, **No Nut**, **Iron Will**, **Quitzilla**, **NoFap.io**, **Root**, **Monke Reset**.
- **I Am Sober** (I Am Sober LLC, 2013). The gentle counterpart: sobriety day counters, daily pledges, milestones and badges, money/time saved, and community. **iOS 4.88★ / 191,746; Play 12.9M installs.** Freemium "Sober Plus" ($9.99/mo, $29.99–39.99/yr). Third-party revenue estimates conflict ($10K vs $200K/month). Complaints: paying for more than 2 counters, **a subscription popup right after a user presses "I am having self-harm urges"** ("really toxic"), age-ban false positives, and over-moderated community.
- **Lesson**: Quit apps convert extremely well (shame and urgency), with heavy weekly pricing. They are also the most ethically fragile segment of the market.

---

# Part D: Plain and lightly gamified habit trackers (streaks, charts, minimal game)

## 20. Streaks

- **Developer**: Crunchy Bagel (Australia), 2015. iOS/watchOS/macOS only. **Paid upfront $5.99**, no subscription. Apple Design Award winner (2016) and frequently featured.
- **Mechanics**: Up to 24 tasks with a **streak** for each, Apple Health auto-completion, negative habits, timers, widgets and watch complications. The only "game" is the streak number and the satisfying ring.
- **Store**: iOS 4.81★ / 27,353.
- **Why it matters**: It proves a premium, one-time-purchase, beautifully crafted single mechanic can sustain a business for a decade. Its users love its calm and its honest pricing.

## 21. Habitify

- **Developer**: Unstatic Ltd Co (Vietnam), 2016. iOS, Android, Mac, web. API and **MCP server** (one reviewer: "it has an MCP and an API my agents can connect to to monitor me"). AI features and challenges.
- **Monetization**: Freemium, premium subscription plus lifetime.
- **Store**: iOS 4.59★ / 7,210; Play 4.20★ / 6,679 / 686K installs.
- **Complaints** (26%): A "big upsell banner eats up the main view", features moved from free to premium, lifetime buyers watch quality decline, sync bugs between Android and web, and a scoring change that broke weekly/monthly habit stats.

## 22. Productive – Habit Tracker

- **Developer**: Mosaic S.r.l. (Italy). The Play package `com.apalon.to.do.list` suggests an Apalon (IAC) connection or acquisition. iOS 2015.
- **Monetization**: Premium $10.99/mo, $19.99–79.99/yr, a weekly bundle $5.99.
- **Store**: iOS 4.60★ / 91,063; Play 3.66★ / 20,899 / 3.2M installs.
- **Complaints** (30%): **Can't add a 5th habit without subscribing**, subscription screen on every open, repeated questionnaires, cloud sync loss, and notifications that bypass Do Not Disturb at night.

## 23. Loop Habit Tracker

- **Developer**: Álinson S. Xavier. **Open source (GPL), free, no ads, no account.** Android only, 2016.
- **Mechanics**: "Habit strength" score (an exponential-decay formula, more forgiving than streaks), charts, widgets, and yes/no or numeric habits.
- **Store**: **Play 4.72★ / 63,754 / 8.0M installs; only 2.4% of recent reviews are 1–2★.** It is the happiest user base in this study.
- **Lesson**: Users reward **respect** (no paywall, no ads, privacy) with near-perfect sentiment. The "habit strength" score is a well-loved alternative to brittle streaks.

## 24. HabitNow, HabitKit, Habit Rabbit, Grit, Bloom, Tangerine, Rise, (Not Boring) Habits

- **HabitNow** (Play 4.75★ / 93,801 / 7.3M installs). **One-off pricing** is cited as a reason for love ("not a greedy subscription"). Complaints are about widgets and notifications on new Android versions.
- **HabitKit** (Sebastian Röhl, Germany, 2022). GitHub-style contribution-grid aesthetic. iOS 4.84★ / 2,619; Play 778K installs.
- **Habit Rabbit** (2021). Pixel bunny with a room to decorate using carrots earned from habits (a mini Finch). iOS 8,867; Play 644K installs. The same developer makes **Study Bunny** (iOS 22,080).
- **Grit: Daily Habit Tracker** (GrittyApps, 2023). iOS 4.78★ / 16,423. Clean streak tracker, $1.99–9.99/mo, $12.99–29.99/yr, lifetime $19.99–44.99. (On Play, "Grit" is a different open-source app by shub39, with 18K installs.)
- **Bloom**: there is no category leader. "Bloom: Your Habit Tracker" (Serafin Lüthi, Play 40K installs), "Blossom Daily Habit Tracker" (iOS 102) and many "Bloom" garden-metaphor trackers with fewer than 100 users. The name is commoditized.
- **Tangerine: Self-care & Goals** (Bitdreams OÜ, Estonia, 2020). iOS 4.71★ / 6,640; $6.99/mo or $39.99/yr. Habits plus mood plus self-care in a soft pastel style. iOS only.
- **"Rise"**: ambiguous. The strongest "Rise" in this space is **Life Reset (formerly "Rise: life reset in 66 days")**, covered above. **RISE: Sleep Tracker** (Rise Science; iOS 74,914 ratings) is a sleep-debt/energy app, not gamified. Many tiny "Rise" habit apps have fewer than 30 ratings.
- **(Not Boring) Habits** (Not Boring Software / Andy Works, 2021). Listing says "Apple Design Award winner". **Explicitly "No streaks. No guilt."** You complete 60 repetitions to master a habit (anti-streak), with gorgeous 3D skins sold as IAP ($4.99–9.99) and a subscription. iOS 4.78★ / 6,397.
- **Do Habits** (Kodeon), iOS 4.05★ / 16,877. **Way of Life** (Denmark), iOS 4.82★ / 5,349, Play 744K. **Strides**, iOS 19,284. **Atoms** (official *Atomic Habits* app by James Clear, 2024), iOS 4.83★ / 10,820: identity-based habits.

---

# Part E: Focus, sleep, hydration and walking "grow something" games

## 25. Forest: Stay Focused

- **Developer**: Seekrtech (Taiwan), 2014. iOS, Android, Chrome. Historically **paid upfront on iOS**; Wikipedia says it **moved to free download plus a Forest Plus subscription in Dec 2025** (US IAP: monthly $5.99 "early bird", annual $35.99, plus "Sunshine Elixir" and "Crystal" consumables at $0.99–21.99).
- **Mechanics**: Plant a seed and it grows over your focus session. **Leaving the app kills the tree.** Coins buy new species. A forest of all your sessions builds up over time. You can plant **real trees** with Trees for the Future (2M+ planted). Group planting with friends (everyone's tree dies if one person leaves). Achievements.
- **Store**: iOS 4.79★ / 49,616; **Play 4.29★ / 814,394 / 50M real installs**.
- **Revenue**: AppGoblin estimates ~$100K+/month per platform. ScreensDesign estimates $50K/month (low confidence).
- **Complaints** (36% 1–2★ recently, after a UI overhaul): "app slowly turns into Duolingo slop… coins and crystals… click 3 times to accept I achieved my goal"; "too many pointless distracting features, ironic for a focus app"; free tier gutted (no pause, one sound); notifications broken.
- **Lesson**: **Feature and currency creep on a beloved simple loop triggers revolt.**

## 26. Flora – Green Focus

- **Developer**: AppFinca Inc. (Taiwan), 2017. Forest-like, but **free**, with an optional real-money **"bet"** (pay if you fail, money funds real tree planting). Social challenges. IAP: virtual "tours" $0.99–1.99.
- **Store**: iOS 4.76★ / 83,050; Play 240K installs.

## 27. Focus Plant / Focus Quest / Walking RPG / Pocket Plants / Wokamon (Shikudo)

- **Developer**: Shikudo Co., Ltd. (Taiwan). A portfolio studio of gamified walking and focus apps.
- **Focus Plant**: Forest-style focus timer plus app blocker with a **"Focus Passport"** battle pass ($4.99–39.99) and season packs. Play 4.16★ / 58,148 / **4.2M installs**; iOS 5,473.
- **Focus Quest: Pomodoro ADHD app**: an RPG hero whose **story advances only while you focus**. Play 4.53★ / 847K installs. Complaints: server disconnects lose progress, "too many features to engage you, despite its selling point being to keep you off your phone", unclear cancellation.
- **Walking RPG: Fitness Hero** (iOS 2,131), **Pocket Plants** (walking garden, iOS 3,996), **Wokamon** (pedometer Tamagotchi).
- **Lesson**: A studio model of many small gamified utilities sharing an engine and art pipeline.

## 28. Focus Friend by Hank Green (2025 breakout)

- **Developer**: Honey B Games (Bria Sullivan) with Hank Green. Launched July/Aug 2025.
- **Mechanics**: A **bean knits socks while you focus**. Leaving the app makes it stop (or unravel). Earn currency to decorate the bean's room. Deep-focus app blocking. Minimal, sweet, low-pressure.
- **Press**: **Reached #1 overall on the US App Store in Aug 2025, above ChatGPT** (TechCrunch, NBC, Fast Company, Appfigures). It later fell to about #48 within two weeks.
- **Store**: iOS 4.84★ / 10,638; Play 4.89★ / 13,522 / 2.14M installs.
- **Monetization**: Pro $3.99/mo (raised from $1.99), $19.99/yr, $29.99–39.99 lifetime; cosmetic bean packs $2.99–5.99.
- **Complaints** (only 4.5%): price raise on legacy subscribers, upsell notifications, the allow-list is paid, "just another idle game".
- **Lesson**: **Creator-led distribution plus a single adorable metaphor can hit #1 overnight.** Retention after the spike is the open question.

## 29. SleepTown

- **Developer**: Seekrtech (Taiwan), 2017. Paid on iOS ($1.99); IAP on Play.
- **Mechanics**: Set a bedtime and wake time. If you don't touch your phone in between, a **building is completed**; otherwise it turns to rubble. You build a town, and friends can build together.
- **Store**: iOS 4.65★ / 1,468; Play 4.07★ / 13,973 / 1.6M installs.
- **Complaints**: Buildings destroyed despite compliance, crashes, no support response, a fixed sleep-duration cap (users needing 10+ hours can't use it), and weekend rules too strict.

## 30. Pokémon Sleep (big-IP benchmark)

- **Developer**: The Pokémon Company / Select Button, Jul 2023.
- **Mechanics**: Sleep tracking (phone on the pillow or Pokémon GO Plus+) yields "sleep styles". Pokémon gather around Snorlax; Snorlax grows with your **sleep score** and with Pokémon you feed. Research collection, weekly islands, events.
- **Revenue**: AppMagic **$182.8M by 2nd anniversary (Jul 2025)**; **≈$234.9M by Jul 2026**; ≈$5.7M/month average in year 3. About 9.8M downloads in year 1. Play 13.6M installs.
- **Lesson**: A gamified sleep app can earn $60M+/yr when the IP and collection layer are strong. Monetization is **gacha-lite consumables, not a gated core**.

## 31. Plant Nanny / Walkr / Fortune City (SPARKFUL, formerly Fourdesire, Taiwan)

- **Plant Nanny** (water tracker). Every glass waters a cute plant, and the plant wilts if you're dehydrated. Collect plants and pots. iOS 4.72★ / 106,736; Play 4.65★ / 180,946 / 6.3M installs. Moved from free/IAP to the **SPARKFUL membership** ($3.99–7.99/mo, $69.99/yr, covering all their apps) plus clover currency. Complaints: unskippable ads, can't edit an intake mistake without subscribing, can't customize amounts.
- **Walkr**: steps fuel a spaceship to discover planets. Play 1.2M; iOS 8,087.
- **Fortune City**: expense tracking builds a city. Play 2.0M installs.
- **Lesson**: One studio, one shared membership across several gamified trackers.

## 32. Waterllama

- **Developer**: Llama Luna Apps Inc., 2019. iOS only (the Play "Waterllama" is a 2.6K-install lookalike).
- **Mechanics**: Water tracking with an adorable **llama** and many characters, **challenges**, streaks, drinks beyond water, Apple Health and widgets. Subscription $0.99–19.99.
- **Store**: **iOS 4.87★ / 165,150**, an extremely loved single-behavior gamified tracker.

## 33. Zombies, Run! / The Walk / Pikmin Bloom / Fantasy Hike / Stompers (narrative and IP fitness)

- **Zombies, Run!** (Six to Start, UK, 2012). Audio-drama missions during runs, a base-building meta-game and zombie chases. iOS 4.79★ / 24,155; Play 3.3M installs.
- **Pikmin Bloom** (Niantic → Scopely, 2021). Walking grows Pikmin and plants flowers on the real map. Play 9.4M; iOS 71,395.
- **Fantasy Hike** (Forge7 AB, Sweden): steps move you along fantasy worlds. iOS 15,112.
- **Stompers** (2024): iOS 16,291.
- **Lesson**: Story and collection beat raw XP for long-term motivation.

---

# Part F: Routine and planner coaching apps (light gamification)

## 34. Fabulous: Daily Habit Tracker / Routine Planner

- **Developer**: TheFabulous. Incubated at **Duke University's Center for Advanced Hindsight** (Dan Ariely's lab). Founders Sami Ben Hassine (CEO), Amine Laadhari (CTO) and Taylor Ling (design). Google Play 2013; iOS 2017. Google Play "Best Self-Improvement App" and Apple features in the late 2010s. Company claims 30M+ downloads.
- **Mechanics**: **"Journeys"**: story-driven, narrated multi-week habit programs that start tiny (drink water each morning, then add steps). Morning and evening ritual builder, coaching audio, letters, challenges, a "Sphere" community, and streak-like progress. More narrative than game.
- **Monetization**: Aggressive. Premium at $16.99–59.99 (several SKUs), web-checkout subscriptions **outside Apple and Google billing**, and cross-sell of sister apps (Shape, Sphere, Ambiance).
- **Store**: iOS 4.42★ / 89,622; **Play 3.82★ / 590,428 / 27.8M installs**.
- **Revenue**: Sensor Tower snapshot (undated) about $70K/month on US iOS and about $20K/month on US Play, which is very small for its install base.
- **Reputation crisis**: **60.5% of the 400 newest Play reviews are 1★ or 2★**: charges after cancellation, **32 retry attempts on a card**, charges for a sister-app subscription "Shape Premium" users never signed up for, a 90% discount appearing only when cancelling, ads for other services everywhere, "AI games shoved in", slow screens. BBB Scamtracker reports (Oct 2025) about web-checkout billing bypassing store records.
- **Lesson**: The clearest example in this set of **dark-pattern monetization destroying a once-beloved, science-branded product.**

## 35. Me+ Lifestyle Routine

- **Developer**: Enerjoy Pte. Ltd. (Singapore). iOS Jan 2022; Play Jun 2023.
- **Mechanics**: Quiz onboarding generates a routine with self-care tasks, mood, water, fasting, hydration, "glow-up" programs and short videos. Light gamification (streaks, badges, cute style).
- **Monetization**: VIP/Premium $7.99–12.99/mo, $29.99–69.99/yr, "AlarmMe VIP".
- **Store**: iOS 4.80★ / 249,016; **Play 4.71★ / 865,836 / 23.9M installs**. It is quietly one of the largest apps in this whole space.
- **Revenue**: Sensor Tower US iOS Q2 2024 weekly peak around $702K/week (early May 2024), falling to about $418K/week by late June. That implies a US iOS run-rate in the tens of millions per year at peak.
- **Complaints**: A 40-question survey before login, a "free trial" that charges immediately, no refunds, "videos you can find on YouTube", heavy ads.

## 36. Routinery

- **Developer**: Routinery Corp (Daejeon, South Korea; CEO Seo In-seok). About ₩200M seed in Dec 2020 (Digital Healthcare Partners, Invention Lab). Planned a ~₩2B pre-Series A in 2024 (KED). Claims 5M+ users in 200 countries.
- **Mechanics**: Step-by-step **routine player** with a timer per step, voice narration, auto-next and "a gentle race" against time. Streak levels named after growth ("forest-level streak"). Popular with ADHD coaches.
- **Monetization**: Premium $5/mo, $36/yr, family $49.99.
- **Store**: iOS 4.71★ / 18,228; Play 4.41★ / 18,864 / 2.26M installs.
- **Complaints** (19%): **Free tier now capped at 2 routines** ("an entire app about routines, where you need to pay to put more than two"), "got more greedy", an update broke narration.

## 37. Structured

- **Developer**: unorderly GmbH (Germany), 2020. A visual timeline day planner (ADHD-friendly). Claims 1.5M+ planners. iOS 4.79★ / 169,243; Play 2.6M installs.
- **Monetization**: Pro $2.99–7.99/mo, $9.99–49.99/yr, $99.99 lifetime.
- **Gamification**: Minimal (satisfying check-offs, energy monitor).
- **Complaints**: **Daily repeat locked behind Pro**, a lifetime purchase that crashes with no support.

## 38. Tiimo

- **Developer**: Tiimo ApS (Copenhagen, Denmark). Founded by Helene Lassen Nørlem and Melissa Würtz Azari. **Apple iPhone App of the Year 2025**; 2024 Apple Design Award finalist (Inclusivity). Funding about €4.3–4.8M total (≈$4.7M per PitchBook via Business Insider; €1.4M round Aug 2024).
- **Mechanics**: A visual, colorful timeline with icons, an AI planner that breaks down tasks, focus timers and checklists. Not a game: emotional design for neurodivergent users.
- **Monetization**: Pro $7–14/mo, $36–54/yr.
- **Store**: iOS 4.60★ / 21,886; Play 141K installs.
- **Complaints** (28%): Overpriced versus TickTick, "basically a simple to-do list", no carry-over of unfinished tasks, data lost on re-login.

## 39. Brili Routines

- **Developer**: Brili GmbH (Germany). Originally a kids' routine app (Brili Kids), with a separate adult app since 2021.
- **Mechanics**: Timed routine runner with a visual timer, "time-boxed" steps, and adaptation to running late.
- **Monetization**: Subscription $3.99–7.99/mo, $24.99–49.99/yr. Paywall on first screen.
- **Store**: iOS 4.65★ / 605; Play 3.95★ / 1,131 / 95K.
- **Complaints** (31%): Not listed as paid but unusable without subscribing, no cross-device sync, stuck on the logo screen, support absent.

## 40. SuperBetter

- **Developer**: SuperBetter, LLC. Created by game designer **Jane McGonigal** after a concussion recovery (2009). App 2012; book 2015. The developer cites a University of Pennsylvania RCT (30 days of play improved mental health and resilience) and an Ohio State depression study.
- **Mechanics**: You are the hero. You **adopt power-ups** (quick positive actions), **battle bad guys** (obstacles and triggers), **complete quests**, recruit **allies**, and pursue an **epic win** (goal). Resilience scores in four areas (physical, mental, emotional, social).
- **Monetization / pivot**: **Redesigned in early 2023 for educators and the youth mental-health crisis**. Old accounts didn't migrate (history lost), and the original web app closed at the end of 2023. Now a free Player account (squad play only) and a **Hero plan at $24.99/yr** with a 14-day trial.
- **Store**: iOS 4.65★ / 7,883; Play 4.04★ / 6,554 / 343K installs.
- **Complaints**: "Used to be absolutely amazing… recent updates rendered it useless", "no longer free → subscription", mandatory registration, a broken date-of-birth picker, endless loading.
- **Why it declined**: Strong theory and press, but it never built a compelling *game* (mostly text and lists). It then broke continuity for loyal users during the pivot.

---

# Part G: Benchmarks

## 41. Duolingo (streak and gamification gold standard)

- **Developer**: Duolingo, Inc. (Pittsburgh, US), NASDAQ: DUOL. Launched 2012.
- **Q3 2026 (shareholder letter / 10-Q)**: **DAUs 64.9M (+29% YoY)**, MAUs ≈153.1M (+13%), **paid subscribers ≈13.1M** (+14%), total bookings $316.1M (+12%), subscription bookings $278.4M.
- **Streak data**: **10M+ users with a 365-day streak** (Jan 2026, Pocket Gamer Connects; earlier figures put it at 5M+). The longest recorded streak is 4,000+ days.
- **Mechanics**: **Streak** with streak freezes, repair and weekend amulets. **XP**. **Leagues** (weekly 30-person leaderboards, Bronze→Diamond with promotion and demotion). **Gems** currency. **Hearts/energy** (mistakes cost lives; Super removes the cap). Daily quests, friend quests, monthly badges/challenges. Duo the owl's guilt-trip notifications (a meme in their own right). Year in Review shareables. Characters with personality.
- **Monetization**: Super / Max subscriptions (Play IAP up to $239.99), plus gems.
- **Store**: iOS 4.72★ / **5.6M ratings**; Play 4.75★ / 52M ratings / 1B+ installs.
- **Criticisms relevant to us**: "Streak anxiety", learning versus "playing the streak", an energy system that blocks learners, and AI-first content backlash in 2025. "Duolingo-ification" is now an insult in other apps' reviews (Forest: "turning into Duolingo slop").
- **Lesson**: **Streak plus social comparison plus loss aversion works at massive scale**, provided streak protection tools exist so one miss doesn't end the relationship.

---

# Patterns, gaps and lessons

## 1. Six archetypes, and how each performs

| Archetype | Examples | Scale achieved | Typical sentiment | Core weakness |
|---|---|---|---|---|
| **A. Avatar RPG plus self-authored tasks** | Habitica, Do It Now, LifeUp, LifeRPG, Levla, Habit Hunter, 50+ clones | Low to mid (Habitica ~8M lifetime Play installs over a decade; clones mostly <50K) | Devoted niche; 7–20% negative | Setup burden, honor-system cheating, thin game, dated UI, punishment spirals |
| **B. Cozy companion / pet** | Finch, Habit Rabbit, Cub, Voidpet, Quabble, Joon, Waterllama, Plant Nanny | **Highest** (Finch 16.8M Play installs, 778K iOS ratings at 4.95★) | Very positive; ~10% negative | Novelty fade at ~2 months, cosmetic-only depth, energy caps, data-loss bugs |
| **C. "System / level-up / lock-in" hard-paywall funnels** | Arise, Lock In, Life Reset, DAWG, Monke, Seed, Unchaind, QUITTR, Solo Leveller | Fast growth (Arise Play 2.2M installs in ~18 months; QUITTR claims >$500K/mo) | Inflated store averages (in-funnel rating prompts) masking **16–67% recent negatives** | Quiz then paywall bait, AI-generic plans, refund fights, male-only framing, privacy (QUITTR leak) |
| **D. Grow-something focus/sleep/hydration** | Forest, Flora, Focus Plant, Focus Friend, SleepTown, Pikmin Bloom, Pokémon Sleep | Huge (Forest 50M Play installs; Pokémon Sleep ≈$235M lifetime) | Positive until currency/feature creep (Forest recent negatives 36%) | Single behavior only; creep; strict rules fail edge cases |
| **E. Minimal streak trackers** | Streaks, Loop, HabitNow, HabitKit, Grit, (Not Boring) Habits | Large but low-revenue (Loop 8M, HabitNow 7.3M) | **Best sentiment** (Loop 2.4%, HabitNow 3.5% negative) | Little motivation for people who need motivation; monetization weak |
| **F. Routine coaching / planners** | Fabulous, Me+, Routinery, Structured, Tiimo, Brili | Very large (Me+ 23.9M, Fabulous 27.8M installs) | Polarized; Fabulous 60% negative | Dark-pattern billing, free tier gutting, "YouTube-level" content |

## 2. Mechanics that work (evidence-based)

1. **A visible living companion with no death and no shame** (Finch, Waterllama, Plant Nanny, Focus Friend). It is the strongest driver of scale and love in the dataset. Users explicitly credit not being punished ("never feel bad") and the cuteness. Finch's model (the pet goes on adventures and tells you stories) turns your progress into *someone else's* narrative, which reduces self-judgment.
2. **Accumulating, collectible proof of effort** (Forest's forest, SleepTown's town, Monke's islands, Pokémon Sleep's dex, Habitica's pets and mounts). A visible world that grows is the long-term retention object; XP numbers alone are not.
3. **Streaks with forgiveness**: Duolingo's 10M+ year-long streaks exist *because of* freezes and repair. Apps without forgiveness generate the angriest reviews (Finch's time-zone streak loss, Habitica's cron deaths). Loop's decaying "habit strength" and Not Boring's "60 reps, no streaks" are loved alternatives.
4. **Ranks and OVR scores from competitive gaming** (Liftoff ranks, Lock In OVR, Solo Leveling E→S, Duolingo leagues) resonate strongly with Gen Z men. Liftoff reached 100K+ ratings on both stores.
5. **Real-world anchors**: real trees (Forest/Flora), real money bets (Flora), parents gating game time (Joon), Apple Health auto-completion (Streaks). These solve the honor-system problem by bringing in an external referee.
6. **Creator-led virality around a single adorable or aspirational metaphor**: Focus Friend reached #1 overall in Aug 2025 via Hank Green; QUITTR via TikTok (one video: 10M views, $100K). Arise and Lock In rode anime and "Great Lock-In" trends.
7. **Gentle social layers**: Finch's good-vibes gifting, Forest's group planting, Habitica parties with shared boss damage. Users love accountability with *friends*. Public open chat was a moderation liability (Habitica killed Tavern and Guilds).

## 3. Mechanics and practices that fail

1. **Punitive damage, death and HP loss on a missed day** creates a shame spiral and churn ("feel like I'm losing at life", "app kills me for a sync bug"). Levla markets itself on removing this ("a missed day never costs your character health or gear").
2. **Self-authored everything** (Habitica, LifeUp, Do It Now): "spend more time managing the app than the habits", "takes a LOT of work to set up", "overwhelming for ADHD". Conversely, *preset* content that can't be edited also fails (Skilltree "I don't want to meditate", Fabulous "I don't eat breakfast", Do It Now preset tasks lowering stats). **Users want smart defaults that are fully editable.**
3. **Quiz-funnel then hard paywall** (Arise, Lock In, Life Reset, DAWG, Seed, Monke, Brili, Unchaind). The #1 complaint across the whole 2024–26 wave. It works for revenue short-term, but recent 1–2★ shares of 20–67% show it burns word-of-mouth. **Asking for a store rating before the user has experienced the app** is called out as a "red flag" and makes high averages untrustworthy.
4. **Billing dark patterns** (Fabulous web checkout, retry charges, surprise cross-app subscriptions; Finch and Liftoff trials auto-converting to annual). These produce the most toxic reviews and regulatory risk.
5. **Currency and feature creep on a simple loop** (Forest 5.x: "coins and crystals", "click 3 times"; Plant Nanny ads; Routinery 2-routine cap; Habitify banners; Productive 5-habit cap).
6. **"AI slop" backlash**: generative AI bolted on (LifeUp, Voidpet chatbot, Fabulous "AI games", Arise "AI character/AI plan") earns 1★ reviews from loyal users. AI that is invisible and useful (Habitify's API/MCP, Tiimo's task breakdown) is welcomed.
7. **Shallow, repetitive game layers**: the same battle animation (EpicWin), static Habitica boss fights, cosmetic-only Finch, Solo Leveller's grind wall at levels 6–8. Users ask for **real game depth** ("make an actual playable game that levels up with exercise like Voidpet", "add monsters that drop loot").
8. **Monetizing vulnerable moments**: I Am Sober showing a subscription popup after "I'm having self-harm urges"; mental-health paywalls (Voidpet, SuperBetter); weekly pricing for porn-recovery teens (Unchaind $7.99/week). This is ethical and reputational risk.
9. **Exclusionary framing**: "alpha male" content (Skilltree), "he"-only copy (Monke), "bro" tone (ARISE SOLO) alienate women and non-"grindset" users. The level-up genre is heavily male, and the cozy genre heavily female. **Almost nobody serves both.**
10. **Broken continuity**: SuperBetter's 2023 rebuild wiped history; Habitica removed Guilds and lost chat archives; Finch data-loss glitches. Long-term users' accumulated progress is the most valuable asset and the most fragile.

## 4. Why apps died or declined

- **EpicWin**: paid-upfront and iOS-only, so no recurring revenue for content. No social layer. Removed 2024.
- **LifeRPG**: solo developer, no monetization or polish. Pulled from Play.
- **SuperBetter**: a great theory with weak game execution, then a pivot to schools that orphaned consumers.
- **Habitica (stagnation, not death)**: an open-source volunteer model kept it alive and free but slowed UX modernization. Removing the Tavern and Guilds shrank community gravity.
- **Fabulous (decline)**: dark-pattern billing turned a Google "Best App" into a 3.8★ app where 60% of recent reviews are 1–2★.
- **Many 2025 "System" clones**: zero distribution, AI-generated art, quiz-paywall, so they sit at 0–50 ratings.

## 5. Unmet needs and white space (opportunities)

1. **A real game, not a skin.** Across 50+ RPG habit apps, none offers game depth comparable to an actual mobile game: meaningful progression, story, collection, base-building, co-op bosses with friends. Pokémon Sleep (≈$235M) and Pikmin Bloom show the revenue ceiling when the game is real. **Biggest gap: Finch-level warmth plus genuine game depth plus self-improvement breadth.**
2. **Non-punitive stakes.** Users want consequences that motivate without shame: decay, a pet that gets sad but recovers, streak freezes earned through effort, "comeback" quests after lapses, relapse-friendly design (I Am Sober-style resets, but framed as a new arc).
3. **Verification without friction.** HealthKit and Google Fit, screen time, location and photo proof, friends as witnesses, or a parent/partner referee (Joon). The honor-system problem is still largely unsolved.
4. **Smart editable defaults with fast setup** (under 2 minutes to first reward), especially for ADHD users, who are a huge share of every review set (Habitica, Finch, Routinery, Tiimo, Structured, Focus Quest, Monke).
5. **Cross-domain "whole life" progression** (fitness + mind + focus + sleep + quitting + learning) in one character. Today users stack Forest + Finch + Duolingo + a habit tracker + a quit app. The "System" fantasy is exactly this unified stat sheet, but current apps are fitness-only (Arise) or generic.
6. **Inclusive "level up"**: an aspirational, rank-based self-improvement game that doesn't alienate women or non-"grindset" users. Equally, a cozy game that doesn't bore people who want challenge. A dual-mode (cozy ↔ hardcore) difficulty setting is unexplored, apart from Skilltree's gamified/minimalist toggle and Levla's no-penalty stance.
7. **Honest monetization as a differentiator**: a usable free tier, a clear trial, ratings asked *after* value, lifetime options, cosmetic or battle-pass revenue instead of gating the core (Focus Plant's passport, Not Boring skins, Habitica gems). HabitNow, Loop and Streaks show users actively praise fair pricing in reviews.
8. **Friends-first social** (small parties, co-op bosses, gentle gifting, shared worlds) rather than public chat that needs heavy moderation.
9. **Trustworthy data**: cloud backup, export, cross-device sync, offline mode, and robustness to time zones and night shifts (repeat complaints in Finch, Habitica, LifeUp, Brili, Productive).
10. **Privacy and ethics in sensitive niches**: quit and mental-health apps handle extremely sensitive data (QUITTR exposure reported by 404 Media). A privacy-first stance is a credible wedge.
11. **Distribution playbook**: winners in 2024–26 came from **creators and trends** (Hank Green, anime, Great Lock-In, NoFap TikTok), not ASO. An app built so users want to **share their character, rank or world** (Duolingo Year in Review-style cards, OVR cards) has built-in virality.

## 6. One-paragraph synthesis

The market splits into a **cozy, female-skewing, non-punitive companion segment led by Finch** (bootstrapped, eight-figure revenue, ~17M Play installs, 4.95★ on 778K iOS ratings) and a **fast-growing, male-skewing "System / Level Up / Lock In" segment** (Arise, Lock In, Life Reset, DAWG, QUITTR) that monetizes through quiz-funnel hard paywalls and rides anime and TikTok trends but has weak trust and retention signals. The original RPG trackers (Habitica, Do It Now, LifeUp, EpicWin, LifeRPG) proved the concept but stalled on setup friction, punishment, thin game layers and dated UX. The grow-something apps (Forest, Pokémon Sleep, Focus Friend) show that a single delightful metaphor plus collectible accumulation scales enormously, and that currency creep kills goodwill. Nobody yet combines **real game depth, unified whole-life progression, forgiving stakes, light verification, friends-first co-op and honest pricing** in one product. That is the open position.

---

### Sources (selected)
- Hard numbers: Apple iTunes Search/Lookup API and apps.apple.com US pages; Google Play via google_play_scraper (pulled 2026-11-22).
- Habitica Tavern/Guild shutdown FAQ (habitica.fandom.com/wiki/Tavern_and_Guild_Shutdown_FAQ); Habitica Wikipedia.
- Finch: Adapty paywall library; ScreensDesign; Review Rounds; @ArfurRock on X (x.com/ArfurRock/status/1924499333929373958); Finch Care LinkedIn; sparrowapps newsletter.
- QUITTR: LA Weekly; Inc.; New York magazine via search summaries; Starter Story; 404 Media (data exposure) as cited in search results.
- Tiimo: Wikipedia; Daring Fireball (2025 App Store Award winners); Business Insider/AOL (funding via PitchBook); tiimoapp.com newsroom.
- Fabulous: Digital News Asia; Nibble blog; BBB Scamtracker; Sensor Tower overview pages.
- Me+: Sensor Tower blog Q1/Q2 2024 wellness reports.
- Routinery: Korea Economic Daily (kedglobal, Jul 2024); thevc.kr.
- Joon: Y Combinator company page and announcements.
- Focus Friend: TechCrunch (2025-08-18), NBC News, Fast Company, Appfigures insights.
- Forest: Wikipedia (Forest (application)); AppGoblin; AppBrain.
- Pokémon Sleep: PocketGamer.biz (2nd and 3rd anniversary AppMagic figures); Appfigures.
- Solo Leveling: Arise: PocketGamer.biz (AppMagic $138.9M first 6 months).
- Duolingo: Q3 2026 8-K shareholder letter and 10-Q (sec.gov); PocketGamer.biz (10M+ 365-day streaks).
- EpicWin: Gameranx (2010), Gamecola, AppBrain (removal date), Wikipedia (Supermono Studios).
- SuperBetter: App Store listing (2023 redesign, Penn RCT claim).
- LifeRPG: AlternativeTo; Android Authority; Google Play 404 check.
- Voidpet: a16z Speedrun company page.
- Streak research context: The Decision Lab "Streak Creep"; JMIR Mental Health gamification review (as cited by secondary sources).
