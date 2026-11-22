# 05 — Social Accountability, Commitment Contracts, Group Challenges & Market Data

Research slice: social-accountability, commitment-contract ("bet on yourself"), competitive/group-challenge and community-driven self-improvement apps, plus market and business data for the space. Also a specific check on whether the name **JIKO** is already in use.

**Data snapshot:** store numbers were pulled on **2026-11-22**.
- iOS: iTunes Search/Lookup API (US storefront). Format is `avg rating (rating count)`.
- Android: `google_play_scraper` (US, en). Format is score, rating count, install band, and the "real" install estimate the scraper exposes.
- Reviews: iOS customer-review RSS and Google Play newest-review pulls on the same date.
- Revenue and download figures marked "est." come from third-party estimators (Sensor Tower, Appfigures, AppMagic, Adapty, AppGoblin, Screensdesign). These estimators often disagree by about 10x.
- Where I couldn't find or verify something, the entry says so. I did not invent any numbers.

---

## 0. TL;DR for JIKO

1. **Name check.** No habit, self-improvement or gamified-challenge app called "Jiko"/"JIKO" exists on the US App Store or Google Play. There is also no live US trademark for JIKO in software (Class 9), fitness/education/entertainment services (Class 41) or health/wellness services (Class 44). Three things need attention (full details in §3):
   - **Jiko: Spendable T-Bills** (Jiko Technologies, Inc.) is a live fintech app: iOS 4.42 (48), Android 50K+ installs, domain jiko.com.
   - **JIKO Life** (built by Momence, Inc.) is a tiny Health & Fitness booking app for a sauna and cold-plunge wellness studio in Salt Lake City/Draper, UT (jikolife.com). It sits in the same store category JIKO would use.
   - **Disney Enterprises** holds a registered, renewed JIKO mark in Class 30 (coffee), tied to its "Jiko – The Cooking Place" restaurant. It doesn't block software, but Disney enforces aggressively.
2. **The money-stakes category is small, old, buggy and trust-sensitive.** stickK (2007/08) has 2.56★ on iOS from 27 ratings. Beeminder (2011/12) has 3.75★ on Android with an outdated UI. Pact died in 2017 after FTC action. The current leader, Forfeit (YC, 2022), has about 25K Android installs and roughly 400 ratings on each store. Nobody has made stakes mainstream. The things that kill trust:
   - being charged when the app or server breaks
   - opaque payment flows
   - charging a subscription on top of forfeits ("greedy")
