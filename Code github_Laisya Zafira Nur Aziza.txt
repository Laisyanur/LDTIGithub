import pandas as pd
import json

# Buka file JSON
with open("LAISYA ZAFIRA NUR AZIZA_V392547_TI-A.json", "r", encoding="utf-8") as f:
    data = json.load(f)

# Tampilkan tabel dari masing-masing bagian
print("=== Sensor IoT ===")
df_sensor = pd.DataFrame(data["sensor_iot"])
print(df_sensor)

print("\n=== User Reports ===")
df_reports = pd.DataFrame(data["user_reports"])
print(df_reports)

print("\n=== Shinobi Intel ===")
df_intel = pd.DataFrame(data["shinobi_intel"])
print(df_intel)

print("\n=== Historical Data ===")
df_history = pd.DataFrame(data["historical_data"])
print(df_history)
