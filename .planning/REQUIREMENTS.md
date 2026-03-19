# Requirements: AI Humanizer Skill

**Defined:** 2026-03-19
**Core Value:** Humanization so accurate it passes every major detector AND reads as genuinely human writing

## v1 Requirements

### Core Quality

- [ ] **CORE-01**: Rewritten text passes GPTZero on standard test passages
- [ ] **CORE-02**: Rewritten text passes Turnitin AI detection on academic-register passages
- [ ] **CORE-03**: Rewritten text passes Originality.ai on content/blog-register passages
- [ ] **CORE-04**: Rewritten text passes Grammarly AI Detector on business-register passages
- [ ] **CORE-05**: Rewritten text reads as authentically human to human readers (no obvious AI tells)
- [ ] **CORE-06**: Kill list has no critical omissions — all tier-1 words reliably flagged and replaced
- [ ] **CORE-07**: Dual-pass calibration (Detector Pass + Reader Pass) catches failure modes that single-pass misses

### Process Efficiency

- [ ] **PROC-01**: Skill completes a rewrite without asking unnecessary clarifying questions
- [ ] **PROC-02**: Multi-pass strength levels implemented — Light (vocab only), Standard (full pipeline), Aggressive (restructure + strong voice)
- [ ] **PROC-03**: Register mismatch detection — skill flags inconsistent voice in input before rewriting

### Format Coverage

- [ ] **FORM-01**: Academic format rewrite preserves in-text citations and direct quotes untouched
- [ ] **FORM-02**: All 7 register types (academic, LinkedIn, blog, email, news, technical docs, creative) produce appropriately calibrated output

### Distribution

- [ ] **DIST-01**: Skill installs cleanly via `git clone https://github.com/Gal3xy/ai-humanizer-skill.git ~/.claude/skills/ai-humanizer`
- [ ] **DIST-02**: Skill triggers reliably in Claude Code on all trigger phrases (humanize, de-AI, pass Turnitin, etc.)
- [ ] **DIST-03**: SKILL.md description optimized for triggering accuracy
- [ ] **DIST-04**: README accurately documents install, trigger phrases, and what the skill does

## v2 Requirements

### Advanced Features

- **ADV-01**: Length delta tracking — show word count change between input and output
- **ADV-02**: Word count targeting — rewrite stays within specified length constraint
- **ADV-03**: Before/after diff annotation — highlight exactly what changed sentence by sentence
- **ADV-04**: Tone preservation scoring — verify core argument and intent survived the rewrite

### Tooling

- **TOOL-01**: Automated detector simulation (would require third-party API)
- **TOOL-02**: Context injection questionnaire UI

## Out of Scope

| Feature | Reason |
|---|---|
| Web app or UI | Claude Code skill only — no standalone product in v1 |
| API / programmatic access | Out of scope until there's demand |
| Paid tiers | Public and free |
| Scripts or executables | Skill format is markdown only |
| Detector API integration | Requires paid third-party accounts |

## Traceability

| Requirement | Phase | Status |
|---|---|---|
| CORE-01 | Phase 3 | Pending |
| CORE-02 | Phase 3 | Pending |
| CORE-03 | Phase 3 | Pending |
| CORE-04 | Phase 3 | Pending |
| CORE-05 | Phase 3 | Pending |
| CORE-06 | Phase 1 | Pending |
| CORE-07 | Phase 1 | Pending |
| PROC-01 | Phase 1 | Pending |
| PROC-02 | Phase 2 | Pending |
| PROC-03 | Phase 2 | Pending |
| FORM-01 | Phase 2 | Pending |
| FORM-02 | Phase 1 | Pending |
| DIST-01 | Phase 3 | Pending |
| DIST-02 | Phase 3 | Pending |
| DIST-03 | Phase 3 | Pending |
| DIST-04 | Phase 3 | Pending |

**Coverage:**
- v1 requirements: 16 total
- Mapped to phases: 16
- Unmapped: 0 ✓

---
*Requirements defined: 2026-03-19*
*Last updated: 2026-03-19 after roadmap creation*
