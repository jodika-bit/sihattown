# SihatTown — Team NADI Nexus

**The health pulse of tomorrow's township.**
Sime Darby Property University Hackathon 2026 · Theme: PEOPLE (community wellbeing, healthy lifestyles)

SihatTown connects home blood-pressure monitoring to the township itself. When a resident's readings drift, the township responds with nearby activities, the family gets a clear alert, a partner clinic gets a short summary, and the township operator sees only anonymous precinct trends that guide planning.

## Run it
**Live demo:** https://jodika-bit.github.io/sihattown/

Or open `index.html` in any modern browser. No build step, no server, no install.
To host: enable GitHub Pages on this repository (Settings → Pages → Deploy from branch → `main` / root).

## Demo journey (8 steps)
1. **Meet Pak Rahman** — 62, lives alone in Precinct C, managing hypertension.
2. **Morning reading at home** — simulated Bluetooth cuff sends 146/93 mmHg.
3. **SihatTown spots the trend** — 3-day average above the 135/85 home target → Amber.
4. **Community prescription** — shaded walking group and free screening day nearby; Mata Sihat points.
5. **Family stays in the loop** — caregiver alert to his daughter, with consent.
6. **The next morning** — third high reading in a row → automatic clinic referral.
7. **Clinic follow-up** — partner clinic sees a 7-day summary and books a teleconsult.
8. **The township learns** — anonymised precinct dashboard and a planning recommendation.

You can also enter any reading (try 186/114) to see the urgent (Red) flow, switch the resident app between English and Bahasa Melayu, and turn each consent on or off.

## Risk engine (rule-based, transparent)
| Level | Rule |
|---|---|
| Red | Latest reading ≥180 systolic or ≥110 diastolic, or red-flag symptoms reported |
| Amber | 3-reading average ≥135/85, or 2+ consecutive readings ≥135/85 |
| Green | Otherwise |
| Clinic referral | Red, or 3+ consecutive readings ≥135/85 (only with resident consent) |

Thresholds use the 135/85 mmHg home-reading threshold from the Malaysian hypertension clinical practice guideline. Final rules would be set with the clinical partner. SihatTown is a wellness and escalation tool, not a diagnostic device.

## Privacy by design
- Consent per recipient (caregiver, clinic, township insights), revocable any time.
- The township dashboard receives counts only; groups under 10 residents are suppressed.
- Designed for Malaysia's Personal Data Protection Act 2010.

## Tech
Single-file HTML, CSS and vanilla JavaScript. All data is simulated in the browser. Production path: device SDKs over Bluetooth → mobile app → secure cloud API → clinic integration and aggregated analytics.

## Team
**NADI Nexus**
- Johanes Dedi Kanchau (Team Leader) — UiTM, PhD Medicine
- Dr. NoorHasmirah — UNIMAS, Cognitive Sciences & Human Development
- Dr. Iman Nabilah — UiTM, PhD Medicine
- Dr. Nashuha Omar — PhD Biomedical Engineering
- Tabisco George — Kinabalu Commercial College, Accounting
