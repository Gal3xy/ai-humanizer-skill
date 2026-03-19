# Roadmap: AI Humanizer Skill

## Overview

The skill already exists and is functional. This roadmap covers three phases of improvement: sharpening the core content (kill list, pipeline, registers), extending the process with strength levels and edge-case handling, then validating against real detectors and shipping a clean distribution. Every phase delivers something verifiable on its own.

## Phases

**Phase Numbering:**
- Integer phases (1, 2, 3): Planned milestone work
- Decimal phases (2.1, 2.2): Urgent insertions (marked with INSERTED)

Decimal phases appear between their surrounding integers in numeric order.

- [ ] **Phase 1: Core Content** - Sharpen the kill list, dual-pass system, and register coverage so the baseline pipeline has no critical gaps
- [ ] **Phase 2: Process Extension** - Add strength levels, register mismatch detection, and academic citation preservation
- [ ] **Phase 3: Validate and Ship** - Run against real detectors, lock distribution, and finalize README and trigger phrases

## Phase Details

### Phase 1: Core Content
**Goal**: The kill list, dual-pass calibration, and register system have no critical gaps — a human running the skill against any of the 7 registers gets a fully calibrated rewrite with no obvious AI tells
**Depends on**: Nothing (first phase)
**Requirements**: CORE-06, CORE-07, PROC-01, FORM-02
**Success Criteria** (what must be TRUE):
  1. Kill list covers all tier-1 AI vocabulary patterns with no known critical omissions and includes false-positive guards for legitimate usage
  2. Dual-pass calibration (Detector Pass then Reader Pass) produces output that no single-pass approach would catch — the second pass demonstrably catches what the first misses
  3. Skill completes a rewrite end-to-end without asking unnecessary clarifying questions
  4. All 7 register types (academic, LinkedIn, blog, email, news, technical docs, creative) produce appropriately calibrated output with distinct voice per register
**Plans**: TBD

### Phase 2: Process Extension
**Goal**: The skill handles variable AI intensity through strength levels, catches voice inconsistency before rewriting, and preserves academic citations through the rewrite intact
**Depends on**: Phase 1
**Requirements**: PROC-02, PROC-03, FORM-01
**Success Criteria** (what must be TRUE):
  1. Light mode changes vocabulary only, Standard runs the full pipeline, Aggressive restructures and introduces strong authentic voice — each mode produces visibly different output on the same input
  2. Skill flags register mismatch in the input before rewriting, giving the user a chance to resolve it rather than silently rewriting inconsistent voice
  3. Academic rewrites leave in-text citations and direct quotes completely untouched — citation text is byte-for-byte identical before and after rewrite
**Plans**: TBD

### Phase 3: Validate and Ship
**Goal**: The skill demonstrably passes all four target detectors on real test passages and installs cleanly for any new user with accurate documentation
**Depends on**: Phase 2
**Requirements**: CORE-01, CORE-02, CORE-03, CORE-04, CORE-05, DIST-01, DIST-02, DIST-03, DIST-04
**Success Criteria** (what must be TRUE):
  1. Rewritten standard passage passes GPTZero, Turnitin (academic register), Originality.ai (blog register), and Grammarly AI Detector (business register) when run manually
  2. Rewritten text reads as authentically human to a human reader — no flagging of robotic sentence structures, filler phrases, or hedging language
  3. Skill triggers reliably on all documented trigger phrases (humanize, de-AI, pass Turnitin, etc.) without requiring exact phrasing
  4. New user can install via `git clone https://github.com/Gal3xy/ai-humanizer-skill.git ~/.claude/skills/ai-humanizer` and use the skill immediately with no additional setup
  5. README accurately documents install steps, all trigger phrases, strength levels, and what the skill does
**Plans**: TBD

## Progress

**Execution Order:**
Phases execute in order: 1 → 2 → 3

| Phase | Plans Complete | Status | Completed |
|-------|----------------|--------|-----------|
| 1. Core Content | 0/TBD | Not started | - |
| 2. Process Extension | 0/TBD | Not started | - |
| 3. Validate and Ship | 0/TBD | Not started | - |
