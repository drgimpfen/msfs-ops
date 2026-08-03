# FlyByWire A320NX – Standard Operating Procedures (SOP)

Dieser Leitfaden beschreibt die Standard Operating Procedures (SOP) für den **FlyByWire A320NX** im **MSFS 2024**. Er führt präzise und chronologisch durch alle Flugphasen vom Cold & Dark Setup bis zum finalen Shutdown – abgestimmt auf das Zusammenspiel mit ATC (z. B. **BeyondATC**, **VATSIM**, **IVAO**), **SimBrief**, dem **FlyPad (EFB)** und der Nutzung des **Winwing Sim URSA Minor** Hardware-Equipments.

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
Der Flug beginnt im stromlosen Zustand am Gate oder Standplatz. Ziel dieser Phase ist die Herstellung der elektrischen Versorgungsbereitschaft, die Abwicklung der Bodenabfertigung (Betankung, Beladung, Boarding) sowie die vollständige Programmierung und Initialisierung der Navigations- und Flugmanagementsysteme (FMGS/MCDU).

*   **Elektrik einschalten:** Auf dem Overhead Panel nacheinander **BAT 1** und **BAT 2** einschalten. Das FlyPad (EFB) an der linken Seite hochfahren.
*   **Initiale Lichter am Boden:** Direkt nach der Bestromung das **NAV & LOGO** Light auf **1** (oder **2**) schalten. Dies signalisiert dem Bodenpersonal die elektrische Versorgungsbereitschaft des Flugzeugs.
*   **Ground Services (via FlyPad):** Im EFB in das Menü *Ground Services* wechseln. Die Ground Power Unit (GPU) anfordern. Sobald am Overhead Panel das grüne *AVAIL*-Licht leuchtet, **EXT PWR** drücken (leuchtet blau *ON*).
    *   Über das EFB den Jetway (Fluggastbrücke) an das Flugzeug andocken.
    *   Im FlyPad in das Menü *Fuel/Payload* wechseln, SimBrief-Daten laden und das *Refueling* (Betankung) sowie den *Boarding*-Prozess für Passagiere und Fracht starten.
*   **Overhead Panel Setup:** 
    *   **CREW SUPPLY** (Sauerstoff) auf **ON** schalten.
    *   Alle sechs **FUEL PUMPS** (L TK, C TK, R TK) auf **ON** schalten.
    *   Passagier- und Notfallsignale: **EMER EXIT LT** auf **ARM** setzen. **NO SMOKING** (bzw. **NO PORTABLE ELEC DEVICE**) auf **ON** oder **AUTO** setzen. **SEAT BELTS** auf **ON** setzen.
*   **ATC IFR Clearance:** Einholen der Streckenfreigabe bei ATC (Delivery): *"Request IFR Clearance"*. Nach Erhalt von Route, initialer Steigflughöhe und Squawk-Code die freigegebene Höhe an der FCU (Flight Control Unit) eindrehen.
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
Diese Phase umfasst die unmittelbare Startvorbereitung. Ziel ist die Inbetriebnahme der Hilfskraftanlage (APU), die Abkopplung von Bodenstrom und Bodenabfertigung, die Durchführung des Zurückschiebens (Pushback) sowie das sichere Anlassen beider Triebwerke.

*   **APU Start (ca. 10 Min vor Pushback):**
    *   **APU MASTER SW** auf **ON** schalten.
    *   **APU START** auf **ON** schalten (ON-LED leuchtet).
    *   Sobald auf dem ECAM *APU AVAIL* leuchtet: **APU BLEED** auf **ON** schalten (Zapfluft- & Klimatisierungsübernahme).
*   **Bodenstrom trennen (GPU Disconnect):**
    *   **EXT PWR** am Overhead Panel auf **OFF** schalten (blaue ON-Anzeige erlischt, grüne AVAIL-Anzeige bleibt).
    *   Im FlyPad (EFB) unter *Ground Services* die Bodenstromversorgung (GPU) abkoppeln lassen.
*   **ATC Freigabe & Beacon Light:**
    *   Bei ATC (GND): *"Request Pushback and Engine Start"* anfordern.
    *   Nach Erhalt der Freigabe (*"Pushback and Engine Start approved"*) das **BEACON** Light auf **ON** schalten. Das rote Blinklicht signalisiert dem Vorfeldverkehr den unmittelbaren Beginn der Pushback- und Anlasssequenz.
