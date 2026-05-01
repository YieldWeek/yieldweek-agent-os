# Reality Check Workflow

## Purpose

Verify factual claims, reduce hallucination, and prevent risky outbound or public-facing work.

## Trigger

Any agent produces public, commercial, legal, sponsor, speaker, or partnership-facing material.

## Agents involved

- Primary agent: Reality Checker Agent
- Requesting agent: any agent
- Reviewer: Orchestrator Agent when escalation is needed

## Inputs

- Draft content or message
- Intended recipient/audience
- Source links
- Claims requiring verification
- Approval deadline

## Steps

1. Identify claims
   - Owner: Reality Checker Agent
   - Output: claim list

2. Classify claims
   - Owner: Reality Checker Agent
   - Output: confirmed, inferred, unsupported, risky

3. Verify sources
   - Owner: Reality Checker Agent
   - Output: source-backed corrections

4. Edit or block
   - Owner: Reality Checker Agent
   - Output: approved, approved with edits, needs source, escalate, or blocked

5. Escalate if needed
   - Owner: Orchestrator Agent
   - Output: founder approval request

## Human approval points

Founder approval required if material contains unsupported strategic claims, legal/commercial commitments, partner claims, sponsor claims, or reputational risk.

## Outputs

- Claim review notes
- Corrected draft
- Block or approval status
- Escalation notes

## Success metrics

- no unsupported public claims
- no invented partnerships
- no unapproved commercial commitments
- lower reputational risk
