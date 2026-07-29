# ✈️ ATR 42/72-600 Quick Turnaround Guide (GPU & Refueling - Remote Stand)

> **Operational Standard Procedure**  
> Dieser Flow basiert auf der Stromversorgung über eine **GPU (Ground Power Unit)** auf einer Außenposition (Apron/Remote). Beide Triebwerke werden abgestellt, um das Betankungspanel am rechten Flügel gefahrlos bedienen zu können.

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

### [2] PARKING & ARRIVAL AT REMOTE STAND
* **Taxi Light** .................... OFF
* **Parking Brake** ................. SET
* **Power Levers (1 & 2)** .......... GI (Ground Idle)
* **GPU (via EFB / Ground)** ........ CONNECT & EXT PWR SWITCH ON
* **Condition Levers (1 & 2)** ...... CUT OFF *(Beide Triebwerke komplett AUS)*
* **Beacon Light** .................. OFF *(Signal an Ground: Triebwerke stehen)*
* **Seatbelt Signs** ................ OFF
* **Passenger Door (Left Rear)** .... OPEN / AIRSTAIRS DOWN *(Passagiere aussteigen)*
* **Cargo Doors (Right Side)** ...... OPEN *(Haupt- & Heck-Gepäckraum entladen)*

### [3] COCKPIT RE-PREPARATION, SIMBRIEF & REFUELING
* **EFB** ........................... DE-BOARDING & UNLOADING STARTEN
* **EFB (SimBrief Import)** ......... SIMBRIEF DATA FETCH / IMPORT *(Neuen OFP laden)*
* **EFB / Tankwagen** ............... REFUELING STARTEN *(Ziel-Treibstoff aus OFP übernehmen)*
* **EFB** ........................... BOARDING & LOADING STARTEN *(Payload an Sim senden)*
* **AHRS 1 & 2 / ADC 1 & 2** ........ CHECK NORMAL *(Automatisches Alignment aktiv)*
* **FGCP (Flight Guidance)** ........ FD 1 & FD 2 OFF *(Alte Flugmodi zurücksetzen)*

### [4] FMS RE-PROGRAMMING (SimBrief Route & Performance)
* **FMS INIT / ROUTE Page** ......... SELECT
* **SimBrief Load (AOC/REQ)** ........ EXECUTE *(Origin, Dest & Enroute-Waypoints laden)*
* **DEP Page** ...................... SET SID *(Startbahn & Abflugroute manuell wählen)*
* **FPLN Page** ..................... CHECK DISCONTINUITIES *(Discontinuities mit CLR entfernen)*
* **PERF / WEIGHT Page** ............ UPDATE *(ZFW & Fuel aus EFB bestätigen)*
* **PERF / TAKEOFF Page** ........... V-SPEEDS COMPUTE & ACCEPT *(V1, VR, V2 im PFD aktivieren)*

### [5] BEFORE ENGINE START
* **Cargo Doors (Right Side)** ...... CLOSED & LOCKED
* **Passenger Door (Left Rear)** .... CLOSED & LOCKED / AIRSTAIRS RETRACT
* **EFB** ........................... BOARDING COMPLETE / DOORS CLOSED
* **FGCP (Flight Guidance)** ........ FD 1 & FD 2 ON *(Basis-Modi aktiviert)*
* **FGCP Target Altitude** .......... SET *(Erste Freigabe-Höhe)*
* **Baro / QNH** .................... SET
* **Beacon Light** .................. ON *(Signal an Ground: Startbereitschaft)*
* **Fuel Pumps (1 & 2)** ............ ON

### [6] NORMAL ENGINE START (GPU / Battery)
* **Engine Start Selector** ......... START / 2
* **Condition Lever 2** ............. START & FEATHER *(sobald NH % steigt)*
* **Engine Start Selector** ......... OFF / ABORT *(nach Stabilisierung Engine 2)*
* **Condition Lever 2** ............. AUTO
* **EXT PWR Switch** ................ OFF
* **GPU (via EFB / Ground)** ........ DISCONNECT *(Muss vor Taxi getrennt werden)*
* **Engine Start Selector** ......... START / 1
* **Condition Lever 1** ............. START & FEATHER *(sobald NH % steigt)*
* **Engine Start Selector** ......... OFF / ABORT *(nach Stabilisierung Engine 1)*
* **Condition Lever 1** ............. AUTO
* **ACW / DC Generators** ........... CHECK ALL ON
* **Bleed 1 & 2 / Packs** ........... ON

### [7] TAXI & BEFORE TAKEOFF
* **Gust Lock** ..................... RELEASE *(Vor dem Rollen entriegeln)*
* **Probes & Window Heating** ....... ON *(Manuell aktivieren)*
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