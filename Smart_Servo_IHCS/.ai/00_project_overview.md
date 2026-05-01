# Project Overview

## Product
Intelligent Hierarchical Control System (IHCS) for a servo conveyor with advisory AI and human-in-the-loop control.

## Goal
Build a laptop-first Phase 1 pipeline that generates or ingests data, trains models, and exports artifacts for future edge deployment.

## Stack
- Python
- SQLite
- TensorFlow / Keras
- Gymnasium + Stable-Baselines3
- ONNX / ONNX Runtime
- NumPy / Pandas
- PyYAML

## Scope
- Phase 1 data generation, preprocessing, training, and export
- Phase 2 advisory scaffold (no real PLC writes)

## Non-goals
- Cloud services
- Autonomous actuation without human approval
- Yocto deployment in this phase

## Notes
- SQLite is the canonical historian.
- Raw PLC input is intentionally minimal and enriched on the laptop.
