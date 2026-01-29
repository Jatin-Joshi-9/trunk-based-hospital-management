
# Trunk-Based Development – Hospital Management System

This repository demonstrates **Trunk-Based Development (TBD)** using a simple **Hospital Management System** application.
The purpose of this project is to showcase how Trunk-Based Development works in practice, including frequent integration, short-lived branches, and continuous release readiness.

---

## What is Trunk-Based Development?

Trunk-Based Development is a Git branching strategy where all developers work close to a **single main branch (called the trunk)**.
Instead of maintaining multiple long-lived branches, changes are integrated **early and often**.

The key idea is:
> Keep the codebase always in a deployable state.

---

## Core Branching Rules

- `main` is the **trunk**
- `main` is always stable and deployable
- No long-lived branches like `develop` or `release`
- Feature branches (if used) are **short-lived**
- Frequent merges into `main`

---

## Application Overview

The application logic is intentionally kept simple to focus on **branching strategy and workflow**.

---

## Trunk-Based Workflow Implemented

### Stage 1: Initial Setup (Main Branch)
- Repository created
- Base Hospital Management System application added
- Code committed **directly to `main`**

**Purpose:** Establish the trunk as the single source of truth

### Stage 2: Short-Lived Feature Branch
- A small feature branch (`feature/patient-message`) was created from `main`
- Minimal change related to patient module messaging added
- Branch merged back into `main` immediately
- Feature branch deleted



### Stage 3: Frequent Integration
- Additional small improvements committed directly to `main`
- Each commit keeps the application in a deployable state

**Purpose:** Reduce merge conflicts and encourage continuous integration

### Stage 4: Continuous Release Readiness
- No release branches created
- Releases handled using Git tags on `main`

Example:
```bash
git tag v1.0.0
git push origin v1.0.0
```
