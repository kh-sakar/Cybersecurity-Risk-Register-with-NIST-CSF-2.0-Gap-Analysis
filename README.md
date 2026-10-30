# Cybersecurity Risk Register with NIST CSF 2.0 Gap Analysis

An Excel assessment of a fictional US-based dental clinic (BrightPath Dental, 40 staff, one location). It scores the clinic against selected NIST CSF 2.0 outcomes, then records the cyber risks those gaps create, rates them, and shows the expected residual risk after treatment.

All data is fictional and the scores are illustrative.

![Current vs target maturity](screenshot.png)

## What it covers
- 26 selected NIST CSF 2.0 outcomes across all six functions (Govern, Identify, Protect, Detect, Respond, Recover). This is not the full framework.
- Current and target scores with the evidence and reasoning behind each rating
- A ranked list of gaps (Gap x Impact)
- 10 cyber risks scored by likelihood and impact, with treatment, planned action, owner, due date, and status
- Residual risk after the planned action is complete
- A link from each risk to the CSF outcome and gap behind it
- A radar chart of current vs target maturity by function

## Files
```
risk-register/
├── README.md
├── risk_register_nist_csf_gap_analysis.xlsx
└── screenshot.png
```

| Sheet | Contents |
|---|---|
| Assessment Info | Date, scope, framework coverage, method, evidence sources, assumptions, limitations |
| Risk Register | 10 risks with inherent and residual ratings, linked to CSF outcomes |
| Gap Assessment | 26 outcomes with current state, evidence, scores, priority, and recommended action |
| Gap Summary | Averages by CSF function and the radar chart |
| Scales | Likelihood, impact, and maturity scales; thresholds; risk counts |

## Method
- **Maturity score (0 to 4):** my own scale (0 not implemented, 1 initial, 2 partial, 3 defined, 4 managed). NIST CSF is outcome-based and does not define maturity levels, so this is not a NIST scale.
- **Gap priority:** Gap (target minus current) x Impact (1 to 5).
- **Risk score:** Likelihood (1 to 5) x Impact (1 to 5).
- **Levels:** High is 12 or more, Medium is 6 to 11, Low is below 6.
- **Residual risk:** the same scales, applied to the expected likelihood and impact once the planned action is done.

I set High at 12 so that a risk needs both a realistic chance of happening and a serious impact to reach it (for example, likelihood 3 and impact 4). A rare but severe risk (2 x 5 = 10) lands in Medium. The same thresholds are used for risks and for gap priorities.

## Sample results
- Inherent risk: 7 High, 2 Medium, 1 Low
- Residual risk: 0 High, 2 Medium, 8 Low
- Average current maturity 0.7 against a target of 2.8
- Largest average gaps: Respond (2.7), Identify (2.5), and Recover (2.3), mainly because there is no incident response or recovery plan
- The two Medium residual risks (phishing and a vendor breach) would need further treatment or a written acceptance by the owner

## Limitations
- One fictional company and one assessor, so the scores are subjective
- Qualitative scoring, with no technical testing or scanning
- A selected subset of CSF outcomes, with shortened wording
- Evidence is fictional

## Possible next steps
- Map the outcomes to ISO 27001 Annex A controls
- Add a risk heat map
- Track risk status and residual scores over time

## Source
NIST Cybersecurity Framework 2.0: https://www.nist.gov/cyberframework
