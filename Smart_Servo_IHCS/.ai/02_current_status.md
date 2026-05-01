# Current Status

## Current Goal
Maintain a clean Phase 1 pipeline that supports both simulation data and minimal raw PLC ingestion.

## Done
- SQLite schema and data repository
- Virtual plant simulation and dataset export
- LSTM autoencoder training and TFLite export
- PPO training and ONNX export
- Phase 2 advisory scaffold
- Raw PLC CSV preprocessing (4 signal minimum)

## In Progress
- None identified

## Next
- Calibrate preprocessing heuristics with real PLC data
- Map PLC alarm bits to `fault_type` when available
- Tune PPO batch size if needed

## Important Files
- `Phase_1_PC_Training/config_pc.yaml`
- `Phase_1_PC_Training/01c_preprocess_raw_plc_csv.py`
- `Phase_1_PC_Training/modules/raw_plc_preprocessor.py`
- `Phase_1_PC_Training/02_train_model1_lstm.py`
- `Phase_2_Yocto_Deployment/main_hmi_loop.py`

## Blockers
None identified
