# Therapilatics — Brand & Design System Reference
*Paste this at the start of any new conversation to maintain consistency.*

---

## The Business

**Therapilatics** — private classical Pilates studio, Melbourne FL
Parent entity: **Pilates Footworks LLC**
Address: 478 N Babcock St, Melbourne, FL 32935
Email: info@therapilatics.com
Phone: +1 321-766-7246 (updated from 561 at October 2026 launch)
Website: therapilatics.com
Booking: Setmore — therapilatics.setmore.com (paid plan, embed available)
Sunday residency: Jonathan's Landing, Jupiter FL

---

## Positioning

**Core line:** "One room. One client. Every session."
**Tagline:** Mending with Movement
**Key claim:** The only Gratz studio on the Space Coast (verified — no other Gratz studio in Brevard County)
**Target client:** 45–65+, disposable income, managing a specific physical issue — chronic pain, post-surgical recovery, structural limitation, mobility loss. Includes Melbourne aerospace/defense workforce, medical community, active retirees. Male demographic (injured golfer, tennis player) is underserved by current wellness marketing and must not be alienated.
**Not the target:** Fitness enthusiasts, group class converts, Club Pilates demographic.

**Against competitors:**
- Pilates on Fifth (Indialantic): $90 shared equipment room. Therapilatics: $125 genuinely private room, full Gratz suite.
- Club Pilates: franchise, reproduction equipment, group model. Different category entirely.
- No competitor on the Space Coast uses Gratz apparatus.

---

## Language Rules

- "Assessment" not "Consult" or "Consultation" — signals diagnostic, not sales
- "Instructor" in classical Pilates context (clients are the practitioners of the method); "practitioner" used on the website for the target audience because it signals clinical credibility
- No "LIIT," no wellness spa language, no warm/soft positioning
- Do not over-explain the Jonathan's Landing signal — place it quietly, those who know will know
- Never use italics anywhere — accessibility decision for low vision clients
- Body text minimum 18px / 1rem
- No beige, linen, or warm tones anywhere

---

## Pricing (confirmed)

| Service | Price | Notes |
|---|---|---|
| Introductory Assessment | $85 | One hour. New clients only. Movement assessment, not a session. |
| Foundation Period | $375 | 5 sessions / 3 weeks. New clients only. Not a discount — a structured methodology. |
| Private Session | $125 | One hour. Existing clients. |
| Monthly Retainer | $500 | 4 sessions/month. Weekly slot held. Not a discount — a held slot in a limited practice. The slot is yours as long as the retainer is active. |

**Cancellation policy:** All services prepaid. Late arrivals receive remainder of hour. Cancellations 24+ hours notice may reschedule within same calendar week subject to availability. Cancellations within 24 hours forfeit the session.

---

## Design System

### Typography
- **Display/Headers:** Barlow Condensed — weight 500–600, uppercase, letter-spacing 0.01–0.1em
- **Body:** Barlow — weight 400 minimum (never 300 — fails on mobile for older eyes)
- **No italics anywhere** — accessibility decision
- **Body text minimum:** 18px / 1rem
- **Line length:** under 70–75 characters on desktop

Google Fonts import:
```
https://fonts.googleapis.com/css2?family=Barlow:wght@400;500;600&family=Barlow+Condensed:wght@400;500;600;700&display=swap
```

### Color Palette (strict — do not introduce warm tones)
```css
:root {
  --teal: #3D9A97;
  --teal-dark: #2E7B78;
  --teal-pale: #E4F2F1;
  --black: #0E0E0D;
  --dark: #1E1C1A;
  --body: #2E2C2A;
  --mid: #4A4745;
  --light: #767270;
  --rule: #C8C4BC;
  --pale: #F0EEEB;
  --grey: #E8E6E3;
  --grey-mid: #D4D1CD;
  --white: #FAFAF6;
}
```

