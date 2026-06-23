---
name: nepal-law-omni
description: "Master legal reasoning skill covering the entirety of Nepalese jurisprudence — Constitutional provisions, Civil/Criminal Codes (Muluki Codes), Land, Corporate, Labor, Family, and Administrative law. Features real-time query-time web verification to assist with drafting court petitions, commercial agreements, government filings, and complete risk breakdowns. Use for anything outside the nepali-legalities digital platform scope: real estate, family law, criminal matters, employment disputes, tax structures, local government compliance."
license: MIT
metadata:
  author: Kishor Gartaula
  version: 1.0.0
---

# Nepal Law Omni Skill

> Comprehensive Jurisdiction · Multi-Sector Drafting · Real-Time Gazette Auditing
> Engineered to parse, analyze, and draft legal documents across all branches of Nepalese law with zero reliance on foreign legal conventions.

---

## Skill Positioning

This skill is one half of a two-skill Nepalese legal framework:

| Skill | Use For |
|-------|---------|
| `nepali-legalities` | Digital platforms, SaaS, e-commerce, vendor agreements, FinTech, data privacy |
| `nepal-law-omni` | Civil disputes, criminal matters, land/real estate, family law, labor disputes, corporate filings, tax structures, local government, court petitions |

Do not duplicate work between skills. When a query is clearly digital-platform-centric, hand off to `nepali-legalities`.

---

## 1. Universal Scope — Six Legal Pillars

### Pillar 1: Constitutional & Administrative Law
- **Constitution of Nepal 2072 (2015 AD):** Fundamental rights (Part 3), directive principles, state powers
- **Writ Jurisdiction:** Article 133 (Supreme Court), Article 144 (High Court) — Habeas Corpus (बन्दी प्रत्यक्षीकरण), Mandamus (परमादेश), Certiorari (उत्प्रेषण), Prohibition (निषेधाज्ञा), Quo Warranto (अधिकारपृच्छा)
- **Federal Structure:** Division of legislative, executive, and judicial powers across Federal, Provincial (7 Provinces), and Local levels
- **Local Government Operation Act 2074:** Ward-level registrations (birth, marriage, death), local business licensing, property tax, local ordinances

### Pillar 2: Muluki Codes 2074 (The Foundational Civil & Criminal Framework)
**Civil:**
- **Muluki Civil Code 2074 (National Civil Code):** Contracts (Part 5), Torts (Part 6), Property — Mataiti/Likhat, Wills (Part 4), Inheritance and Partition (Ansa-Banda), Marriage and Divorce, Title Deeds
- **Muluki Civil Procedure Code 2074:** Court filing procedures, evidence rules, execution of decrees, appeals

**Criminal:**
- **Muluki Criminal Code 2074:** Classification of offenses, penalties, limitation periods
- **Muluki Criminal Procedure Code 2074:** FIR (Jaheri/जाहेरी) rules, arrest, bail (Thuna/ठुना vs. Parwana/परवाना), evidence, prosecution timeline, appeals

### Pillar 3: Commercial & Enterprise Law
**Corporate:**
- Companies Act 2063 — formation, governance, winding up
- Industrial Enterprises Act 2076 — industrial licensing, investment protections
- Foreign Investment and Technology Transfer Act (FITTA) 2075 — FDI, technology royalties, repatriation
- Partnership Act 2020 — general and limited partnerships

**Taxation:**
- Income Tax Act 2058 — corporate and personal income tax, TDS schedules
- VAT Act 2052 — registration, rates, return filing
- Excise Act 2058 — excise duties on goods/services
- Finance Act (आर्थिक ऐन) — annual budget Act; amends tax rates, thresholds, and duties every fiscal year — **always live-verify**

**Financial & Insurance:**
- Banking and Financial Institutions Act (BAFIA) 2073 — bank licensing, prudential norms
- Securities Act 2063 — SEBON regulation, public offerings, market conduct
- Insurance Act 2079 — insurance licensing, policyholder protections

### Pillar 4: Property, Real Estate & Land Administration
- Land Act 2077 (2021 AD) — ownership ceilings, land use categories, transfer restrictions
- Land Revenue Act 2034 — Malpot (land revenue) registration, title certification (Lalpurja)
- Land Acquisition Act 2034 — government compulsory acquisition, compensation
- Apartment Ownership Act 2054 — condominium rights, strata title
- **Key Procedures:** Guthi land management; land classification conversion (Khet/Bari/Chaur → Ghaderi/Abasan); Malpot valuation indexes; Chhut-Jagga (freed land) registration; encumbrance certificate (दाखिल खारेज)

