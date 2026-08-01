# FlyByWire A320NX – Standard Operating Procedures (SOP)
Willkommen im Flight Deck, Captain! Im Folgenden findest du die detaillierten und streng an realen Airline-SOPs angelehnten Verfahren für den FlyByWire A320NX. Diese Anleitung führt dich chronologisch durch einen kompletten Flug, fokussiert auf korrekte Systembedienung, das Management der Außenlichter und Passagiersignale, ATC-Kommunikation und die präzise Bedienung des Autopiloten (FCU-Logik). Besonderes Augenmerk liegt auf der Nutzung des EFB (FlyPad) und der korrekten Bedienung deines "Winwing Sim URSA Minor" Joysticks.

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
Wir starten am Gate. Das Flugzeug ist komplett stromlos. Das primäre Ziel ist es, das Flugzeug zu bestromen, die Bodenabfertigung zu koordinieren und das FMGS (Flight Management Guidance System) zu programmieren.

*   **Elektrik einschalten:** Auf dem Overhead Panel nacheinander **BAT 1** und **BAT 2** einschalten. Das FlyPad (EFB) an der linken Seite hochfahren.
*   **Initiale Lichter am Boden:** Direkt nach der Bestromung zwingend das **NAV & LOGO** Light auf **1** (oder 2) schalten. Dies zeigt dem Bodenpersonal, dass das Flugzeug nun elektrisch versorgt wird.
*   **Ground Services (via FlyPad):** Gehe im EFB in das Ground/Service-Menü. Fordere die Ground Power Unit (GPU) an. Sobald am Overhead das grüne *AVAIL*-Licht leuchtet, **EXT PWR** drücken (leuchtet nun blau *ON*).
    *   Docke über das EFB den Jetway (Fluggastbrücke) an das Flugzeug an.
    *   Wechsle im FlyPad in das Menü *Fuel/Payload*. Lade die SimBrief-Daten und starte das *Refueling* (Betankung) sowie den *Boarding*-Prozess für Passagiere und Fracht.
*   **Overhead Panel Setup:** 
    *   **CREW SUPPLY** (Sauerstoff) auf **ON**.
    *   Alle sechs **FUEL PUMPS** (L TK, C TK, R TK) auf **ON**.
    *   Passagier- und Notfallsignale: **EMER EXIT LT** auf **ARM** setzen. **NO SMOKING** (bzw. **NO PORTABLE ELEC DEVICE**) auf **ON** oder **AUTO** setzen. **SEAT BELTS** auf **ON** setzen (die Passagiere betreten das Flugzeug).
*   **ATC IFR Clearance:** Kontaktiere Delivery via BeyondATC: *"Request IFR Clearance"*. Du erhältst Freigabe, Route, initialen Steigflug und den Squawk-Code. Drehe die initiale Freigabehöhe in das FCU (Flight Control Unit) ein.
*   **Initialisierung ADIRUs:** Auf dem Overhead Panel die drei Schalter des ADIRS nacheinander (1, dann 2, dann 3) von OFF auf **NAV** drehen.
*   **Detailliertes MCDU / FMGS Setup:** 
    *   **SimBrief Uplink (AOC):** Drücke die physische Taste **MCDU MENU** $\rightarrow$ drücke den Line Select Key (LSK) **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ LSK **INIT DATA REQ**.
    *   **INIT A Page:** Drücke die physische Taste **INIT**. Drücke den LSK neben **INIT REQUEST**. Das System füllt **FROM/TO**, **FLT NBR**, **COST INDEX** und **CRZ FL** aus.
    *   **F-PLN (Flight Plan):** Drücke die Taste **F-PLN**. 
        *   Drücke den linken LSK neben deinem Startflughafen $\rightarrow$ wähle LSK **DEPARTURE** $\rightarrow$ wähle deine Runway und SID (gemäß ATC Clearance) $\rightarrow$ drücke LSK **INSERT**.
    *   **INIT B Page:** Drücke erneut **INIT**, danach die Taste **NEXT PAGE** (oder die rechte Pfeiltaste). Drücke den rechten LSK neben **ZFW/ZFWCG** und zweimal den rechten LSK neben **BLOCK**, um den SimBrief-Spritwert zu übernehmen.
    *   **PERF Page:** Drücke die Taste **PERF**. Trage die V-Speeds (**V1**, **VR**, **V2**) ein, die du im FlyPad berechnet hast (Werte tippen, linken LSK drücken). Trage die **FLEX TO TEMP** in den entsprechenden rechten LSK ein. Trage die Flap/Trim-Einstellung bei **THS/FLAPS** ein (z.B. `1/UP0.5`) und bestätige mit dem LSK.
