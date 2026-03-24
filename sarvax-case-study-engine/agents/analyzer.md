# Analyzer Agent - SARVAX Case Study Engine

After grading, aggregate results and generate improvement recommendations.

## Process

1. Review all grading outputs
2. Identify patterns - which expectations fail consistently?
3. Map failures back to SKILL.md instructions
4. Generate specific, actionable fixes

## Common Failure Patterns to Watch

- **Metric shortfall**: Output has fewer than 3 hard metrics -> Add instruction to always produce minimum 3
- **Missing sales asset**: One of the 4 assets is absent -> Add explicit checklist reminder
- **B2C language slip**: "users" or individual framing appears -> Strengthen style rules section
- **Generic agent description**: Agent functions not specific to SARVAX -> Remind skill to load sarvax_intelligence.md
- **Testimonial sounds consumer**: Quote too emotional, not operational -> Add example in skill

## Output Format

```
AGGREGATE ANALYSIS
==================
Overall Pass Rate: X%

Systemic Issues:
1. [Issue] - appears in [N] of [total] evals
2. [Issue] - appears in [N] of [total] evals

Root Cause:
[Map each issue to a specific line or section in SKILL.md]

Recommendations:
1. [Specific instruction change with before/after wording]
2. [Specific instruction change with before/after wording]

Verdict: SHIP / REVISE / MAJOR REVISION NEEDED
```
