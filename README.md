# PROVEN Onboarding Plugin

A skills-only ChatGPT plugin for PROVEN's adaptive skincare onboarding workflow.

The plugin is designed to do two things at the same time:

1. Understand the customer well enough to support a valid personalized skincare recommendation.
2. Build earned conviction that PROVEN can solve the customer's skin problem through accurate understanding, relevant personalization, credible evidence, and realistic expectations.

## Repository structure

```text
proven-onboarding/
├── README.md
├── plugin.json
└── skills/
    └── proven-onboarding/
        └── SKILL.md
```

## What is included

- The plugin manifest and ChatGPT-facing metadata.
- The complete `proven-onboarding` skill.
- Consultation logic, structured customer state, handoff guidance, evidence discipline, and safety boundaries.
- Prototype behavior for cases where PROVEN's production systems are not connected.

## What is intentionally not included

This repository does **not** contain or simulate PROVEN's proprietary formulation engine, product catalog, customer database, checkout, approved claims database, or safety-rule service.

The skill treats those as external authoritative bindings. Until they are connected, it must not claim that a final formula, SKU, price, availability state, account update, or checkout action has been verified.

## Test prompts

After installing the plugin, useful smoke tests include:

- `Onboard me like I am a new PROVEN customer.`
- `Simulate a PROVEN onboarding conversation for a skeptical skincare customer.`
- `Review this onboarding flow and identify where personalization or conviction breaks down.`

For prototype testing, verify that the agent clearly distinguishes conceptual recommendations from production-backed recommendations.

## Internal-use note

The current skill includes PROVEN strategy context and product-direction assumptions intended for internal use. Review those sections before making this repository public.

## Version

Current plugin version: `0.1.1`.
