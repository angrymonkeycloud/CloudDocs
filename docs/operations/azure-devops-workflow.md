---
title: Azure DevOps Workflow Standard
description: Default Azure DevOps board and workflow setup for Angry Monkey projects.
keywords:
  - Azure DevOps workflow
  - project board setup
  - agile operations
---

# Azure DevOps Workflow Standard

This standard defines the baseline Azure DevOps setup for project tracking.

## Initial Project Setup

- Process: Agile
- Version control: Git
- Visibility: Private

## Work Item Configuration

- Manage bugs with requirements in the selected process model.

## Board Columns and Limits

- Backlog
- To Do
  - Preferred WIP limit: 20
  - State mapping: Active
- In Progress
  - Preferred WIP limit: 5
  - State mapping: Active
- Done
  - WIP limit: 0
  - State mapping: Active
- Staging
  - WIP limit: 0
  - State mapping: Active
- Ready
  - WIP limit: 0
  - State mapping: Resolved
- Production

## Operational Guidance

- Keep WIP limits realistic to maintain flow.
- Ensure state mapping is consistent across projects.
- Review board health weekly.
