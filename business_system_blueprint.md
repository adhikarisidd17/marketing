# AI Content System Blueprint: Diabetic + Healthy Fat-Loss Recipe Reels

## 1) Goal
Build a repeatable system that discovers high-performing healthy recipes, turns them into short-form videos (Reels/Shorts), and publishes daily with optimization loops for Instagram, YouTube, and Facebook.

## 2) Business Model (Monetization Paths)
1. **Platform-native monetization**
   - YouTube Partner Program (ad revenue for long-form + Shorts revenue share once eligible).
   - Meta monetization options when account becomes eligible.
2. **Affiliate revenue**
   - Kitchen tools, glucose-friendly food products, meal-prep containers, nutrition books.
3. **Digital products**
   - Paid recipe packs (e.g., 30-day diabetic-friendly meal plans).
   - Low-cost eBook + premium subscription meal planner.
4. **Brand sponsorships**
   - Diabetes-focused food brands, fitness apps, meal services.
5. **Lead generation**
   - Capture emails through free lead magnet ("7-day diabetic breakfast plan").

## 3) End-to-End System Architecture

### A. Recipe Discovery Engine
**Purpose:** Find recipes with proven audience demand and engagement.

**Inputs (daily):**
- YouTube Shorts search results
- Instagram hashtag/trending topic signals
- Pinterest/TikTok trend keywords
- Recipe blogs + Reddit discussions

**Scoring model (0-100):**
- Engagement proxy (likes/comments per 1,000 views): 30%
- Save/share intent proxy (where available): 20%
- Topic momentum (search trend + recency): 20%
- Diabetes suitability score (low added sugar, controlled carbs, high protein/fiber): 20%
- Production simplicity score (<=8 ingredients, <=30 min): 10%

**Output:**
- Top 10 recipe candidates/day
- 3 selected for production queue (one per content angle)

**Angles to rotate:**
1. "High-protein diabetic breakfast"
2. "10-minute low-carb lunch"
3. "Craving fix dessert under X carbs"

---

### B. Content Intelligence Layer
For each chosen recipe, generate:
1. **Hook variants (5)**
   - "If you have diabetes, try this 12g-carb dinner."
2. **Script variants (2 lengths)**
   - 20–25 sec version
   - 35–45 sec version
3. **SEO metadata pack**
   - Platform-specific titles
   - Description + CTA
   - Hashtag sets (broad + niche + intent)
4. **Compliance notes**
   - Avoid medical cure language
   - Add disclaimer: educational, not medical advice

---

### C. AI Video Production Pipeline
**Preferred visual formats:**
- Hands-only cooking B-roll style
- Ingredient card overlays
- Step-by-step kinetic text
- Before/after nutrition panel

**Automated flow:**
1. Generate shot list from script
2. Create visuals (stock + AI visuals + your brand templates)
3. Generate voiceover (or clone own voice with consent)
4. Auto-caption with emphasis words
5. Add music + platform-safe audio
6. Render 9:16 (1080x1920), 24–30 fps
7. Export per-platform variants

**Length targets:**
- Instagram Reels: 15–35 sec primary
- YouTube Shorts: 20–40 sec primary
- Facebook Reels: 20–45 sec primary

---

### D. Daily Publishing & Scheduling System
Instead of assuming a universal "best time", use **adaptive scheduling**:
1. Start with 2 candidate windows per platform.
2. Split-test for 14 days.
3. Keep top-performing window by watch-through + saves/shares.
4. Re-test monthly.

**Initial baseline windows (US-focused, local audience time):**
- Instagram: 11:30 AM, 6:30 PM
- YouTube Shorts: 12:00 PM, 8:00 PM
- Facebook Reels: 1:00 PM, 7:00 PM

**Cadence:**
- 1 primary reel/day cross-posted to all 3 platforms
- 1 optional repost/remix/day from top historical content

**Scheduler stack options:**
- Meta Business Suite (Instagram/Facebook)
- YouTube Studio scheduler
- Optional orchestration via Zapier/Make + Airtable/Notion queue

