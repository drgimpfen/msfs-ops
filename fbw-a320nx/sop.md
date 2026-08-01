# FlyByWire A320NX – Standard Operating Procedures (SOP)

Dieser Leitfaden beschreibt die Standard Operating Procedures (SOP) für den **FlyByWire A320NX** im **MSFS 2024**. Er führt präzise und chronologisch durch alle Flugphasen vom Cold & Dark Setup bis zum finalen Shutdown – abgestimmt auf das Zusammenspiel mit **BeyondATC**, **SimBrief**, dem **FlyPad (EFB)** und der Nutzung des **Winwing Sim URSA Minor** Hardware-Equipments.

> **Transit- / Turnaround-Hinweis:**
> Bei kurzen Zwischenstopps ohne vollständiges Herunterfahren des Flugzeugs kann direkt die zeitoptimierte [Transit SOP](transit-sop.md) genutzt werden.

## Inhaltsverzeichnis
- [1. Pre-Flight & Cockpit-Vorbereitung (Cold & Dark am Gate)](#1-pre-flight--cockpit-vorbereitung-cold--dark-am-gate)
- [2. Engine Start & Pushback](#2-engine-start--pushback)
- [3. Taxi & Vorbereitung zum Start](#3-taxi--vorbereitung-zum-start)
- [4. Takeoff & Departure](#4-takeoff--departure)
- [5. Cruise, Descent Planning & Approach Setup](#5-cruise-descent-planning--approach-setup)
- [6. Approach & Landing](#6-approach--landing)
- [7. After Landing, Taxi & Shutdown](#7-after-landing-taxi--shutdown)

---

### 1. Pre-Flight & Cockpit-Vorbereitung (Cold & Dark am Gate)
Der Flug beginnt am Gate im komplett stromlosen Zustand. Ziel dieser Phase ist die elektrische Bestromung, die Koordinierung der Bodenabfertigung und die vollständige Programmierung des FMGS (Flight Management Guidance System).

*   **Elektrik einschalten:** Auf dem Overhead Panel nacheinander **BAT 1** und **BAT 2** einschalten. Das FlyPad (EFB) an der linken Seite hochfahren.
*   **Initiale Lichter am Boden:** Direkt nach der Bestromung das **NAV & LOGO** Light auf **1** (oder **2**) schalten. Dies signalisiert dem Bodenpersonal die elektrische Versorgungsbereitschaft des Flugzeugs.
*   **Ground Services (via FlyPad):** Im EFB in das Menü *Ground Services* wechseln. Die Ground Power Unit (GPU) anfordern. Sobald am Overhead Panel das grüne *AVAIL*-Licht leuchtet, **EXT PWR** drücken (leuchtet blau *ON*).
    *   Über das EFB den Jetway (Fluggastbrücke) an das Flugzeug andocken.
    *   Im FlyPad in das Menü *Fuel/Payload* wechseln, SimBrief-Daten laden und das *Refueling* (Betankung) sowie den *Boarding*-Prozess für Passagiere und Fracht starten.
*   **Overhead Panel Setup:** 
    *   **CREW SUPPLY** (Sauerstoff) auf **ON** schalten.
    *   Alle sechs **FUEL PUMPS** (L TK, C TK, R TK) auf **ON** schalten.
    *   Passagier- und Notfallsignale: **EMER EXIT LT** auf **ARM** setzen. **NO SMOKING** (bzw. **NO PORTABLE ELEC DEVICE**) auf **ON** oder **AUTO** setzen. **SEAT BELTS** auf **ON** setzen.
*   **ATC IFR Clearance:** Einholen der Streckenfreigabe via BeyondATC (Delivery): *"Request IFR Clearance"*. Nach Erhalt von Route, initialer Steigflughöhe und Squawk-Code die freigegebene Höhe an der FCU (Flight Control Unit) eindrehen.
*   **Initialisierung ADIRUs:** Auf dem Overhead Panel die drei ADIRS-Schalter nacheinander (1, 2, 3) von OFF auf **NAV** drehen.
*   **Detailliertes MCDU / FMGS Setup:** 
    *   **SimBrief Uplink (AOC):** Taste **MCDU MENU** drücken $\rightarrow$ Line Select Key (LSK) **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ LSK **INIT DATA REQ**.
    *   **INIT A Page:** Taste **INIT** drücken. LSK neben **INIT REQUEST** betätigen. Das System füllt **FROM/TO**, **FLT NBR**, **COST INDEX** und **CRZ FL** aus.
    *   **F-PLN (Flight Plan):** Taste **F-PLN** drücken. Linken LSK neben dem Abflughafen wählen $\rightarrow$ LSK **DEPARTURE** $\rightarrow$ Startbahn und SID gemäß ATC-Freigabe auswählen $\rightarrow$ LSK **INSERT** drücken.
    *   **INIT B Page:** Erneut **INIT** drücken, danach Taste **NEXT PAGE** wählen. Den rechten LSK neben **ZFW/ZFWCG** betätigen und zweimal den rechten LSK neben **BLOCK** drücken, um die Treibstoffwerte aus SimBrief zu übernehmen.
    *   **PERF Page:** Taste **PERF** drücken. Die im FlyPad berechneten V-Speeds (**V1**, **VR**, **V2**) eintragen. Die **FLEX TO TEMP** in den entsprechenden rechten LSK eintragen. Klappen-/Trimm-Einstellung bei **THS/FLAPS** eintragen (z. B. `1/UP0.5`) und mit dem LSK bestätigen.
*   **Abschluss des Boardings:** Nach Abschluss des Boardings (Anzeige im EFB) den Jetway über das EFB entfernen. Die Türen werden geschlossen.

---

### 2. Engine Start & Pushback
Vorbereitung und Durchführung des Zurückschiebens sowie des Triebwerksstarts.

*   **APU Start:** Ca. 10 Minuten vor dem Pushback **APU MASTER SW** auf **ON** und anschließend **APU START** auf **ON** schalten. Sobald auf dem ECAM *APU AVAIL* erscheint: **APU BLEED** auf **ON** schalten.
*   **Bodenstrom abkoppeln:** **EXT PWR** am Overhead Panel ausschalten und über das EFB trennen lassen.
*   **ATC Freigabe & Beacon Light:** Bei BeyondATC (GND): *"Request Pushback and Engine Start"*. Nach Erhalt der Freigabe (*"Pushback and Engine Start approved"*) das **BEACON** Light auf **ON** schalten. Das rote Blinklicht signalisiert dem Bodenpersonal den bevorstehenden Pushback und Triebwerksstart.
*   **Before Start Flow & Checklist:** Parkbremse lösen und Before Start Checklist abarbeiten.
*   **Triebwerksanlass-Prozedur:**
    *   Den **ENG MODE SELECTOR** (Mittelkonsole) auf **IGN/START** drehen.
    *   **ENG MASTER 2** auf **ON** schieben.
    *   *Überwachung:* N2-Anstieg, Zündung, Fuel Flow und EGT-Anstieg kontrollieren.
    *   Sobald Triebwerk 2 stabil läuft (*AVAIL* im ECAM), **ENG MASTER 1** auf **ON** schieben.
    *   Nachdem beide Triebwerke stabil laufen (*AVAIL*): **ENG MODE SELECTOR** zurück auf **NORM** stellen.
    *   **APU BLEED** auf **OFF** und **APU MASTER SW** auf **OFF** schalten.

---

### 3. Taxi & Vorbereitung zum Start

*   **ATC Freigabe & Rollbeleuchtung:** Bei BeyondATC: *"Request Taxi"*. Nach Erhalt der Rollfreigabe im *After Start / Taxi Flow* das **NOSE** Light auf **TAXI** schalten. Beim Rollen auf oder über Landebahnen und Taxiways zusätzlich die **RWY TURN OFF** Lights auf **ON** schalten.
*   **After Start Flow / T/O Config:**
    *   **FLAPS** auf die berechnete Start-Einstellung setzen (z. B. **FLAPS 1**).
    *   **GND SPOILERS** armieren (Speed Brake Hebel nach oben ziehen).
    *   **PITCH TRIM** Wheel auf den berechneten CG-Wert aus der MCDU einstellen (z. B. 0.5 UP).
    *   **AUTOBRAKE** auf **MAX** setzen.
*   **Flight Controls Check:** ECAM F/CTL Page überwachen: Stick Full Up, Down, Neutral; Stick Full Left, Right, Neutral; Rudder Pedals Full Left, Right, Neutral.
*   **Flight Instruments Check:** Den blauen **T/O CONFIG** Button auf der Mittelkonsole drücken (alle Memos im ECAM müssen grün sein).

---

### 4. Takeoff & Departure
Ankunft am Holding Point der aktiven Startbahn.

*   **ATC Freigabe:** Bei BeyondATC *"Ready for Departure"* melden. Auf *"Line up and wait"* oder *"Cleared for Takeoff"* warten.
*   **Lichter für den Startlauf (Line-up):** Beim Einrollen auf die Startbahn:
    *   **STROBE** von AUTO auf **ON** schalten.
    *   **LANDING** Lights (beide) auf **ON** schalten.
    *   **NOSE** Light von TAXI auf **T.O.** (Takeoff) schalten.
*   **Takeoff Roll:**
    *   **THRUST LEVERS** auf ca. 50% N1 vorschieben und Stabilisierung abwarten.
    *   Schubhebel in die **FLEX**- oder **TOGA**-Raste stellen.
    *   **FMA-Check:** **"MAN FLEX"** (oder MAN TOGA), **"SRS"**, **"RWY"**, **"A/THR BLUE"** verifizieren.
    *   Bei VR: Rotieren.
*   **Nach dem Abheben & Departure Handoff:**
    *   Bei positiver Steigrate: **GEAR UP**.
    *   **BeyondATC Handoff:** Bei Anweisung durch den Tower den Frequenzwechsel zu Departure/Radar bestätigen und durchführen.
    *   **Aktivierung des Autopiloten & FCU Logik im Steigflug:** Ab 100 ft AGL kann **AP1** durch Drücken des **AP1**-Buttons an der FCU aktiviert werden.
        *   **Managed Climb (Push / CLB):** Für den Standard-Steigflug gemäß Flugplan den Höhen-Drehknopf (**ALT**-Knopf) an der FCU drücken ("Push"). Im FCU-Display erscheint ein Punkt (Dot) neben der Höhe, das FMA zeigt **CLB**. Das System folgt dem MCDU-Profil unter Beachtung aller Höhen- und Geschwindigkeitsrestriktionen der SID.
        *   **Open Climb (Pull / OP CLB):** Bei Aufhebung von Restriktionen durch ATC (*"cancel level restrictions"*) oder Radar-Vektoren den **ALT**-Knopf ziehen ("Pull"). Der Punkt erlischt, das FMA zeigt **OP CLB**. Das Flugzeug steigt direkt auf die eingedrehte Zielhöhe.
    *   Bei der Thrust Reduction Altitude (meist 1.500 ft AAL) blinkt **LVR CLB** im FMA: **THRUST LEVERS** manuell in die **CLB**-Raste zurückziehen.
    *   **Acceleration Altitude & Clean Up:** Bei Erreichen der Acceleration Altitude senkt sich der Pitch zur Beschleunigung. Beobachtung des Speed Tapes im PFD:
        *   Sobald die Geschwindigkeit die S-Speed übersteigt: Klappen auf **FLAPS 0** einfahren.
        *   Anschließend den Speed-Brake-Hebel manuell nach unten drücken, um die **GND SPOILERS** zu disarmieren.
*   **10.000 ft AAL (Climb):**
    *   **LANDING** Lights auf **OFF**. **NOSE** Light auf **OFF**. **RWY TURN OFF** Lights auf **OFF**.
    *   **SEAT BELTS** auf **OFF** schalten (sofern wetter- und betriebsbedingt möglich).

---

### 5. Cruise, Descent Planning & Approach Setup

> **Airmanship & Workload Management:**
> Die Reiseflugphase dient der frühzeitigen Anflugvorbereitung und dem Briefing (*Aviate, Navigate, Communicate*). Das Energiemanagement hat stets Priorität. Eine Plausibilitätsprüfung des Sinkflugs (3 NM Distanz pro 1.000 ft Höhenverlust) ist durchzuführen.

*   **Reiseflug-Überwachung:** Regelmäßige Überprüfung des Treibstoffs (MCDU PROG Page).
*   **Wetter & Arrival Clearance (BeyondATC Handoff):** Ca. 100 NM vor dem Top of Descent (TOD) ATIS abrufen, Frequenzwechsel via BeyondATC durchführen und Arrival/Approach Clearance bestätigen lassen.
*   **Detailliertes MCDU Arrival Setup:**
    *   Taste **F-PLN** drücken, zum Zielflughafen scrollen und **ARRIVAL** wählen.
    *   Anflugverfahren (z. B. ILS 08R), STAR und VIA auswählen und mit **INSERT** bestätigen.
    *   Flugplan auf **F-PLN DISCONTINUITY** prüfen und gegebenenfalls mit **CLR** bereinigen.
*   **MCDU Performance Setup für den Anflug:**
    *   Taste **PERF** drücken und zur **APPR** Page navigieren.
    *   **QNH**, **TEMP**, **MAG WIND** sowie die **BARO / RADIO** Minimums eintragen.
*   **Sinkflug-Vorbereitung & FCU Bedienung (DES vs. OP DES):**
    *   **FCU Altitude Pre-Select:** Ca. 5–10 NM vor dem Top of Descent (TOD) die freigegebene untere Flughöhe an der **FCU** eindrehen.
    *   **Managed Descent (Push / DES):** Am TOD den **ALT**-Knopf drücken ("Push"). Ein Punkt (Dot) erscheint im FCU-Display, das FMA zeigt **DES**. Das Flugzeug folgt dem berechneten Profil unter Beachtung aller MCDU-Restriktionen.
    *   **Open Descent (Pull / OP DES):** Den **ALT**-Knopf ziehen ("Pull"). Der Punkt erlischt, das FMA zeigt **OP DES**. Das Flugzeug sinkt mit Leerlaufschub direkt auf die eingewählte Höhe.
*   **10.000 ft AAL (Descent):**
    *   **LANDING** Lights auf **ON** schalten.
    *   **SEAT BELTS** auf **ON** schalten.

---

### 6. Approach & Landing

> **Airmanship & Deceleration Tips:**
> Zur Vermeidung von "High and Fast"-Szenarien können bei ATC-Abkürzungen frühzeitig die **SPEED BRAKES** (bis zur Hälfte) in Kombination mit **OP DES** oder das Ausfahren des Fahrwerks (**GEAR DOWN**) als Luftwiderstand genutzt werden.

*   **ATC Freigabe:** Empfang von *"Cleared ILS Approach"* und im Endanflug *"Cleared to land"*.
*   **Verlangsamung & Flaps Timeline:**
    *   Bei Green Dot Speed: **FLAPS 1** setzen. Tasten **LS** und **APPR** an der FCU drücken, um Localizer und Glideslope zu aktivieren.
    *   Bei S-Speed: **FLAPS 2** setzen.
    *   Ca. 2.000 ft AAL (oder 1/2 Dot unter Glideslope): **GEAR DOWN** ausfahren, **GND SPOILERS** armieren, **NOSE** Light auf T.O. und **RWY TURN OFF** Lights auf ON schalten.
    *   Unterhalb VFE für Flaps 3: **FLAPS 3** setzen, gefolgt von **FLAPS FULL** bei F-Speed.
*   **Autobrake & Checklist:** **AUTOBRAKE** auf **MED** oder **LOW** setzen. Landing Checklist abarbeiten.
*   **Deaktivierung des Autopiloten (Manual Landing):**
    *   Sobald die Startbahn in Sicht ist und das Flugzeug stabilisiert im Anflug liegt (typischerweise zwischen 1.000 ft und 500 ft AGL), wird die Steuerung manuell übernommen.
    *   **Hardware-Bedienung:** Das Abschalten erfolgt über den **AP Disconnect Button** am **Winwing Sim URSA Minor** Joystick mittels **Doppelklick**: Der erste Klick trennt den Autopiloten, der zweite Klick quittiert und stoppt die akustische Warnung sofort.
*   **Touchdown:** 
    *   Bei der Ansage *"Retard"* die **THRUST LEVERS** auf **IDLE** ziehen und das Flugzeug abfangen.
    *   Nach dem Aufsetzen: **REVERSERS** (Schubumkehr) auf MAX oder IDLE setzen. Bei 70 Knoten Reverser einfahren, bei 40 Knoten manuell ausrollen.

---

### 7. After Landing, Taxi & Shutdown
Sicheres Einrollen und Abstellen des Flugzeugs am Gate.

*   **Runway Vacated (Nach Verlassen der Startbahn):**
    *   **STROBE** zurück auf **AUTO**, **LANDING** Lights auf **OFF**, **NOSE** Light auf **TAXI**.
    *   **FLAPS** auf **0** einfahren, **GND SPOILERS** disarmieren.
*   **ATC Freigabe:** Rollfreigabe zum Gate via BeyondATC anfordern.
*   **Triebwerkskühlung & APU Start:** Nach Verlassen der Piste **APU MASTER SW** auf **ON** und **APU START** auf **ON** schalten (Triebwerks-Abkühlzeit von ca. 3 Minuten beachten).
*   **Parking / Gate Arrival:**
    *   Am Gate stoppen, **PARKING BRAKE** auf **ON** setzen.
    *   **Lichter zur Vermeidung von Blendschutz (Ground Crew Safety):** Unmittelbar nach dem Anhalten am Gate das **NOSE** Light auf **OFF** und die **RWY TURN OFF** Lights auf **OFF** schalten, um Marshaller, Jetway-Operator und Bodenpersonal nicht zu blenden.
    *   Über das EFB den Jetway anfordern.
    *   Sobald im ECAM *APU AVAIL* angezeigt wird, **APU BLEED auf ON schalten**, um die Klimatisierung nahtlos auf die APU zu übernehmen.

> **Transit- / Turnaround-Hinweis:**
> Wenn ein direkter Weiterflug (Folgesegment) geplant ist, wird der nachfolgende reguläre Shutdown Flow nicht ausgeführt. Stattdessen wird direkt in die [Transit SOP (Abschnitt 1: Arrival, Parking & Transit Setup)](transit-sop.md#1-arrival-parking--transit-setup) gewechselt (APU und APU BLEED verbleiben **ON**, ADIRS verbleiben in **NAV**).

*   **Shutdown Flow:**
    *   **ENG MASTER 1** und **ENG MASTER 2** auf **OFF** schalten.
    *   Nach Stillstand der Triebwerke ($N_1 < 5\%$): **BEACON** Light auf **OFF** schalten (Freigabe für das Bodenpersonal), alle **FUEL PUMPS** auf **OFF** schalten.

*   **Passagiersignale ausschalten:**
    *   **SEAT BELTS** auf **OFF**, **NO SMOKING** auf **OFF**, **EMER EXIT LT** auf **OFF**.

*   **Final Shutdown (Cold & Dark):**
    *   **CREW SUPPLY** auf **OFF**.
    *   ADIRS 1, 2, 3 auf **OFF**.
    *   **NAV & LOGO** Light auf **OFF**.
    *   **APU BLEED** auf **OFF**, **APU MASTER SW** auf **OFF**.
    *   Zuletzt **BAT 1** und **BAT 2** auf **OFF** schalten.

Das Flugzeug befindet sich wieder im vollständigen Cold & Dark Zustand.
