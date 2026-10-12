# TP3 report

The DHT22 supplies temperature and humidity only. TP2's 12-feature pipeline
cannot accept these two inputs without the missing sensors. A new two-feature
pipeline was therefore trained on the same smoke dataset, 80/20 stratified split,
seed 42. This follows TP3's stated two-input requirement rather than inventing
the other ten readings. This model is different from TP2's full model.

Accuracy: 0.771116; F1: 0.858984; recall: 0.975533.
Mean, scale, coefficients and intercept are saved in parameters.json and embedded
as constants directly in src/main.cpp. The float32 manual inference formula
matches sklearn across all 12526 test readings, maximum probability error
1.224e-07. Seven floats describe the two means, two scales, two weights
and one bias (about 28 bytes), excluding program and sensor-library memory.

The complete sketch standardizes Temperature then Humidity, computes the weighted
sum and sigmoid, prints probability/class, and controls the Uno's built-in LED.
PlatformIO builds use an Arduino Uno and DHT22 connected to digital pin 2.
The sketch prints on-device inference microseconds when run. Desktop numerical
agreement does not certify real-world fire detection. Hardware/Wokwi observations
must be recorded separately; no fabricated board measurements are included.

Source: https://github.com/ahmed3991/AIoT-2025/blob/main/TP3/TP3_Logistic_Arduino.md
