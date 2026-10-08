# Product Marketing Context

**Document version:** v1
**Last updated:** 2026-10-09

## Product Overview
**One-liner:** BOSD consulting that turns chaotic agency ops into Sheets + Apps Script systems teams actually follow.
**What it does:** Designs standardized workflows (lead → setup → delivery → reporting), builds ₹0-running-cost automations (invoicing + reminders + thank-yous), and hands over SOPs + Looms so teams run it without the consultant.
**Product category:** Business operations consulting / ops automation for SMB agencies.
**Product type:** Service (productized builds + audits).
**Business model:** Fixed-scope builds (3–7 days) + 2-week fix window; optional monthly check. No software resale — client owns Sheet, Drive, script.

## Target Audience
**Target companies:** 5–30 person Indian service businesses on monthly retainers (digital agencies first: SEO/SMM; applicable to any retainer business).
**Decision-makers:** Founder / ops manager / account manager who chases payments.
**Primary use case:** Stop chasing invoices manually; know who owes what, since when, reminded how many times — automatically.
**Jobs to be done:**
- Get paid on time without awkward follow-ups
- See cash position in one sheet without asking the team
- Hand over ops to a junior without things breaking
**Use cases:**
- Retainer billing (Advance due-day-1/5/10 + Postpaid previous-month)
- Pre-due / overdue / recurring reminders on Email + WhatsApp within business hours
- Payment thank-yous + audit log for every send

## Personas
| Persona | Cares about | Challenge | Value we promise |
|---------|-------------|-----------|------------------|
| Founder | Cash in on time, no team nagging | Month-end chasing on WhatsApp | Reminders go themselves; you see Paid/Overdue in one view |
| Account manager | Not looking like the bad guy | Awkward follow-ups, missing emails | Friendly templates, threaded per invoice, failures visible not silent |
| Ops hire | Clear steps, no guesswork | Scattered sheets, duplicate IDs | Validation colors + 1-page SOP + Loom; hard to break |

## Problems & Pain Points
**Core problem:** Retainer collections run on memory + WhatsApp. No single view of who owes what, reminders depend on someone remembering, thank-yous get skipped.
**Why alternatives fall short:**
- Manual follow-up — inconsistent tone, forgotten when busy
- Zoho/QuickBooks — subscription cost + still needs follow-up discipline + threading/WhatsApp gaps for this segment
- Hiring an assistant — recurring salary for work a free script does daily at 8:30am
**What it costs them:** 2+ hrs/week chasing, late payments stretching 10–30 days, awkward client moments, founder doing ops instead of sales.
**Emotional tension:** Dread before the 1st/5th/10th; embarrassment nudging a good client; doubt whether the invoice was even sent.

## Competitive Landscape
**Direct:** Zoho Books / QuickBooks + reminder add-ons — falls short because subscription + setup + still not WhatsApp-first + overkill for a 10-client agency.
**Secondary:** Virtual assistant doing follow-ups — falls short because recurring cost, inconsistent tone, no audit log.
**Indirect:** "We'll remember this month" — falls short because busy weeks = skipped reminders = late cash.

## Differentiation
**Key differentiators:**
- ₹0 running cost (Sheets + Apps Script free tier + existing Gmail/WhatsApp)
- WhatsApp-first + Email-threaded per invoice (matches how Indian SMBs actually pay)
- Validation guardrails (duplicate/missing/overpayment colors) + every send logged with reason
- You own everything; 1-page SOP + Loom so a junior can run it
**How we do it differently:** Start from collections (highest ROI), ship in days on tools they already use, prove with 260+ logged sends — not slides.
**Why that's better:** Cash faster without new software, hires, or behavior change. Which means founders stop chasing and managers stop apologizing.
**Why customers choose us:** Live system proof (not a template sale) + fixed scope + handover that sticks.

## Objections
| Objection | Response |
|-----------|----------|
| Will free-tier Gmail/WhatsApp scale? | Yes to ~50–100 invoices/mo per account; daily batches inside 10:00–19:00 + failure log shows limits before they hurt. Above that we split senders or graduate to paid — you approve first. |
| Is our client data safe? | You own the Sheet/Drive/script; no third-party server; tokens in Script Properties, never in code; PII never in this public repo. |
| What if the script breaks? | 2-week fix window + SystemHealth checks + log makes debugging a 10-min read; SOP covers the 3 common failures (missing email, bad Drive link, paused toggle). |
| Can't we just buy Zoho? | You can — and I tell you when that's right (50+ staff, GST e-invoicing needs). For 5–30 retainers, this is faster and free to run. |

**Anti-persona:** Businesses wanting GST e-invoicing/compliance automation, 100+ invoices/mo needing SLAs, or teams unwilling to keep one Client Master clean.

## Switching Dynamics
**Push:** Late payments, month-end chasing stress, no visibility for the founder.
**Pull:** Live 260-send proof, ₹0 run cost, 3–7 day ship, junior-runnable SOP.
**Habit:** "Sheet + memory works fine" + fear of breaking what exists mid-month.
**Anxiety:** Will automation spam clients? (Answered: business-hours guard + per-invoice pause + threaded polite tone + test mode on demo client first.)

## Customer Language
**How they describe the problem:**
- "Chasing payments on WhatsApp"
- "No single view of who owes what"
- "Reminders depend on someone remembering"
**How they describe us:**
- "Reminders go themselves"
- "SOP + Loom so the team runs it"
**Words to use:** retainer, due date, overdue, audit log, handover, SOP, fixed scope, you own it.
**Words to avoid:** revolutionary, game-changing, seamless, robust, 10x, secret, guaranteed, cutting-edge.
**Glossary:**
| Term | Meaning |
|------|---------|
| Advance / Postpaid | Bill current month vs previous month |
| Pre-due / Overdue / Recurring | T-5/T-2 → grace → D+2/+5/+10 → every 7d |
| Collection Status | Paid / Overdue / Upcoming derived from TODAY() vs Due |

## Brand Voice
**Tone:** Direct, practical, founder-to-founder. No hype.
**Style:** Concrete, numbered, show-the-sheet. Short sentences mixed with specifics.
**Personality:** Operator, honest, helpful, calm, specific.

## Proof Points
**Metrics:** 260+ logged communications; 30-file Apps Script project; pre-due/overdue/recurring cadence running daily 10:00–19:00 Asia/Kolkata.
**Customers:** Indian digital marketing agency (SEO/SMM retainers) — names redacted in public repo; shared under NDA.
**Testimonials:** _Pending — using operator note until first quotable client line arrives (ask sent)._
> Operator note (live use, Sep 2026): 260+ logged sends across welcome, invoice, pre-due 1/2, overdue 1/2, and payment confirmations on Email + WhatsApp. Daily batches inside 10:00–19:00 Asia/Kolkata; single-address failures (e.g. missing email) logged with reason without breaking the batch. Client names and amounts redacted in public; full log shared with prospects under NDA.
**Value themes:**
| Theme | Proof |
|-------|-------|
| Paid faster, less chasing | Pre-due + overdue + recurring on two channels; failure log prevents silent drops |
| One true view | Client → Invoice → Payment → Log linked by CL/INV/PAY/LOG IDs |
| Junior-runnable | Validation colors + 1-page SOP + Loom + 2-week fixes |

## Goals
**Business goal:** 2–3 retainer-agency builds/quarter from this repo + Loom.
**Conversion action:** Book a 15-min flow-mapping call (email with subject "Map my collections").
**Current metrics:** Repo live; Loom pending; testimonials pending.

## Changelog
- v1 (2026-10-09) — Initial context auto-drafted from repo + portfolio PDF + invoicing dump.
