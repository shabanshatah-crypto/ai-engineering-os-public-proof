# Case Study Template

## How to Use This Template

This template helps you document a pilot engagement **without exposing customer data**. Fill in the anonymized sections after completing a 2-week pilot. Store the completed case study in your **private** working documents, not in this public repository.

---

## Case Study: [Anonymized Identifier]

### Executive Summary

| Field | Value |
|-------|-------|
| **Industry** | [e.g., FinTech, HealthTech, E-commerce] |
| **Team Size** | [e.g., 8-person engineering team] |
| **Workflow Type** | [e.g., API contract generation, client SDK creation] |
| **Pilot Duration** | 2 weeks |
| **Baseline Period** | [e.g., Previous 4 sprints] |
| **Data Classification** | Synthetic / Approved Test Data |

---

### The Problem (Before Pilot)

**Describe the pain point in their own words (anonymized):**

> "[Quote from stakeholder about the problem they were facing]"

**Quantified Baseline:**

| Metric | Before Pilot |
|--------|--------------|
| Time to first artifact | [e.g., 3-5 days per workflow] |
| Review/rework cycles | [e.g., 4-6 iterations] |
| Validation failures | [e.g., 30% of generated code] |
| Audit readiness | [e.g., No traceable evidence trail] |
| Vendor dependency | [e.g., Locked into single AI provider] |

**Root Causes Identified:**

- [ ] No standardized contract definition
- [ ] Manual verification processes
- [ ] Missing evidence trail for compliance
- [ ] Provider-specific implementation
- [ ] Security review bottlenecks
- [ ] Other: _______________

---

### The Pilot Engagement

**Selected Workflow:**

```
[Describe the narrowly-scoped workflow tested]
Example: Generate REST API client from OpenAPI spec with validation evidence
```

**Success Criteria (Pre-agreed):**

| Criterion | Target | Rationale |
|-----------|--------|-----------|
| Time reduction | ≥40% faster | Must beat current baseline |
| Rework cycles | ≤2 iterations | Reduce review burden |
| Evidence completeness | 100% of runs | Audit requirement |
| Security gates passed | 0 violations | Non-negotiable |

**Implementation Approach:**

1. **Week 1:** Setup, baseline measurement, workflow definition
2. **Week 2:** Execution, measurement, comparison analysis

**Data Handling:**

- [x] All test data was synthetic or explicitly approved
- [x] No customer PII or production credentials used
- [x] Results stored in private working documents only

---

### Results (After Pilot)

**Quantified Outcomes:**

| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| Time to first artifact | [X days] | [Y days] | [Z% faster] |
| Review/rework cycles | [X iterations] | [Y iterations] | [Z% reduction] |
| Validation failures | [X%] | [Y%] | [Z% reduction] |
| Evidence completeness | [X%] | [Y%] | [Z% improvement] |
| Team satisfaction | [X/10] | [Y/10] | [Z% increase] |

**Qualitative Feedback:**

> "[Quote from engineering lead about the experience]"

> "[Quote from developer about daily workflow impact]"

> "[Quote from security/compliance stakeholder]"

**Unexpected Benefits Discovered:**

- [e.g., Faster onboarding for new team members]
- [e.g., Improved cross-team communication via standardized contracts]
- [e.g., Reduced audit preparation time from days to hours]

**Challenges Encountered:**

| Challenge | How It Was Addressed |
|-----------|---------------------|
| [e.g., Initial learning curve] | [e.g., 1-hour training session + cheat sheet] |
| [e.g., Integration with existing CI/CD] | [e.g., Custom adapter built in week 1] |
| [e.g., Stakeholder skepticism] | [e.g., Daily demo of progress] |

---

### Decision & Next Steps

**Pilot Outcome:**

- [ ] ✅ **Proceed to Production** — Metrics exceeded targets, team adopted
- [ ] ⚠️ **Expand Pilot** — Promising results, need broader testing
- [ ] ❌ **Not a Fit** — Workflow too complex / different priorities
- [ ] ⏸️ **Pause** — Timing issues / resource constraints

