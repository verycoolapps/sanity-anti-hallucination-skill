---
name: Hallucination Report
about: Report a case where SANITY Protocol failed to prevent an AI hallucination
title: '[HALLUCINATION] '
labels: hallucination, bug
assignees: ''
---

## Hallucination Report

### What type of hallucination occurred?

- [ ] Phantom Function (non-existent API/function cited)
- [ ] Ghost File (file content claimed without reading)
- [ ] Version Fraud (wrong/nonexistent version cited)
- [ ] False Certainty (confident claim without evidence)
- [ ] Citation Fabrication (fake references/links)
- [ ] Confident Completion (fake implementation for unknown API)
- [ ] Math Error (calculation without verification)
- [ ] Self-Contradiction (contradictory claims in same response)
- [ ] Other: ___

### Describe the hallucination

What did the AI claim that turned out to be false?

```
[Paste the incorrect AI statement here]
```

### What should have been done instead?

Which SANITY Protocol step was missing?

- [ ] Should have Read() the file first
- [ ] Should have Grep() to verify function existence
- [ ] Should have labeled with training cutoff warning
- [ ] Should have requested clarification instead of assuming
- [ ] Should have used lower confidence tier
- [ ] Other: ___

### How was it discovered?

- [ ] Compile error
- [ ] Runtime error
- [ ] Manual inspection
- [ ] Test failure
- [ ] Production incident
- [ ] Other: ___

### Impact

How much time was wasted due to this hallucination?

- [ ] < 30 minutes
- [ ] 30 min - 2 hours
- [ ] 2 - 8 hours
- [ ] > 8 hours

### Additional context

Any other context about the hallucination case.
