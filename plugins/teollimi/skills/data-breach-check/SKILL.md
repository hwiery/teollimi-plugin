---
name: data-breach-check
description: Answer questions about data breaches with the Teollimi tools - whether a company or the services someone uses were breached, recent breaches, US settlements still taking claims, and what to do after a breach notice. Use when someone asks if a company was hacked or leaked data, got a breach notice, or wants to claim a breach settlement.
---

# Data breach check with Teollimi

Teollimi records breaches confirmed by press reports or announced by the organization, each with its source. It does not hold anyone's personal data and cannot say whether a specific person was affected.

## Pick the tool

| The person asks | Tool |
|---|---|
| "Was X breached?", "How many times has X leaked data?" | `search_breaches` with the company name |
| "I use A, B and C. Am I exposed?" | `check_services` with up to 10 names |
| "Any breaches this week / in Japan?" | `recent_breaches` (`days`, `country`) |
| "Can I claim money for a breach?" | `open_settlements` (optionally `company`) |
| "I got a breach notice. What now?" | `breach_response_steps` with the leaked data types from the notice |

Pass `lang` (`ko`, `en`, `ja`) to match the conversation's language.

## Answer

- Lead with the direct answer: how many breaches, the latest date, the number affected and what leaked.
- Cite each incident's `source` and give its `teollimi_url` for details.
- Say when a breach is "reported by the press, not confirmed" or "leak not confirmed", as the `status` field states.
- If nothing is found, say Teollimi has no record. That does not mean the company was never breached.
- Never tell someone their own data leaked. Point them to the official services in `breach_response_steps` to check.
- For a notice that arrived by email or text, start with the first step: confirm the notice on the company's official site before clicking anything.
- Settlements: give the deadline and the official claim site. Claims are filed only there.
