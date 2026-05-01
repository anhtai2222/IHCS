# Architecture

## High-Level Structure
- `shared/` common config, schema, and DB helpers
- `Phase_1_PC_Training/` simulation, preprocessing, training, validation, tests
- `Phase_2_Yocto_Deployment/` advisory-only scaffold and safety gates

## Main Layers
- Data layer: SQLite historian and CSV exports
- Training layer: LSTM autoencoder + PPO supervisory policy
- Advisory layer: inference wrappers, bounded ramp/MPC scaffold, approval gate
- Tests: lightweight Phase 1 coverage

## Data Flow
Simulation or raw PLC CSV -> preprocessing -> SQLite -> CSV export -> model training -> artifact export -> validation.

## Conventions
- Prefer small, focused modules
- Keep naming consistent with the existing codebase
- Avoid unnecessary abstraction
- Prefer incremental changes over broad rewrites

## Risks / Tech Debt
- PPO batch size warning (not fatal, but can be tuned)
- Raw PLC preprocessing uses heuristic labels until real PLC alarms are mapped
