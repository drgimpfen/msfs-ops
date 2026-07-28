# ✈️ A320neo / A32NX Quick Turnaround Guide (APU-Only)

> **Operational Standard Procedure**  
> Dieser Flow basiert auf einem ununterbrochenen APU-Betrieb während des Bodenaufenthalts (*APU Bleed Always Active*). Die ADIRS verbleiben in `NAV`, um einen zeitraubenden Re-Alignment-Zyklus zu vermeiden.

---

## 📋 Cockpit & Ground Checklist

### [1] AFTER LANDING (Beim Verlassen der Piste)
* **Landing Lights** ................ OFF
* **Strobe Light** .................. AUTO
* **Taxi Light** .................... TAXI
* **RWY Turn Off Lights** ........... ON
* **Radar & PWS** ................... OFF
* **TCAS** .......................... STBY / TA ONLY
* **Flaps / Slats** ................. RETRACT
* **Spoilers** ...................... DISARM
* **APU MASTER SW** ................. ON
* **APU START** ..................... ON

### [2] PARKING & ARRIVAL AT GATE
* **Taxi Light** .................... OFF *(um Bodencrew nicht zu blenden)*
* **RWY Turn Off Lights** ........... OFF
* **Parking Brake** ................. SET
* **Brake Temp** .................... CHECK *(falls >300°C: Brake Fan ON)*
* **APU BLEED** ..................... ON *(sobald APU AVAIL – VOR Triebwerks-Aus!)*
* **Engine Master 1 & 2** ........... OFF
* **Seatbelt Signs** ................ OFF
* **Fuel Pumps (all 6)** ............ OFF
* **Beacon Light** .................. OFF *(Signal an Ground Crew: Engines off)*
* **Jetway** ........................ CONNECT
* **EFB** ........................... DE-BOARDING & UNLOADING STARTEN

### [3] COCKPIT RE-PREPARATION (Turnaround)
* **EFB** ........................... REFUELING STARTEN
* **EFB** ........................... BOARDING & LOADING STARTEN
* **Flight Director 1 & 2** ......... OFF *(beide Seiten kurz aus zum Reset)*
* **ADIRS (IRS 1, 2, 3)** ........... IN NAV LASSEN *(nicht anrühren)*
* **APU** ........................... CHECK RUNNING
* **APU BLEED** ..................... CHECK ON *(Klimatisierung läuft weiter)*

### [4] MCDU RE-PROGRAMMING
* **MCDU Setup** .................... COMPLETE *(siehe separater MCDU-Flow)*

### [5] BEFORE PUSHBACK
* **EFB** ........................... BOARDING COMPLETE / DOORS CLOSED
* **Jetway** ........................ DISCONNECT
* **Flight Director 1 & 2** ......... ON *(beide Seiten wieder an)*
* **FCU Target Altitude** ........... SET *(erste Freigabe-Höhe)*
* **Baro / QNH** .................... SET *(aktuelles QNH)*
* **Fuel Pumps (all 6)** ............ ON
* **Brake Fan** ..................... OFF *(falls in Phase 2 aktiviert)*
* **Beacon Light** .................. ON *(Signal an Ground Crew: Pushback/Start)*

### [6] ENGINE START & AFTER START
* **Packs 1 & 2** ................... OFF *(für maximalen Startdruck)*
* **Engine Mode Sel** ............... IGN / START
* **Engine Master 2** ............... ON ➔ *Warten auf AVAIL*
* **Engine Master 1** ............... ON ➔ *Warten auf AVAIL*
* **Engine Mode Sel** ............... NORM
* **APU BLEED** ..................... OFF *(Triebwerke übernehmen)*
* **APU MASTER SW** ................. OFF *(nach Abkühlphase)*
* **Packs 1 & 2** ................... ON

### [7] TAXI & BEFORE TAKEOFF
* **Taxi Light** .................... TAXI *(beim Losrollen)*
* **RWY Turn Off Lights** ........... ON
* **Flaps** ......................... SET FOR TAKEOFF *(z.B. 1 oder 2)*
* **Spoilers** ...................... ARM
* **Pitch Trim** .................... SET
* **Flight Controls** ............... CHECK
* **Auto Brake** .................... MAX
* **TCAS** .......................... TA/RA
* **Radar / Predictive Windshear** .. ON / AUTO

### [8] LINE UP (Auffahren auf die Piste)
* **Landing Lights** ................ ON
* **Strobe Light** .................. ON *(für maximale Sichtbarkeit)*
* **Taxi Light** .................... T.O. *(Takeoff)*

---

# 💻 MCDU Quick-Setup Flow (Departure Only)

> [1. AOC / ATSU] ──► [2. INIT A] ──► [3. F-PLN] ──► [4. INIT B] ──► [5. PERF TO]

---

### 1. AOC / ATSU Menu
* **MCDU MENU** ➔ **ATSU** *(oder bei iniBuilds: AOC / HOOK)* ➔ **INIT/PRES**
* **INIT DATA REQ** drücken ➔ *SimBrief-Flugplan wird geladen*

### 2. INIT A (Fast Alignment & Cruise)
* **INIT**-Taste drücken
* **INIT REQUEST** drücken *(übernimmt FROM/TO, Flight Number & Cost Index)*
* **IRS INIT** ➔ **ALIGN ON REF** drücken *(Fast Re-Alignment in ~30 Sekunden)*
* **CRZ FL** *(Reiseflughöhe)* prüfen und ggf. anpassen

### 3. F-PLN (Departure Only)
* **F-PLN**-Taste drücken
* Departure Airport *(Softkey oben links)* ➔ **DEPARTURE**
* Startbahn & SID auswählen ➔ **INSERT**
* 🔍 **Discontinuity Check:** Durch den Flugplan scrollen und Unterbrechungen nach der SID mit der **CLR**-Taste löschen.
* ⚠️ *Ankunft (Arrival/Approach) explizit leer lassen.*

### 4. INIT B (Weight & Fuel)
* **INIT**-Taste ➔ Pfeil nach rechts (**INIT B**)
* **ZFW / ZFWCG** Softkey zweimal drücken ➔ *Lädt Werte direkt via Uplink*
* **BLOCK FUEL** für das neue Leg manuell eintragen

### 5. PERF (Takeoff Performance)
* **PERF**-Taste drücken *(öffnet TAKE OFF)*
* **FLAPS / THS** eintragen *(z. B. 1/UP0.5)*
* **FLEX TO TEMP** eintragen *(z. B. 55 für Flex-Start)*
* **V1**, **VR**, **V2** durch zweimaliges Drücken der jeweiligen Softkeys übernehmen