*   **Before Start Flow & Checklist:**
    *   **THRUST LEVERS:** Verifizieren, dass beide Schubhebel in der **IDLE**-Raste stehen.
    *   **PARKING BRAKE:** Bleibt vorerst auf **ON** gesetzt.
    *   Before Start Checklist abarbeiten.
*   **Pushback-Initiierung & Schlepper-Kopplung:**
    *   Pushback-Vorgang über das EFB, den MSFS-Groundservice oder BeyondATC/Toolbar-Pushback auslösen.
    *   Das Ankoppeln des Schleppers abwarten.
    *   Sobald die Bodencrew / der Schlepper meldet: *"Pushback tractor connected, release parking brake"*:
        *   **PARKING BRAKE** auf **OFF** schalten.
*   **Triebwerksanlass-Prozedur (Engine Start Flow):**
    *   Den **ENG MODE SELECTOR** (Mittelkonsole) von NORM auf **IGN/START** drehen (ECAM schaltet automatisch auf die ENG-Seite um und zeigt Zapfluftdruck an).
    *   **Start Triebwerk 2 (Rechtes Triebwerk zuerst):**
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
    *   Entkoppeln des Schleppers bestätigen lassen und auf das finale Signal der Bodencrew (Bypass-Pin gezeigt) an der Cockpit-Seite achten.

---

### 3. Taxi & Vorbereitung zum Start
Diese Phase beinhaltet das Einrollen zur aktiven Startbahn. Ziel ist das sichere Manövrieren am Boden, das Konfigurieren aller flight-relevanten Systeme (Klappen, Trimming, Spoilers, WXR/TCAS) sowie die finale technische Startüberprüfung (T/O Config & Flight Controls Check).

*   **ATC Freigabe & Rollbeleuchtung:** Bei ATC: *"Request Taxi"*. Nach Erhalt der Rollfreigabe im *After Start / Taxi Flow* das **NOSE** Light auf **TAXI** schalten. Beim Rollen auf oder über Landebahnen und Taxiways zusätzlich die **RWY TURN OFF** Lights auf **ON** schalten.
*   **After Start Flow / T/O Config:**
    *   **FLAPS** auf die berechnete Start-Einstellung setzen (z. B. **FLAPS 1**).
    *   **GND SPOILERS** armieren (Speed Brake Hebel nach oben ziehen).
    *   **PITCH TRIM** Wheel auf den berechneten CG-Wert aus der MCDU einstellen (z. B. 0.5 UP).
    *   **AUTOBRAKE** auf **MAX** setzen.
*   **Wetterradar & Anti-Ice Setup:**
    *   **WXR RADAR PANEL:** **SYS** auf **1** (oder **2**), **PWS** auf **AUTO**, **MODE** auf **WX** oder **WX+T** stellen.
    *   **ENG ANTI ICE:** Bei OAT $\le 10^\circ\text{C}$ und sichtbarer Feuchtigkeit (Nebel, Regen, Schnee, Nässe am Boden) **ENG ANTI ICE 1 & 2** auf **ON** schalten.
*   **Transponder & TCAS Setup:**
    *   **ATC / XPDR MODE:** Auf **AUTO** (oder **ON**) stellen.
    *   **ALT RPTG:** Auf **ON** stellen.
    *   **TCAS MODE:** Auf **TA/RA** stellen.
*   **Flight Controls Check:** ECAM F/CTL Page überwachen: Stick Full Up, Down, Neutral; Stick Full Left, Right, Neutral; Rudder Pedals Full Left, Right, Neutral.
*   **Flight Instruments & T/O CONFIG Test:** Den blauen **T/O CONFIG** Button auf der Mittelkonsole **einmalig** drücken. Dies testet die technische Startkonfiguration (Klappen, Trimmung, Spoiler). Die ECAM-Zeile **CABIN READY** verbleibt vorerst auf blau **CHECK**, bis das Kabinensignal eintrifft.
*   **Brake Fan Check:** ECAM WHEEL-Seite prüfen. Verifizieren, dass die Bremstemperaturen unter 150°C liegen und **BRK FAN** auf **OFF** steht.

---

### 4. Takeoff & Departure
Ankunft am Holding Point und Durchführung des Startlaufs. Ziel dieser Phase ist das Einholen der Startfreigabe, das Herstellen der Startkonfiguration und Triebwerksleistung, der sichere Abhebevorgang sowie der Erststeigflug und die Übergangsanpassung im Steigprofil (Thrust Reduction & Clean-Up).