**If Proceeding:**

| Item | Details |
|------|---------|
| **Scope Expansion** | [e.g., From 1 workflow to 5 workflows] |
| **Timeline** | [e.g., Production rollout in Q3 2025] |
| **Success Metrics** | [e.g., 50% reduction in sprint rework time] |
| **Investment** | [e.g., Annual enterprise agreement] |
| **Ownership** | [e.g., VP Engineering + Head of Platform] |

**If Not Proceeding:**

| Reason | Learnings |
|--------|-----------|
| [e.g., Workflow too bespoke for current product] | [e.g., Need more customization options] |
| [e.g., Timing conflict with major release] | [e.g., Revisit in next quarter] |
| [e.g., Different priority emerged] | [e.g., Stay in touch for future opportunities] |

---

### Evidence Artifacts (References Only)

**Note:** Actual artifacts are stored privately. This section lists what *would* be included.

| Artifact | Description | Location |
|----------|-------------|----------|
| `pilot-contract.json` | Workflow definition used in pilot | Private repo |
| `baseline-metrics.csv` | Pre-pilot measurement data | Private docs |
| `pilot-results.csv` | Pilot period measurement data | Private docs |
| `evidence-samples/` | Sample verification records | Private repo |
| `team-feedback.md` | Compiled qualitative feedback | Private docs |

---

### Lessons Learned (Internal Use)

**What Worked Well:**

- [e.g., Starting with a narrowly-scoped workflow reduced friction]
- [e.g., Daily standups kept momentum and surfaced blockers quickly]
- [e.g., Synthetic data approach satisfied security concerns]

**What Would We Do Differently:**

- [e.g., Involve security team earlier in the process]
- [e.g., Provide more training materials upfront]
- [e.g., Set clearer expectations about integration effort]

**Product Improvements Identified:**

| Priority | Feature Request | Rationale |
|----------|----------------|-----------|
| P0 | [e.g., CI/CD plugin for Jenkins] | Customer uses Jenkins exclusively |
| P1 | [e.g., Custom evidence export formats] | Audit team needs specific format |
| P2 | [e.g., Multi-workflow dashboard] | Teams want to compare workflows |

---

### Approval & Distribution

| Role | Name (Anonymized) | Date | Approval |
|------|-------------------|------|----------|
| Pilot Lead | [Engineering Manager A] | [Date] | ✅ |
| Customer Stakeholder | [VP Engineering B] | [Date] | ✅ |
| Security Review | [Security Lead C] | [Date] | ✅ |
| Case Study Author | [Your Name] | [Date] | ✅ |

**Distribution List:**

- [ ] Internal product team
- [ ] Sales team (for similar prospects)
- [ ] Marketing (for website/collateral — if approved by customer)
- [ ] Investors (as traction evidence)

**Confidentiality Level:**

- 🔒 **Internal Only** — Do not share externally without explicit customer approval
- 📋 **Sanitized Version Available** — Can be shared with prospects under NDA
- 🌐 **Public Case Study** — Customer approved public announcement

---

## Quick Reference: Strong Signals vs. Weak Signals

Use this during discovery to qualify pilot candidates:

### ✅ Strong Signals (Proceed)

- Specific recent problem with named owner
- Measurable baseline already tracked
- Willingness to commit 2 weeks + access
- Clear success criteria defined upfront
- Budget or authority to make decision

### ⚠️ Weak Signals (Qualify Further)

- General enthusiasm without specific use case
- "Let's try it and see" without metrics
- No clear owner or decision maker
- Waiting for "perfect timing"
- Requests broad feature list before pilot

### ❌ Red Flags (Decline)

- Unwilling to define baseline or success criteria
- Expects production results in 2 weeks
- Wants to use real customer data without approval
- No budget or path to purchase identified
- Competitor evaluation with no differentiation ask

---

*This template is part of the AI Engineering OS Discovery Kit. Store completed case studies in private working documents, not in this public repository.*
