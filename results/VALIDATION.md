# Validation

- All 7 notebook code cells executed successfully; genuine outputs are saved.
- Notebook format validated with nbformat.
- Python solution/support modules pass syntax compilation.
- Report and Arabic explanation are included.
- Float32 exported inference matches sklearn for all 12,526 test rows.
- Local Arduino Uno PlatformIO build PASSED: 219/2048 bytes static RAM, 6084/32256 bytes Flash.
- GitHub firmware build runs on push; see Actions for its final result.
- No real-board runtime measurements or Wokwi observations are claimed.

## GitHub firmware build

**PASSED**: [Build run](https://github.com/ggdh17934/AIoT-2025--TP3/actions/runs/38261375861).

The included firmware and pinned platform configuration compiled successfully on GitHub's Linux runner.
This proves compilation; board execution, sensor/LCD behavior and runtime timing remain separate observations.
