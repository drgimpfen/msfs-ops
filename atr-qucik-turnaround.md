# ✈️ ATR 42/72-600 Quick Turnaround Guide (GPU & Refueling)

> **Operational Standard Procedure**  
> Dieser Flow basiert auf der Stromversorgung über eine **GPU (Ground Power Unit)** am Gate. Beide Triebwerke werden abgestellt, um das Betankungspanel am rechten Flügel gefahrlos bedienen zu können.

---

## 📋 Cockpit & Ground Checklist

### [1] AFTER LANDING (Beim Verlassen der Piste)
* **Landing Lights** ................ OFF
* **Strobe Light** .................. OFF / NAV
* **Taxi Light** .................... TAXI
* **Radar & WX** .................... OFF
* **TCAS** .......................... STBY
* **Flaps** ......................... RETRACT (0°)
* **Pitch Trim** .................... RESET (0.0 / TO Neutral)
* **Gust Lock** ..................... ENGAGED *(Arretierung der Steuerflächen)*

### [2] PARKING & ARRIVAL AT GATE
* **Taxi Light** .................... OFF
* **Parking Brake** ................. SET
* **Power Levers (1 & 2)** .......... GI (Ground Idle)
* **GPU (via EFB / Ground)** ........ CONNECT
* **EXT PWR Switch** ................ ON *(Grüne AVAIL-Taste drücken)*
* **Condition Levers (1 & 2)** ...... CUT OFF *(Beide Triebwerke komplett AUS)*
* **Beacon Light** .................. OFF *(Signal an Ground: Triebwerke stehen)*
* **Seatbelt Signs** ................ OFF
* **Passenger Door (Left Rear)** .... OPEN *(De-Boarding starten)*
* **Cargo Doors (Right Side)** ...... OPEN *(Gepäck/Fracht entladen)*

### [3] COCKPIT RE-PREPARATION & REFUELING
* **EFB** ........................... DE-BOARDING & UNLOADING STARTEN
* **EFB / Tankwagen** ............... REFUELING STARTEN *(Gefahrlos möglich, da Triebwerke AUS)*
* **EFB** ........................... BOARDING & LOADING STARTEN
* **AHRS / ADIRS** .................. IN NAV LASSEN *(Kein Re-Alignment nötig)*
* **Flight Director 1 & 2** ......... OFF / RESET

### [4] FMS RE-PROGRAMMING
* **FMS Setup** ..................... COMPLETE
  * *Flight Plan (Init)* ............ Neue Route & Dep/Arr eingeben
  * *Weights & Fuel* ................ ZFW & Ziel-Treibstoff aus EFB übernehmen
  * *V-Speeds* ...................... In Perf Page berechnen & PFD senden

### [5] BEFORE ENGINE START
* **Cargo Doors (Right Side)** ...... CLOSED & LOCKED
* **Passenger Door (Left Rear)** .... CLOSED & LOCKED
* **EFB** ........................... BOARDING COMPLETE / DOORS CLOSED
* **Flight Director 1 & 2** ......... ON
* **FCU Target Altitude** ........... SET *(Erste Freigabe-Höhe)*
* **Baro / QNH** .................... SET
* **Beacon Light** .................. ON *(Signal an Ground: Startbereitschaft)*
* **Fuel Pumps (1 & 2)** ............ ON

### [6] NORMAL ENGINE START (GPU / Battery)
* **Engine Start Selector** ......... START / 2
* **Condition Lever 2** ............. START & FEATHER *(sobald NH % steigt)*
* **Engine Start Selector** ......... OFF / ABORT *(nach Stabilisierung Engine 2)*
* **Condition Lever 2** ............. AUTO
* **EXT PWR Switch** ................ OFF
* **GPU (via EFB / Ground)** ........ DISCONNECT
* **Engine Start Selector** ......... START / 1
* **Condition Lever 1** ............. START & FEATHER *(sobald NH % steigt)*
* **Engine Start Selector** ......... OFF / ABORT *(nach Stabilisierung Engine 1)*
* **Condition Lever 1** ............. AUTO
* **ACW / DC Generators** ........... CHECK ALL ON
* **Bleed 1 & 2 / Packs** ........... ON

### [7] TAXI & BEFORE TAKEOFF
* **Gust Lock** ..................... RELEASE *(Vor dem Rollen entriegeln)*
* **Taxi Light** .................... TAXI
* **Flaps** ......................... SET FOR TAKEOFF (15°)
* **Pitch Trim** .................... SET FOR TAKEOFF
* **Flight Controls** ............... CHECK (Full Free & Correct)
* **PWR MGT Selector** .............. TO (Takeoff)
* **Auto Trim** ..................... ARM / ON
* **TCAS** .......................... TA/RA

### [8] LINE UP (Auffahren auf die Piste)
* **Landing Lights** ................ ON
* **Strobe Light** .................. ON
* **Taxi Light** .................... OFF / T.O.
* **Radar / WX** .................... ON
* **Transponder** .................... ALT / ON
