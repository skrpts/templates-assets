---
type: workflow
id: templates-assets
title: "Asset Templates"
description: "Asset templates — reports, personas, rubrics, checklists, and glossaries"
tags: [Production, Templates]
connections:
  - target: asset-output-template
    type: uses
  - target: asset-email-template
    type: uses
  - target: asset-persona
    type: uses
  - target: asset-evaluation-rubric
    type: uses
  - target: asset-glossary
    type: uses
  - target: asset-checklist
    type: uses
  - target: asset-style-guide
    type: uses
  - target: asset-faq
    type: uses
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "1 minute"
  trigger: manual
  template: true
output_step: "asset-output-template"
composite_steps:
  - "asset-output-template"
  - "asset-email-template"
  - "asset-persona"
  - "asset-evaluation-rubric"
  - "asset-glossary"
  - "asset-checklist"
  - "asset-style-guide"
  - "asset-faq"
execution:
  - skill: "asset-output-template"
    step_type: "generation"
---

## Overview

This skrpt contains 8 asset templates for use when creating new asset nodes. Import this skrpt to add these templates to your template picker.

## Templates

### Template

- **Report Template** — Structured report with summary, findings, and recommendations
- **Email Template** — Professional email structure with subject, body, and call to action
- **Checklist** — Reusable checklist for quality or process control
- **FAQ Template** — Frequently asked questions template

### Configuration

- **AI Persona** — Reusable persona definition for consistent AI behaviour across prompts
- **Evaluation Rubric** — Scoring criteria for review and validation steps

### Reference

- **Domain Glossary** — Key terms and definitions for consistent language across workflows
- **Style Guide** — Writing or brand style guide

