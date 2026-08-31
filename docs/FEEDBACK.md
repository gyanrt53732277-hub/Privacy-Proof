# ProofFolio Preprod Feedback Loop

Collection window: 20–26 August 2026. Source: [submitted feedback export](../README.md#feedback-loop). Duplicate submissions were retained in the source export; onboarding counts use unique wallet addresses.

## What users said

- Privacy and selective disclosure were strongest themes: users liked proving a claim without sharing a transcript.
- Wallet safety needed stronger guidance: users asked for an address example and a clear seed-phrase warning.
- Users wanted clearer completion states, mobile spacing, a final review step, and simpler ZK language.
- Revocation and expiry needed plain-language explanations.
- Employer users asked for clearer verification outcomes and a failed-verification example.

## What changed

| Feedback theme | Product change | Evidence |
| --- | --- | --- |
| Wallet field format unclear | Added `mn_addr_preprod1…` example and public-address-only guidance to issuer onboarding. | [University application](../frontend/app/university/apply/page.tsx) |
| Seed phrase safety | Added visible “Never enter a seed phrase or private key” warnings on student and issuer flows. | [Student portal](../frontend/app/student/page.tsx), [University application](../frontend/app/university/apply/page.tsx) |
| ZK explanation too technical | Added plain-language explanation: employer confirms claim without receiving name, transcript, or secret key. | [Student portal](../frontend/app/student/page.tsx) |
| Final review requested | Added review panel listing disclosed claims and credential validity date before submission. | [Student portal](../frontend/app/student/page.tsx) |
| Success confirmation too subtle | Changed completion state to “Proof submitted successfully” and added explorer link. | [Student portal](../frontend/app/student/page.tsx) |
| Revocation and expiry unclear | Added explicit pre-submit and employer guidance that revoked or expired credentials cannot produce a valid proof. | [Student portal](../frontend/app/student/page.tsx), [Employer portal](../frontend/app/employer/page.tsx) |
| Employer outcome unclear | Added “Verification passed” / “Verification failed” labels around result messages. | [Employer portal](../frontend/app/employer/page.tsx) |
| Selective disclosure wording | Updated landing-page employer step to describe selected claims, not broad institution data. | [Landing page](../frontend/app/page.tsx) |

## Collection notes

The attached feedback export contains 52 submissions from 50 unique `mn_addr_preprod` wallet addresses. Two submissions share Mohammad Faizan’s wallet and were kept as separate feedback events. The canonical unique-user table is [USERS.md](USERS.md).