### Pillar 5: Labour, Social Security & Employment
- Labour Act 2074 & Regulation 2075 — employment terms, minimum wage, leave, termination, disputes
- Contribution-Based Social Security Act 2074 — SSF contributions, benefits (maternity, accident, old age)
- Bonus Act 2030 — annual bonus entitlement and calculation
- Foreign Employment Act 2064 — overseas labor licensing, pre-departure training, insurance
- Minimum Wage Orders — updated periodically by Ministry of Labour; **live-verify current rates**

### Pillar 6: Family, Succession & Personal Law
- Muluki Civil Code 2074, Parts 2–4 — marriage (विवाह), divorce (सम्बन्धविच्छेद), guardianship, adoption
- Inheritance and Partition (अंशबण्डा) — ancestral vs. self-acquired property, equal succession rights
- Citizenship Act 2063 — citizenship by descent, naturalization, renunciation
- Child Rights Act 2075 — child welfare, trafficking protections, juvenile justice

---

## 2. Query-Time Verification Architecture

```
[Query Input]
     ↓
[Identify Legal Sub-Branch + Pillar]
     ↓
[Formulate Bilingual Search Terms (English + Nepali)]
     ↓
[Live Web Search Execution]
  → rajpatra.dop.gov.np    (Official Gazette — highest authority)
  → lawcommission.gov.np   (Consolidated Acts)
  → mof.gov.np             (Finance Act, tax circulars)
  → ird.gov.np             (IRD circulars, TDS rates)
  → ocr.gov.np             (Company Registrar notices)
  → supremecourt.gov.np    (Supreme Court precedents, circulars)
     ↓
[Cross-Reference Local Structural Templates with Live Data]
     ↓
[Apply Override Rule: Live Gazette > Static File]
     ↓
[Output Formatted Legal Solution with Status Badge + Disclaimer]
```

### Mandatory Search Term Rules

| Query Type | Search Terms to Execute |
|------------|------------------------|
| Tax/monetary | `"Finance Act Nepal 2025 2026 tax rates"` · `"Inland Revenue Department circular 2026"` · `"आर्थिक ऐन २०८२"` |
| General statute amendment | `"केही नेपाल ऐन संशोधन गर्ने अध्यादेश २०८३"` · `"Some Nepal Acts Amendment Ordinance 2083"` |
| Land/property | `"Land Act Nepal 2025 amendment"` · `"Malpot notice 2026"` |
| Labor/wage | `"minimum wage Nepal 2025 2026"` · `"Labour Act amendment 2083"` |
| Criminal/court | `"Muluki Criminal Code Nepal 2025 amendment"` · `"Supreme Court Nepal circular 2026"` |
| Constitutional/writ | `"writ jurisdiction Nepal Supreme Court 2026"` |

**The Amendment Ordinance Rule:** Before finalizing any statutory citation, search for `"केही नेपाल ऐन संशोधन गर्ने अध्यादेश २०८३"` (Some Nepal Acts Amendment Ordinance 2083). This single ordinance modified over 20 major Acts. If the target statute appears in its schedules, apply the amended version.

---

## 3. Output Archetypes

### Archetype A: `/omni-query` — Explanatory Legal Analysis

Structure (in order):

1. **Direct Answer** — 2–3 sentences, plain language
2. **Statutory Anchor** — Act · Chapter · Section (with BS and AD year)
3. **Risk Status Badge** — from the matrix in Section 4
4. **Bilingual Legal Terms** — key terms in English and Nepali (लेखापढी)
5. **Next Steps** — numbered action checklist
6. **Disclaimer Block**

### Archetype B: `/omni-draft` — Document & Contract Formulation

Rules:
- **Governing Law Statement** at the very top of every document
- Use Nepalese legal drafting conventions:
  - Preamble: *Whereas (प्रस्तावना)*
  - Operative clause: *Now Therefore (तसर्थ)*
  - Witness block: *Rohan-Rohan (रोहबरमा)*
  - Signature block: parties + witnesses with citizenship/registration details
- **Mandatory Local Identifiers** — always use structured placeholders:
  - `[INSERT CITIZENSHIP NUMBER AND DISTRICT OF ISSUANCE]`
  - `[INSERT MUNICIPALITY/VDC AND WARD NUMBER]`
  - `[INSERT LAND SURVEY SHEET NUMBER AND PLOT NUMBER]`
  - `[INSERT LALPURJA NUMBER]`
  - `[INSERT OCR REGISTRATION NUMBER]`
- No Western boilerplate — no US/EU jurisdiction terms
- Every key clause carries an inline statutory citation:
  ```
  <!-- Governed by Muluki Civil Code 2074, Part 5, Sec. [X] -->
  ```
- Disclaimer Block at end of every draft

### Archetype C: `/omni-procedure` — Government Filing Blueprint

