# Nepal Law Omni Skill for Claude Code

**Original Author:** Kishor Gartaula ([@thisiskishor](https://github.com/thisiskishor))  
**License:** MIT — Use freely, modify, and share with attribution (see [LICENSE](LICENSE) and [NOTICE.md](NOTICE.md) for details)

---

A Claude Code skill for comprehensive Nepali legal assistance across all areas of law. Covers civil, criminal, property, corporate, family, labour, and administrative law. Generates bilingual legal documents, court petitions, government filing blueprints, and procedure guides grounded in the Muluki Civil Code 2074, Muluki Criminal Code 2074, Companies Act 2063, and the full body of Nepali statutes.

---

## What's Included

A Claude Code skill that answers legal questions, drafts documents, and maps out government procedures across the entire spectrum of Nepali law.

**Handles:**
- Civil matters: contracts, property transactions, partition deeds, mortgages, loans, gifts (Daanpatra), wills
- Criminal matters: FIR drafting, offense classification, remand and bail rules, limitation periods
- Family law: marriage, divorce petitions (mutual consent and contested), adoption procedures, Will (Wasiyatnama)
- Property law: land sale deeds (Rajinama), Malpot transfer procedures, commercial and residential leases
- Corporate law: board resolutions, shareholders agreements, joint venture agreements, MoUs, franchise and agency agreements
- Labour law: employment termination letters, warning and show cause notices, disciplinary procedure chains
- Court documents: writ petitions (5 types), legal notices, settlement deeds (Milapatra), surety and guarantee bonds, Power of Attorney
- Government procedures: company registration, industrial registration, Malpot ownership transfer, trademark and IP registration, VAT registration, consumer tribunal complaints, foreign employment compliance

**Verification:** All outputs are cross-checked against live Nepal government sources at query time before being finalized. The skill includes a mandatory sweep for Nepal Acts Amendment Ordinance 2083 before citing any statute, since a single ordinance modified 20+ Acts.

---

## Status & Ongoing Development

**Nepal Law Omni is functional and covers the core of Nepali jurisprudence.** Built on the Muluki Civil Code 2074, Muluki Criminal Code 2074, Companies Act 2063, Labour Act 2074, FITTA 2075, and related statutes. Some section numbers are marked `[VERIFY]` where the live Gazette is the authoritative source.

**Current strengths:**
- Full civil and criminal code structural maps
- 23 legal document templates covering personal, commercial, and court use
- 6 government procedure guides with step-by-step filing instructions
- Bilingual drafting with Nepali legal terms (जाहेरी, मालपोत, अख्तियारनामा, रोहबर, etc.)
- Physical presence flags wherever Malpot or biometric presence is mandatory and online processing is unavailable

**Areas being expanded:**
- Additional court pleading formats for District and High Court matters
- Insurance and social security (SSF) procedure guides
- Intellectual property dispute resolution workflows

**Your contributions help!** If you find outdated provisions or want to add coverage, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Quick Start

### Installation

**Option A — Download as ZIP (easiest)**

1. Click the green **Code** button at the top
2. Click **Download ZIP**
3. Extract the ZIP
4. Copy the `nepal-law-omni` folder into your Claude skills directory:

**Mac/Linux:**
```bash
cp -r nepal-law-omni ~/.claude/skills/skills/legal/
```

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse nepal-law-omni "$env:USERPROFILE\.claude\skills\skills\legal\"
```

If the `legal` folder does not exist yet:
```bash
mkdir -p ~/.claude/skills/skills/legal
```

### Option B — Clone the repo

```bash
git clone https://github.com/thisiskishor/nepal-law-omni.git
cp -r nepal-law-omni ~/.claude/skills/skills/legal/
```

The skill loads automatically — no restart needed.

---

## How to Use

Once installed, invoke the skill with natural language or trigger phrases:

### Direct Commands
```
/omni-query "what are the grounds for divorce under Muluki Civil Code 2074?"
/omni-draft "land sale deed for property in Kathmandu"
/omni-procedure "how do I register a trademark in Nepal?"
```

### Trigger Phrases (activate automatically)
- "draft a [document] under Nepal law"
- "how do I file a FIR in Nepal?"
- "what are my inheritance rights under Nepal law?"
- "draft a shareholders agreement for a Nepal company"
- "explain the Malpot transfer process"
- "draft a writ petition to the Supreme Court of Nepal"
- Any question about Nepali civil, criminal, property, family, or corporate law

### Output Types

| Type | Command | What You Get |
|---|---|---|
| Legal Query | `/omni-query` | Plain-language explanation with statute citations |
| Document Draft | `/omni-draft` | Bilingual legal document ready for advocate review |
| Procedure Guide | `/omni-procedure` | Step-by-step government filing blueprint with office names and documents |

### Examples

**Legal Query**
```
User: "What happens to property when someone dies without a will in Nepal?"

Output: Explanation of intestate succession under Muluki Civil Code 2074, Part 4
- Priority order of heirs
- Compulsory share provisions
- Surviving spouse protections
- How adopted children are treated
- Limitation periods for partition claims
```

**Document Draft**
```
User: "Draft a Gift Deed (Daanpatra) for transferring land to my son in Nepal"

Output: Full bilingual Daanpatra template with:
- Nepali / English field names
- Kitta No., Lalpurja No., boundary table (चारकिल्ला)
- Donor declarations and Donee acceptance
- Witness clause (रोहबर)
- Malpot endorsement block
- Stamp duty rates table for family transfers
- Physical presence mandatory flag
```

**Procedure Guide**
```
User: "How do I transfer land ownership at Malpot in Nepal?"

Output: Step-by-step procedure covering:
- Pre-transfer checklist (6 steps)
- Documents required table
- Stamp duty rates by transaction type
- 35-day registration deadline warning
- Special situations (gift, inheritance, mortgage, PoA transfers)
- Common rejection reasons
- Physical presence mandatory flag at Malpot
```

---

## Risk Classification

Legal outputs include one of four status badges:

| Status | Meaning |
|---|---|
| COMPLIANT / CLEAR | Meets current legal requirements |
| PROCEDURAL LOCK | A court filing or government registration is required before proceeding |
| HIGH LIQUID RISK | Exposure to civil liability or regulatory action |
| CRIMINAL LIABILITY | Violation carries criminal penalties under Muluki Criminal Code 2074 |

---

## Files

```
.
├── README.md
├── SKILL.md                                        — Skill definition and verification protocol
└── references-omni/
    ├── codes/
    │   ├── muluki-civil-code-summary.md
    │   └── muluki-criminal-code-summary.md
    ├── templates/
    │   ├── land-sale-deed.md
    │   ├── commercial-lease-agreement.md
    │   ├── residential-lease.md
    │   ├── court-petition-writ.md
    │   ├── power-of-attorney.md
    │   ├── board-resolution.md
    │   ├── affidavit.md
    │   ├── shareholders-agreement.md
    │   ├── memorandum-of-understanding.md
    │   ├── legal-notice.md
    │   ├── will-wasiyatnama.md
    │   ├── loan-agreement.md
    │   ├── partition-deed.md
    │   ├── mortgage-deed.md
    │   ├── joint-venture-agreement.md
    │   ├── settlement-milapatra.md
    │   ├── termination-letter.md
    │   ├── warning-letter.md
    │   ├── surety-guarantee-bond.md
    │   ├── franchise-agreement.md
    │   ├── agency-agreement.md
    │   ├── fir-police-complaint.md
    │   ├── gift-deed-daanpatra.md
    │   ├── divorce-petition.md
    │   └── adoption-deed.md
    └── procedures/
        ├── industrial-registration.md
        ├── malpot-ownership-transfer.md
        ├── trademark-ip-registration.md
        ├── consumer-tribunal-complaint.md
        ├── vat-registration.md
        └── foreign-employment-compliance.md
```

---

## Authoritative Sources

The skill cross-references these sources at query time:

| Source | What it covers |
|---|---|
| rajpatra.dop.gov.np | Official Nepal Gazette — highest authority for all Acts |
| lawcommission.gov.np | Consolidated Acts, Regulations, and Codes |
| supremecourt.gov.np | Supreme Court rules and court procedures |
| ocr.gov.np | Company registration and corporate filings |
| dofe.gov.np | Foreign employment licensing and procedures |
| ird.gov.np | Tax, TDS, and VAT obligations |

---

## Who Benefits

- **Individuals** navigating property transfer, inheritance, family law, or personal legal disputes in Nepal
- **Business owners** needing commercial contracts, board resolutions, shareholder agreements, or JV structures
- **Advocates and legal professionals** needing bilingual drafting starting points for Nepal-jurisdiction documents
- **HR teams** handling Labour Act 2074 terminations, warning letters, and disciplinary procedures
- **Foreign nationals and investors** understanding Nepal's property, corporate, and investment laws
- **Workers going abroad** understanding their Foreign Employment Act 2064 rights and procedures

---

## Difference from Nepali Legalities Skill

This skill and [nepali-legalities](https://github.com/thisiskishor/nepali-legalities) are designed to work alongside each other without overlap:

| nepal-law-omni | nepali-legalities |
|---|---|
| Civil, criminal, property, family, corporate, labour | Digital platforms, SaaS, e-commerce, FinTech |
| General population, businesses of all types | Tech founders, digital product teams |
| Malpot, courts, government procedures | OCR, DoCSCP, NRB, IRD digital compliance |
| Muluki Civil Code, Criminal Code focus | E-Commerce Act 2081, Privacy Act 2075 focus |

---

## License & Attribution

This work is licensed under the MIT License with an **attribution requirement**.

If you modify and republish this skill, you must:
- Retain the copyright notice: "Copyright (c) 2026 Kishor Gartaula"
- Credit the original author and link to https://github.com/thisiskishor
- Clearly indicate what you modified
- Include the LICENSE file with your distribution

See [NOTICE.md](NOTICE.md) for full details.

**Original author:** [Kishor Gartaula](https://github.com/thisiskishor) — [kishorgartaula.com.np](https://www.kishorgartaula.com.np)

---

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Worth contributing:**
- Corrections to any section number or provision marked [VERIFY]
- New templates for areas not yet covered (insurance, healthcare, education sector)
- Court pleading formats for High Court or Supreme Court filings
- Real procedure outcomes or updated government fee schedules

---

## Support This Work

If you find Nepal Law Omni valuable, consider supporting the creator:

Ko-fi: https://ko-fi.com/thisiskishor  
Local Payment (ESewa | Khalti): https://www.kishorgartaula.com.np/buy-coffee

---

## Related Projects

- **[nepali-legalities](https://github.com/thisiskishor/nepali-legalities)** — Digital platform and SaaS legal compliance for Nepal
- **[nepali-writer](https://github.com/thisiskishor/nepali-writer)** — Native Nepali writing and translation skill
- **[code-recon](https://github.com/thisiskishor/code-recon)** — Codebase topology mapping before touching code
- **[code-brain](https://github.com/thisiskishor/code-brain)** — Persistent memory skill for project sessions

---

**Built for anyone who needs to understand, navigate, or draft documents under Nepali law**