*   **Abschluss des Boardings:** Wenn das EFB anzeigt, dass das Boarding abgeschlossen ist, entferne den Jetway über das EFB. Die Türen werden geschlossen.

---

### 2. Engine Start & Pushback
Das Flugzeug ist bereit für das Zurückschieben und den Triebwerksstart.

*   **APU Start:** Ca. 10 Minuten vor Pushback **APU MASTER SW** auf **ON**, dann **APU START** auf **ON**. Sobald im ECAM *APU AVAIL* steht: **APU BLEED** auf **ON**. 
*   **EXT PWR** am Overhead abschalten und über das EFB abkoppeln lassen.
*   **ATC Freigabe:** Bei BeyondATC (GND): *"Request Pushback and Engine Start"*.
*   **Warnlichter (WICHTIG):** Unmittelbar BEVOR die Chocks entfernt werden, zwingend das **BEACON** Light auf **ON** schalten! Das rote Blinklicht ist das internationale Zeichen für Bodencrews: "Achtung, das Flugzeug steht unter Druck und die Triebwerke werden gleich angelassen!"
*   **Before Start Flow & Checklist:** Before Start Checklist (Down to the line / Below the line) abarbeiten.
*   **Reale Anlassprozedur der Triebwerke:**
    *   Den **ENG MODE SELECTOR** (Mittelkonsole) auf **IGN/START** drehen.
    *   **ENG MASTER 2** auf **ON** schieben. 
    *   *Überwachung:* N2 steigt. Zündung, gefolgt von Fuel Flow und EGT-Anstieg. 
    *   Sobald Triebwerk 2 stabil läuft (*AVAIL* auf dem ECAM), **ENG MASTER 1** auf **ON** schieben.
    *   Nachdem beide Triebwerke stabil laufen (*AVAIL*): **ENG MODE SELECTOR** zurück auf **NORM**.
    *   **APU BLEED** auf **OFF** und **APU MASTER SW** auf **OFF**.

---

### 3. Taxi & Vorbereitung zum Start

*   **ATC Freigabe:** Bei BeyondATC: *"Request Taxi"*.
*   **Lichter für das Rollen:** Sobald wir uns aus eigener Kraft bewegen, schalten wir das **NOSE** Light auf **TAXI** und die **RWY TURN OFF** Lights auf **ON**.
*   **After Start Flow / T/O Config:**
    *   **FLAPS** auf die berechnete Start-Einstellung setzen (z.B. **FLAPS 1**).
    *   **GND SPOILERS** armieren (Speed Brake Hebel nach oben ziehen).
    *   **PITCH TRIM** Wheel auf den berechneten CG-Wert aus der MCDU setzen (z. B. 0.5 UP).
    *   **AUTOBRAKE** auf **MAX** setzen.
*   **Flight Controls Check:** ECAM F/CTL Page überwachen: Stick Full Up, Down, Neutral. Stick Full Left, Right, Neutral. Rudder Pedals Full Left, Right, Neutral.
*   **Flight Instruments Check:** Drücke den blauen **T/O CONFIG** Button auf der Mittelkonsole (Memos müssen grün sein, kein blau).

---

### 4. Takeoff & Departure
Wir erreichen den Holding Point der Startbahn.

*   **ATC Freigabe:** Melde bei BeyondATC *"Ready for Departure"*. Warte auf *"Line up and wait"* oder *"Cleared for Takeoff"*.
*   **Lichter für den Startlauf (Line-up):** Beim Einrollen auf die Startbahn:
    *   **STROBE** auf **ON**.
    *   **LANDING** Lights (beide) auf **ON**.
    *   **NOSE** Light von TAXI auf **T.O.** (Takeoff).
*   **Takeoff Roll:**
    *   **THRUST LEVERS** vorschieben auf ca. 50% N1. Warten auf Stabilisierung.
    *   Dann die Hebel in die **FLEX** oder **TOGA** Detent rasten.
    *   **FMA-Check:** **"MAN FLEX"** (oder MAN TOGA), **"SRS"**, **"RWY"**, **"A/THR BLUE"**.
    *   Bei VR: Rotieren.
