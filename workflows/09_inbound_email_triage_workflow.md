# Inbound Email Triage Workflow

## Purpose

Classify inbound emails and route them to the correct agent or founder action.

## Trigger

A new inbound email arrives in an approved YieldWeek inbox or alias.

## Agents involved

- Primary agent: Orchestrator Agent
- Supporting agents: Commercial Agent, Editorial Agent, Operations Agent, Reality Checker Agent

## Inputs

- Email sender
- Sender organization
- Recipient address
- Subject
- Body
- Thread history
- Related CRM record if available

## Steps

1. Classify inbound
   - Owner: Orchestrator Agent
   - Output: category and priority

2. Route to agent
   - Owner: Orchestrator Agent
   - Output: assigned agent and workflow

3. Draft response
   - Owner: assigned agent
   - Output: draft reply and recommended next action

4. Risk review if needed
   - Owner: Reality Checker Agent
   - Output: approval, edits, or escalation

5. Send or escalate
   - Owner: Orchestrator Agent
   - Output: autonomous send if permitted, otherwise founder approval request

## Categories

- sponsor interest
- organiser / badge interest
- speaker / editorial
- media inquiry
- operations / logistics
- legal / contract
- unsubscribe / negative reply
- spam / irrelevant
- founder escalation

## Human approval points

Founder approval required for VIPs, pricing, legal terms, negative or sensitive replies, public claims, and strategic partnerships.

## Outputs

- Email category
- Assigned owner
- Draft reply
- CRM or pipeline update
- Escalation status

## Success metrics

- fast routing
- low missed-opportunity rate
- no unauthorized commitments
- clean inbox state