*   **ATC Freigabe:** Bei ATC *"Ready for Departure"* melden. Auf *"Line up and wait"* oder *"Cleared for Takeoff"* warten.
*   **Lichter & System-Check für den Startlauf (Line-up):** Beim Einrollen auf die Startbahn:
    *   **STROBE** von AUTO auf **ON** schalten.
    *   **LANDING** Lights (beide) auf **ON** schalten.
    *   **NOSE** Light von TAXI auf **T.O.** (Takeoff) schalten.
    *   **CALLS PANEL (Overhead):** Den **ALL**-Knopf drücken (oder **SEAT BELTS** Signs triggern), um der Kabinenbesatzung den unmittelbaren Startlauf zu signalisieren (*"Cabin Crew, take your seats for takeoff"*).
    *   **TCAS & PWS Check:** Verifizieren, dass **TCAS** auf **TA/RA** und **PWS** auf **AUTO** steht.
    *   **ECAM T/O MEMO Sichtprüfung:** Sobald die Kabine bereit ist, wechselt `CABIN READY` im ECAM automatisch auf **grün**. Visuell verifizieren, dass alle Zeilen im ECAM T/O MEMO grün sind.
*   **Takeoff Roll:**
    *   **THRUST LEVERS** auf ca. 50% N1 vorschieben und Stabilisierung abwarten.
    *   Schubhebel in die **FLEX**- oder **TOGA**-Raste stellen.
    *   **FMA-Check:** **"MAN FLEX"** (oder MAN TOGA), **"SRS"**, **"RWY"**, **"A/THR BLUE"** verifizieren.
    *   Bei VR: Rotieren.
*   **Nach dem Abheben & Departure Handoff:**
    *   Bei positiver Steigrate: **GEAR UP**.
    *   **ATC Handoff:** Bei Anweisung durch den Tower den Frequenzwechsel zu Departure/Radar bestätigen und durchführen.
    *   **Aktivierung des Autopiloten & FCU Logik im Steigflug:** Ab 100 ft AGL kann **AP1** durch Drücken des **AP1**-Buttons an der FCU aktiviert werden.
        *   **Managed Climb (Push / CLB):** Für den Standard-Steigflug gemäß Flugplan den Höhen-Drehknopf (**ALT**-Knopf) an der FCU drücken ("Push"). Im FCU-Display erscheint ein Punkt (Dot) neben der Höhe, das FMA zeigt **CLB**. Das System folgt dem MCDU-Profil unter Beachtung aller Höhen- und Geschwindigkeitsrestriktionen der SID.
        *   **Open Climb (Pull / OP CLB):** Bei Aufhebung von Restriktionen durch ATC (*"cancel level restrictions"*) oder Radar-Vektoren den **ALT**-Knopf ziehen ("Pull"). Der Punkt erlischt, das FMA zeigt **OP CLB**. Das Flugzeug steigt direkt auf die eingedrehte Zielhöhe.
    *   Bei der Thrust Reduction Altitude (meist 1.500 ft AAL) blinkt **LVR CLB** im FMA: **THRUST LEVERS** manuell in die **CLB**-Raste zurückziehen.
    *   **Acceleration Altitude & Clean Up:** Bei Erreichen der Acceleration Altitude senkt sich der Pitch zur Beschleunigung. Beobachtung des Speed Tapes im PFD:
        *   Sobald die Geschwindigkeit die S-Speed übersteigt: Klappen auf **FLAPS 0** einfahren.
        *   Anschließend den Speed-Brake-Hebel manuell nach unten drücken, um die **GND SPOILERS** zu disarmieren.
*   **Transition Altitude (Baro Reference Switch):**
    *   Beim Passieren der im MCDU/SID definierten Transition Altitude (Blinken der Baro-Druckanzeige im PFD): den **BARO**-Knopf ziehen (**BARO KNOB PULL**), um von QNH auf **STD** (Standard 1013.25 hPa / 29.92 inHg) umzuschalten.
*   **10.000 ft AAL (Climb):**
    *   **LANDING** Lights auf **OFF**. **NOSE** Light auf **OFF**. **RWY TURN OFF** Lights auf **OFF**.
    *   **SEAT BELTS** auf **OFF** schalten (sofern wetter- und betriebsbedingt möglich).

---

### 5. Cruise, Descent Planning & Approach Setup
Diese Phase umfasst den Reiseflug sowie die Vorbereitung auf die Landung. Ziel ist die kontinuierliche System- und Treibstoffüberwachung, das Einholen der aktuellen Anflugwetterdaten sowie die vollständige MCDU/FCU-Programmierung für den Sink- und Endanflug.