*   **Nach dem Abheben:**
    *   Positive Rate: **GEAR UP**.
    *   **Aktivierung des Autopiloten & FCU Logik im Steigflug:** Ab 100 ft AGL darf der **AP1** aktiviert werden (meist zwischen 400 ft und Thrust Reduction Altitude). Ein Drücken des **AP1** Buttons koppelt den Autopiloten ein.
        *   **Managed Climb (Push / CLB):** Für den Standard-Steigflug gemäß Flugplan drückst du den Höhen-Drehknopf (**ALT**-Knopf) am FCU in Richtung Panel ("Push"). Im FCU-Display erscheint neben der Höhe nun ein **kleiner Punkt** (Dot). Das FMA zeigt **CLB**. Das System folgt dem MCDU-Profil und respektiert alle Höhen- und Geschwindigkeitsrestriktionen der SID (z.B. max 5000 ft).
        *   **Open Climb (Pull / OP CLB):** Wenn dir der Lotse sagt *"cancel level restrictions"* oder dir Radar-Vektoren abseits deiner Route gibt, ziehst du den **ALT**-Knopf zu dir heran ("Pull"). Der **Punkt** verschwindet. Das FMA zeigt **OP CLB**. Das Flugzeug steigt nun direkt und ohne Beachtung von MCDU-Wegpunkt-Restriktionen auf die eingedrehte Höhe.
    *   Bei der Thrust Reduction Altitude (meist 1.500 ft AAL) blinkt **LVR CLB** im FMA. **THRUST LEVERS** manuell in die **CLB** Detent zurückziehen.
    *   **Acceleration Altitude & Clean Up:** Erreicht das Flugzeug die Acceleration Altitude, senkt sich der Pitch ab, um von der Startgeschwindigkeit auf die anfängliche Steigfluggeschwindigkeit (z.B. 250 Knoten) zu beschleunigen. Beobachte das Speed Tape im PFD:
        *   Wenn du mit **FLAPS 1** gestartet bist, warte, bis die Geschwindigkeit das grüne **"S"** (S-Speed) übersteigt, und setze dann die Klappen auf **FLAPS 0**.
        *   Unmittelbar danach drückst du den Speed-Brake-Hebel physisch nach unten, um die **GND SPOILERS** zu disarmieren (der weiße Ring erlischt).
*   **10.000 ft AAL (Climb):**
    *   **LANDING** Lights auf **OFF**. **NOSE** Light auf **OFF**. **RWY TURN OFF** Lights auf **OFF**.
    *   **SEAT BELTS** auf **OFF** (sofern das Wetter und die ATC es zulassen).

---

### 5. Cruise, Descent Planning & Approach Setup

> **Airmanship & Workload Management:**
> Die "Quiet Zone" im Cruise ist ideal für das Approach Setup und Briefing. Bereite den Anflug frühzeitig vor! *Aviate, Navigate, Communicate.* Das Energy Management hat stets Vorrang. Plane mentale Windkorrekturen ein und überprüfe die Plausibilität deines Sinkflugs (3 NM Distanz pro 1.000 ft Höhenverlust).

*   **Reiseflug-Überwachung:** Regelmäßig Fuel Check durchführen (MCDU PROG Page).
*   **Wetter & Arrival Clearance:** Etwa 100 NM vor dem Top of Descent (TOD) ATIS abrufen und Arrival/Approach Clearance von BeyondATC bestätigen lassen.
*   **Detailliertes MCDU Arrival Setup:**
    *   Drücke die **F-PLN** Taste, scrolle zum Zielflughafen, wähle **ARRIVAL**.
    *   Bestimme Approach (z.B. ILS 08R), STAR und VIA, drücke **INSERT**.
    *   Prüfe auf **F-PLN DISCONTINUITY** und entferne diese gegebenenfalls mit **CLR** und dem entsprechenden LSK.
*   **MCDU Performance Setup für den Anflug:**
    *   Drücke **PERF** und navigiere zur **APPR** Page.
    *   Trage **QNH**, **TEMP**, **MAG WIND** sowie die **BARO / RADIO** Minimums ein.
*   **Sinkflug einleiten & FCU Bedienung (DES vs. OP DES):**
    *   **Managed Descent (Push / DES):** Drücke den **ALT**-Knopf nach vorne ("Push"). Ein **Punkt** (Dot) erscheint neben der Zielhöhe, FMA zeigt **DES**.
        *   *Wann nutzen?* Bei Vorhandensein einer Profilfreigabe (z.B. *"Descend via STAR"*). Das Flugzeug folgt dem wirtschaftlichen Idle-Profil unter strikter Beachtung aller MCDU-Restriktionen.
    *   **Open Descent (Pull / OP DES):** Ziehe den **ALT**-Knopf zum Piloten ("Pull"). Der **Punkt** erlischt, FMA zeigt **OP DES**.
        *   *Wann nutzen?* Bei Radar-Vektoren, Aufhebung von Restriktionen durch die ATC (*"cancel level restrictions"*) oder wenn das Flugzeug zu hoch auf dem Profil liegt. Die Triebwerke gehen direkt auf IDLE und das Flugzeug sinkt so schnell wie möglich.
*   **10.000 ft AAL (Descent):**
    *   **LANDING** Lights auf **ON**.
    *   **SEAT BELTS** auf **ON** (Kabine auf die Landung vorbereiten).