3. **Social group-accountability apps also stay small.** HabitShare (~100K+ Android installs, not updated since Jan 2023), Squad (~22K Android installs), HabitLink (354 iOS ratings) and SquadGoals all show the same pattern: **cold-start and "dead group" churn**. A Squad reviewer put it this way: "It lost its motivating feature very quickly when no one was really interested in offering support."
4. **Scale goes to emotionally designed, solo-first apps with optional social features.** Finch (778K iOS ratings, 16.8M Android installs, ~$1M/month est., bootstrapped). Focus Friend (#1 US App Store in Aug 2025; Google Play Best App 2025; Apple Cultural Impact award). Life Reset (13K ratings). Lock In – Reset Your Life (27.8K iOS ratings within ~17 months, riding TikTok's "Great Lock In").
5. **Paywall backlash is the biggest complaint theme of 2025–26.** It shows up across 75 Hard (moved paid-once users to a subscription), Atoms, Lock In and Forfeit. RevenueCat 2026 puts Health & Fitness medians at $9.99/month and about $39.94/year, with 2.9% download-to-paid.
6. **Trend tailwinds:** the "Great Lock In" (Sep–Dec 2025), 75 Hard/Soft and "Winter Arc", Solo-Leveling-style "system" apps, side-quest apps, run clubs (Strava clubs nearly 4x in 2025), Gen Z loneliness (Cigna 2025: 67% lonely), and AI coaches (Google Health Coach at $9.99/month from May 2026).

---

## 1. Competitor profiles

Grouped by mechanic: (A) money-stake commitment contracts, (B) peer/friend accountability and habit sharing, (C) human or AI accountability coaching, (D) program/challenge apps (75 Hard etc.), (E) group fitness challenges, (F) gamified/RPG and "lock in" apps, (G) solo habit trackers often used socially, and (H) substitutes (Discord, BeReal/Locket, Focusmate).

### A. Money-stake / commitment-contract apps

#### 1. stickK
- **Developer / origin:** stickK.com, LLC. Founded **2007** in New Haven by Yale economists **Dean Karlan** and **Ian Ayres** plus Yale SOM student **Jordan Goldberg**. Founders put in $150K, then raised about **$2M in two rounds** ([Wikipedia](https://en.wikipedia.org/wiki/StickK)). Freakonomics covered the launch in Jan 2008 ([Freakonomics](https://freakonomics.com/2008/01/stickk-to-your-commitments)).
- **Platforms:** Web, iOS (id776128765, iOS release Dec 2013), Android.
- **Core loop:**
  - You sign a "Commitment Contract" with a goal, a reporting cadence (usually weekly), optional stakes, an optional **Referee** who verifies your reports, and optional **Supporters**.
  - Money you forfeit goes to a friend, a charity, or an **anti-charity** (an organisation you oppose). stickK's help page calls anti-charity its most popular option.
  - It's self-report based. There's no proof capture.
- **Monetization:**
  - Free for individuals. The original plan was ads, then B2B: co-branded corporate wellness versions ([Wikipedia](https://en.wikipedia.org/wiki/StickK)).
  - The terms say forfeited stakes go to the recipient "less certain fees and transaction costs." Users can also name stickK itself as the recipient ([stickK T&C](https://stickk.zendesk.com/hc/en-us/articles/206119378)).
- **Scale:** stickK claims a 600K+ user community. A Cambridge study of 17,654 contracts found **under 33% used money stakes**, and anti-charity stakes added about 6 percentage points to success ([JDM/Cambridge](https://cambridge.org/core/services/aop-cambridge-core/content/view/C3F10EAADD79CA9212F03FA2924A6FDF/S1930297523000013a.pdf/choosing-more-aggressive-commitment-contracts-for-others-than-for-the-self.pdf)). Goldberg said users with money plus a referee succeeded 78% of the time versus 35% with no money.
- **Store data:**
  - iOS **2.56★ (27 ratings)**, last updated 2026-02-23.
  - Google Play **2.81★, 100K+ installs**.
- **What users love:** "Using stickK every week, without fail, for over a dozen years." The anti-charity mechanic works. People say putting money on the line is "really motivating."
- **Complaints** (iOS RSS, 2019–2026, overwhelmingly 1★):
  - "Still glitching years later… you won't be able to log in" (Nov 2026).
  - Charged when servers were down: "Server crashed… still got charged."
  - Can't reset password; no customer service.
  - 8 clicks to submit a report.
  - Charity list ideologically loaded.
  - "A LEGALLY binding contract disguised as a fun app."
- **Status:** Alive but stagnant, with legacy UX.
- **Lesson:** Self-report plus money with no robust appeals and unreliable infrastructure produces "scam" reviews. **Reliability and a grace or appeal process are table stakes before any money mechanic.**

#### 2. Beeminder
- **Developer / origin:** Maker and Baker LLC / "The Beehive Collective of Obtuse Nerdtastic Tools", founded by Daniel Reeves and Bethany Soule. The iOS app launched Aug 2012. The founders aren't confirmed by a source I fetched; this is well known but unverified here.
- **Platforms:** Web-first, plus iOS and Android.
- **Core loop:**
  - You set a quantified goal and stay on the "Bright Red Line" (formerly the "Yellow Brick Road").
  - Data comes from manual entry or many **autodata integrations** (Fitbit, RescueTime, Duolingo, YNAB, GitHub, etc.).
  - If you go off the line you "derail" and pay the pledge.
  - Pledges escalate **$5 → $10 → $30 → $90 …** ([Habi review](https://habi.app/insights/accountability-apps/)). A one-week "akrasia horizon" prevents impulsive edits to a goal.
- **Monetization:**
  - **Most revenue comes from pledges paid on derailments** ([beeminder.com/premium](https://beeminder.com/premium)). It was profitable on pledges alone by 2013 ([blog](https://blog.beeminder.com/premium)).
  - About half of pledge revenue comes from $5–$10 pledges ([blog](https://blog.beeminder.com/exponential)).
  - Premium tiers (Infinibee/Bee Plus/Beemium, up to ~$50/month historically) gate power features ([blog](https://blog.beeminder.com/infinibee)).
  - You need a card on file to create a goal ([beeminder.com/money](https://beeminder.com/money)).
- **Store data:**
  - iOS **4.19★ (77)**.
  - Google Play **3.75★ (517 ratings), 50K+ installs (~92K est.)**, updated Sep 2026.
- **What users love:** "Best there is for time-tracking nerds." The team is responsive and honest ("everything is extremely above board"). People call it life-changing.
- **Complaints:** "UI incredibly outdated… looks developed in 2000." Dark patterns: you have to contact support to pause a goal that's about to charge. The card-on-signup requirement feels "deplorable." No Google login.
- **Status:** Alive, profitable niche, nerd-coded.
- **Lesson:** Pledge revenue alone can sustain a tiny team, but it doesn't scale to consumers. Integrations (autoverification) are the moat. The UX caps the audience.

#### 3. Forfeit (Forfeit: Habit Contracts)
- **Developer / origin:** Forfeit, Inc. Y Combinator–backed; a third-party aggregator lists a **$500K pre-seed in Apr 2023** with YC as investor, location Manchester UK (unverified, [VCBacked](https://www.vcbacked.co/company/forfeit)). Product Hunt launch Jan 2022; iOS release 2022-07-13 ([YC launch](https://www.ycombinator.com/launches/IAg-forfeit-app-complete-your-habits-or-we-take-your-money)).
- **Platforms:** iOS, Android.
- **Core loop:** "Complete your habits or we take your money." You set a task, a deadline and a stake, then submit evidence. Verification options:
  - photo (AI-checked)
  - timelapse (human-reviewed)
  - self-verify
  - friend-verify
  - Apple Health thresholds
  - GPS check-in or avoid (100 m)
  - RescueTime
  - Pomodoro (leaving the timer = fail)
  - Strava, Whoop and MyFitnessPal integrations
  - Screen Time blocking

  Appeals are reviewed by a human within hours. Leniency modes are lenient, normal and hard (hard = no appeals). "**Overlord**" is an AI accountability agent that chats, emails your partners, calls you, blocks apps and reviews evidence ([App Store](https://apps.apple.com/us/app/forfeit-habit-contracts/id1633125787)).
- **Monetization:** **Forfeited money goes to Forfeit** (reviews), plus subscriptions:
  - Premium $7.99/month or $59.99/year
  - Pro $12.99/month or $99.99/year
  - weekly plans $3.99–$5.99
  - Overlord $12.99/month
- **Claims:** "20k+ users… 94% success rate on over 75k forfeits" (developer claim).
- **Store data:**
  - iOS **4.77★ (378)**, updated Oct 2026.
  - Google Play **4.54★ (426), 10K+ installs (~24.8K est.)**.
- **What users love:** "One of the few apps that has genuinely changed my life." "Overlord has become my life coach."
- **Complaints:**
  - "Adding a paid subscription to an app where the whole point is that you pay them is incredibly greedy" (Aug 2025).
  - Bugs and instability, with dropped SMS and wiped schedules.
  - The block-apps timer can be changed to cheat.
  - Login failures.
  - "Charges for things that aren't even goals" after the AI updates.
- **Status:** Active and the most modern of the money-stake apps, but still small.
- **Lesson:** Multi-modal **proof plus human appeals** is the right shape. Double-dipping (subscription plus keeping forfeits) creates resentment. Notably, an unrelated clone "Forfeit: Habit Commitment" (Storq Labs BV, 2026) appeared, which shows how low the barrier to copying is.

#### 4. Pact (GymPact), defunct
- **Origin:** Pact, Inc. Founded around 2011 by Harvard grads **Yifan Zhang** and **Geoffrey Oberhofer**. Users pledged money per missed workout and were paid from the losers' pool when they hit their goals (gym GPS check-ins, later veggies and food logging).
- **Why it died:**
  - It shut down in **July 2017** by email, with no explanation.
  - In **Sept 2017 the FTC** settled charges that Pact kept charging users who had met their goals, who had cancelled, or whose workouts the app failed to track (gym check-in failures). It also cited failures to honor cancellations, under the FTC Act and **ROSCA**.
  - Judgment was **$1.5M**, mostly suspended for inability to pay. Pact had to refund **$948,788** ([FTC complaint](https://www.ftc.gov/system/files/documents/cases/1523010pactcomplaint.pdf), [Fortune](https://fortune.com/2017/09/23/exercise-app-pact-settlement/), [MobiHealthNews](https://www.mobihealthnews.com/news/ftc-pact-must-pay-950k-users-who-were-charged-erroneously)).
- **Lessons for JIKO:**
  - Any money mechanic is regulated consumer billing. Getting **verification failure wrong means unauthorized charges, which means FTC exposure.**
  - Clear disclosure and express informed consent before billing are required (ROSCA).
  - A pooled "get paid by losers" model also brushes against **gambling and sweepstakes law**. App Store guideline 5.3 requires real-money gaming to be licensed and geo-restricted.
  - Pact's unit economics depended on users failing, which is a perverse incentive.

#### 5. "Bet on yourself" newcomers (Hourglass / Payback / Goal Hero / Stakes)
- **No apps named "Hourglass", "Payback" or "Goal Hero" with stake mechanics exist on the US App Store** (searches on 2026-11-22). Results returned porn-blocking "accountability" apps (Covenant Eyes etc.) and unrelated games.
- "Habit Hunter: Gamified Routine" (Active User Studio, Android package `co.au.goalhero`, 4.46★, 100K+ installs) is probably the old "Goal Hero". It's a gamified tracker, not a stake app.
- What actually exists is a long tail of tiny 2024–2026 stake apps, each with fewer than 25 ratings. That signals lots of founder interest and little traction:

| App | Dev | Mechanic | iOS rating |
|---|---|---|---|
| Stakely – Bet on Yourself | W. R. Varquez (2025) | self-imposed price per goal, points, levels | 4.17 (6) |
| Panbit | Panbit LLC (2025) | "commitment locks", donation-based stakes, friend challenges | 5.0 (24) |
| Real Stake | Xiang Xing (2025) | cash or **reputation** consequences (text a friend) | 4.2 (5) |
| Oath – Discipline Reimagined | Gutierrez Hustles (2026) | 1v1 friend challenges, verification, winner-takes-pot | 5.0 (6) |
| STICK: Routine Challenges | Ahdiverse (2026) | **buy into a shared pot**, split among finishers | 5.0 (1) |
| UPROOF | T. Komine (2026) | timestamped photo or pay a fine ($1→$5→$10), group votes on proof | 0 ratings |
| Pledge – Bet On Yourself | Wolk Creative (2023) | stakes | 5.0 (3), abandoned 2024 |
| Habit Hustle | N. Wylie (2024) | log payments to friends or charity | 5.0 (4), abandoned |
| Kiri | Product Hunt | stake money plus proof | n/a |

- **Lesson:** Lots of founders try "bet on yourself", but none break out. Distribution and trust, not mechanics, are the bottleneck. **Reputation stakes** (Real Stake, Forfeit's "text your buddy") are a legally safer alternative to cash.

### B. Peer / friend accountability and habit-sharing apps

#### 6. HabitShare
- **Developer:** Lucas (Luke) Bickston, solo. iOS launched **Nov 2015**. Android also exists.
- **Core loop:** A simple habit tracker. You share selected habits with chosen friends, set per-habit privacy, see friends' check grids and send messages. Free, no ads, unlimited habits.
- **Monetization:** None visible (free, no IAP).
- **Store data:**
  - iOS **4.60★ (668)**, **last updated 2023-01-27**.
  - Google Play **4.29★, 100K+ installs**.
- **What users love:** "No BS, super simple, completely free." "Like 8 years… hasn't changed one bit." Seeing friends' green checks.
- **Complaints:** Repeated requests for widgets, reordering, dark mode and Apple Watch. "Can't add friends." Reminders don't work. Not VoiceOver-accessible. Users note "there hasn't been an update in 2 years."
- **Status:** Zombie. It works and is beloved, but is unmaintained.
- **Lesson:** There's latent demand for **simple, free, private-by-default friend sharing**. Even unmaintained, it keeps 4.6★. It never monetized, so it never grew.

#### 7. Squad: Habit Accountability ("joinsquad")
- **Developer:** Squad Habits (Android `co.joinsquad.app`). Released Apr 2023. Product Hunt launch Jan 15, 2024. A maker named Junu Yang appears on one listing (unverified) ([BetaList](https://betalist.com/startups/joinsquad), [Product Hunt](https://www.producthunt.com/products/squad-7)).
- **Core loop:**
  - Small groups ("squads") run 1–4-week shared challenges with daily check-ins.
  - **Credits are earned or lost** on check-ins, with rewards, penalties and progress reports.
  - An **AI coach ("Quazilla", ChatGPT-based) lives in the group chat** and on WhatsApp.
- **Monetization:** IAP $8.99–$74.99.
- **Store data:** Google Play **3.95★ (149), 10K+ installs (~21.6K est.)**, updated Jul 2026.
- **What users love:** "The AI bot is surprisingly really motivating… in the Squad check-in groupchat." Several users with ADHD say it changed their life.
- **Complaints:**
  - Google sign-in failures with no fallback.
  - Can't join a friend's group via link.
  - Can't backfill missed check-ins or edit goals.
  - "**It lost its motivating feature very quickly when no one was really interested in offering support**."
  - Lag and crashes.
- **Lesson:** An AI participant in the group chat is a promising way to keep groups alive. But stranger squads die fast, and onboarding and auth bugs kill viral invites.

#### 8. HabitLink: Habits with Friends
- **Developer:** Andrei Mikheev (iOS, Jun 2025).
- **Core loop:** Social habit tracking with visible streaks and friend check-in notifications. Challenges where "losing a challenge hurts — your friends are watching."
- **Store data:** iOS **4.71★ (354)**.
- **Lesson:** This is a recent indie entrant. It shows the "friends are watching" positioning still resonates.

#### 9. "Streaks with friends" / photo-proof social apps (the long tail)

| App | Dev / year | Mechanic | iOS rating |
|---|---|---|---|
| HabitLeague: Friends Streak | T. Thornton 2025 | friend streak leagues | 4.85 (13) |
| Folksable Photo Accountability | D. Reddy 2024 | social contracts, photo proof to friends | 4.65 (17) |
| Loop Club | camcad 2025 | group "loops", photo, voice and video check-ins, group gallery | 5.0 (12) |
| REACH Together | 2026 | friends verify daily proof, "call you out" | 5.0 (10) |
| Commit: Accountability Partner | WeFit Labs 2026 | one goal with one partner | 5.0 (1) |
| Compadre | M. Schaefer 2023 | partner per step, alerts on missed check-ins | 5.0 (2), abandoned Jan 2024 |
| SquadGoals! | (id1603697577) | 3–6-month goals with a squad | n/a |
| Goals: Fitness Accountability | Goals Inc. 2026 | group accountability, auto-tracks workouts (Apple Watch, Garmin, Fitbit), commitments billed outside the App Store | 5.0 (7) |
| Accountable: Social Challenges | Starnez 2026 | social challenges | 5.0 (2) |
| Habit Share: HabitRix | M. Elatabany 2025 | shared habits (Android 10K+) | 4.47 (34) |
| Shared Habit Tracker: Habitomo / DailyDuo | 2026 | pair tracking | ~0 ratings |
| Tandem – Habit Buddy / Tandem: Better habits together | 2025–26 | partnered habits | 0 ratings |
| Supporti: Social Motivation | (id1477119134) | social motivation | n/a |

- **Lesson:** This is a crowded indie long tail with almost no breakout. **Photo proof, friend verification and pair mode are commoditised.** Differentiation has to come from distribution, a feel-good design system and retention loops, not the feature list.

#### 10. Paired (couples app; the "Tandem"-style partnered-challenge reference)
- **Developer:** Better Half Ltd (London). Seed rounds of $1M (2020) and **$3.6M (May 2021, led by Eka Ventures)**, $4.6M total ([TechCrunch](https://techcrunch.com/2021/05/27/paired-pulls-in-3-6m-to-encourage-more-couples-to-get-cosy-with-app-based-relationship-care)). The App Store listing claims 8M downloads. A job post claims 250K+ DAU (undated).
- **Core loop:** Daily questions and quizzes that **both partners answer**, with answers revealed only after both respond, plus streaks.
- **Monetization:** Subscription.
- **Store data:** iOS **4.72★ (211,330)**; Google Play 4.57★, 1M+ installs.
- **Lesson:** **Dyadic "both must answer to unlock" loops plus streaks** retain extremely well. This is the strongest evidence that *pair* accountability beats *group* accountability for consumer scale. The adjacent Cozy Couples (47K ratings), Evergreen (55K) and Agapé (26K) confirm the pattern.

#### 11. Strava clubs (brief)
- **Strava:** iOS **4.81★ (381,968)**; Google Play 4.61★, **100M+ installs (~139M est.)**.
- **Clubs and challenges:** **New clubs nearly 4x in 2025, reaching 1M total clubs**. Running clubs grew 3.5x and hiking clubs 5.8x. 39% of Gen Z exercise to meet people ([Strava Year in Sport 2025 via BikeRadar/Endurance Sportswire](https://www.endurancesportswire.com/strava-releases-12th-annual-year-in-sport-trend-report-revealing-that-doomscrolling-is-out-movement-is-in/), [SGB](https://sgbonline.com/stravas-year-in-sport-trend-report-highlights-gen-zs-passion-for-run/)).
- **Business:** Acquired **Runna** (Apr 2025). Valued at **$2.2B** (May 2025). Sacra estimates 2025 revenue at about $490M (unverified) ([startups.co.uk](https://startups.co.uk/news/runna-acquired-by-strava/), [Sacra](https://sacra.com/chat/h/9a26bab8-d4f8-4b60-8189-3f6d27d6f075/)).
- **Lesson:** Social accountability works at scale when it rides **real-world community** (clubs, events) and **automatic proof** (GPS). Kudos is the lightest possible social reward.

### C. Human / AI accountability coaching

#### 12. Coach.me (formerly Lift)
- **Developer:** Coach Kendra Inc. Originally **Lift**, built by Tony Stubblebine and Jon Crosby and incubated at Obvious Corp (Ev Williams/Biz Stone). Launched **Aug 2012**. TechCrunch reported "single-digit millions" of users in Dec 2014, plus a $1.1M raise. Rebranded to **Coach.me** in Dec 2014/Jan 2015, with a coaching marketplace from **$15/week** ([TechCrunch](https://techcrunch.com/2014/12/16/goal-tracking-and-self-improvement-app-lift-adds-personal-coaching-raises-1-1m-more), [VentureBeat](https://venturebeat.com/ai/goal-setting-app-lift-becomes-coach-me-focuses-on-marketplace-for-coaching)). Stubblebine later left to run Medium. Coach Kendra Kinnison became CEO.
- **Core loop:** Habit check-ins with community "props" (likes) and Q&A per habit, plus paid human coaches.
- **Store data:**
  - iOS **3.51★ (172)**, updated Nov 2026.
  - Google Play **3.15★, 500K+ installs**.
- **Complaints:** "Freezes… apparently has been abandoned by the developer… lost all my years of data." The app runs very slowly. **Loyalists:** "Still my favorite… using it back when it was called Lift."
- **Lesson:** This was the original "social props" habit app, with millions of users. It pivoted to coaching revenue because community alone didn't monetize, and then decayed technically. **Community props drive engagement; they do not drive revenue.**

#### 13. GoalsWon
- **Developer:** Goals Won Pty Ltd (Australia, founded ~2020). iOS Oct 2021, Android Dec 2020.
- **Core loop:** **A dedicated human accountability coach** you message every day. The coach covers goal-setting, daily check-ins and behavioural coaching (procrastination, dopamine, binge behaviour).
- **Monetization:** Expensive subscription: App Store shows **$99.99/month, $269.99/quarter, $699.99/year**; a review cites about $90/month after a 7-day trial ([App Store](https://apps.apple.com/app/id1544973743), [Business Dive](https://thebusinessdive.com/goalswon-review)).
- **Store data:** iOS **4.87★ (115)**; Google Play 4.63★ (136), **1K+ installs (~4.4K)**.
- **Lesson:** Human accountability gets very high satisfaction, but at $100/month it's a niche market. AI is now collapsing this price point: Squad's Quazilla, Forfeit's Overlord, and WhatsApp bots like Habit Hero, NeverGiveUp and Habitchat ([search results](https://microlaunch.net/h/how-to-receive-motivational-support-through-whatsapp-and-imessage)).

#### 14. Supergoal
- **Not found.** I found no app or company called "Supergoal" in the accountability space on the App Store, Google Play or the web. App Store results were soccer games. If the brief meant an AI or WhatsApp accountability coach, the comparables are Habit Hero (AI coach "Geoffrey" on WhatsApp), NeverGiveUp (WhatsApp/iMessage coach), Habitchat (YES/NO replies on WhatsApp) and Coachcall.ai (voice calls).

#### 15. Peerbound
- **Not found** on either store or the web. The closest analogs are REACH, Compadre, GoalGroup, GoalBud and SquadGoals (see §9).

### D. Program / challenge apps (75 Hard, 75 Soft, Monk Mode)

#### 16. 75 Hard (official)
- **Developer:** 44Seven Media, LLC (Andy Frisella). iOS **Jun 2020**; Android Jun 2020.
- **Core loop:** A 75-day daily checklist: two 45-minute workouts (one outdoors), a diet, no alcohol, a gallon of water, 10 pages of reading and a progress photo. Miss anything and you restart at Day 1. Later phases continue it ("Phase 1 of 30" etc.). It's solo, with no group features of note.
- **Monetization:**
  - It was **once a paid app (~$6.99)**.
  - It is now a **subscription**: ~$4.99/month or $39.99/year in the US. Regional pricing is €5.99/month or €44.99/year, and a UK review cites £35/year or £5/month.
  - Screensdesign estimates revenue at about $50K/month (unreliable).
- **Store data:**
  - iOS **4.55★ (6,406)**.
  - Google Play **3.62★ (819), 100K+ installs (~188K)**.
- **What users love:** It changes lives. The simple, daily, binary rules suit people ("#LOCKEDIN").
- **Complaints (2026):**
  - "**Revoked my lifetime membership purchase… made everyone go on a monthly subscription**."
  - "Holy cashgrab… 5 bucks a month for a checklist."
  - Charged after deleting the account.
- **Lesson:** The brand is huge but the app is a thin checklist. **Converting paid-once users to a subscription causes review collapse** (Android 3.62★).

#### 17. 75 Soft / clones / Her 75

| App | Developer | iOS | Android |
|---|---|---|---|
| 75 Days Challenge Tough & Soft | BeHard, Inc. (2023) | **4.82 (8,959)** | "BeHard: 75 Hard Challenge" **1.45★ (170), 50K+**: a huge iOS/Android rating gap, likely aggressive paywall or billing complaints |
| Her 75 | HER 75 (Jun 2025) | **4.82 (5,370)** | n/a |
| 75 Tough & Soft Challenge | Solowei Group (2021) | 4.23 (3,732) | n/a |
| 75 Soft Challenge™ Official | Big TLK LLC (2024) | 4.30 (50) | 1K+ |
| 75 Day Challenge: Better | A. Parnev (2024) | 4.77 (696) | n/a |
| 75 Day Challenge: Soft Edition | Inkolab (2024) | 4.72 (423) | 5K+ |
| 75 Days Challenge – Reset75 | EHM Tech (2026) | 4.85 (121) | 10K+ |
| 75 Days Hard Challenge Tracker | Abenidev | n/a | 4.6★, 50K+ |

- **Lesson:** Named challenge formats are a **powerful acquisition hook**. Clones out-rank the official app on iOS ratings. Her 75 shows that **gender-specific reframes of a viral challenge** can gain about 5K ratings within ~17 months.

#### 18. Monk Mode apps
These are all tiny: Monk Mode – Take Control (13 ratings), Monk Mode: Habit Tracker (39), Monk Mode: Screen Time Control (6), and several 2026 apps with 0 ratings. "Monk mode" is a content trend, not an app category with a winner.

### E. Group fitness / step challenges

#### 19. Fitbit Challenges, now Google Health
- **History:**
  - Fitbit's Challenges (Workweek Hustle, Weekend Warrior etc.), Adventures and Open Groups were among its most-loved social features. Some open groups had hundreds of thousands of members.
  - **Google removed them on March 27, 2023.** It said it was "streamlining." Users were furious: a forum thread ran 49+ pages, and people threatened to switch to Samsung ([Engadget](https://engadget.com/fitbit-challenges-adventures-and-open-groups-join-the-google-graveyard-today-204519144.html), [9to5Google](https://9to5google.com/2023/03/27/fitbit-challenges-groups-removed/), [Fitbit community](https://community.fitbit.com/t5/Product-Feedback/Don-t-remove-Challenges-amp-Adventures/idi-p/5335785/page/49)).
- **2026:** The app was renamed **Google Health** (rollout May 19, 2026) with a **Gemini-based "Google Health Coach"**. Premium is **$9.99/month or $99/year** ([Google blog](https://blog.google/products-and-platforms/products/google-health/google-health-app/), [TechCrunch](https://techcrunch.com/2026/05/07/googles-9-99-per-month-ai-health-coach-launches-may-19/)).
- **Store data:**
  - iOS "Google Health (Fitbit)" **4.46★ (713,968)**.
  - Google Play **3.60★ (1.33M), 100M+ installs (~317M)**.
- **Lesson:** Big tech treats social challenges as expendable and has moved to AI coaching. That orphaned a large audience that **loved group challenges**, which is an opening for independents.

#### 20. Stridekick and Strive (Fitbit-challenge refugees)
- **Stridekick Activity Challenges:** Google Play **4.65★ (3,949), 100K+ installs (~486K)**. IAP $12.99–$549.99 (group or corporate plans).
- **Strive: Step Challenge App:** iOS **4.78★ (3,072)**, Android 1.69★ (5K+). Pricing is $5.99/month or $24.99/year individual, plus group plans.
- **Lesson:** Cross-device **step leaderboards among friends and coworkers** keep a durable niche, with group plans as monetization.

#### 21. "Fitbod-style squad features" and others
Fitbod itself has no notable squad feature. The social-gym tracking leader is Hevy (feed, follows, likes on workouts). I didn't find anything on a Strava–Hevy deal; that remains unverified. Peloton's leaderboard and "Here Now" set the benchmark for synchronous competition.

### F. Gamified / RPG / "lock in" / side-quest apps (adjacent; the "Solo Leveling system" trend)

#### 22. Lock In – Reset Your Life
- **Developer:** Omega Labs, LLC. iOS **Jun 25, 2025**; Android package `com.aclo.lockin`.
- **Core loop:** Habits plus an **OVR (Overall Rating) "player card"**, XP, leveling, and "reset your life" programs. Heavy questionnaire onboarding leads to a hard paywall.
- **Monetization:** Subscription; Android IAP $9.99–$34.99, plus weekly plans.
- **Store data:**
  - iOS **4.75★ (27,777)**: very fast accumulation.
  - Google Play **4.72★ (5,749), 50K+**.
- **Revenue:** A Nov 2026 analysis says the app rode the "Great Lock In 2026" TikTok wave: 30-day downloads up 82% and revenue up 476% month over month, with daily revenue peaking near $5K ([Huxiu](https://www.huxiu.com/article/4902720.html)). Estimates conflict: Adapty says ~$20K/month, Screensdesign ~$260K/month, AppGoblin under $10K/month with ~909K installs.
- **Complaints:** "Everything is blocked behind a paywall after a long questionnaire." "Had to pay even though I'm a broke high schooler." Charged without confirmation.
- **Lesson:** The **Gen Z "lock in" language plus a sports-style rating** is a strong hook. Hard paywalls monetize but generate teen backlash.

#### 23. Life Reset: 66 Day Habit (formerly Rise)
- **Developer:** Savvy Tech Ltd (Apr 2024).
- **Core loop:** Real goals become daily quests, XP and streaks, with widgets. The developer claims "over 1.5 million" users.
- **Store data:** iOS **4.71★ (13,319)**; Google Play 4.66★, 500K+ installs.
- **Lesson:** A clear time-boxed frame (66 days) plus quests works.

#### 24. Solo Leveling "System" apps
- Dual: Solo Leveling For Life: 4.66 (139).
- Quest Leveling: Arise: 36 ratings.
- Solo X Player Leveling Workout: 36.
- Solo Leveling Your Self: 5.
- Solo Level: System; Solo Hunter: Level Up; Solo Leveller; Awakened: Habit RPG.
- A "Solo Leveling System" launch on Product Hunt, Jan 2, 2026.
- ClickUp has published "Solo Leveling system templates" ([ClickUp](https://clickup.com/blog/solo-leveling-system-templates)).
- **No breakout.** The aesthetic (blue "System" windows, E→S rank, daily quests, penalty zones) is widely copied, and no app owns it.
- Monke – Habit Game (Myles Root, Dec 2025): iOS 4.83 (2,023), Android 2.38★. The same developer previously shipped "Lock In – Transform Yourself" (6 ratings).
- Skilltree: 4.72 (285), friend leaderboard.
- Habitica: see §25.

#### 25. Habitica (HabitRPG, Inc.)
- **Origin:** Started 2013 (Kickstarter as HabitRPG). Incorporated 2014. Open source. CB Insights lists one investor, Backstage Capital.
- **Core loop:** A party-based RPG: tasks deal damage to bosses, and **party members take damage when you skip dailies**, which is social accountability through game mechanics. Challenges with gem prizes.
- **Store data:**
  - iOS **4.33★ (3,731)**.
  - Google Play **4.63★ (76,522), 5M+ installs (~8.4M)**.
- **Key event:** On **Aug 8, 2023 Habitica removed the Tavern and all Guilds.** Its reasons were that they were used by "a disproportionately small percentage" of players and that moderation and compliance burden was too heavy. This followed a volunteer moderator strike in Dec 2022 and moderation being taken in-house ([Habitica wiki FAQ](https://habitica.fandom.com/wiki/Tavern_and_Guild_Shutdown_FAQ)). Parties and challenges remain. **No acquisition found.**
- **Lesson:** **Open public community is a moderation liability** for a small team. Small private parties are the durable social unit.

#### 26. Side-quest apps (2025–26 TikTok trend)
SideQuest – Walk & Level Up (4.94, 220), Sidequest: Explore Your City (4.37, 222), SideQuest: Tiny Adventures, Sidequests HQ. All launched 2025–26 and are all small. This is an emerging aesthetic with no category winner.

### G. Solo habit trackers frequently compared (light or no social features)

| App | Developer | Launch | iOS rating | Android | Social features | Notes |
|---|---|---|---|---|---|---|
| **Atoms** (James Clear) | Atomic Development Inc. | Feb 2024 | **4.83 (10,820)** | 3.10★ (692), 100K+ (~237K) | Fortune said it added "accountability partners" at launch ([Fortune](https://fortune.com/well/2024/02/14/atomic-habits-james-clear-app-goals-atoms/)), but the current listing shows none, and a reviewer requests partner matching | Pro $4.99/month, $39.99/year. Android complaints: "Rip off. After the free trial you have one habit reminder per day," doesn't work offline, confusing goal setup. Lesson: an author brand (20M+ book readers) wins iOS installs, but the paywall on basic tracking hurts Android ratings |
| **Way of Life** | Way of Life ApS (DK) | 2010 | 4.82 (5,349) | 3.63★ (1,351), 500K+ | none | Green/red/skip journal. IAP $4.99–$6.49 |
| **Strides** | Goals LLC / Make Progress LLC | 2013 | **4.79 (19,284)** | small (1K+) | none | Goals plus habits, iOS-centric |
| **HabitNow** | HabitNow Apps | 2019 | (no US iOS app; an iOS namesake by another dev has 10 ratings) | **4.75★ (93,801), 5M+ (~7.3M)** | none | Android-first, cheap IAP $0.99–$11.99 |
| **TickTick** (habits module) | Appest/TickTick Ltd | 2013 | 4.86 (47,116) | 4.61★ (167K), 10M+ | shared lists only | Habits are bundled into a to-do app; a common substitute |
| **Habit Rabbit** | SuperByte (Justin Patrick Silang; also Study Bunny, 22K ratings) | Sep 2021 | 4.66 (8,867) | 4.61★ (7,824), 500K+ (~644K) | **no meaningful friend features** found | Virtual bunny pet, coins, outfits. IAP $1.99–$59.99 |
| **Momentum** | name collision: Momentum – Habits & Goals (Orion Dev, 2026, 10 ratings), Momentum: Energising Habits (Odyssey Labs, 20), etc. | | | | | The once-popular Mac "Momentum Habit Tracker" has no notable current presence. **There is no single "Momentum" competitor** |
| **Streaks** | Crunchy Bagel | 2015 | 4.81 (27,353), paid $5.99 | | | Apple Design Award winner, paid-up-front |
| **(Not Boring) Habits** | Not Boring Software | 2021 | 4.78 (6,397) | | | Premium design |
| **Grit** | GrittyApps | 2023 | 4.78 (16,423) | | | |
| **HabitKit** | Sebastian Röhl | 2022 | 4.84 (2,619) | 4.54★ (12,265), 500K+ | | |
| **Loop Habit Tracker** | open source | 2016 | | 4.72★ (63,753), 5M+ (~8M) | | Free |
| **Habit Tracker** | Inner Grow | 2019 | **4.79 (149,093)** | | | Dominates generic search |
| **Fabulous** | Fabulous SAS (Paris; Duke Center for Advanced Hindsight; co-founders Sami Ben Hassine, Taylor Ling, Amine Laadhari, 2014) | | 4.42 (89,622) | 3.82★ (590K), 10M+ (~27.8M) | | Coaching "journeys", aggressive paywall. **No acquisition found** in 2024–26 searches. One blog's claim that "Headway Inc" publishes it is unverified |
| **Finch: Self-Care Pet** | Finch Care PBC (Stephanie Yuan & Nino) | May 2021 | **4.95 (778,291)** | 4.88★ (643,560), 10M+ (~16.8M) | **friends: "Tree Town", sending "good vibes"** (soft social) | Bootstrapped (friends and family only). Revenue est. **~$380K/month (Jun 2025) → ~$1M/month (Jun 2026)** per Sensor Tower via Review Rounds; one blog claims $30–40M ARR (low-rigor) ([Review Rounds](https://review-rounds.com/finch-business-model-bootstrapped-self-care-pet-app/), [Sparrow](https://blog.sparrowapps.io/p/finch-how-a-self-care-app-hit-30m-arr-without-vc-money), [Adapty](https://adapty.io/paywall-library/finch/)). FoxData: 2.34M downloads per 90 days, 62% US. **The category benchmark for warmth-driven retention** |

### H. Substitutes and "BeReal for habits"

#### 27. Focusmate (virtual coworking / body doubling)
- **What it is:** Web-first. You get 25/50/75-minute 1:1 video sessions with a stranger: state your goal, work on camera, report back at the end. That's peer accountability via **synchronous presence**.
- **Pricing:** Free with 3 sessions/week. Plus is ~$8/month annual or ~$12/month monthly ([G2](https://www.g2.com/products/focusmate/pricing), [lifestack](https://lifestack.ai/blog/focusmate-pricing)).
- **Funding:** Conflicting. CB Insights says $940K over 7 rounds (seed 2020). Crowdability says $350K (CoVenture, Betaworks, Towerview).
- **Store presence:** No official Focusmate app is findable on the US App Store or Google Play under that name. Results were clones ("Focus-Mate", "FocusMate – Pomodoro Timer", "Focused Space: Body Doubling").
- **Lesson:** **Live co-presence** is a strong accountability primitive, especially for ADHD users. It's productivity-coded rather than gamified.

#### 28. Focus Friend by Hank Green
- **What it is:** B-Tech Consulting Group, launched Jul 23, 2025. A solo focus timer where interrupting makes your bean sad; you earn decor.
- **Rankings:** Hit **#1 on the US App Store** in Aug 2025, beating ChatGPT. 740K downloads per Fast Company, 1M+ on Android. **Google Play Best App of 2025**, and Apple's 2025 **Cultural Impact** award ([Fast Company](https://www.fastcompany.com/91388304/focus-friend-app-store-hank-green-bria-sullivan), [Appfigures](https://appfigures.com/resources/insights/20250905?f=1), [Google](https://blog.google/products/google-play/best-apps-games-2025/)).
- **Store data:** iOS **4.84★ (10,638)**.
- **Lesson:** **Creator distribution plus a cozy, guilt-based pet mechanic** can top the charts without any social features. Appfigures noted it fell to #48 overall within two weeks, so the spike decays fast.

#### 29. BeReal / Locket (the "BeReal for habits" reference)
- **BeReal:**
  - iOS 4.77★ (1.16M); Google Play 4.55★, ~38M installs.
  - **Acquired by Voodoo for €500M** (Jun 2024, cash plus earnout) with ~40M "active users".
  - Its DAUs fell ~61% from Oct 2022 to Mar 2023 ([TechCrunch](https://techcrunch.com/2024/06/11/bereal-is-being-acquired-by-mobile-apps-and-games-company-voodoo-for-e500m), [Engadget](https://www.engadget.com/bereal-the-buzziest-app-of-2022-has-been-bought-by-a-mobile-game-publisher-175016152.html)).
- **Locket Widget:** iOS 4.76★ (594,499); Google Play ~37M installs.
- **Widgetable:** 4.92★ (389K).
- **"Sesh" habit app: not found.** Gratitude-with-friends apps (OpenThanks 13 ratings, Gratitude Board 13, GratiFlow 0) are tiny. Gratitude Plus (21K) is the leading gratitude journal, and its social features are secondary.
- **Lesson:** **Time-boxed, photo-based, close-friends-only proof** is a proven Gen Z mechanic: the BeReal prompt and Locket's home-screen presence. Nobody has successfully applied it to habits; all the photo-proof habit apps are under 20 ratings. BeReal's DAU collapse also warns that **novelty-driven daily prompts fade without an intrinsic goal**.

#### 30. Discord accountability servers (free substitute)
- **Study Together:** ~**1.06M members**, ~56K online. Bills itself as the largest study/productivity server, with cam, screenshare and chat rooms ([Discord](https://discord.com/servers/study-together-595999872222756885)).
- **Others:** Study With Me (~49K), Enrico's Study Family (~49K), plus many small "accountability partner" servers.
- **Lesson:** Free, community-run, bot-driven (pomodoro, leaderboards, roles) accountability is the default substitute for Gen Z. An app must beat Discord on **intimacy, low friction and visible progress**, not on chat.

#### 31. "Tribe" / "Rally" / "Daily challenge with friends" / "Habit Squad"
- **No meaningful apps named "Tribe" or "Rally"** in this space. ThriveTribe – Group Challenges has 1 rating. "Rally" results are racing games or Rally Health (UnitedHealth's corporate wellness platform, not consumer).
- **"Habit Squad": not found as a distinct app.**
- **Daily-challenge-with-friends winners are games:** **playus: Daily Group Challenge** (Dapps, Dec 2025, **4.85★, 1,835 ratings**) runs a daily 1-minute mini-game with a group leaderboard and season winner. That's a useful structural template: daily shared prompt, group leaderboard, seasons.
- Other small apps: Hype – Challenges with Friends (school polls and photo challenges), Leap: Daily Social Challenge (17 ratings).

---

## 2. Cross-cutting patterns (what users love and hate)

**What users love**
- Seeing friends' check-ins: HabitShare ("Green checks = gold stars").
- An AI or human "coach" presence inside the group: Squad, Forfeit Overlord, GoalsWon.
- Simple binary daily rules: 75 Hard.
- Warm, non-judgmental companions: Finch, Focus Friend.
- Sports or game identity: Lock In OVR, RPG levels.
- Long-term record of streaks: Way of Life, Coach.me loyalists.

**What users hate (ranked by frequency across ~600 reviews pulled)**
1. **Paywalls on basic tracking, and subscriptions replacing paid-once or lifetime purchases** (75 Hard, Atoms, Lock In, Forfeit, Fabulous).
2. **Being charged because the app failed**: login bugs, server outages, verification failing (stickK, Pact/FTC, Forfeit).
3. **Auth and invite failures** that break the social loop: Google sign-in only, invite links not working (Squad, HabitShare, Beeminder).
4. **Dead groups**: nobody else engages (Squad).
5. **Rigid rules**: can't backfill or edit, no grace day (Squad, stickK).
6. **Abandonment**: no updates in years, data loss (HabitShare, Coach.me).
7. Long questionnaires followed by a hard paywall (Lock In).

**Reddit and community sentiment** (r/getdisciplined, r/productivity, r/selfimprovement). My searches didn't surface direct Reddit threads; the search engine didn't index them. Secondary discussion (LessWrong, EA Forum, review blogs) consistently says:
- Money stakes work for a subset of people ("akratics").
- Self-report invites cheating.
- Stakes "feel punitive" and don't suit people with money anxiety or ADHD.
- People want the money to go to good causes, not the company ([LessWrong](https://www.lesswrong.com/posts/DRrAMiekmqwDjnzS5/my-experience-using-financial-commitments-to-overcome), [EA Forum](https://forum.effectivealtruism.org/posts/DJKquqvFQR94QysDe/launching-euzoia-beeminder-for-effective-charities)).

Treat Reddit-specific sentiment as **not directly verified** in this slice.

---

## 3. JIKO name check (specific findings)

### App Store (US), searched 2026-11-22 for "Jiko", "JIKO", "jiko habit", "jiko life", "jiko quest", "jiko self"

| App | Developer | Category | Release | Rating | Notes |
|---|---|---|---|---|---|
| **Jiko: Spendable T-Bills** | Jiko Technologies, Inc. (jiko.com) | Finance | 2019-10-21 | 4.42 (48) | Treasury-bill cash account, the "Jiko Pockets" product. Active, updated Nov 2026 |
| **JIKO Life** | Momence, Inc. (white-label studio-booking platform) | **Health & Fitness** | 2025-12-10 | 5.0 (5) | Class booking and messaging for **JIKO Life**, a sauna, cold-plunge, IV-therapy and breathwork wellness center in Salt Lake City/Draper, Utah ([jikolife.com](https://jikolife.com/)). Not a habit or gamified app |

No other "Jiko" app exists; the remaining results were fuzzy matches (Jiro, Nekopara).

### Google Play (US)

| App | Package | Installs | Rating |
|---|---|---|---|
| Jiko: Spendable T-Bills | `com.jikoservices.jikoapp` | 50K+ (~68.6K) | 3.94★ (111) |
| JIKO Life | `com.ribbon.jikolife` (Momence; released Jan 22, 2026) | 10+ (~48) | none |
| JIKO Life (alternate listing) | `com.fitnessmobileapps.jiko42616` | n/a | n/a |

The alternate JIKO Life listing appeared in web search results as a Mindbody-style branded app but is not resolvable via the scraper now, so it's likely delisted or region-limited. **No habit, gamification or self-improvement app called Jiko exists on Google Play.**

### USPTO (pulled live from TSDR status pages)

| Serial | Mark | Owner | Classes | Status |
|---|---|---|---|---|
| 87821939 | JIKO (standard characters) | Jiko Group, Inc. (the fintech) | 9, 36, 42 (banking software) | **Abandoned** after a TTAB inter partes decision (opposition), 2022-09-19 |
| 87822408 | JIKO (stylized, fish in the "O") | Jiko Group, Inc. | 9, 36, 42 | **Abandoned**: no Statement of Use, 2023-12-04 |
| 87822333 | MYJIKO | Jiko Group, Inc. | 9, 36, 42 | **Abandoned** after a TTAB decision, 2022-09-19 |
| 86114280 | JIKO | **Disney Enterprises, Inc.** | 30 (coffee) | **Registered** (Reg. 4676456, 2015). **Renewed** 2025-06-06 |
| 90699603 | JIKO | Sorting Robotics Inc. | 7 (pre-roll injection machinery) | **Registered** 2025-12-02 |
| 99045708 | JIKO | Dauus Corporation | 3 (laundry detergent / dish soap) | Pending; first extension of time for a Statement of Use granted 2026-03-13 |

### Interpretation (not legal advice)
- No live US registration or application for JIKO covers Class 9 (software or apps), Class 41 (education, entertainment, fitness instruction, online games) or Class 44 (health and wellness). The fintech's Class 9 filings were **opposed and abandoned**, which suggests someone opposed them; the opposer isn't identified here.
- Disney's JIKO (a coffee brand tied to its Animal Kingdom restaurant "Jiko – The Cooking Place") is a famous-brand owner with an aggressive enforcement history. It's a different class, but a knockout search by counsel is advisable.
- **Practical conflicts:**
  - Jiko Technologies owns **jiko.com** and an active "Jiko" app, so expect search and ASO confusion and a domain constraint.
  - **JIKO Life** is in the **same store category (Health & Fitness)** with a wellness positioning. It's tiny, but there's a likelihood-of-confusion and ASO overlap risk.
- **Not checked:** EUIPO, WIPO Madrid, UKIPO, JPO and state or common-law use. These should be checked before launch.
- **Linguistic notes:**
  - Japanese **自己 (jiko) = "self"**, as in 自己啓発 *jiko-keihatsu*, "self-development". That's on-theme.
  - Japanese 事故 (jiko) means "accident".
  - Swahili **jiko** means "kitchen/stove", which is Disney's usage.

---

## 4. Market & business data

### 4.1 Market size estimates (they vary by more than 10x, so treat them as directional)

| Source (date) | Scope | Figure |
|---|---|---|
| Straits Research (2024/25 eds.) | Habit-tracking apps | **$1.7B (2024) → $5.5B (2033)**, 14.2% CAGR; later edition **$1.94B (2025) → $6.41B (2034)** ([Straits](https://straitsresearch.com/report/habit-tracking-apps-market)) |
| Market Research Future | Habit tracker apps | **$1.5B (2024) → $3.0B (2035)** ([MRFR](https://www.marketresearchfuture.com/reports/habit-tracker-app-market-66871)) |
| Market Reports World | Habit tracking apps | **$1.145B (2025) → $3.548B (2034)**, 15.18% CAGR |
| DataHorizzon | Habit tracking apps | **$512M (2024) → $1.22B (2033)**, 14.8% CAGR |
| QY Research via Orbis (Feb 2024) | Habit tracking apps (narrow) | **$37M (2023) → $75M (2030)**, 9.6% CAGR ([Orbis](https://orbisresearch.com/reports/index/habit-tracking-apps-global-market-share-and-ranking-overall-sales-and-demand-forecast-2024-2030)) |
| Global Info Research via Orbis | narrow | $38M (2023) → $70M (2030), 9.2% |
| **Sensor Tower, State of Mobile 2026** | **All Health & Fitness IAP** | **Record $4.5B consumer IAP spend in 2025** ([Sensor Tower](https://sensortower.com/blog/state-of-mobile-health-and-fitness-in-2025), via [sahha.ai](https://sahha.ai/blog/health-fitness-app-market-2026/)) |
| Business of Apps | Health apps | 405M health-app downloads in 2025. **WeightWatchers was the top-grossing health app in 2025 at $368M**, followed by MyFitnessPal ([BoA](https://www.businessofapps.com/data/health-app-market/)) |

**Working view:** "Habit tracking" narrowly is a sub-$2B category with roughly 9–15% CAGR. The real addressable spend is the **$4.5B/year Health & Fitness IAP pool**, which RevenueCat says produces at least twice the revenue of all other subscription categories combined among both bottom-quartile and top-5% earners, plus Productivity and Lifestyle self-improvement.

### 4.2 Top-grossing Health & Fitness / self-improvement apps
- **US weekly revenue, Sensor Tower 2025:**
  - MyFitnessPal peaked around $3.8M/week (Q1).
  - Flo around $1.2–1.4M/week.
  - Strava around $1.5M/week (late Q3).
  - Calm around $1M/week.
  - Fitbit around $1.1M/week.
  - AllTrails $0.9–1.8M/week.
  ([Q1](https://sensortower.com/blog/2025-q1-unified-top-5-health%20and%20fitness-revenue-us-600af518241bc16eb8dce802), [Q3](https://sensortower.com/blog/2025-q3-unified-top-5-health%20and%20fitness-revenue-us-600af518241bc16eb8dce802))
- **Strava:** about $490M 2025 revenue (Sacra est.); valued at $2.2B (May 2025).
- **Self-improvement specific:**
  - Finch: ~$1M/month est., Jun 2026.
  - Fabulous: 27.8M Android installs, revenue undisclosed.
  - Lock In: $20K–$260K/month est.
  - 75 Hard: ~$50K/month est. (unreliable).
  - Umax (looksmaxxing): founder-claimed ~$500K/month in mid-2024 and 7M downloads ([Fortune](https://fortune.com/2024/07/01/looksmaxxing-apps-rate-teen-boys-faces-mental-health)). AppMagic estimates ~$2M lifetime, falling 52% to about $173K in Aug 2024 ([AppMagic](https://appmagic.rocks/blog/tiktok-trends-non-gaming-apps)).
- **Concentration:** The top 10% of H&F apps capture **92.6%** of category revenue (Adapty 2026).

### 4.3 Typical subscription prices
- **RevenueCat, State of Subscription Apps 2026** (2025 data; [RevenueCat](https://www.revenuecat.com/state-of-subscription-apps-2026/)):
  - H&F medians: **$4.99/week, $9.99/month, ~$39.94/year**.
  - All-category medians: $5.99/week, $10/month, $34.80/year (up from $31.60).
- **Observed in this slice:**
  - Atoms: $4.99/month, $39.99/year.
  - 75 Hard: ~$4.99/month, $39.99/year.
  - Forfeit: $7.99–$12.99/month, $59.99–$99.99/year.
  - Lock In: weekly ~$9.99, Android range $9.99–$34.99.
  - Strive: $5.99/month, $24.99/year.
  - Focusmate Plus: $8–12/month.
  - Google Health Premium: $9.99/month, $99/year.
  - Strava: ~$79.99/year. Runna: ~$119.99/year.
  - GoalsWon: $99.99/month (human coach).
- **AI coach apps:** typically $50–$120/year ([macaron.im](https://macaron.im/blog/best-ai-life-coach-apps-2026)).

### 4.4 Conversion benchmarks
- **RevenueCat 2026, H&F:**
  - Download→trial (D30) **6.9%** median; top performers over 23%.
  - Trial→paid **37.7%** median; top quartile over 51.4%.
  - Download→paid (D35) **2.9%** median, versus a 2.0% all-category median; top quartile over 6.2%.
  - Revenue per install **$0.48 at D14, $0.66 at D60** (highest category).
  - Realized LTV per payer $24.23 at month 1 and $35.64 at year 1.
  - 54% of H&F trials are 5–9 days long.
  - 2025 edition: H&F RPI $0.63 at D60 vs a $0.31 overall median. H&F is the category most often bought via trial (24%).
- **Adapty 2026, H&F:**
  - Install→trial 11.2% global, 14.5% North America.
  - Install→paid direct ~3.7%.
  - Weekly-plan funnel: 9.5% install→trial, **42.2% trial→paid**.
  - **86.1% of trials start on Day 0** (so the onboarding paywall is decisive).
  - Annual plans grew from 51% (2023) to 61% (2025) of H&F revenue.
  - 12-month install LTV **$1.21** (highest category).
  - Hard paywalls deliver 21% higher LTV; soft paywalls convert about 50% better on raw conversion.
  - Renewal retention (all categories): 59.2% at the first renewal, then 45.1%, 37.1%, 31.6%, 27.6% ([Adapty](https://adapty.io/blog/health-fitness-app-subscription-benchmarks/)).
- **RevenueCat 2025:** cheap annual plans keep up to 36% of subscribers after a year; high-priced monthly plans keep 6.7%.

### 4.5 Retention benchmarks (Day 1 / 7 / 30, health & fitness)

| Source | D1 | D7 | D30 |
|---|---|---|---|
| Adjust (via Business of Apps) | 27% | n/a | **8%** |
| AppsFlyer (via BoA) | n/a | n/a | **3%** |
| Sendbird (via Lovable) | 20–27% | ~7% | ~3% |
| Braze | n/a | n/a | 3.9% iOS / 3.4% Android |
| UXCam 2026 (via Userpilot) | n/a | n/a | 8–12% |
| OneSignal 2024 (all categories) | 28.3% | 17.9% | 7.9% |

([Business of Apps](https://businessofapps.com/data/health-fitness-app-benchmarks), [Braze](https://www.braze.com/resources/articles/mobile-app-retention), [Stream](https://getstream.io/blog/app-retention-guide), [UXCam](https://uxcam.com/blog/mobile-app-retention-benchmarks/))

**Rule of thumb: H&F is about 25% at D1, 7–15% at D7 and 3–8% at D30.** There's strong January seasonality. A social or pair mechanic that lifts D30 above ~10% would be top-decile.

### 4.6 CAC / UA cost trends
- **Average CPI 2025** (Adapty): $4.70 iOS and $3.70 Android, "a sharp increase from a few years earlier."
- **H&F CPI by source:**
  - Airbridge: median $5.78 on iOS.
  - Adapty: $3–$6, with fully loaded CAC typically 2–3x CPI.
- **Cost per trial:** Airbridge calls $20–$40 a healthy blended cost per trial. It puts H&F **cost per paying user at about $23–29**.
- **Spend growth:** H&F **iOS UA spend grew 97% year over year (2024→2025)** (Airbridge) ([Airbridge](https://airbridge.io/en/blog/cost-per-trial-cost-per-subscription-subscription-app-ua-metrics), [Adapty](https://adapty.io/blog/customer-acquisition-cost/)).
- **Implication:** Paid UA payback needs Year-1 LTV per payer of roughly $35 or more (RevenueCat H&F median $35.64). That's tight. **Organic and viral loops (invites, TikTok formats, creator distribution) are mandatory.** Focus Friend (creator), Locket (TikTok, 600K downloads/day at peak per [OMR](https://omr.com/de/locket-social-app-tiktok/)) and Lock In (TikTok trend) show the playbook.

### 4.7 Acquisitions, funding and corporate events

| Event | Date | Detail |
|---|---|---|
| **Headspace + Ginger merger**, forming Headspace Health | Aug 2021 (closed Oct 2021) | About a **$3B** combined valuation; Ginger was previously valued at $1B ([Bloomberg](https://www.bloomberg.com/news/articles/2021-08-25/meditation-app-headspace-acquires-blackstone-backed-ginger), [STAT](https://www.statnews.com/2021/08/25/headspace-ginger-merger-mental-health/)). Later layoffs: about 50 jobs (~4%) in Dec 2022 ([Becker's](https://www.beckershospitalreview.com/digital-health/headspace-lays-off-about-50-employees/)). I did not verify 2024–25 layoffs |
| **BeReal → Voodoo** | Jun 2024 | €500M, cash plus earnout |
| **Strava → Runna** | Apr 2025 | Undisclosed. Strava valued at $2.2B in May 2025 |
| **Fitbit app → Google Health** | May 2026 | Rebrand plus Gemini Health Coach. Earlier, Fitbit's social challenges were removed (Mar 2023) |
| **Fabulous** | — | **No acquisition found.** Independent Fabulous SAS (Paris), Duke incubation |
| **Finch** | — | **No institutional funding**; bootstrapped PBC. Revenue est. up to ~$1M/month (2026) |
| **Habitica (HabitRPG Inc.)** | — | **No acquisition found.** Small team, open source. Tavern and Guilds removed in Aug 2023 |
| **Pact** | 2017 | Shutdown, then FTC settlement ($948,788 in refunds) |
| **Coach.me/Lift** | 2012–15 | Obvious-incubated. Raised a $1.1M add-on in 2014 and pivoted to paid coaching |
| **stickK** | 2007– | About $2M raised in two rounds; B2B pivot |
| **Forfeit** | 2023 | YC. $500K pre-seed per an aggregator (unverified) |
| **Paired** | 2020–21 | $4.6M seed total |

### 4.8 Trends, 2024–2026
1. **AI coaches go mainstream:**
   - Google Health Coach (Gemini), $9.99/month, May 2026.
   - Forfeit "Overlord" (an AI that emails your partners, calls you and reviews evidence).
   - Squad's in-chat AI.
   - WhatsApp coaches (Habit Hero, NeverGiveUp, Habitchat).
   - Users now ask for AI features in reviews (Atoms Android: "AI is needed").
   - ACCA (Aug 2026): "AI coaching is becoming mainstream."
   - **Risk:** AI-driven charging errors (a Forfeit 1★ review: "this ai needs serious help").
2. **"Solo Leveling system" / RPG self-improvement:** dozens of copycat "System" apps and templates appeared in 2025–26, and no winner owns the aesthetic. Life Reset (13K ratings), Monke (2K) and Lock In's OVR card show **game identity plus progression** sells.
3. **TikTok trends:**
   - **"The Great Lock In"** (Sep 1–Dec 31, 2025) means self-chosen rules. "Lock in" was the American Dialect Society's "most useful" term of 2024. Fortune, CBC, Marie Claire and others covered it, including critiques that it slides into hustle culture or "skinnytok" ([Fortune](https://fortune.com/2025/09/11/what-is-the-great-lock-in-gen-z-millennial-hustle-culture-burnout/), [CTV](https://www.ctvnews.ca/lifestyle/article/the-great-lock-in-heres-everything-you-need-to-know-about-the-new-social-media-trend/)).
   - It recurred as "Great Lock In 2026" and boosted Lock In's revenue (+476% month over month, Huxiu).
   - Related formats: **Winter Arc**, 75 Hard/Soft, Her 75, Monk Mode and **side quests** (several 2025–26 apps).
4. **Looksmaxxing / glow-up:**
   - Umax (51.8K iOS ratings, 7M downloads claimed), LooksMax AI (42.8K), LooxUP (37K), UCHAD (13K, 2025), PSL – Looksmax & Ascend (12.7K, Nov 2025).
   - High revenue spikes and fast decay (Umax down 52%).
   - Teen mental-health scrutiny ([Fortune 2024](https://fortune.com/2024/07/01/looksmaxxing-apps-rate-teen-boys-faces-mental-health)).
   - JIKO should avoid face-rating mechanics, which carry reputational and regulatory risk.
5. **Gen Z loneliness:**
   - Cigna 2025: **67% of Gen Z classified as lonely**, versus 65% of millennials, 60% of Gen X and 44% of boomers.
   - Gallup 2025: 25% of young US men lonely vs 17% of other adults ([ScienceBlog/Cigna](https://scienceblog.com/t-gen-z-loneliness-67-percent-baby-boomers-44-percent/), [Fortune](https://fortune.com/well/2025/05/21/gen-z-millennial-men-loneliness/)).
   - Strava: 39% of Gen Z exercise to meet people. Run clubs exploded.
   - This favors **small-circle, IRL-adjacent social features** over public feeds.
6. **Digital minimalism / screen-time backlash:**
   - Opal (91.9K iOS ratings), Forfeit's Screen Time blocking, Focus Friend.
   - Strava's 2025 tagline: "Doomscrolling is out, movement is in."
   - Cal Newport commentary on the Great Lock In ([calnewport.com](https://calnewport.com/the-great-lock)).
7. **Neurodivergent-friendly design wins awards:**
   - Apple **iPhone App of the Year 2025 = Tiimo** (AI visual planner for ADHD).
   - **Google Play Best App 2025 = Focus Friend**, which also won Apple's Cultural Impact award ([Apple Newsroom](https://apple.com/newsroom/2025/12/apple-unveils-the-winners-of-the-2025-app-store-awards), [Google](https://blog.google/products/google-play/best-apps-games-2025/)).
   - Finch has also been an App Store Editors' Choice.
   - **Apple and Google featuring favors gentle, non-punitive, accessible design.** Money penalties and face rating don't get featured.
8. **Creator-led apps:** Atoms (James Clear), Focus Friend (Hank Green), 75 Hard (Andy Frisella), The Wave – Bet On Yourself (Molly Grantham). An audience is the cheapest form of CAC.

---

## 5. Implications for JIKO (synthesis)

1. **Make pair or small-circle accountability the core.** Pair mechanics scale well: Paired has 211K ratings and Finch's friend features are soft. Stranger squads and public guilds don't: Squad churns, Habitica removed its Tavern. Design for 2–6 known friends, plus an **AI companion** that keeps the circle alive when humans go quiet (Squad's best-reviewed feature).
2. **Proof should be lightweight and multimodal:** time-boxed photo (BeReal-style prompt), HealthKit/Google Health auto-verify, GPS, and friend-verify. Include a **grace or appeal path** (Forfeit's human appeals). Never punish the user for the app's own failure.
3. **Use reputation or charity stakes instead of house-kept cash:**
   - If money is involved: forfeits to charity or friends, clear ROSCA-compliant consent, no double-dipping on top of a subscription, and no pooled "win money" mechanics without gambling and sweepstakes review (Pact/FTC precedent; App Store 5.3).
   - Reputation stakes ("your circle sees you missed", "a text to your buddy") get most of the effect with less risk.
4. **Monetization:**
   - Price near category norms (~$9.99/month, ~$39.99–59.99/year).
   - Put the paywall at onboarding, since 86% of H&F trials start on Day 0, but **keep basic tracking and the social loop free**. The paywall-on-basics backlash is the #1 complaint theme.
   - Never retroactively take away paid features (75 Hard).
5. **Distribution:**
   - Package challenges as **shareable, named, time-boxed formats** (a "JIKO 30", "Lock-In Season", side quests) to ride TikTok cycles.
   - Invites must work flawlessly: offer Apple, Google and email sign-in plus deep links. Auth bugs killed Squad and HabitShare invites.
6. **Positioning white space:** No one combines (a) Finch-grade warmth and identity, (b) a game "System" or level aesthetic, (c) close-friend proof, and (d) an AI coach, all without punitive money. The closest pieces are Lock In (game and paywall, no friends), Finch (warmth, light social), Squad (group and AI, buggy and small) and Forfeit (proof and AI, punitive).
7. **Name:** **JIKO** looks clear in software and health classes in the US, and "jiko" means "self" in Japanese, which is a good story. Still:
   - resolve jiko.com versus an alternative domain
   - assess ASO confusion with Jiko (fintech) and JIKO Life (wellness studio, same category)
   - run a professional clearance including EUIPO, Madrid and common-law use, and Disney's Class 30 registration

---

## 6. Method notes and gaps
- **iOS data:** iTunes Search/Lookup API, US, 2026-11-22.
- **Android data:** google_play_scraper (`app`, `search`, `reviews`), US. Packages that couldn't be resolved: stickK, HabitShare, Coach.me, Focusmate (official).
- **Reviews:** iOS RSS (most recent 50) and Google Play newest 120 per app, for Forfeit, Beeminder, Squad, 75 Hard, Atoms, Lock In, stickK, HabitShare and Coach.me.
- **Trademark:** USPTO TSDR status pages fetched directly. Justia and markinton were blocked or unreachable.
- **Not found or unverifiable:**
  - Supergoal, Peerbound, Hourglass, Payback, Goal Hero (as a stake app), Sesh, "Tribe"/"Rally" community apps, "Habit Squad", a single "Momentum" competitor.
  - Direct Reddit threads.
  - Beeminder user and revenue totals; stickK totals.
  - Forfeit and Squad founder names (one maker name for Squad is unconfirmed).
  - Fabulous ownership changes; Headspace layoffs in 2024–25.
  - Official revenue for any app in this slice. All revenue figures are third-party estimates or founder claims, as labeled.