**No warm beige, no linen, no warm white.** Grey and charcoal only for neutrals. Teal (#3D9A97) is the only accent color. All text must pass WCAG AA contrast.

### Layout System
- **Nav:** 3px black top border, 1px rule bottom. Logo left, nav links center (desktop), Book button right. Mobile: logo left, hamburger right.
- **Section headers:** 2px black top rule, 1px rule bottom
- **Teal used as:** left border accent (3px), rule accent, color emphasis only
- **Dark/charcoal used for:** page headers, featured sections, footer, distinction strips
- **Mobile-first, single column collapse**
- **Tap targets:** minimum 44px height

### Page Header Pattern (consistent across all pages)
- Background: `--dark` (#1E1C1A)
- Bottom border: 3px solid `--teal`
- Two-column grid on desktop (title left, intro text right)
- Eyebrow label in teal, page title in Barlow Condensed 500 uppercase white
- Collapses to single column on mobile

### Nav Pattern
```
Desktop: [Logo] ........... [Services] [Apparatus] [About] [Locations] ........... [Book a Session]
Mobile:  [Logo] ................................................................ [☰]
```
Hamburger animates to X. Mobile menu slides in from top, dark border bottom, links stack vertically with Book as last item (black background).

### Footer Pattern
- Background: `--black`
- Three-column grid: Brand/legal | Contact | Locations
- Footer logo with teal accent on "pilatics"
- Tagline: "Mending with Movement"
- Legal: "© 2026 Pilates Footworks LLC. All Rights Reserved."

---

## Site Architecture (6 pages)

| Page | File | Status |
|---|---|---|
| Home | index.html | Built — unified desktop+mobile |
| Services | services.html | Built — needs Assessment swap confirmed |
| About | about.html | Built — photos placed |
| Locations | locations.html | Built |
| The Apparatus | apparatus.html | Pending |
| Book | book.html | Pending — Setmore embed ready |

All pages share the same nav, footer, color system, and type system. One file per page — CSS handles both desktop and mobile breakpoints. Mobile breakpoint: 768px.

---

## Photography

**Confirmed usable photos (filename → use):**

| File | Use |
|---|---|
| img-coaching-primary.png | Primary action shot — Laini hands-on, client standing on Reformer |
| img-hands-detail.png | Detail/About — hands with glass bead bag on Reformer carriage |
| img-cadillac.png | Apparatus hero — Cadillac frame and springs, clean white wall |
| img-coaching-secondary.jpeg | Secondary coaching — Laini guiding arm extension, seated client |
| img-male-client.png | Client action — white-haired male on Reformer, curtain background |

**Photography rules:**
- No solo headshots of Laini — show her working, hands on apparatus or client
- No photos of Jupiter studio equipment (Balanced Body, not Gratz)
- Remove before shooting: monitors, red Solo cup, cardboard boxes, wire rack clutter, leaning mirrors, laptop, power strips
- Best shooting angle: from Cadillac end toward curtain wall — avoids monitors, gives clean grey wall and geometric curtain background
- Pedi-Pole photo still needed
- Chair/apparatus shot (Image 1 from latest batch) usable — clock visible but acceptable

**Parkinson's detail note (for About page):**
A client with Parkinson's unable to quiet an involuntary hand movement found the connection through a glass bead bag pressed against the palm — and held it through the exercise. This story lives in the About page detail block. The hands photo is the visual reference. Do not name the condition or client explicitly.

---

## The Apparatus (Gratz Industries — complete suite)

| Piece | Label | Copy direction |
|---|---|---|
| Gratz Cadillac | Therapeutic Foundation | Most versatile piece; works with post-surgical/deconditioned clients who can't yet access Reformer or mat |
| Gratz Reformer | The Familiar Anchor | Foundation of classical work; built to original specifications by Gratz Industries |
| Gratz Pedi-Pole | Rare Specialist Piece | Spinal alignment, postural feedback, decompression; rarely found outside specialist classical studios — photo pending |
| Gratz Ladder Barrel | Structural | Spinal extension, lateral flexion, hip work; addresses restrictions from sitting, surgery, chronic tension |
| Gratz High Chair / Wunda Chair | Precision and Function | NOT split pedal — this is a common error, do not use that description |
| Correctors | Micro-Precision | Foot, toe, hand correctors; fine-motor compensations driving bigger problems up the chain |

**Note:** The wall-mounted desk in the studio is NOT apparatus. Do not reference or photograph it for the site.

---

## About Page Copy (final — use verbatim)

Laini Byfield came to Pilates by necessity, not by choice.

A series of accidents left her with spinal and shoulder injuries. Physical therapy helped — but not enough to pick up her toddler or raise her right arm above her head. Pilates did.

Before she finished healing, she wanted to teach. As an MIT-trained engineer, she recognized something in the classical system: every piece exists in relationship to the others. Any one part is less effective than the whole. That's why this studio runs on a complete Gratz apparatus suite and why the training here goes to Third Degree — the full system, not a version of it.

Therapilatics exists for people who have tried the obvious options and are still not where they need to be.

**Precision paragraph (add after engineering paragraph):**
The method rewards thinking. Three precise repetitions do more than nine approximate ones — the nervous system learns the pattern when the body executes it correctly, not when it works through repetition. This is why a session might stop at the third rep instead of the ninth: because those three were right, and adding more would overwrite the pattern rather than reinforce it. Pilates is not a sport where more is better. It is a practice where precision is the point.

**Credentials block:**
- Third Degree Classical Pilates, Romana Kryzanowska Lineage — Real Pilates NYC
- B.S. Engineering, MIT
- NBC-HWC, National Board Certified Health & Wellness Coach
- MPH Candidate, GWU Milken Institute School of Public Health
- Brian Grant Foundation — Exercise for Parkinson's
- Pre & Postnatal Pilates certified
- Pilates for Blind & Low Vision certified
- ATM System — Treating the Rotational Athlete
- CCP Candidate, WorldatWork (in progress)

**Article reference:** Featured in Hometown News Brevard, September 2024
https://www.hometownnewsbrevard.com/news/local/melbourne/boost-your-confidence-with-therapilatics/article_b61b37b5-e339-5581-b236-ae756adc6cfd.html

---

## Setmore Notes

- URL: therapilatics.setmore.com
- Paid plan — embed available
- Setmore "About" description needs updating to match site copy
- Industry set to "Spa" — should be changed to Pilates Studio
- Services list has 23 entries — needs cleanup to match confirmed pricing before launch
- Cancellation window in Setmore set to 12 hours — site copy says 24 hours — reconcile before launch

---

## Standing Instructions

- Never soften criticism to protect ego. "This fails because X" is more useful than "have you considered X."
- When uncertain, say so rather than presenting guesses as facts.
- No italics in any design output.
- No beige, linen, or warm tones — grey/charcoal/white/teal only.
- Do not reintroduce Rocket Medical strategy or NPI into website copy — those belong in separate B2B documents.
- The studio is scalable — copy should reflect the practice standard, not Laini personally, except on the About page.
- "Assessment" not "Consult" — always.
- Jonathan's Landing is never explained — placed quietly near credentials or location.
