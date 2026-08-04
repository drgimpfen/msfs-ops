# iniBuilds Airbus A330-300P2F (Cargo) – Standard Operating Procedures (SOP)

Dieser Leitfaden beschreibt die Standard Operating Procedures (SOP) für den **iniBuilds Airbus A330-300P2F** (Freighter) im **MSFS 2024**. Er führt präzise und chronologisch durch alle Flugphasen vom Cold & Dark Setup am Cargo Stand bis zum finalen Shutdown – abgestimmt auf das Zusammenspiel mit ATC (z. B. **BeyondATC**, **VATSIM**, **IVAO**), **SimBrief**, dem **iniBuilds EFB (Tablet)** und der Nutzung des **Winwing Sim URSA Minor** Hardware-Equipments.

> **Transit- / Turnaround-Hinweis:**
> Bei kurzen Zwischenstopps ohne vollständiges Herunterfahren des Flugzeugs kann direkt die zeitoptimierte [Transit SOP](transit-sop.md) genutzt werden.

## Inhaltsverzeichnis
- [1. Pre-Flight & Cockpit-Vorbereitung (Cold & Dark am Cargo Stand)](#1-pre-flight--cockpit-vorbereitung-cold--dark-am-cargo-stand)
- [2. Engine Start & Pushback](#2-engine-start--pushback)
- [3. Taxi & Vorbereitung zum Start](#3-taxi--vorbereitung-zum-start)
- [4. Takeoff & Departure](#4-takeoff--departure)
- [5. Cruise, Fuel Trim Tank & Approach Setup](#5-cruise-fuel-trim-tank--approach-setup)
- [6. Approach & Landing](#6-approach--landing)
- [7. After Landing, Taxi & Shutdown](#7-after-landing-taxi--shutdown)

---

### 1. Pre-Flight & Cockpit-Vorbereitung (Cold & Dark am Cargo Stand)
Der Flug beginnt im stromlosen Zustand am Cargo Standplatz. Ziel dieser Phase ist die Herstellung der elektrischen Versorgungsbereitschaft, die Abwicklung der Fracht-Bodenabfertigung (Betankung, ULD Cargo Container Load, Main Deck Cargo Door) sowie die vollständige Programmierung und Initialisierung der Navigations- und Flugmanagementsysteme (FMGEC/MCDU).

*   **Elektrik einschalten:** Auf dem Overhead Panel nacheinander **BAT 1** und **BAT 2** auf **ON** schalten. Die Batteriespannung auf den Voltmeter-Anzeigen prüfen ($> 25{,}5\text{ V}$). Das iniBuilds EFB (Tablet) hochfahren.
*   **Initiale Lichter am Boden:** Direkt nach der Bestromung das **NAV & LOGO** Light auf **1** (oder **2**) schalten. Position 1 schaltet das primäre Navigationslicht via AC Essential Bus ein und signalisiert dem Bodenpersonal die Versorgungsbereitschaft.
*   **Ground Services & GPU (via EFB):** Im EFB unter *Ground Services* die Ground Power Unit (GPU) anfordern. Sobald am Overhead Panel das grüne *AVAIL*-Licht leuchtet, **EXT PWR** drücken (leuchtet blau *ON*).
    *   Über das EFB / GSX die **Main Deck Cargo Door** öffnen und Cargo Loaders sowie ULD Container beistellen lassen.
    *   Im EFB unter *Payload/Fuel* SimBrief-Daten laden und den Betankungs- sowie Beladungsprozess für Fracht initiieren.
*   **Overhead Panel Setup:**
    *   **CREW SUPPLY** (Sauerstoff) auf **ON** schalten.
    *   Treibstoffpumpen (**MAIN PUMPS 1 & 2**, **STANDBY PUMPS**, **CENTER PUMP**, **TRIM TANK PUMP**) auf **ON** bzw. **AUTO** prüfen.
    *   Signale & Notbeleuchtung: **EMER EXIT LT** auf **ARM** setzen. **NO SMOKING** auf **ON** oder **AUTO** setzen. **SEAT BELTS** auf **ON** setzen (schaltet die Anschnallzeichen für den Courier / Supernumerary Crew Bereich ein).
*   **ATC IFR Clearance:** Streckenfreigabe bei ATC (Delivery/Ground) einholen: *"Request IFR Clearance"*. Nach Erhalt die freigegebene Höhe an der FCU (Flight Control Unit) eindrehen und Squawk am Transponder einstellen.
*   **ADIRUs Initialisierung:** Auf dem Overhead Panel die drei ADIRS-Wahlschalter (1, 2, 3) von OFF auf **NAV** drehen.
*   **Detailliertes MCDU / FMGEC Setup:**
    *   **SimBrief Uplink (AOC):** Taste **MCDU MENU** drücken $\rightarrow$ Line Select Key (LSK) **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ LSK **INIT DATA REQ**.
    *   **INIT A Page:** Taste **INIT** drücken. LSK neben **INIT REQUEST** betätigen. **FROM/TO**, **FLT NBR**, **COST INDEX** und **CRZ FL** aus SimBrief übernehmen. Alignment auf GPS/ADIRS auf der MCDU verifizieren.
    *   **F-PLN (Flight Plan):** Taste **F-PLN** drücken. Linken LSK neben Abflughafen wählen $\rightarrow$ LSK **DEPARTURE** $\rightarrow$ Startbahn und SID auswählen $\rightarrow$ LSK **INSERT** drücken. Enroute-Waypoints sowie STAR/Approach am Zielflughafen eingeben.
    *   **INIT B Page:** Erneut **INIT** drücken und **NEXT PAGE** wählen. LSK neben **ZFW/ZFWCG** und **BLOCK** betätigen, um ZFW, Schwerpunkt (CG) und Block Fuel einzutragen.
    *   **PERF Page:** Taste **PERF** drücken. Im EFB berechnete Startwerte für **V1**, **VR**, **V2**, **FLEX TO TEMP** sowie Klappen-/Trimmwert (**THS/FLAPS**, z. B. `1/UP0.8`) manuell eintragen.
*   **Abschluss des Cargo Loadings:** Nach Abschluss des Beladungsprozesses die Main Deck Cargo Door über das EFB schließen.

---

### 2. Engine Start & Pushback
Diese Phase umfasst die unmittelbare Startvorbereitung. Ziel ist die Inbetriebnahme der Hilfskraftanlage (APU), die Abkopplung von Bodenstrom und Bodenabfertigung, die Durchführung des Zurückschiebens (Pushback) sowie das sichere Anlassen beider Großfan-Triebwerke.

*   **APU Start (ca. 10 Min vor Pushback):**
    *   **APU MASTER SW** auf **ON** schalten.
    *   **APU START** auf **ON** schalten (ON-LED leuchtet).
    *   Sobald auf dem ECAM *APU AVAIL* leuchtet: **APU BLEED** auf **ON** schalten (Zapfluft- & Klimatisierungsübernahme).
*   **Bodenstrom trennen (GPU Disconnect):**
    *   **EXT PWR** am Overhead Panel auf **OFF** schalten (blaue ON-Anzeige erlischt, grüne AVAIL-Anzeige bleibt).
    *   Über das EFB unter *Ground Services* die Bodenstromversorgung (GPU) abkoppeln lassen.
*   **ATC Freigabe & Beacon Light:**
    *   Bei ATC (Ground): *"Request Pushback and Engine Start"* anfordern.
    *   Nach Erhalt der Freigabe (*"Pushback and Engine Start approved"*) das **BEACON** Light auf **ON** schalten. Das rote Blinklicht signalisiert dem Vorfeldverkehr den Beginn der Anlasssequenz.
*   **Before Start Flow & Checklist:**
    *   **THRUST LEVERS:** Beide Schubhebel in der **IDLE**-Raste verifizieren.
    *   **PARKING BRAKE:** Bleibt vorerst auf **ON** gesetzt.
    *   Before Start Checklist abarbeiten.
*   **Pushback-Initiierung & Schlepper-Kopplung:**
    *   Pushback-Vorgang über das EFB, den MSFS-Groundservice oder BeyondATC/GSX auslösen.
    *   Das Ankoppeln des Schleppers abwarten.
    *   Sobald die Bodencrew / der Schlepper meldet: *"Pushback tractor connected, release parking brake"*:
        *   **PARKING BRAKE** auf **OFF** schalten.
*   **Triebwerksanlass-Prozedur (Engine Start Flow):**
    *   Den **ENG MODE SELECTOR** (Mittelkonsole) von NORM auf **IGN/START** drehen (ECAM schaltet automatisch auf die ENG-Seite um und zeigt Zapfluftdruck an).
    *   **Start Triebwerk 2 (Rechtes Großfan-Triebwerk zuerst):**
        *   **ENG MASTER 2** auf **ON** schieben.
        *   *ECAM-Überwachung:* $N_2$-Anstieg beobachten. Bei $N_2 \ge 16\%$ erfolgt die Zündung (IGN-Anzeige). Treibstofffluss (Fuel Flow) und Abgastemperatur (EGT) steigen an, gefolgt vom $N_1$-Anstieg. Bei ca. $50\% N_2$ klinkt der Starter aus. Bei ca. $58–60\% N_2$ erscheint im ECAM grün *AVAIL* $\rightarrow$ Triebwerk 2 läuft stabil.
    *   **Start Triebwerk 1 (Linkes Triebwerk):**
        *   Sobald Triebwerk 2 *AVAIL* zeigt: **ENG MASTER 1** auf **ON** schieben.
        *   Identische ECAM-Überwachung ($N_2 \rightarrow$ Zündung $\rightarrow$ FF/EGT $\rightarrow N_1 \rightarrow$ *AVAIL*) durchführen.
*   **After Start Flow (Nach Ende von Pushback & Engine Start):**
    *   Sobald die Maschine auf der Rollgasse zum Stehen kommt und der Pushback beendet ist:
        *   **PARKING BRAKE** auf **ON** setzen (Rückmeldung an Bodencrew: *"Parking brake set"*).
    *   **ENG MODE SELECTOR:** Den **ENG MODE SELECTOR** zurück auf **NORM** drehen, sobald beide Triebwerke stabil laufen (grünes *AVAIL* im ECAM).
    *   **APU BLEED** auf **OFF** schalten.
    *   **APU MASTER SW** auf **OFF** schalten (APU kühlt herunter und schaltet ab).
    *   Entkoppeln des Schleppers bestätigen lassen und auf das finale Signal der Bodencrew (Bypass-Pin gezeigt) achten.

---

### 3. Taxi & Vorbereitung zum Start
Diese Phase beinhaltet das Einrollen zur aktiven Startbahn. Ziel ist das sichere Manövrieren am Boden, das Konfigurieren aller flight-relevanten Systeme (Klappen, Trimming, Spoilers, WXR/TCAS) sowie die finale technische Startüberprüfung (T/O Config & Flight Controls Check).

*   **ATC Freigabe & Rollbeleuchtung:** Bei ATC: *"Request Taxi"*. Nach Erhalt der Rollfreigabe im *After Start / Taxi Flow* das **NOSE** Light auf **TAXI** schalten. Beim Rollen auf oder über Landebahnen und Taxiways zusätzlich die **RWY TURN OFF** Lights auf **ON** schalten.
*   **After Start Flow / T/O Config:**
    *   **FLAPS** auf berechnete Startstellung (z. B. **FLAPS 1** oder **FLAPS 2** je nach Abfluggewicht) setzen.
    *   **GND SPOILERS** armieren (nach oben ziehen).
    *   **PITCH TRIM** Wheel gemäß MCDU-Wert (THS, z. B. 0.8 UP) einstellen.
    *   **RUD TRIM:** Verifizieren, dass die Rudertrimmung auf `0.0°` steht (**RESET** betätigen falls erforderlich).
    *   **AUTOBRAKE** auf **MAX** setzen.
*   **Wetterradar & Anti-Ice Setup:**
    *   **WXR RADAR PANEL:** **SYS** auf **1** (oder **2**), **PWS** auf **AUTO**, **MODE** auf **WX** oder **WX+T** stellen.
    *   **ENG / WING ANTI ICE:** Bei OAT $\le 10^\circ\text{C}$ und sichtbarer Feuchtigkeit entsprechend zuschalten.
*   **Transponder & TCAS Setup:**
    *   **ATC / XPDR MODE:** Auf **AUTO** (oder **ON**) stellen.
    *   **ALT RPTG:** Auf **ON** stellen.
    *   **TCAS MODE:** Auf **TA/RA** stellen.
*   **Flight Controls Check:** ECAM F/CTL Page überwachen: Stick Full Up, Down, Left, Right; Rudder Pedals Left, Right.
*   **Flight Instruments & T/O CONFIG Test:** Den blauen **T/O CONFIG** Button auf der Mittelkonsole **einmalig** drücken. Dies testet die technische Startkonfiguration. Grünes *NORMAL* auf ECAM verifizieren.
*   **Brake Fan Check:** ECAM WHEEL-Seite prüfen. Verifizieren, dass die Bremstemperaturen unter 150°C liegen und **BRK FAN** auf **OFF** steht.

---

### 4. Takeoff & Departure
Ankunft am Holding Point und Durchführung des Startlaufs. Ziel dieser Phase ist das Einholen der Startfreigabe, das Herstellen der Startkonfiguration und Triebwerksleistung, der sichere Abhebevorgang sowie der Erststeigflug und die Übergangsanpassung im Steigprofil (Thrust Reduction & Clean-Up).

*   **ATC Freigabe:** Bei ATC *"Ready for Departure"* melden. Auf *"Line up and wait"* oder *"Cleared for Takeoff"* warten.
*   **Lichter & System-Check für den Startlauf (Line-up):** Beim Einrollen auf die Startbahn:
    *   **STROBE** von AUTO auf **ON** schalten.
    *   **LANDING L & R** Schalter (beide Schalter der Fixed Wing-Root Lichter) auf **ON** schalten.
    *   **NOSE** Light von TAXI auf **T.O.** (Takeoff) schalten.
    *   **CALLS PANEL (Overhead):** Den **ALL**-Knopf drücken (oder **SEAT BELTS** Signs triggern), um der Kabinenbesatzung den Startlauf zu signalisieren (*"Cabin Crew, take your seats for takeoff"*).
    *   **TCAS & PWS Check:** Verifizieren, dass **TCAS** auf **TA/RA** und **PWS** auf **AUTO** steht.
    *   **ECAM T/O MEMO Sichtprüfung:** Sobald die Kabine bereit ist, wechselt `CABIN READY` im ECAM auf **grün**. Visuell verifizieren, dass alle Zeilen im ECAM T/O MEMO grün sind.
*   **Takeoff Roll & Power Set:**
    *   Bremse lösen, Schubhebel symmetrisch auf ca. 50% $N_1$ schieben und Stabilisierung abwarten.
    *   Schubhebel in die **FLEX/MCT**- (oder **TOGA**-) Raste schieben.
    *   **FMA-Check:** **"MAN FLEX"** (oder MAN TOGA), **"SRS"**, **"RWY"**, **"A/THR BLUE"** verifizieren.
    *   Bei VR: Rotieren (ca. 3° pro Sekunde auf Pitch ca. 15°).
*   **Nach dem Abheben & Departure Handoff:**
    *   Bei positiver Steigrate: *"Positive Climb"* $\rightarrow$ **LANDING GEAR** Lever auf **UP** schalten.
    *   **ATC Handoff:** Frequenzwechsel zu Departure/Radar durchführen.
    *   **Aktivierung des Autopiloten & FCU Logik im Steigflug:** Ab 100 ft AGL kann **AP1** durch Drücken des **AP1**-Buttons an der FCU aktiviert werden.
        *   **Managed Climb (Push / CLB):** **ALT**-Knopf an der FCU drücken ("Push"). Punkt erscheint im FCU-Display, FMA zeigt **CLB**.
        *   **Open Climb (Pull / OP CLB):** **ALT**-Knopf ziehen ("Pull"). Punkt erlischt, FMA zeigt **OP CLB**.
    *   Bei Thrust Reduction Altitude (LVR CLB blinkt auf FMA): **THRUST LEVERS** manuell in die **CL**-Raste zurückziehen.
    *   **Acceleration Altitude & Clean Up:** Klappen stufenweise gemäß F/S-Speed einfahren (**FLAPS 0**). **GND SPOILERS** entwaffnen.
*   **Transition Altitude (Baro Reference Switch):**
    *   Beim Passieren der Transition Altitude den **BARO**-Knopf ziehen (**BARO KNOB PULL**), um auf **STD** (Standard 1013.25 hPa / 29.92 inHg) umzuschalten.
*   **10.000 ft AAL (Climb):**
    *   **LANDING L & R** Schalter auf **OFF**. **NOSE** Light auf **OFF**. **RWY TURN OFF** Lights auf **OFF**.
    *   **SEAT BELTS** auf **OFF** schalten (sofern wetterbedingt möglich).

---

### 5. Cruise, Fuel Trim Tank & Approach Setup
Diese Phase umfasst den Reiseflug sowie die Vorbereitung auf die Landung. Ziel ist die kontinuierliche System- und Treibstoffüberwachung (inkl. automatischem A330 Trim Tank Transfer zur CG-Optimierung), das Einholen der aktuellen Anflugwetterdaten sowie die vollständige MCDU/FCU-Programmierung für den Sink- und Endanflug.

> **Airmanship & Workload Management:**
> Die Reiseflugphase dient der frühzeitigen Anflugvorbereitung und dem Briefing (*Aviate, Navigate, Communicate*). Das Energiemanagement hat stets Priorität. Eine Plausibilitätsprüfung des Sinkflugs (3 NM Distanz pro 1.000 ft Höhenverlust) ist durchzuführen.

*   **Reiseflug- & Trim Tank Überwachung:**
    *   Flugweg, Treibstoffverbrauch und FMA-Status (`SPEED`, `ALT CRZ`, `NAV`) regelmäßig überwachen.
    *   *Trim Tank System (A330 Besonderheit):* Im Steigflug transferiert das automatische A330 Fuel System Treibstoff aus den Wingtanks in den Trim Tank im Leitwerk, um den Schwerpunkt (CG) für optimalen Reiseflug-Widerstand nach hinten zu verlagern. Im Reiseflug erfolgt die automatische Austrimmung.
*   **Descent Planning & Approach Setup (ca. 80 NM vor Top of Descent):**
    *   Wetter am Zielflughafen (ATIS) abfragen.
    *   **MCDU PERF APPR Page:** QNH, Temperatur, MAG WIND, Decision Altitude (**BARO** / **RADIO**) und Landeklappenstellung (**CONF FULL** oder **CONF 3**) eintragen.
    *   **F-PLN:** STAR und Approach im Flugplan prüfen und aktivieren.
*   **Sinkflug-Vorbereitung & FCU Bedienung (DES vs. OP DES):**
    *   Ca. 5–10 NM vor TOD die freigegebene untere Flughöhe an der **FCU** eindrehen.
    *   **Managed Descent (Push / DES):** Am TOD den **ALT**-Knopf drücken ("Push"). Punkt erscheint im FCU-Display, FMA zeigt **DES**.
    *   **Open Descent (Pull / OP DES):** **ALT**-Knopf ziehen ("Pull"). Punkt erlischt, FMA zeigt **OP DES**.
*   **Passieren von FL100 / 10.000 ft AAL (Descent):**
    *   **LANDING L & R** Schalter auf **ON** schalten.
    *   **SEAT BELTS** auf **ON** schalten.
    *   **EFIS Panel:** **LS**-Button vorbereiten, barometrische Referenz (**BARO**) auf Ziel-QNH umstellen (spätestens bei Transition Level).
    *   **MCDU RAD NAV:** ILS-Frequenz und Inbound-Kurs auf Plausibilität verifizieren.
    *   *(Hinweis: Ein Passagier-Cabin-Call entfällt beim Cargo-Frachter).*

---

### 6. Approach & Landing
Diese Phase beschreibt den Sink- und Endanflug bis zum Aufsetzen. Ziel ist das Herstellen der Landekonfiguration, das Erfassen des Anflugpfades (z. B. ILS Localizer & Glideslope), der zeitgerechte Übergang in den manuellen Flug sowie die sichere Landung und Abbremsung auf der Piste.

> **Airmanship & Deceleration Tips:**
> Zur Vermeidung von "High and Fast"-Szenarien können bei ATC-Abkürzungen frühzeitig die **SPEED BRAKES** (bis zur Hälfte) in Kombination mit **OP DES** oder das Ausfahren des Fahrwerks (**GEAR DOWN**) als Luftwiderstand genutzt werden.

*   **Initial Approach & LS-Aktivierung:**
    *   **LS Button (EFIS Panel):** Beim Einrollen in den Anflugsektor die **LS**-Taste drücken, um ILS-Skalen (Localizer & Glideslope Rauten) im PFD einzublenden.
    *   Bei Green Dot Speed: **FLAPS 1** setzen.
*   **Approach Clearance & APPR-Aktivierung (FCU):**
    *   Nach Erhalt der Freigabe von ATC (*"Cleared ILS Approach Runway..."*) und auf Intercept-Kurs:
        *   **APPR Button:** Taste an der FCU drücken (FMA zeigt `LOC` blau und `G/S` blau).
        *   **AP2 Button:** Zusätzlich **AP2**-Taste an der FCU drücken, um Dual-Channel Autoland / CAT III vorzubereiten (FMA zeigt `AP 1+2`).
*   **Established-Meldung (ATC Communication):**
    *   Sobald der Localizer abgefangen ist (FMA zeigt `LOC` grün): Bei ATC melden: *"Established ILS Runway [Pistenbezeichnung]"*.
*   **Final Approach Sequence & Flaps Timeline:**
    *   Bei S-Speed: **FLAPS 2** setzen.
    *   Ca. 2.000 ft AAL (oder 1/2 Dot unter Glideslope): **GEAR DOWN** ausfahren, **GND SPOILERS** armieren, **NOSE** Light auf T.O. und **RWY TURN OFF** Lights auf ON schalten.
    *   Unterhalb VFE für Flaps 3: **FLAPS 3** setzen, gefolgt von **FLAPS FULL** bei F-Speed.
    *   **AUTOBRAKE:** Auf **MED** oder **LOW** setzen. Landing Checklist abarbeiten.
*   **Deaktivierung des Autopiloten (Manual Landing):**
    *   Sobald die Startbahn in Sicht ist und das Flugzeug stabilisiert liegt (zwischen 1.000 ft und 500 ft AGL), Steuerung manuell übernehmen.
    *   **Autopilot Disconnect:** Abschalten über den **AUTOPILOT OFF** Button am Joystick mittels Doppelklick (erster Klick trennt AP, zweiter Klick quittiert akustische Warnung).
*   **Touchdown & Reverser:** Bei Ansage *"Retard"* **THRUST LEVERS** auf **IDLE** ziehen. Nach Aufsetzen **REVERSERS** auf **REV MAX** oder **REV IDLE**. Bei 70 kt Reverser auf Idle zurücknehmen und vor Abrollen schließen. Landebahn verlassen.

---

### 7. After Landing, Taxi & Shutdown
Nach dem Verlassen der Piste beginnt das Abrollen zur Parkposition. Ziel dieser Phase ist das Zurücksetzen der Start- und Anflugsysteme im Taxi-In, das geordnete Abstellen der Triebwerke am Gate/Standplatz sowie die schlussendliche Übergabe in den Cold & Dark Zustand.

> **Airmanship & Taxi-In Management:**
> * **Runway Vacated:** Nach dem Überrollen der gelben Holding-Linie nicht anhalten. Das Flugzeug rollt flüssig weiter, während die Systeme umgestellt werden und der Funkspruch an Ground erfolgt.
> * **Triebwerks-Abkühlzeit:** Die 3-minütige Abkühlphase bei Idle-Schub schützt die Turbinenwellen vor thermischem Schock. Die Rollzeit vom Verlassen der Piste bis zum Gate wird dabei vollständig als Abkühlzeit angerechnet.

*   **Runway Vacated:**
    *   Sobald Holding-Linie überrollt ist: **STROBE** auf **AUTO** (oder **OFF**), **LANDING L & R** Schalter auf **OFF**, **NOSE** Light auf **TAXI**. **RWY TURN OFF** Lights auf **OFF**.
    *   **WXR RADAR PANEL:** **SYS** und **PWS** auf **OFF** schalten.
    *   **TCAS & XPDR:** **TCAS MODE** auf **STBY** (oder `TA ONLY`), **ATC/XPDR MODE** auf **AUTO** / **STBY**.
    *   **FLAPS:** Klappen auf **0** einfahren. **GND SPOILERS:** Spoilers disarmieren.
    *   **ENG ANTI ICE:** Falls zuvor aktiviert, ausschalten.
*   **Taxi to Gate & APU Management:**
    *   Rollfreigabe zum Gate bei ATC anfordern (*"Request taxi to gate"*).
    *   Ca. 3 Minuten vor Erreichen der Parkposition **APU MASTER SW** auf **ON** und **APU START** auf **ON** schalten.
*   **Parking Position & Shutdown:**
    *   **Ground Crew Safety:** Beim Eindrehen in den Standplatz (Sichtkontakt mit Marshaller / VDGS) das **NOSE** Light (Taxi) auf **OFF** schalten, um den Einweiser nicht zu blenden.
    *   Flugzeug exakt auf der Stop-Markierung anhalten, **PARKING BRAKE** auf **ON** setzen.
    *   Sobald im ECAM *APU AVAIL* leuchtet: **APU BLEED** auf **ON** schalten.
    *   Über das EFB / GSX Cargo Loaders anfordern (falls GPU genutzt wird: **EXT PWR** auf **ON** schalten).
    *   **BRK FAN:** ECAM WHEEL-Seite prüfen. Bei Bremstemperaturen über 150°C am Standplatz auf **ON** schalten.
*   **Engine Shutdown Flow:**
    *   **ENG MASTER 1 & 2:** Nach Verifizierung der 3-minütigen Abkühlzeit auf **OFF** schalten.
    *   Sobald die Triebwerke vollständig zum Stillstand gekommen sind ($N_1 < 5\%$): **BEACON** Light auf **OFF** schalten, alle **FUEL PUMPS** auf **OFF** schalten.
    *   **Main Deck Cargo Door** öffnen und Entladung der ULD Container via EFB/GSX initiieren.

> **Transit- / Turnaround-Verfahren:**
> Bei einem unmittelbaren Folgesegment entfällt die nachfolgende Prozedur *Securing the Aircraft*. Der Weiterflug erfolgt direkt gemäß [Transit SOP – Abschnitt 1: Arrival, Parking & Transit Setup](transit-sop.md#1-arrival-parking--transit-setup).

*   **Securing Aircraft (Cold & Dark):**
    *   **NO SMOKING** auf **OFF**, **EMER EXIT LT** auf **OFF**.
    *   **APU BLEED** auf **OFF**, **CREW SUPPLY** (Sauerstoff) auf **OFF**.
    *   ADIRS 1, 2, 3 nacheinander auf **OFF**, **NAV & LOGO** Light auf **OFF**.
    *   **BRK FAN** auf **OFF** (nach Abkühlung), **APU MASTER SW** auf **OFF**, **BAT 1 & 2** auf **OFF**.

Das Flugzeug befindet sich wieder im vollständigen, stromlosen Cold & Dark Zustand.

