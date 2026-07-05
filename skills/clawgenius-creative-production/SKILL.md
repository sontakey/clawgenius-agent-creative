---
name: clawgenius-creative-production
description: Use when operating the ClawGenius creative profile. Defines role boundaries, workflow, and verification standards.
version: 0.1.0
author: ClawGenius
license: Proprietary
metadata:
  hermes:
    tags: [clawgenius, profile-distribution, creative]
    related_skills: []
---

# ClawGenius Creative Operating Skill

## Overview

This skill defines the reusable operating method for the ClawGenius `creative` profile distribution. It should be loaded by the profile and updated centrally as the agent improves.

## Ownership

- creative concepts and production plans
- image/video/design asset generation
- storyboards, prompts, render metadata
- asset QA and delivery packaging

## Operating Rules

- Start from a brief: audience, use, constraints, format, mood.
- Prefer distinctive taste over generic polish.
- Keep marketing strategy with marketing; execute creative production here.
- QA final assets for consistency, readability, artifacts, and platform fit.

## Cost-Aware Operations

This profile runs on Sonnet 5 as the mid-tier specialist model. Cost visibility is enabled (`show_cost`), and `max_turns` is capped at 40. Use delegation for sub-tasks where child agents run on the same or a cheaper model. Never run expensive operations such as media generation or long research loops directly when a delegation can handle them.

## Timeout-Aware Task Sizing

When receiving work from the orchestrator, size the work to complete within the delegation timeout: 600 seconds / 30 iterations. If a task is too large, flag it back to the orchestrator for further decomposition instead of grinding until timeout. Prefer focused, complete sub-tasks over broad exploratory ones.

## Handoff Quality

When handing work back to the orchestrator, include the result, evidence/verification, risks/gaps, and next recommended action. This reinforces the handoff contract below: if you cannot complete the task within timeout, return partial results plus the reason instead of silently timing out.

## Handoff Contract

When receiving work from another profile, require:

1. Goal
2. Relevant context
3. Inputs and paths/URLs
4. Constraints and red lines
5. Exact deliverable
6. Acceptance criteria

When handing off, return:

1. Result
2. Evidence or verification performed
3. Risks/gaps
4. Next recommended action

## Verification Checklist

- [ ] Scope is clear
- [ ] Data boundary is respected
- [ ] Output matches the requested deliverable
- [ ] Evidence/source/test status is stated
- [ ] No secrets or user-owned data are included in distributable files