> **Airmanship & Workload Management:**
> Die Reiseflugphase dient der frühzeitigen Anflugvorbereitung und dem Briefing (*Aviate, Navigate, Communicate*). Das Energiemanagement hat stets Priorität. Eine Plausibilitätsprüfung des Sinkflugs (3 NM Distanz pro 1.000 ft Höhenverlust) ist durchzuführen.

*   **Reiseflug-Überwachung:** Regelmäßige Überprüfung des Treibstoffs (MCDU PROG Page).
*   **Wetter & Arrival Clearance (ATC Handoff):** Ca. 100 NM vor dem Top of Descent (TOD) ATIS abrufen, Frequenzwechsel via ATC durchführen und Arrival/Approach Clearance bestätigen lassen.
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
Diese Phase beschreibt den Sink- und Endanflug bis zum Aufsetzen. Ziel ist das Herstellen der Landekonfiguration, das Erfassen des Anflugpfades (z. B. ILS Localizer & Glideslope), der zeitgerechte Übergang in den manuellen Flug sowie die sichere Landung und Abbremsung auf der Piste.

> **Airmanship & Deceleration Tips:**
> Zur Vermeidung von "High and Fast"-Szenarien können bei ATC-Abkürzungen frühzeitig die **SPEED BRAKES** (bis zur Hälfte) in Kombination mit **OP DES** oder das Ausfahren des Fahrwerks (**GEAR DOWN**) als Luftwiderstand genutzt werden.

*   **Initial Approach & LS-Aktivierung:**
    *   **LS Button (EFIS Panel):** Beim Einrollen in den Anflugsektor (vor dem Abfangen des Localizers) die **LS**-Taste am EFIS Control Panel drücken, um die ILS-Skalen (Localizer & Glideslope Rauten) im PFD einzublenden.
    *   Bei Green Dot Speed: **FLAPS 1** setzen.
*   **Approach Clearance & APPR-Aktivierung (FCU):**
    *   Nach Erhalt der Freigabe von ATC (*"Cleared ILS Approach Runway..."*) und auf Intercept-Kurs:
        *   **APPR Button:** Die **APPR**-Taste an der FCU drücken (FMA zeigt `LOC` blau und `G/S` blau).
        *   **AP2 Button:** Zusätzlich die **AP2**-Taste an der FCU drücken, um Dual-Channel Autoland / CAT III vorzubereiten (FMA zeigt `AP 1+2`).
*   **Established-Meldung (ATC Communication):**
    *   Sobald der Localizer abgefangen und zentriert ist (FMA zeigt `LOC` grün): Bei ATC (Approach / Tower) melden: *"Established ILS Runway [Pistenbezeichnung]"*.
*   **Final Approach Sequence & Flaps Timeline:**
    *   Bei S-Speed: **FLAPS 2** setzen.
    *   Ca. 2.000 ft AAL (oder 1/2 Dot unter Glideslope): **GEAR DOWN** ausfahren, **GND SPOILERS** armieren, **NOSE** Light auf T.O. und **RWY TURN OFF** Lights auf ON schalten.
    *   Unterhalb VFE für Flaps 3: **FLAPS 3** setzen, gefolgt von **FLAPS FULL** bei F-Speed.
    *   **AUTOBRAKE:** Auf **MED** oder **LOW** setzen. Landing Checklist abarbeiten.
*   **Deaktivierung des Autopiloten (Manual Landing):**
    *   Sobald die Startbahn in Sicht ist und das Flugzeug stabilisiert im Anflug liegt (typischerweise zwischen 1.000 ft und 500 ft AGL), wird die Steuerung manuell übernommen.
    *   **Autopilot Disconnect:** Das Abschalten erfolgt über den **AUTOPILOT OFF** Button am Joystick mittels Doppelklick: Der erste Klick trennt den Autopiloten, der zweite Klick quittiert und stoppt die akustische Warnung.
*   **Touchdown & Reverser:** Bei der Ansage *"Retard"* die **THRUST LEVERS** auf **IDLE** ziehen. Nach dem Aufsetzen des Hauptfahrwerks **REVERSERS** auf **REV MAX** oder **REV IDLE** setzen. Bei 70 Knoten auf **REV IDLE** zurücknehmen und vor dem Abrollen vollständig auf **IDLE** einfahren.

---

### 7. After Landing, Taxi & Shutdown
Sicheres Einrollen, Abstellen und vollständiges Herunterfahren des Flugzeugs am Gate.