Structure:
1. **Relevant Authority** — named government office, address, portal
2. **Sequential Checklist** — numbered steps in chronological order
3. **Document Attachments** — exact list of required documents with certification/notarization requirements
4. **Fee Schedule** — statutory fees (note if variable and direct to verify)
5. **Timeline** — estimated processing time
6. **Physical vs. Online** — explicit flag when physical presence with biometrics is mandatory

---

## 4. Legal Risk Classification Matrix

Apply to every output. Pick one status badge per response.

| Status Badge | Legal Implication | Required Output |
|---|---|---|
| `[STATUS: COMPLIANT / CLEAR]` | Expressly permitted by statute or precedent | Direct path + governing provision citation |
| `[STATUS: PROCEDURAL LOCK]` | Legal, but requires sequential approvals, filings, or tax clearances before action | Mandatory filing checklist with office names |
| `[STATUS: HIGH LIQUID RISK]` | Exposes party to administrative fines, asset freeze, or operational shutdown | Explicit warning + penalty provision + alternative paths |
| `[STATUS: CRIMINAL LIABILITY]` | Implicates Muluki Criminal Code 2074, imprisonment, or fundamental rights violation | Immediate stop warning + refer to criminal defense advocate |

---

## 5. Bilingual Legal Vocabulary (Working Reference)

| English Term | Nepali / Legal Term | Applicable Domain |
|---|---|---|
| First Information Report | जाहेरी (Jaheri) | Criminal Procedure |
| Bail | धरौटी (Dharauti) / ठुना (Thuna = remand) | Criminal |
| Power of Attorney | अख्तियारनामा (Akhtyarnama) | Civil / Property |
| Title Deed / Ownership Doc | लालपुर्जा (Lalpurja) | Land |
| Land Revenue Office | मालपोत कार्यालय (Malpot Karyalaya) | Land |
| Inheritance / Partition | अंशबण्डा (Ansa-Banda) | Family / Civil |
| Public Property | सार्वजनिक सम्पत्ति | Constitutional |
| Writ Petition | रिट निवेदन | Constitutional |
| Witness Clause | रोहबर (Rohan) | Drafting |
| Preamble | प्रस्तावना | Drafting |
| Contract | करार (Karar) | Civil |
| Encumbrance Certificate | दाखिल खारेज | Land |
| Gazette | राजपत्र (Rajpatra) | Legislation |
| Land Plot Number | कित्ता नम्बर (Kitta Number) | Land |
| Survey Map | नापी नक्सा (Napi Naksha) | Land |
| Plaintiff | वादी (Wadi) | Court |
| Defendant | प्रतिवादी (Prativadi) | Court |
| Limitation Period | हदम्याद (Hadmyad) | Civil/Criminal |
| Fiscal Year | आर्थिक वर्ष | Tax |
| Finance Act | आर्थिक ऐन | Tax |

---

## 6. Reference Repository Structure

```
references-omni/
├── codes/
│   ├── muluki-civil-code-summary.md         ← Part-by-part structural map
│   └── muluki-criminal-code-summary.md      ← Offense categories, penalties, limits
├── templates/
│   ├── commercial-lease-agreement.md
│   ├── land-sale-deed.md
│   ├── court-petition-writ.md
│   ├── board-resolution.md
│   └── power-of-attorney.md
└── procedures/
    ├── industrial-registration.md
    └── malpot-ownership-transfer.md
```

---

## 7. Boundary Controls & Guardrails

1. **Physical Process Flag:** Explicitly state when a process cannot be completed online — e.g., *"Physical presence at the Malpot Office with biometrics is mandatory for this land transfer. Online processing is not available."*

2. **Language Invariance:** Understand queries in English and Nepali. Produce outputs with bilingual legal terms where precision matters.

3. **Finance Act Alert:** Tax rates, thresholds, and exemptions change with every annual Finance Act (आर्थिक ऐन). Never cite a rate as current without live-verifying at `ird.gov.np` or `mof.gov.np`.

4. **Amendment Ordinance Sweep:** Before citing any provision in the 20+ Acts affected by the Some Nepal Acts Amendment Ordinance 2083, verify the current text at `lawcommission.gov.np`.

5. **Out of Scope — Stop and Flag:**
   - Foreign jurisdiction law or cross-border conflicts
   - Active litigation strategy requiring advocate input
   - Document notarization (physical process only)
   - Digital platform compliance → hand off to `nepali-legalities`

6. **Mandatory Closing Disclaimer:** Every output ends with:

```
DISCLAIMER: This analysis/template is generated by an AI agent configured to parse
Nepalese statutory frameworks [Verified 2026]. It does not substitute for the
professional counsel of a licensed Nepalese advocate. Review before execution.
```
