# AI Model Red Teaming Framework

Developed by Tirthankar Dutta — AIShield Labs
github.com/AIShieldLabs/ai-redteam-framework

## Quick start

git clone https://github.com/AIShieldLabs/ai-redteam-framework
cd ai-redteam-framework

python ai_redteam.py --target demo
python ai_redteam.py --target ollama --model mistral
python ai_redteam.py --target openai --api-key sk-xxx --model gpt-4
python ai_redteam.py --target anthropic --api-key sk-ant-xxx --model claude-3-5-sonnet-20241022
python ai_redteam.py --target ollama --model mistral --judge ollama --judge-model mistral --output report.html
python ai_redteam.py --target demo --output report.html --json results.json

## Attack categories

PI — Prompt Injection & Jailbreaking — LLM01:2025 — 5 probes
AE — Adversarial Inputs & Evasion — LLM07:2025 — 5 probes
ME — Model Extraction & Inversion — LLM10:2025 — 5 probes
BT — Bias & Toxicity Probing — LLM09:2025 — 5 probes
MT — Multi-turn Manipulation — LLM01:2025 — 5 probes

## Frameworks

MITRE ATLAS v4.5.2 / OWASP LLM Top 10 2025 / NIST AI RMF 1.0 / EU AI Act / ISO 42001

## Changelog

v1.1.0 — LLM-as-Judge scoring, false positive reduction, --judge flags
v1.0.0 — Initial release, 25 probes, 5 categories, HTML + JSON output
