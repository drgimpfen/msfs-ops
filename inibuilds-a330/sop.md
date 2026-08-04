# Airbus A330 (A330-200 & A330-300P2F) – Standard Operating Procedures (SOP)

Dieser Leitfaden beschreibt die Standard Operating Procedures (SOP) für den **iniBuilds Airbus A330-200** (Passagier) sowie den **iniBuilds Airbus A330-300P2F** (Freighter) im **MSFS 2024**. Er führt präzise und chronologisch durch alle Flugphasen vom Cold & Dark Setup bis zum finalen Shutdown – abgestimmt auf das Zusammenspiel mit ATC (z. B. **BeyondATC**, **VATSIM**, **IVAO**), **SimBrief**, dem **iniBuilds EFB (Tablet)** und der Nutzung des **Winwing Sim URSA Minor** Hardware-Equipments.

> **Transit- / Turnaround-Hinweis:**
> Bei kurzen Zwischenstopps ohne vollständiges Herunterfahren des Flugzeugs kann direkt die zeitoptimierte [Transit SOP](transit-sop.md) genutzt werden.

## Inhaltsverzeichnis
- [1. Pre-Flight & Cockpit-Vorbereitung (Cold & Dark am Gate / Stand)](#1-pre-flight--cockpit-vorbereitung-cold--dark-am-gate--stand)
- [2. Engine Start & Pushback](#2-engine-start--pushback)
- [3. Taxi & Vorbereitung zum Start](#3-taxi--vorbereitung-zum-start)
- [4. Takeoff & Departure](#4-takeoff--departure)
- [5. Cruise, Fuel Trim Tank & Approach Setup](#5-cruise-fuel-trim-tank--approach-setup)
- [6. Approach & Landing](#6-approach--landing)
- [7. After Landing, Taxi & Shutdown](#7-after-landing-taxi--shutdown)

---

### 1. Pre-Flight & Cockpit-Vorbereitung (Cold & Dark am Gate / Stand)
Der Flug beginnt im stromlosen Zustand am Gate oder Standplatz (bzw. Cargo Stand). Ziel dieser Phase ist die Herstellung der elektrischen Versorgungsbereitschaft, die Abwicklung der Bodenabfertigung (Betankung, Beladung, Boarding / ULD Cargo Load) sowie die vollständige Programmierung und Initialisierung der Navigations- und Flugmanagementsysteme (FMGEC/MCDU).

*   **Elektrik einschalten:** Auf dem Overhead Panel nacheinander **BAT 1** und **BAT 2** auf **ON** schalten. Das EFB (Tablet) hochfahren.
*   **Initiale Lichter am Boden:** Direkt nach der Bestromung das **NAV & LOGO** Light auf **1** (oder **2**) schalten, um die Versorgungsbereitschaft dem Bodenpersonal anzuzeigen.
*   **Ground Services & GPU (via EFB):** Im EFB unter *Ground Services* die Ground Power Unit (GPU) anfordern. Sobald am Overhead Panel das grüne *AVAIL*-Licht leuchtet, **EXT PWR** drücken (leuchtet blau *ON*).
    *   *Passagiervariante (A330-200):* Über das EFB den Jetway / Passenger Stairs ankoppeln.
    *   *Frachtvariante (A330-300P2F):* Main Deck Cargo Door öffnen und Cargo Loaders / ULD Containers via EFB/GSX anfordern.
    *   Im EFB unter *Payload/Fuel* SimBrief-Daten laden und den Betankungs- sowie Beladungsprozess starten.
*   **Overhead Panel Setup:**
    *   **CREW SUPPLY** (Sauerstoff) auf **ON** schalten.
    *   Treibstoffpumpen (**MAIN PUMPS 1 & 2**, **STANDBY PUMPS**, **CENTER PUMP**, **TRIM TANK PUMP**) auf **ON** bzw. **AUTO** prüfen.
    *   Signale & Notbeleuchtung: **EMER EXIT LT** auf **ARM** setzen. **NO SMOKING** auf **ON** oder **AUTO** setzen. **SEAT BELTS** auf **ON** setzen.
*   **ATC IFR Clearance:** Streckenfreigabe bei ATC (Delivery/Ground) einholen: *"Request IFR Clearance"*. Nach Erhalt die freigegebene Höhe an der FCU (Flight Control Unit) eindrehen und Squawk am Transponder einstellen.
*   **ADIRUs Initialisierung:** Auf dem Overhead Panel die drei ADIRS-Wahlschalter (1, 2, 3) von OFF auf **NAV** drehen.
*   **MCDU / FMGEC Setup:**
    *   **INIT A Page:** Taste **INIT** drücken. LSK **INIT REQUEST** betätigen. **FROM/TO**, **FLT NBR**, **COST INDEX** und **CRZ FL** aus SimBrief übernehmen. Alignment auf GPS/ADIRS auf der MCDU verifizieren.
    *   **F-PLN (Flight Plan):** Taste **F-PLN** drücken. Departure Runway und SID auswählen $\rightarrow$ **INSERT**. Enroute-Waypoints sowie STAR/Approach am Zielflughafen eingeben.
    *   **INIT B Page:** Erneut **INIT** drücken und **NEXT PAGE** wählen. LSK neben **ZFW/ZFWCG** und **BLOCK** betätigen, um ZFW, Schwerpunkt (CG) und Block Fuel einzutragen.
    *   **PERF Page:** Taste **PERF** drücken. Startwerte für **V1**, **VR**, **V2**, **FLEX TO TEMP** sowie Klappen-/Trimmwert (**THS/FLAPS**, z. B. `1/UP0.8`) eintragen.

---

### 2. Engine Start & Pushback
Diese Phase umfasst die unmittelbare Startvorbereitung. Ziel ist die Inbetriebnahme der Hilfskraftanlage (APU), die Abkopplung von Bodenstrom und Bodenabfertigung, die Durchführung des Zurückschiebens (Pushback) sowie das sichere Anlassen beider Großfan-Triebwerke.

*   **APU Start (ca. 10 Min vor Pushback):**
    *   **APU MASTER SW** auf **ON** schalten.
    *   **APU START** auf **ON** schalten.
    *   Sobald *APU AVAIL* leuchtet: **APU BLEED** auf **ON** schalten (Zapfluftversorgung übernehmen).
*   **Bodenstrom trennen (GPU Disconnect):**
    *   **EXT PWR** am Overhead Panel auf **OFF** schalten.
    *   Über das EFB die externe Stromversorgung trennen und Türen / Cargo Doors schalten/schließen.
*   **ATC Freigabe & Beacon Light:**
    *   Bei ATC (Ground): *"Request Pushback and Engine Start"* anfordern.
    *   Nach Erhalt der Freigabe das **BEACON** Light auf **ON** schalten.
*   **Before Start Flow:**
    *   **THRUST LEVERS:** Beide Schubhebel in der **IDLE**-Raste verifizieren.
    *   **PARKING BRAKE:** Bleibt auf **ON**.
    *   Before Start Checklist abarbeiten.
*   **Pushback:**
    *   Pushback auslösen (EFB / GSX / BeyondATC) und Parking Brake auf **OFF** lösen, sobald der Schlepper dazu auffordert.
*   **Triebwerksanlass-Prozedur (Engine Start Flow):**
    *   **ENG MODE SELECTOR** auf **IGN/START** drehen.
    *   **Start Triebwerk 2 (Rechts):**
        *   **ENG MASTER 2** auf **ON** schieben.
        *   *Überwachung:* $N_2$-Anstieg beobachten. Bei Ausklinken des Starters (ca. 50% $N_2$) und EGT/FF-Stabilisierung erscheint *AVAIL* auf dem ECAM.
    *   **Start Triebwerk 1 (Links):**
        *   Sobald Triebwerk 2 stabil läuft: **ENG MASTER 1** auf **ON** schieben.
*   **After Start Flow:**
    *   Nach Ende des Pushbacks: **PARKING BRAKE** auf **ON** setzen.
    *   **ENG MODE SELECTOR** zurück auf **NORM** drehen.
    *   **APU BLEED** auf **OFF** und **APU MASTER SW** auf **OFF** schalten.

---

### 3. Taxi & Vorbereitung zum Start
Diese Phase beinhaltet das Einrollen zur aktiven Startbahn. Ziel ist das sichere Manövrieren am Boden, das Konfigurieren aller flight-relevanten Systeme (Klappen, Trimming, Spoilers, WXR/TCAS) sowie die finale technische Startüberprüfung (T/O Config & Flight Controls Check).

*   **Rollfreigabe & Beleuchtung:** Bei ATC Rollfreigabe anfordern (*"Request Taxi"*). **NOSE** Light auf **TAXI** schalten. **RWY TURN OFF** Lights auf **ON**.
*   **After Start Flow / T/O Config:**
    *   **FLAPS** auf berechnete Startstellung (z. B. **FLAPS 1** oder **FLAPS 2** je nach Abfluggewicht) setzen.
    *   **GND SPOILERS** armieren (nach oben ziehen).
    *   **PITCH TRIM** Wheel gemäß MCDU-Wert (THS) einstellen.
    *   **AUTOBRAKE** auf **MAX** setzen.
*   **Wetterradar & Anti-Ice:**
    *   **WXR RADAR:** **SYS 1**, **PWS AUTO**, **MODE WX+T**.
    *   **ENG / WING ANTI ICE:** Bei Temperaturen $\le 10^\circ\text{C}$ und Feuchtigkeit entsprechend zuschalten.
*   **Transponder & TCAS:**
    *   **ATC / XPDR:** **AUTO** / **ON**, Squawk prüfen.
    *   **TCAS:** **TA/RA**.
*   **Flight Controls Check:** Stick Full Up, Down, Left, Right; Rudder Pedals Left, Right (auf ECAM F/CTL Seite prüfen).
*   **T/O CONFIG Test:** **T/O CONFIG** Button auf der Mittelkonsole drücken. Grünes *NORMAL* auf ECAM verifizieren.

---

### 4. Takeoff & Departure
Ankunft am Holding Point und Durchführung des Startlaufs. Ziel dieser Phase ist das Einholen der Startfreigabe, das Herstellen der Startkonfiguration und Triebwerksleistung, der sichere Abhebevorgang sowie der Erststeigflug und die Übergangsanpassung im Steigprofil (Thrust Reduction & Clean-Up).

*   **Line-up Clearance:** Nach Erhalt der Freigabe zum Betreten der Piste:
    *   **NOSE** Light auf **TO** schalten.
    *   **STROBE** Lights auf **ON** schalten.
    *   **LANDING** Lights auf **ON** schalten.
*   **Takeoff Roll & Power Set:**
    *   Bremse lösen, Schubhebel symmetrisch auf ca. 50% $N_1$ schieben. Nach Triebwerks-Stabilisierung Schubhebel in die **FLEX/MCT**- (oder **TOGA**-) Raste schieben.
    *   FMA-Anzeige verifizieren: `MAN FLEX [Temp]` (oder `MAN TOGA`), `SRS`, `NAV` (oder `CLB`).
*   **Rotate & Initial Climb:**
    *   Bei **VR:** Stick sanft ziehen, Rotationsrate ca. 3° pro Sekunde auf einen Pitch von ca. 15° einnehmen.
    *   Sobald Positiv Rate auf dem PFD angezeigt wird: *"Positive Climb"* $\rightarrow$ **LANDING GEAR** Lever auf **UP** schalten.
*   **Climb Flow & Thrust Reduction:**
    *   Bei **Thrust Reduction Altitude (LVR CLB blinkt auf FMA):** Schubhebel zurück in die **CL**-Raste (Climb Detent) ziehen.
    *   Bei **Acceleration Altitude:** Flugzeug beschleunigt. Klappen stufenweise gemäß F-Speed / S-Speed einfahren (**FLAPS 0**).
    *   **GND SPOILERS** entwaffnen.
*   **Autopilot Aktivierung:**
    *   Autopilot durch Drücken von **AP 1** (oder **AP 2**) an der FCU aktivieren.
*   **Passing 10.000 ft (FL100):**
    *   **LANDING** Lights auf **OFF** / Retract.
    *   **NOSE** Light auf **OFF**.
    *   **SEAT BELTS** je nach Turbulenzlage auf **AUTO** oder **OFF** schalten.
    *   **EFIS Panel:** Barometrischen Druck auf **STD** (Standard 1013 hPa / 29.92 inHg) umstellen durch Ziehen des Baro-Knopfs (*PULL STD*).

---

### 5. Cruise, Fuel Trim Tank & Approach Setup
Diese Phase umfasst den Reiseflug sowie die Vorbereitung auf die Landung. Ziel ist die kontinuierliche System- und Treibstoffüberwachung (inkl. automatischem A330 Trim Tank Transfer zur CG-Optimierung), das Einholen der aktuellen Anflugwetterdaten sowie die vollständige MCDU/FCU-Programmierung für den Sink- und Endanflug.

*   **Cruise Management:**
    *   Flugweg, Treibstoffverbrauch und FMA-Status (`SPEED`, `ALT CRZ`, `NAV`) regelmäßig überwachen.
    *   *Trim Tank System (A330 Besonderheit):* Im Steigflug transferiert das automatische A330 Fuel System Treibstoff aus den Wingtanks in den Trim Tank im Leitwerk, um den Schwerpunkt (CG) für optimalen Reiseflug-Widerstand nach hinten zu verlagern. Im Reiseflug erfolgt die automatische Austrimmung.
*   **Descent Planning & Approach Setup (ca. 80 NM vor Top of Descent):**
    *   Wetter am Zielflughafen (ATIS) abfragen.
    *   **MCDU PERF APPR Page:** QNH, Temperatur, MAG WIND, Decision Altitude (**BARO** / **RADIO**) und Landeklappenstellung (**CONF FULL** oder **CONF 3**) eintragen.
    *   **F-PLN:** STAR und Approach im Flugplan prüfen und aktivieren.
*   **Descent Initiation:**
    *   Neue Zielflughöhe an der FCU eindrehen.
    *   Bei Top of Descent (TOD): **ALT KNOB** an der FCU drücken (**PUSH**) für Managed Descent (`DES`) oder ziehen (**PULL**) für Open Descent (`OP DES`).

---

### 6. Approach & Landing
Diese Phase beschreibt den Sink- und Endanflug bis zum Aufsetzen. Ziel ist das Herstellen der Landekonfiguration, das Erfassen des Anflugpfades (z. B. ILS Localizer & Glideslope), der zeitgerechte Übergang in den manuellen Flug sowie die sichere Landung und Abbremsung auf der Piste.

*   **Passing FL100 / Transition Level:**
    *   Barometrischen Druck von **STD** auf lokalen **QNH** umstellen (FCU Baro Knob drücken/einstellen).
    *   **LANDING** Lights auf **ON** schalten.
    *   **SEAT BELTS** auf **ON** schalten.
    *   **LS** Button am EFIS Panel aktivieren (falls ILS Approach).
*   **Initial & Intermediate Approach:**
    *   Geschwindigkeit im Managed Mode reduzieren lassen (`SPEED` managed).
    *   Bei Passieren der Green Dot Speed: **FLAPS 1** setzen.
    *   Bei Passieren der S-Speed: **FLAPS 2** setzen.
*   **Final Approach & Landing Configuration:**
    *   Bei Erfassen des Glide Slope / Intercept: **LANDING GEAR** Lever auf **DOWN** schalten.
    *   **GND SPOILERS** armieren.
    *   **AUTOBRAKE** auf **LOW** oder **MED** wählen.
    *   Klappen weiter ausfahren: **FLAPS 3**, danach **FLAPS FULL**.
*   **Manual Landing (Deaktivierung Autopilot):**
    *   Im Endanflug den Autopiloten manuell durch Betätigung des **AP Disconnect Buttons** am **Winwing Sim URSA Minor** Joystick ausschalten.
    *   Bei ca. 30–50 ft über Grund: flare einleiten, Schubhebel bei ca. 10–20 ft geschmeidig auf **IDLE** zurückziehen (*"Retard"* Callout).
*   **Rollout & Touchdown:**
    *   Hauptfahrwerk aufsetzen, Bugfahrwerk sanft absenken.
    *   Schubhebel in **REVERSE** ziehen.
    *   Autobrake / manuelle Bremse überwachen. Bei 70 kt Reverser auf Idle zurückfahren und vor Fahrtende ganz schließen.
    *   Landebahn über den Nächsten Schnellabrollweg verlassen.

---

### 7. After Landing, Taxi & Shutdown
Nach dem Verlassen der Piste beginnt das Abrollen zur Parkposition. Ziel dieser Phase ist das Zurücksetzen der Start- und Anflugsysteme im Taxi-In, das geordnete Abstellen der Triebwerke am Gate/Standplatz sowie die schlussendliche Übergabe in den Cold & Dark Zustand.

*   **After Landing Rollout & Taxi Clearing:**
    *   Nach Verlassen der Landebahn stoppen oder weiterrollen.
    *   **STROBE** Lights auf **OFF** / AUTO.
    *   **LANDING** Lights auf **OFF**.
    *   **NOSE** Light auf **TAXI**.
    *   **GND SPOILERS** entwaffnen.
    *   **FLAPS** vollständig einfahren (**FLAPS 0**).
    *   **WXR RADAR** auf **OFF**.
    *   **APU MASTER SW** & **APU START** auf **ON** schalten.
*   **Parking Position & Shutdown:**
    *   An der Parkposition/Gate anhalten: **PARKING BRAKE** auf **ON** setzen.
    *   Sobald *APU AVAIL* leuchtet: **APU BLEED** auf **ON** schalten.
    *   **ENG MASTER 1 & 2** auf **OFF** schalten.
    *   **BEACON** Light auf **OFF** schalten (Bodenpersonal darf an das Flugzeug herantreten).
    *   **SEAT BELTS** auf **OFF** schalten.
    *   *A330-300P2F Cargo Ops:* Main Deck Cargo Door öffnen und Entladung via EFB initiieren.
    *   *A330-200 Pax Ops:* Jetway andocken und De-Boarding auslösen.
*   **Securing Aircraft (Cold & Dark):**
    *   Falls das Flugzeug abgestellt wird: **APU BLEED** auf **OFF**, **APU MASTER SW** auf **OFF**, **EXT PWR** trennen, **NAV & LOGO** auf **OFF**, **BAT 1 & 2** auf **OFF**.
