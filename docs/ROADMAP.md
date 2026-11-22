# Development roadmap / Entwicklungsplan

> Proposed milestones; not a fixed schedule. A milestone is complete only after implementation and hardware validation.

## Phase 1 — Stable playback foundation
- [x] Display/touch bring-up on prototype
- [x] SD WAV test loading
- [x] PCM5102A audible output
- [x] MIDI note-off behavior tested
- [x] Six-voice playback tested
- [ ] Regression tests for varied WAV formats, durations and SD cards
- [ ] Define measurable audio/CPU/PSRAM acceptance criteria

## Phase 2 — Sample library and editing
- [ ] File browser, metadata and sample selection
- [ ] Start/end markers with precise time/sample-position editing
- [ ] Loop start/end, validation, audition and loop modes
- [ ] Zoom and scrolling of long waveforms
- [ ] Save and restore non-destructive editing parameters

## Phase 3 — Keymaps and patches
- [ ] Root notes and keyboard ranges
- [ ] Multisample mapping and velocity strategy
- [ ] Patch parameter model and save/load
- [ ] Envelope, tuning and per-zone settings

## Phase 4 — MIDI and performance
- [ ] MIDI program changes and controller mapping
- [ ] Voice allocation and voice stealing validation
- [ ] Sustain, pitch bend and modulation policy
- [ ] Robust error handling and all-notes-off

## Phase 5 — Release engineering
- [ ] Versioned project data format
- [ ] SD corruption/recovery tests
- [ ] Reproducible build and hardware instructions
- [ ] Audio/MIDI endurance and latency measurements
- [ ] First public firmware release candidate

**Scope note:** advanced features are proposals, not verified current capabilities.
