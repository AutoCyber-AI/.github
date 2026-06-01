<!-- AutoCyber AI - GitHub Organisation Profile -->
<!-- autocyberai.com · crprotocol.io · comply.crprotocol.io -->

<div align="center">

<br/>

# AutoCyber AI

### Secure, Local-First AI Products · Built for Compliance, Cybersecurity & Productivity

[![Website](https://img.shields.io/badge/autocyberai.com-0f172a?style=flat-square&logo=safari&logoColor=white)](https://www.autocyberai.com)
[![CRP Protocol](https://img.shields.io/badge/CRP%20v3.0-open%20standard-7c6ef5?style=flat-square)](https://crprotocol.io)
[![PyPI](https://img.shields.io/pypi/v/crprotocol?label=pip%20install%20crprotocol&color=d4e600&style=flat-square)](https://pypi.org/project/crprotocol/)
[![IETF](https://img.shields.io/badge/IETF-3%20Internet--Drafts-f5a623?style=flat-square)](https://datatracker.ietf.org/doc/draft-vidiniotis-crp-headers/)
[![EU AI Act](https://img.shields.io/badge/EU%20AI%20Act-33%2F35%20controls-4fa8ff?style=flat-square)](https://crprotocol.io/compliance/eu-ai-act/)
[![ISO 42001](https://img.shields.io/badge/ISO%2042001-aligned-3dda84?style=flat-square)](https://crprotocol.io/compliance/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-AutoCyber%20AI-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/company/autocyberai)

<br/>

**We build AI systems that are secure by design, run locally, and scale across industries.**  
*From cybersecurity and compliance to voice agents, automation, and network protection.*

[**autocyberai.com**](https://www.autocyberai.com) &nbsp;·&nbsp; [**Our Products**](https://www.autocyberai.com/products) &nbsp;·&nbsp; [**CRP Protocol**](https://crprotocol.io) &nbsp;·&nbsp; [**Contact Us**](https://www.autocyberai.com/contact)

</div>

---

## Who We Are

AutoCyber AI Pty Ltd is a Sydney, Australia–based AI company specialising in **secure, local-first AI** for cybersecurity, compliance, and enterprise productivity. We believe the future of AI isn't in someone else's cloud - it's on your infrastructure, under your control, governed by your rules.

> *"Most AI vendors ask you to trust their cloud. We don't."*

Everything we ship is built around four non-negotiables: **security by design**, **local-first deployment**, **verifiable compliance**, and **full data sovereignty**. Our products run on your infrastructure - no hidden telemetry, no data resale, no vendor lock-in. Offline and air-gapped deployments supported.

---

## Our Products

### 🔐 Security & Cybersecurity

#### WASA AI - *Out Now*
The first truly agentic security platform. An AI co-pilot that actively works alongside security professionals to discover vulnerabilities, analyse threats, and generate actionable intelligence. 150+ security tools orchestrated as one. Autonomous vulnerability scanning. Compliance-ready reports aligned with NIST, OWASP, and MITRE ATT&CK.

→ [autocyberai.com/products/wasa-ai](https://www.autocyberai.com/products/wasa-ai)

#### NAD AI - *New*
Network anomaly detection and intrusion response. Local-first, real-time threat intelligence.

→ [autocyberai.com/products/nad-ai](https://www.autocyberai.com/products/nad-ai)

#### Spark AI - *New*
AI-powered productivity and automation for security-conscious teams.

→ [autocyberai.com/products/spark-ai](https://www.autocyberai.com/products/spark-ai)

#### SecureEasy AI - *Coming Soon*
Cybersecurity made simple. No IT expertise required. Enterprise-level protection in plain language - one-click fixes, virtual security team for non-technical users.

→ [autocyberai.com/products/secure-easy](https://www.autocyberai.com/products/secure-easy)

---

### ⚖️ Compliance & AI Governance

#### CRP Comply - *Live*
Automated EU AI Act, ISO 42001, GDPR, and NIST AI RMF compliance. Change one URL - every LLM call is automatically PII-scanned, risk-classified, and written to a tamper-evident audit trail. Generate FRIA, DPIA, and Technical Documentation from live protocol data - not questionnaires. Bring your own LLM key.

→ [comply.crprotocol.io](https://comply.crprotocol.io)

#### CRP Scan - *In Development*
GitHub Action for AI governance scanning. Finds ungoverned AI calls in your codebase, shows exactly what safety headers are missing, and links every finding to CRP Comply for remediation.

→ [crprotocol.io/products/scan](https://crprotocol.io/products/scan/)

#### CRP Gateway - *Coming Soon*
Managed hosted AI safety infrastructure. One endpoint change. All 58 safety headers. LLM key vault. Automatic compliance feed. Provider failover.

→ [crprotocol.io/products/gateway](https://crprotocol.io/products/gateway/)

---

## 🌐 Our Biggest Achievement: Context Relay Protocol™ (CRP)

AutoCyber AI is the author and maintainer of **Context Relay Protocol™ (CRP) v3.0** - an open HTTP-header standard for AI safety, context governance, and compliance evidence. CRP is the technical foundation that all of our AI governance products are built on.

```
┌────────────────────────────────────────────────────┐
│  A2A  - Agent-to-Agent Communication               │
├────────────────────────────────────────────────────┤
│  MCP  - Model Context Protocol (Tools)             │
├────────────────────────────────────────────────────┤
│  CRP  - Context Relay Protocol  ◀  AutoCyber AI    │
│         Context · Safety · Compliance · Provenance  │
└────────────────────────────────────────────────────┘
```

MCP gives agents tools. A2A lets agents communicate. **CRP governs every underlying AI call** - with verifiable safety signals, cryptographic provenance, and automated compliance evidence on every response.

### What CRP Does

**One endpoint change. Zero application code changes. Full governance.**

```python
# Before - ungoverned OpenAI call
from openai import OpenAI
client = OpenAI(api_key="sk-...")

# After - full CRP governance, same SDK
from openai import OpenAI
client = OpenAI(
    api_key="crp_gw_...",
    base_url="https://gateway.crprotocol.io/v1"
)
# Every response now carries 58 CRP safety headers.
# Comply receives the audit event automatically.
# Safety Policy enforced at the gateway layer.
```

Or use the SDK directly:

```bash
pip install crprotocol[full]
```

```python
import crp

client = crp.Client(model="gpt-4o-mini")
client.ingest("Your domain knowledge here...")

output, report = client.dispatch(
    system_prompt="You are a senior analyst.",
    task_input="Write a comprehensive compliance report.",
)

print(f"Words:   {len(output.split()):,}")       # 6,993 vs 592 without CRP
print(f"Quality: {report.quality_tier}")         # A
print(f"Risk:    {report.hallucination_risk}")   # LOW
print(f"HMAC:    {report.hmac[:16]}…")           # sha256:4fa8e921…
```

### The Numbers

| Metric | Result |
|--------|--------|
| Content output vs baseline | **11.8×** more |
| Safety headers per response | **58** |
| EU AI Act controls covered | **33 / 35** |
| DPE pipeline overhead | **< 50 ms** |
| Throughput loss | **0%** (4.9 words/sec) |
| Tests passing | **1,537** |
| IETF Internet-Drafts | **3 submitted** |

### What's in a CRP Response

```http
HTTP/1.1 200 OK
CRP-Safety-Hallucination-Risk: LOW
CRP-Safety-Hallucination-Score: 0.14
CRP-Safety-Attribution: CONTEXT_GROUNDED
CRP-Safety-Grounding-Pct: 0.912
CRP-Provenance-HMAC: sha256:4fa8e921abcd...
CRP-Provenance-Chain-Integrity: VALID
CRP-Compliance-EU-AI-Act: LIMITED
CRP-Compliance-GDPR-PII: false
CRP-Compliance-Audit-Trail-URI: https://comply.crprotocol.io/t/7fa3bc
CRP-Compliance-Controls-Met: 33/35
CRP-Context-Quality-Tier: A
CRP-Context-Saturation: 0.994
CRP-Agent-Safety-Budget: 0.78
CRP-Context-Protocol-Version: 3.0.0
```

Every header is readable by any proxy, WAF, SIEM, or middleware in the stack - no SDK required to act on them.

### CRP Regulatory Coverage

| Framework | Coverage |
|-----------|----------|
| **EU AI Act** (Regulation 2024/1689) | 33 / 35 controls · enforcement Aug 2026 |
| **GDPR** (Regulation 2016/679) | Art. 5, 17, 22, 25, 32, 35, 44 |
| **ISO/IEC 42001:2023** | AI Management Systems - Annex A controls |
| **NIST AI RMF 1.0** | GOVERN, MAP, MEASURE, MANAGE |
| **SOC 2 Type II** | CC6, CC7, CC8, CC9 |
| **Australian AI Ethics Framework** | All 8 principles |

### CRP Standards Track

Three Internet-Drafts submitted to the IETF for standardisation:

| Draft | Scope |
|-------|-------|
| [`draft-vidiniotis-crp-core`](https://datatracker.ietf.org/doc/draft-vidiniotis-crp-core/) | Core protocol, axioms, architecture, conformance |
| [`draft-vidiniotis-crp-headers`](https://datatracker.ietf.org/doc/draft-vidiniotis-crp-headers/) | 58 HTTP header field definitions (ABNF grammar) |
| [`draft-vidiniotis-crp-spec-006-safety-policy`](https://datatracker.ietf.org/doc/draft-vidiniotis-crp-spec-006-safety-policy/) | Safety Policy directive language |

**IANA** - HTTP Field Name registry registration in progress. Designated expert confirmed: *"Publication on the Independent Stream is sufficient."* Independent Submission to ISE (Eliot Lear) in progress.

**IEEE SA** - PAR (Project Authorisation Request) in preparation, targeting the AIS (Autonomous and Intelligent Systems) committee.

**ISO/IEC JTC 1/SC 42** - New Work Item in preparation via Standards Australia, as companion standard to ISO 42001.

→ [Full standards track](https://crprotocol.io/standards/)
→ [17 formal specification documents](https://crprotocol.io/spec/)

---

## Why Local-First?

| The Cloud AI Approach | The AutoCyber AI Approach |
|----------------------|--------------------------|
| Data sent to external servers | Data stays on your infrastructure |
| Privacy concerns | Privacy by design |
| Unpredictable costs | Predictable, controlled costs |
| Vendor lock-in | Full ownership |
| Black-box compliance | Verifiable, auditable controls |
| Offline: ✗ | Air-gapped deployment: ✓ |

We're built for environments where **failure isn't an option** - enterprises, regulated organisations, government, critical infrastructure, healthcare, and defence.

---

## Our Principles

We align everything we ship with:

- **ISO/IEC 27001:2022** - Information Security Management
- **ISO/IEC 42001:2023** - AI Management Systems
- **EU AI Act** (Regulation 2024/1689)
- **NIST AI RMF 1.0**
- **OWASP Top 10 (2025)**
- **Australian Privacy Principles**

---

## Get in Touch

<div align="center">

| | |
|---|---|
| 🌐 **Company** | [autocyberai.com](https://www.autocyberai.com) |
| 🔬 **CRP Protocol** | [crprotocol.io](https://crprotocol.io) |
| ⚖️ **CRP Comply** | [comply.crprotocol.io](https://comply.crprotocol.io) |
| 📦 **PyPI** | `pip install crprotocol` |
| 💼 **LinkedIn** | [linkedin.com/company/autocyberai](https://www.linkedin.com/company/autocyberai) |
| 🐦 **X / Twitter** | [@autocyberai](https://twitter.com/autocyberai) |
| 📧 **General** | contact@autocyberai.com |
| 🔐 **Security** | security@autocyberai.com |
| 🤝 **AI Governance** | ai-governance@autocyberai.com |
| 📡 **Standards** | standards@crprotocol.io |

</div>

---

<div align="center">

**AutoCyber AI Pty Ltd** · ABN 22 697 087 166 · Sydney, Australia  
Founded by [Constantinos Vidiniotis](https://www.linkedin.com/in/constantinos-vidiniotis)

*"Context Relay Protocol", "CRP", "CRP Comply", "CRP Gateway", "CRP Scan", and "CRP Visualise" are trademarks of Constantinos Vidiniotis / AutoCyber AI Pty Ltd.*

© 2025–2026 AutoCyber AI Pty Ltd · All rights reserved.

</div>
