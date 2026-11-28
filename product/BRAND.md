# JIKO: Brand

*Working document. Locked items are marked ✅; open items are marked 🔲.*
*Product context: `product/JIKO_SPEC_v1.md`.*

---

## 1. Brand core ✅

**Name:** JIKO, from 自己 (*jiko*), Japanese for "self". Jiko is your braver self, growing.

**Tagline:** *Every brave tradition started with one monkey who went first.*

It's about monkeys and quietly about the user: *you can be the one who goes first.*

**Origin story.** Japan's snow monkeys are famous for two acts of curiosity and courage:
- **The hot springs.** In the early 1960s at Jigokudani, a young female was seen getting into a hot spring. The rest of the troop followed, and bathing became their culture. ([Lonely Planet](https://www.lonelyplanet.com/articles/japanese-snow-monkeys-hot-baths), [Primates, 2018](https://rd.springer.com/article/10.1007/s10329-018-0661-z/fulltext.html))
- **Imo's sweet potatoes.** In 1954 on Koshima island, a young macaque named Imo began washing sandy sweet potatoes in water. Others copied her, and it spread through the troop. ([Atlas Obscura](https://www.atlasobscura.com/articles/2932))

In both cases, one monkey stepped out of her comfort zone, tried something new, and changed life for everyone around her. That is the whole idea behind JIKO.

*Copy note: sources give the first onsen bathing as winter 1962 or January 1963. In public copy, say "the early 1960s".*

---

## 2. Jiko, the character ✅

**Species:** Japanese snow monkey (macaque).

**Personality:** warm, curious and a little nervous. Jiko is brave because it's scared, not because it isn't. It celebrates small wins, notices little things and never judges. (Voice rules: spec §5.1.)

### Design principles
1. **Front-on, always.** Every pose, outfit and part must read from the front.
2. **Round and soft.** A chubby, rounded body, oversized head and stubby limbs. Cute first, realistic second.
3. **The heart-shaped red face** is the signature feature, recognisable at every stage and size, down to an app icon.
4. **Huge, expressive eyes.** Most of the emotion is carried by the eyes and cheeks.
5. **Real hands.** They are a selling point: Jiko can hold items, wave and high-five.
6. **One silhouette family.** Each life stage is clearly the same character, getting bigger and fluffier.
7. **Built for dressing up.** The body proportions must support all 12 Item slots without redrawing the base for each item.

### Life stages

| Stage | Brave Days | Look |
|---|---|---|
| **Snowball** | 0 | A snowball with a tiny sleeping face peeking out. It breathes gently. |
| **Snowdrop** | 1 | Newborn: tiny, mostly head and eyes, wispy fur |
| **Scamp** | 7 | Wobbly baby with fluffier fur. Playful and bouncy. |
| **Wanderer** | 21 | Youngster with longer limbs and a curious posture |
| **Climber** | 42 | Sturdier and confident, with a thick coat |
| **Trailblazer** | 66 | Fully grown, with the full snowy mane (head feature unlocks) |

### Onboarding moment
A snowball sits in the snow, gently breathing: "Something's sleeping in here…" When the user names Jiko, the snow melts away and a baby snow monkey blinks awake.

---

## 3. World ✅

- **Home:** a cosy mountain hut (Finch-style fixed slots).
- **Onsen Garden:** the hut's own outdoor hot spring, unlocked at Body Lv 5. Jiko soaks there after brave days. It has its own slots and seasonal skins (cherry blossom, autumn maple, winter snow…).
- **Wider world flavour:** snowy mountains, cedar forests, stone lanterns, steam and persimmon trees. Wanderings take Jiko through this world.

---

## 4. Art style ✅

- **Finch-style flat 2D vector**, front-on character, with simple shapes and clean silhouettes.
- **Soft shading:** at most one shadow tone and one highlight per shape.
- **Optional subtle grain or texture** on large surfaces (walls, sky) to set us apart from Finch.
- **Season key art and Wrapped cards** may use richer, more illustrative treatments (the TFT model: a simple in-game style, splashy season art).

---

## 5. Colour: Onsen Dawn v2 ✅

*Fresh snow, persimmon lamps, onsen steam. Cosy and hopeful, with a little sunrise in every screen.*
Reviewed board: `product/brand/palette-board-v2.html`. Tokens: `product/tokens/colors.json` and `product/tokens/colors.css`.

### 5.1 Core UI

| Token | Light | Dark (onsen night) | Use |
|---|---|---|---|
| `bg` | `#fffcf8` Snow | `#13242a` Onsen night | App background |
| `surface` | `#ffffff` | `#1e343b` | Cards, sheets |
| `line` | `#ede4dc` | `#2c474f` | Borders, dividers, empty tracks |
| `ink` | `#2a1e1a` | `#f4ede6` | Primary text |
| `muted` | `#6b5a52` | `#afc0c0` | Secondary text |
| `primary` | `#f2803c` Persimmon | `#f58a4a` | Main buttons, pass progress, key actions |
| `on-primary` | `#2a1e1a` | `#1c1410` | Text on primary. **Never white**: white fails AA on persimmon. |
| `secondary` | `#2ba8a0` Onsen teal | `#3cc0b6` | Secondary actions, tags, calm highlights |
| `on-secondary` | `#0d2624` | `#0b2321` | Text on secondary |

### 5.2 Jiko and the hut

| Token | Light | Dark | Use |
|---|---|---|---|
| `jiko-face` | `#ee7c8e` Jiko rose | `#ee7c8e` | Jiko's face, hands and inner ears. **Reserved for Jiko**: never used in UI |
| `jiko-fur` | `#9c897c` | `#a8968a` | Default body colour |
| `jiko-fur-edge` | `#6f5f55` | `#7a695e` | Fur edge, feet, arms |
| `jiko-belly` | `#efe6dd` | `#e3d9cf` | Belly |
| `hut-wall` | `#fbe9da` | `#1c3a40` | Default wallpaper |
| `hut-floor` | `#c98f62` Cedar | `#4a3830` | Default floor |
| `hut-rug` | `#f7eee4` | `#2a4a50` | Rug under Jiko (keeps the silhouette readable) |
| `window-sky` | `#cbede8` | `#2e5866` | Default window view |

### 5.3 Stats

| Stat | Colour | Label text |
|---|---|---|
| Courage | `#f2803c` | dark |
| Curiosity | `#f2b33d` | dark |
| Connection | `#9c8ce0` | dark |
| Body | `#2ba8a0` | dark |
| Mind | `#5868c4` | white |

### 5.4 Status
| Token | Colour | Note |
|---|---|---|
| `success` | `#2f9e6b` | |
| `heads-up` | `#e8a12e` | Gentle warnings. JIKO never punishes, so this is rare. |
| `error` | `#c63340` | System errors only, **never** used for a missed day or a skipped quest |

### 5.5 Fear Forecast scale
1–3 `#2ba8a0` teal (calm) → 4–6 `#f2b33d` gold → 7–10 `#f2803c` persimmon (spicy). **Never red**: fear is not an error.

### 5.6 Spark Gem
Lantern gold `#ffd36b` → onsen teal `#2fb5a8`, a hexagonal gem with a white four-point spark. It must stay visually distinct from the persimmon buttons, so gems never look tappable.

### 5.7 Rules
1. Persimmon leads: about 60% of colour moments are snow and ink, 30% persimmon, 10% teal, gold and stat colours.
2. Jiko rose belongs only to Jiko.
3. Button labels on persimmon, teal and gold are always dark ink.
4. Dark mode is "the hut after dark". Never pure black; always onsen night.
5. Stat colours appear only on stat-related UI (tags, insights, Wrapped).

### 5.8 Measured checks (WCAG 2.1, CIELAB ΔE76)
| Check | Result |
|---|---|
| Text on background, light / dark | 15.8 : 1 / 13.8 : 1 |
| Muted text, light / dark | 6.4 : 1 / 8.5 : 1 |
| Button label on primary, light / dark | 6.1 : 1 / 7.4 : 1 |
| Worst stat chip label | 5.0 : 1 |
| Jiko silhouette vs room, light / dark | 2.8 : 1 / 3.4 : 1 |
| Jiko's face vs primary | ΔE 44.7 |
| Jiko's face vs error red | ΔE 29.4 |
| Spark Gem vs primary | ΔE 41.0 |

---

## 6. Open decisions 🔲

| # | Decision | Notes / seeds |
|---|---|---|
| 1 | **Typography** | Rounded, friendly display face plus a highly legible body face. Nunito is the board placeholder. |
| 2 | **Logo** | Wordmark "jiko". Possibly use Jiko's rose heart-face as the mark or app icon. Keep clear of Disney's JIKO coffee mark (see research). |
| 3 | **Spark Gem final illustration** | Colours locked (§5.6); final drawing to follow |
| 4 | **Pass screen visual design** | TFT single-track reference |
| 5 | **Motion, sound, haptics** | Soft, bouncy and cosy; onsen-steam ambience |
| 6 | **Season 1 naming** | "First Light" is a placeholder; may shift to a snow or onsen theme |