---

### 6. Approach & Landing

> **Airmanship & Deceleration Tips:**
> Vermeide "High and Fast"-Szenarien. Nutze bei unerwarteten ATC-Abkürzungen frühzeitig die **SPEED BRAKES** (bis zur Hälfte) in Kombination mit **OP DES**, oder fahre das Fahrwerk (**GEAR DOWN**) als massiven Luftwiderstand aus.

*   **ATC Freigabe:** Empfang von *"Cleared ILS Approach"* und im Endanflug *"Cleared to land"*.
*   **Verlangsamung & Flaps Timeline:**
    *   Bei Erreichen der Green Dot Speed: **FLAPS 1** setzen. **LS** und **APPR** Buttons am FCU drücken, um Localizer und Glideslope einzufangen.
    *   Bei S-Speed: **FLAPS 2**.
    *   Ca. 2.000 ft AAL (oder 1/2 Dot unter Glideslope): **GEAR DOWN** fahren, **GND SPOILERS** armieren, **NOSE** auf T.O. und **RWY TURN OFF** auf ON.
    *   Unterhalb VFE für Flaps 3: **FLAPS 3**, gefolgt von **FLAPS FULL** bei F-Speed.
*   **Autobrake & Checklist:** **AUTOBRAKE** auf **MED** oder **LOW** setzen. Landing Checklist abarbeiten.
*   **Deaktivierung des Autopiloten (Manual Landing):**
    *   Sobald die Bahn in Sicht ist und das Flugzeug stabilisiert im Anflug liegt (typisch zwischen 1.000 ft und 500 ft AGL), wird manuell übernommen.
    *   **Hardware-Nutzung:** Nutze hierfür exklusiv den **AP Disconnect Button** an deinem **Winwing Sim URSA Minor** Joystick im **zweifachen Klick (Double-Click)**: Der erste Klick trennt den AP (Warnsignal ertönt), der zweite Klick quittiert und stoppt den Alarm sofort.
*   **Touchdown:** 
    *   Bei *"Retard"* die **THRUST LEVERS** auf **IDLE** ziehen und das Flugzeug ausflare.
    *   Nach Aufsetzen: **REVERSERS** (Schubumkehr) auf MAX oder IDLE setzen. Bei 70 Knoten Reverser einfahren, bei 40 Knoten manuell ausrollen.

---

### 7. After Landing, Taxi & Shutdown
Wir bringen das Flugzeug sicher ans Gate.

*   **Runway Vacated (Nach Verlassen der Startbahn):**
    *   **STROBE** auf AUTO/OFF, **LANDING** Lights auf OFF, **NOSE** auf TAXI.
    *   **FLAPS** auf **0** eingefahren, **GND SPOILERS** disarmiert.
*   **ATC Freigabe:** Taxi zum Gate anfordern.
*   **Triebwerkskühlung & APU Start:** Nach Verlassen der Bahn direkt **APU MASTER SW** auf **ON** und **APU START** auf **ON** schalten (warten auf Triebwerks-Cool-Down ca. 3 Minuten).
*   **Parking / Gate Arrival:**
    *   Am Gate stoppen, **PARKING BRAKE** auf **ON**.
    *   Über das EFB Chocks setzen und Jetway anfordern.
    *   Sobald im ECAM *APU AVAIL* angezeigt wird, **zwingend APU BLEED auf ON schalten**, damit die Klimatisierung nahtlos von den Triebwerken auf die APU übergeht (alternativ **EXT PWR** über das EFB verbinden).
*   **Shutdown Flow:**
    *   **ENG MASTER 1** und **ENG MASTER 2** auf **OFF** schalten.
    *   Nach Stillstand der Triebwerke (N1 < 5%): **BEACON** Light auf **OFF**, **NOSE / RWY TURN OFF** Lights auf OFF, alle **FUEL PUMPS** auf **OFF**.
*   **Passagiersignale ausschalten:**
    *   **SEAT BELTS** auf **OFF**, **NO SMOKING** auf **OFF**, **EMER EXIT LT** auf **OFF**.
*   **Final Shutdown (Cold & Dark):**
    *   **CREW SUPPLY** auf **OFF**.
    *   ADIRS 1, 2, 3 auf **OFF**.
    *   **NAV & LOGO** Light auf **OFF**.
    *   **APU BLEED** auf **OFF**, **APU MASTER SW** auf **OFF**.
    *   Zuletzt **BAT 1** und **BAT 2** auf **OFF**.

Das Flugzeug befindet sich wieder im Cold & Dark Zustand. Hervorragende Arbeit im Flight Deck, Captain!
