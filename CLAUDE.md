# Keepr — Project Intelligence

## What Keepr Is

Keepr is an AI-powered receipt and warranty assistant. Users snap a photo of any receipt and the app automatically:

- Files the warranty with all relevant details
- Sends reminders before the warranty or return window expires
- Pre-fills the paperwork for a return or claim
- Finds and stores the product manual

No folders. No spreadsheets. No digging through your inbox when something breaks.

**Primary CTA:** "Forward a receipt, we handle the rest."

---

## Business Model

**Freemium + SaaS subscription.**

- Free tier: limited receipt scans / stored items
- Paid tier: unlimited scans, reminders, claim pre-fills, manual lookup

---

## Target Customer

**Age:** 25–45  
**Profile:** People who buy electronics, appliances, or gadgets and have lost money before by missing a return window, letting a warranty lapse, or losing a receipt at the worst possible moment.  
**Pain:** Companies design fine print and tight deadlines around the assumption you'll forget. Keepr makes sure you don't.

---

## Brand Voice

Anti-corporate. Anti-fine-print. The voice of someone who's tired of companies counting on you to forget your rights — and is making sure you don't.

**Tone attributes:**
- Direct and plain-spoken — no corporate fluff
- Slightly frustrated on the user's behalf (empathy through indignation)
- Confident, never preachy
- Uses "you" liberally — this is personal

**Forbidden words — never use these:**
- organize
- productivity
- seamless
- peace of mind
- declutter

**Writing examples (good):**
- "Companies count on you forgetting. We make that their problem, not yours."
- "Your warranty started the day you bought it. Not the day you remember to file it."
- "Stop letting the fine print win."

---

## Tech Stack

| Layer       | Technology              |
|-------------|-------------------------|
| Frontend    | React / Next.js         |
| AI / OCR    | OpenAI GPT-4o (vision)  |
| Input       | Photo upload / camera   |

---

## Core User Flow

1. User opens Keepr and taps **Scan Receipt**
2. Takes a photo (or uploads image)
3. GPT-4o extracts: product name, purchase date, price, retailer, warranty period
4. Keepr creates a warranty record and sets expiry reminders
5. If the user needs to return or claim: Keepr pre-fills the required form fields
6. Product manual is fetched and linked to the item record

---

## Competitive Positioning

**Primary competitor to differentiate from:** Fetch Rewards  
Fetch is about earning rewards for scanning receipts. Keepr is about protecting what you already paid for. Different job, different user mindset.

**Key differentiator:** Keepr is not a loyalty/rewards app. It's a consumer rights tool. Every feature exists to make sure the user doesn't lose money they're legally owed.

---

## AI Integration Guidelines

- Use **GPT-4o vision** for all receipt parsing
- Extract at minimum: product name, retailer, purchase date, price, warranty duration (if printed)
- If warranty duration is not on the receipt, infer a reasonable default and flag it as estimated
- Confidence scores should gate auto-filing: low-confidence extractions prompt a user confirmation step before saving
- Never silently drop data — if a field can't be extracted, surface it to the user with a manual entry prompt

---

## Development Principles

- Ship the smallest thing that saves the user money or time
- No feature exists to look impressive — only features that directly serve the core flow get built
- Error messages should be human: explain what happened and what the user can do next, never "An error occurred (code 500)"
- Every reminder, notification, and copy touchpoint should reinforce the brand voice — this isn't a utility, it's an advocate

---

## Placeholders / Still Deciding

- [ ] Tagline (not finalized)
- [ ] Backend API framework and database
- [ ] Email forwarding input channel (potential future input in addition to photo)
- [ ] Pricing tiers and limits for free vs. paid