> **Airmanship & Taxi-In Management:**
> * **Runway Vacated:** Nach dem Überrollen der gelben Holding-Linie nicht anhalten. Das Flugzeug rollt flüssig weiter, während die Systeme umgestellt werden und der Funkspruch an Ground erfolgt.
> * **Triebwerks-Abkühlzeit:** Die 3-minütige Abkühlphase bei Idle-Schub schützt die Turbinenwellen vor thermischem Schock. Die Rollzeit vom Verlassen der Piste bis zum Gate wird dabei vollständig als Abkühlzeit angerechnet.

*   **Runway Vacated:**
    *   Sobald die gelbe Holding-Linie vollständig überrollt ist: **STROBE** von ON auf **AUTO** (oder **OFF**), **LANDING** Lights auf **OFF**, **NOSE** Light auf **TAXI**.
    *   **RWY TURN OFF** Lights beim Verlassen des aktiven Rollbahnbereichs auf **OFF** schalten.
    *   **WXR RADAR PANEL:** **SYS** und **PWS** auf **OFF** schalten.
    *   **TCAS & XPDR:** **TCAS MODE** auf **STBY** (oder `TA ONLY`), **ATC/XPDR MODE** auf **AUTO** / **STBY**.
    *   **FLAPS:** Klappen auf **0** einfahren (bei Matsch, Schnee oder Vereisungsgefahr auf den Rollwegen Klappen ausgefahren lassen).
    *   **GND SPOILERS:** Spoilers disarmieren (Hebel manuell nach unten drücken).
    *   **ENG ANTI ICE:** Falls zuvor aktiviert, ausschalten (sofern keine Vereisungsbedingungen auf den Taxiways vorliegen).
*   **Taxi to Gate & APU Management:**
    *   Rollfreigabe zum Gate bei ATC anfordern (*"Request taxi to gate"*).
    *   Ca. 3 Minuten vor Erreichen der Parkposition **APU MASTER SW** auf **ON** und **APU START** auf **ON** schalten.
*   **Parking / Gate Arrival:**
    *   **Ground Crew Safety:** Beim Eindrehen in den Standplatz (Sichtkontakt mit Marshaller / VDGS) das **NOSE** Light (Taxi) auf **OFF** schalten, um den Einweiser nicht zu blenden.
    *   Flugzeug exakt auf der Stop-Markierung anhalten, **PARKING BRAKE** auf **ON** setzen.
    *   Sobald im ECAM *APU AVAIL* leuchtet: **APU BLEED** auf **ON** schalten.
    *   Über das FlyPad (EFB) den Jetway/Fluggastbrücke bzw. die Passagiertreppe anfordern (falls GPU genutzt wird: **EXT PWR** auf **ON** schalten).
    *   **BRK FAN:** ECAM WHEEL-Seite prüfen. Bei Bremstemperaturen über 150°C am Standplatz auf **ON** schalten.
*   **Engine Shutdown Flow:**
    *   **ENG MASTER 1 & 2:** Nach Verifizierung der 3-minütigen Abkühlzeit auf **OFF** schalten.
    *   Sobald die Triebwerke vollständig zum Stillstand gekommen sind ($N_1 < 5\%$): **BEACON** Light auf **OFF** schalten, alle 6 **FUEL PUMPS** auf **OFF** schalten.
    *   **SEAT BELTS** auf **OFF** schalten (akustisches Signal zum Abschnallen und Aussteigen).

> **Transit- / Turnaround-Verfahren:**
> Bei einem unmittelbaren Folgesegment entfällt die nachfolgende Prozedur *Securing the Aircraft*. Der Weiterflug erfolgt direkt gemäß [Transit SOP – Abschnitt 1: Arrival, Parking & Transit Setup](transit-sop.md#1-arrival-parking--transit-setup).

*   **Securing the Aircraft:**
    *   **NO SMOKING** auf **OFF**, **EMER EXIT LT** auf **OFF**.
    *   **APU BLEED** auf **OFF**, **CREW SUPPLY** (Sauerstoff) auf **OFF**.
    *   ADIRS 1, 2, 3 nacheinander auf **OFF**, **NAV & LOGO** Light auf **OFF**.
    *   **Brake Fan Check:** ECAM WHEEL-Seite prüfen. Verifizieren, dass die Bremstemperaturen unter 150°C liegen und **BRK FAN** auf **OFF** steht.
    *   **APU MASTER SW** auf **OFF**.
    *   Zuletzt **BAT 1** und **BAT 2** auf **OFF** schalten.

Das Flugzeug befindet sich wieder im vollständigen, stromlosen Cold & Dark Zustand.
