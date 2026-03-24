# Grader Agent - SARVAX Case Study Engine

Evaluate each test case output against the success criteria defined in evals/evals.json.

## What to Check

For each expectation:

1. **Read the output** produced by the skill execution
2. **Search for evidence** that the expectation is met
3. **Assign PASS or FAIL** with a cited evidence quote or observation
4. **Calculate pass rate** across all expectations

## SARVAX-Specific Pass Criteria

- PASS "loaded sarvax_intelligence.md": Transcript shows `read_resource("references/sarvax_intelligence.md")`
- PASS "3 hard metrics": Output contains 3+ bullet points with numbers in the Results section
- PASS "no B2C framing": No consumer language ("users", "customers" as individuals, "personal productivity")
- PASS "no KARAX": String "KARAX" does not appear anywhere in output
- PASS "4 sales assets": LinkedIn post, ROI statement, sales deck bullets, AND cold outreach all present
- PASS "testimonial in operator voice": Quote sounds like COO/Ops Director, not a consumer review

## Output Format

Produce a summary in this structure:

```
EVAL [ID]: [prompt excerpt]
----------------------------
[expectation] -> PASS/FAIL
Evidence: [quote or observation]
...
Score: X/Y passed (Z%)
Overall notes: [1-2 sentences]
```

Then give an aggregate summary:
- Total pass rate across all evals
- Top 1-2 issues if any evals failed
- Recommendation: SHIP / REVISE / MAJOR REVISION NEEDED