---

### E. Analytics Feedback Loop (the growth engine)
Track each post at 2h, 24h, 72h:

**Core metrics:**
- 3-second hold rate
- Average watch percentage
- Completion rate
- Saves/shares/comments per 1,000 views
- Follows/subscriber conversion per 1,000 views

**Decision rules:**
- If hold rate < 65%: rewrite first 1.5 sec hook
- If completion < 35%: shorten video by 20%
- If saves high but views low: repost with stronger thumbnail/title
- If comments high: produce "Part 2" within 48h

---

## 4) Team + Tools Setup (Lean Solo Founder Mode)

### Core tools
- **Research:** Apify + Google Trends + manual competitor list
- **Data store:** Airtable (recipes, scripts, assets, status)
- **Generation:** GPT workflow for hooks/scripts/metadata
- **Video:** CapCut templates or FFmpeg automation + TTS
- **Scheduling:** Meta Business Suite + YouTube Studio
- **Dashboards:** Looker Studio / Airtable Interfaces

### Minimum daily operating procedure (SOP)
1. 8:00 AM: Pull trending recipe candidates
2. 8:30 AM: Score and select top 3
3. 9:00 AM: Generate scripts/hooks
4. 10:00 AM: Produce/edit 1–2 reels
5. 11:30 AM onward: Publish per queue
6. End of day: Log metrics and insights

---

## 5) 30-Day Launch Plan

### Week 1: Foundation
- Build brand kit: logo, color, text style, intro/outro
- Create 10 reusable reel templates
- Build Airtable pipeline + scoring formula
- Produce 7-post backlog before day 1 launch

### Week 2: Daily posting starts
- Post 1 reel/day on all platforms
- A/B test first hook frame + cover title
- Begin collecting baseline analytics

### Week 3: Optimization
- Double down on top 2 recipe categories
- Start CTA funnel (free PDF in bio)
- Begin email list capture

### Week 4: Monetization activation
- Add affiliate links to tools/ingredients
- Soft-launch paid recipe bundle
- Pitch first 10 micro-brand sponsorships

---

## 6) Content Formats That Usually Perform Well
1. "3 ingredients only"
2. "Under 15g carbs"
3. "Meal-prep for 3 days"
4. "Diabetic dessert swap"
5. "What I eat when craving sugar"
6. "Budget grocery diabetic meals"

Use a **70/20/10 content mix**:
- 70% proven formats
- 20% experimental hooks
- 10% personal story/trust-building

---

## 7) Guardrails (Important)
- Do not claim cure/reversal promises.
- Use educational language and suggest consulting a licensed clinician for individualized medical advice.
- Verify recipe macros before publishing.
- Use only licensed music/assets and rights-safe visuals.

---

## 8) Automation Blueprint (Pseudo-Workflow)
1. Daily cron triggers trend scraper.
2. New ideas written to Airtable.
3. Scoring formula ranks ideas.
4. Top rows trigger script generator.
5. Script + template trigger video rendering pipeline.
6. Final MP4 pushed to "Ready to Post" folder.
7. Scheduler posts at next optimal slot.
8. Metrics pulled back and appended to Airtable.
9. Weekly report suggests next week content priorities.

---

## 9) KPI Targets (First 90 Days)
- Post consistency: 90+ reels published
- Average watch-through: >40%
- Save rate: >20 per 1,000 views
- Followers/subscribers: 5,000 combined
- Email leads: 1,000
- Monthly revenue target: first $500-$2,000 through affiliate + digital products

---

## 10) What To Do Next (Immediate)
1. Pick your niche positioning statement (example: "Diabetic-friendly recipes for busy professionals in under 20 minutes").
2. Set up Airtable pipeline with statuses: `Idea -> Script -> In Production -> Scheduled -> Posted -> Analyzed`.
3. Create your first 14-day content calendar.
4. Record or generate first 7 reels in batch.
5. Start posting daily and optimize hooks every 3 days based on retention.

