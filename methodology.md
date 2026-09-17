# BENNETTAI074 — Methodology

**Program:** BENNETTAI074 — Intertidal Harvest Planning (Bennett Coastal Harvest Intelligence)
**Owner:** Bennett AI Solutions Inc. · **Status:** Concept-stage · **Date:** 2026-09-17

---

## 1. Problem

Licensed gooseneck-barnacle (percebes) harvesters work one of the most dangerous seafood jobs documented in the reviewed literature, on wave-exposed rock under co-managed quotas and permits. Trip planning is informal: tide timing, site choice, permit rules, and harvest limits are held in the crew's head, often until the boat or the rock says otherwise. The result is dead trips, avoidable risk exposure, and pressure on the harvester side of the co-management bargain.

## 2. Method

BENNETTAI074 is a planning copilot. It combines four public rule sets — tide windows, site suitability, permit/site matrix, and a harvest limiter — into a single go/no-go harvest brief before a crew commits to a trip. The method deliberately stops at planning: it produces a reviewable brief for a qualified human. It is the scouting-and-planning layer only.

## 3. Rules (public, no hidden weights)

- **Tide window:** best low-tide exposure ≥ 2.5 h (sample threshold).
- **Swell:** significant wave height ≤ 1.5 m (Galicia sample) / ≤ 1.8 m (BC sample).
- **Site / permit matrix:** open / managed / restricted statuses; managed sites require the licensed or commercial permit.
- **Harvest limiter:** suggested take = min(planned, 80% × regional quota headroom).
- **Wind:** > 20 kn raises a caution flag.

Full tables live in `algorithm.html`.

## 4. Limitations

- **Sample rule sets:** quotas, site statuses, and tide values are illustrative for the demo. Real rules must be versioned from regulator sources (Xunta de Galicia cofradía management plans; DFO and co-managed fishery plans in BC) and re-verified per season.
- **Not field-validated:** density estimates, thresholds, and the 80% factor are hypotheses to test in the pilot, not measured results.
- **No safety function:** this tool is not a marine-safety assessment, a weather service, or a substitute for qualified judgment.
- **No legal function:** it does not grant, verify, or enforce permits or quotas.

## 5. Pilot design (draft)

- **Partners:** 1–2 licensed harvesting crews / one cofradía (Galicia) or one co-managed commercial fishery partner (BC).
- **Duration:** one harvest window (~2–4 months).
- **Scope:** 20–40 planned trips per crew.
- **Primary question:** does a structured pre-trip brief reduce dead trips and permit incidents without reducing legal harvest?
- **Measures:** dead-trip rate, planned-vs-actual records, permit-incident count, crew adoption and trust, limiter usefulness, willingness to continue or pay.
- **Decision rule:** continue (wider cohort), narrow (single region), redesign, or stop — on recorded measures, not impressions.

## 6. Confidentiality and data

No personal, crew, or location data is collected by the simulator; everything runs client-side. In a pilot, trip logs and permit records would be shared only under a written agreement, and only what the partner's regulator permits. No identifiable harvesting-location data would be published without consent.

## 7. Sources (accessed 2026-09-17)

| Fact | Source | Caveat |
|---|---|---|
| Percebes retail ≈ $200/lb | Browne Trading Co. product listing | US retail, not wholesale |
| "One of the most dangerous jobs"; deaths occur; Costa da Morte naming | VICE/Munchies 2015 percebeiro interview; Fine Dining Lovers; Food Insider | Qualitative, no verified death-count statistic |
| Galicia cofradía system; Xunta issues licenses and approves management plans | EDF Fishery Solutions Center, "Spanish Galicia Goose Barnacle Cofradía System" | English-language secondary source |
| BC limited commercial gooseneck fishery, co-managed; five First Nations co-manage small-scale fishery | SeaChoice 2015; SFU thesis etd21191 (2022) | Different regulatory regimes per area |
| Gooseneck barnacles susceptible to overharvest without adaptive management; Oregon stock ≈ 235,000 kg, ~2% harvest-size | Oregon Sea Grant ORESU-S-17-002 (2017); NOAA noaa_35095_DS1.pdf | Research context, not a market figure |
| No autonomous intertidal barnacle harvester identified in the reviewed landscape | Web review, September 2026 | Dated landscape finding — re-check before major publications |

*Concept-stage. No customers, revenue, deployments, pilots underway, patents, or validated outcomes claimed.*
