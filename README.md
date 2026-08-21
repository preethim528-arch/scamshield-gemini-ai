# 🛡️ ScamShield — Multimodal AI Fraud & Threat Detection Engine

An agentic, multimodal safety and quality evaluation pipeline built with **Google Gemini 3.6 Flash** and **Python**. ScamShield inspects deceptive SMS, fraudulent payment screenshots, and malicious links, enforcing deterministic structured JSON guardrails and providing accessible Tamil voice advisories (gTTS).

---

## 🚀 Key Features & Capabilities
* **Multimodal Threat Ingestion:** Processes deceptive screenshot images, SMS text payloads, and destination URLs simultaneously.
* **Strict JSON Policy Guardrails:** Enforces deterministic risk classifications (`APPROVED`, `RESTRICTED`, `DISAPPROVED`) with dynamic confidence scoring (0–100%).
* **Root Cause & Remediation (RCA):** Generates actionable policy explanations and advertiser/user remediation guidance.
* **Vernacular Audio Accessibility:** Converts safety recommendations into regional Tamil audio guidance using `gTTS`.
* **Interactive UI:** Built with Gradio for rapid local and web prototyping.

---

## 🛠️ Tech Stack & Tooling
* **LLM Engine:** Google Gemini 3.6 Flash (`google-genai` SDK)
* **Development Workspace:** Google AI Studio & Google Colaboratory
* **Scripting & Logic:** Python, Structured JSON Schema
* **Voice & UI:** Gradio, gTTS (Google Text-to-Speech), Pillow

---

## 📊 Evaluation Schema
The core model outputs a validated schema for auditing:
```json
{
  "risk_level": "HIGH",
  "threat_category": "Phishing / Payment Fraud",
  "confidence_score": 96,
  "root_cause_analysis": "Deceptive payment screenshot imitating official banking portal with malicious link.",
  "recommended_action": "Do not click link. Block sender immediately."
}
