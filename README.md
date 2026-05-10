# 🔴 AI Model Red Teaming Framework

> Actively red team LLM endpoints across 5 attack categories, 25 probes, mapped to MITRE ATLAS v4.5.2, OWASP LLM Top 10 2025, NIST AI RMF 1.0, EU AI Act, and ISO/IEC 42001.

**Developed by Tirthankar Dutta — AIShield Labs**
`github.com/aishieldlabs/ai-redteam-framework`

---

## What it does

The AI Model Red Teaming Framework runs structured adversarial probes against any LLM endpoint and generates a comprehensive dark-mode HTML report with risk scoring, framework mappings, and response analysis.

Unlike passive checklists, this tool **actively attacks** your model and tells you exactly where it is vulnerable.

---

## Attack categories

| ID | Category | OWASP | Probes |
|---|---|---|---|
| PI | Prompt Injection & Jailbreaking | LLM01:2025 | 5 |
| AE | Adversarial Inputs & Evasion | LLM07:2025 | 5 |
| ME | Model Extraction & Inversion | LLM10:2025 | 5 |
| BT | Bias & Toxicity Probing | LLM09:2025 | 5 |
| MT | Multi-turn Manipulation | LLM01:2025 | 5 |

**Total: 25 probes across 5 attack categories**

---

## Framework coverage

- **MITRE ATLAS v4.5.2** — 12 techniques mapped across all categories
- **OWASP LLM Top 10 2025** — Full coverage
- **NIST AI RMF 1.0** — Controls mapped per finding
- **EU AI Act** — Relevant articles per category
- **ISO/IEC 42001:2023** — Clause references per finding

---

## Quick start

```bash
git clone https://github.com/aishieldlabs/ai-redteam-framework
cd ai-redteam-framework

# Demo mode — simulated responses, no API key needed
python ai_redteam.py --target demo

# Live — OpenAI
python ai_redteam.py --target openai --api-key sk-xxx --model gpt-4

# Live — Anthropic
python ai_redteam.py --target anthropic --api-key sk-ant-xxx --model claude-3-5-sonnet-20241022

# Live — Ollama (local)
python ai_redteam.py --target ollama --model llama2

# Run specific categories only
python ai_redteam.py --target demo --categories prompt_injection model_extraction

# JSON output for CI/CD
python ai_redteam.py --target demo --output report.html --json results.json
```

---

## Output

- **Dark-mode HTML report** — risk rating, per-category breakdown, probe results with response preview
- **JSON output** — structured for CI/CD pipeline integration

---

## Zero dependencies

Pure Python 3.8+. No pip install required.

```bash
python --version  # 3.8+ required
python ai_redteam.py --target demo
```

---

## Part of AIShield Labs

| Tool | What it does |
|---|---|
| [agent-security-auditor](https://github.com/aishieldlabs/agent-security-auditor) | Maps agent architecture to MITRE ATLAS + NIST AI RMF |
| [llm-security-scanner](https://github.com/aishieldlabs/llm-security-scanner) | Active LLM probing — OWASP LLM Top 10 + garak |
| [ai-secure-checklist](https://github.com/aishieldlabs/ai-secure-checklist) | 50-point security assessment across 8 domains |
| [ai-supply-chain-scanner](https://github.com/aishieldlabs/ai-supply-chain-scanner) | HuggingFace + dependency CVE scanning + SBOM |
| **[ai-redteam-framework](https://github.com/aishieldlabs/ai-redteam-framework)** | **Active red teaming — 25 probes, 5 attack categories** |

---

## License

MIT License — free to use, modify, and distribute.

---

*Developed by Tirthankar Dutta · AIShield Labs · CISSP · CISM · CISA · Forbes Technology Council*
