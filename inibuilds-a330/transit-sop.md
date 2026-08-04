# iniBuilds Airbus A330-300P2F (Cargo) – Transit Standard Operating Procedures (SOP)

Diese SOP beschreibt die zeitoptimierte **Transit Procedure** (Turnaround) für Multistop-Frachtflüge mit dem **iniBuilds Airbus A330-300P2F** (Freighter) im **MSFS 2024** gemäß Airbus FCOM Standard.

### Zweck & Prozessbeschreibung des Transit-Ablaufs
Bei kurzen Zwischenstopps am Cargo Stand (Transit) wird das Frachtflugzeug nicht vollständig heruntergefahren. Der Ablauf ist darauf ausgelegt, die Bodenzeit zu minimieren und das Flugzeug ohne Kaltstart sicher und effizient für das nächste Frachtsegment vorzubereiten:
* **Strom- & Zapfluftversorgung:** Die APU läuft durchgehend weiter und übernimmt via **APU BLEED ON** die Klimatisierung sowie die elektrische Versorgung des Flugzeugs. Es ist keine externe Ground Power Unit (GPU) erforderlich.
* **Avionik & Systeme:** Die Trägheitsnavigationssysteme (ADIRS 1, 2, 3) verbleiben im **NAV**-Modus (kein zeitintensives Re-Alignment erforderlich, ggf. Fast Alignment via MCDU). Sauerstoff (**CREW SUPPLY**) und Notbeleuchtung (**EMER EXIT LT**) verbleiben in ihrer aktiven Betriebsstellung.
* **Ablaufkette des Transits:**
  * **[1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup):** Ankunft am Cargo Standplatz, Feststellbremse setzen, Übernahme auf APU BLEED und Abstellen der Triebwerke.
  * **[2. Cargo Unloading, Refueling & Reloading via EFB](#2-cargo-unloading-refueling--reloading-via-efb):** Main Deck Cargo Door öffnen, Entladung der ULD Container, Refueling (Betankung bei laufender APU) und anschließendes Cargo Loading des Folgesegments.
  * **[3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)](#3-mcdu-reset--komplett-neuprogrammierung-transit-setup):** Bereinigung des alten Flugplans durch Initialisierung des neuen SimBrief-Uplinks und Neuprogrammierung von Flugplan, Performance- und Gewichtsdaten im FMGEC.
  * **[4. Übergang zurück in die Standard-SOP](#4-übergang-zurück-in-die-standard-sop):** Vorbereitung zum Pushback und nahtloser Übergang in den Triebwerksstart der [Standard SOP – Abschnitt 2: Engine Start & Pushback](sop.md#2-engine-start--pushback).

---

## Inhaltsverzeichnis
- [1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup)
- [2. Cargo Unloading, Refueling & Reloading via EFB](#2-cargo-unloading-refueling--reloading-via-efb)
- [3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)](#3-mcdu-reset--komplett-neuprogrammierung-transit-setup)
- [4. Übergang zurück in die Standard-SOP](#4-übergang-zurück-in-die-standard-sop)

---

### 1. Arrival, Parking & Transit Setup
Nachdem das Flugzeug am Cargo Stand positioniert, die Parkbremse gesetzt und die Klimatisierung auf APU BLEED übernommen wurde (siehe [Standard SOP – Abschnitt 7: After Landing, Taxi & Shutdown](sop.md#7-after-landing-taxi--shutdown)), beginnt der Transit-Prozess ohne vollständiges Herunterfahren des Flugzeugs:

*   **Triebwerks-Abstellung & Stromversorgung (APU Continuous):**
    *   Die Großfan-Triebwerke nacheinander abschalten (**ENG MASTER 1** und **2** auf **OFF**, sofern mindestens 3 Minuten Abkühlzeit eingehalten wurden).
    *   Da die APU bereits während des Einrollens gestartet wurde und **APU BLEED** am Standplatz auf **ON** geschaltet wurde, verbleiben **APU** und **APU BLEED** durchgehend auf **ON**. Es wird komplett auf eine externe GPU verzichtet.
*   **Cockpit Leftover Management & Bodensicherheit (Transit-Zustand):**
    *   **BEACON Light:** Sobald die Triebwerke auslaufen ($N_1 < 5\%$), das **BEACON** Light auf **OFF** schalten.
    *   **Anti-Glare & Ground Crew Safety:** **NOSE** Light und **RWY TURN OFF** Lights werden sofort nach dem Anhalten am Cargo Stand auf **OFF** geschaltet, um Marshaller und Bodenpersonal nicht zu blenden.
    *   **Lichter-Management:** **NAV & LOGO** verbleibt auf **1** (oder **2**), **STROBE** auf **AUTO**, **LANDING** Lights auf **OFF**.
    *   **Avionik:** Die Avionik (ADIRS 1, 2, 3) verbleibt während des gesamten Turnarounds im **NAV**-Modus (keine Neuausrichtung erforderlich).
    *   **Signale & Notbeleuchtung:** **NO SMOKING** auf **ON** oder **AUTO** und **EMER EXIT LT** auf **ARM** belassen.
    *   **BRK FAN:** ECAM WHEEL-Seite prüfen. Bei Bremstemperaturen über 150°C am Standplatz auf **ON** schalten.

---

### 2. Cargo Unloading, Refueling & Reloading via EFB
Die Steuerung der Fracht-Bodenabfertigung erfolgt über das iniBuilds EFB (Tablet), während im Hintergrund das FMGEC vorbereitet wird.

*   **Cargo Unloading (Frachtentladung):**
    *   Über das EFB / GSX die **Main Deck Cargo Door** öffnen und Cargo Loaders beistellen lassen.
    *   Den **Unloading**-Prozess starten und die Entladung der ULD Container abwarten.
*   **Refueling (Betankung bei laufender APU / Hot Refueling):**
    *   Bei durchlaufender APU kann direkt mit dem Betanken fortgefahren werden.
    *   Im EFB (oder via SimBrief-Integration) den neuen Flugplan und die Fracht-Gewichtsdaten für das Folgesegment laden.
    *   Das neue **Block Fuel** eintragen und den **Refueling**-Prozess starten. Der Tankvorgang wird über die Fuel-Anzeige im ECAM überwacht.
*   **Cargo Reloading für das Folgesegment:**
    *   Sobald das Refueling abgeschlossen ist und die neuen Frachtdaten geladen sind, den **Cargo Loading**-Prozess starten und ULD Container einladen lassen.

---

### 3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)
Für das Folgesegment muss das FMGEC bereinigt und vollständig neu programmiert werden.

*   **ATC IFR Clearance (ATC):**
    *   Vor Abschluss der Beladung Delivery via ATC kontaktieren: *"Request IFR Clearance"*. Die neue Freigabe, initiale Steigflughöhe und den neuen Squawk-Code an der FCU bzw. am Transponder einstellen.
*   **Bereinigung des alten Flugplans (Detaillierter Reset-Workflow):**
    *   **SimBrief ATSU Uplink:** Taste **MCDU MENU** drücken $\rightarrow$ LSK **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ LSK **INIT DATA REQ** drücken, um die neuen Flugplandaten des Folgesegments bereitzustellen.
    *   **INIT-A-Reset:** Taste **INIT** drücken und den Line Select Key (LSK) neben **INIT REQUEST** betätigen. Das System übernimmt das neue *FROM/TO*-Paar und ersetzt den alten Flugplan-Verlauf automatisch.
    *   **Manuelle Flugplan-Bereinigung:** Falls Reste des alten Flugplans im **F-PLN** verbleiben, die Taste **F-PLN** drücken, den alten Abflughafen oder verbliebenen Wegpunkt auswählen, **CLR** drücken und auf den entsprechenden LSK klicken, bis eine saubere Ausgangsbasis entsteht.
*   **Detaillierte Neuprogrammierung der MCDU / FMGEC:**
    *   **INIT A Seite:** Nach dem Uplink überprüfen, ob **FROM/TO**, **FLT NBR**, **COST INDEX** und die neue Reiseflughöhe (**CRZ FL**) korrekt übernommen wurden.
    *   **F-PLN Seite:** Taste **F-PLN** drücken.
        *   Abflughafen wählen $\rightarrow$ LSK **DEPARTURE** $\rightarrow$ neue Runway und SID gemäß ATC-Freigabe auswählen $\rightarrow$ LSK **INSERT** drücken.
        *   Enroute-Routing programmieren (oder via SimBrief-Uplink laden).
        *   Zielflughafen wählen $\rightarrow$ LSK **ARRIVAL** $\rightarrow$ neuen Approach, STAR und ggf. VIA auswählen $\rightarrow$ LSK **INSERT** drücken.
        *   Flugplan auf verbleibende **F-PLN DISCONTINUITY** prüfen und mit **CLR** bereinigen.
    *   **INIT B Seite:** Erneut **INIT** drücken und zur Seite 2 (**NEXT PAGE**) wechseln. Das neue **ZFW / ZFWCG** überprüfen und zweimal den rechten LSK neben **BLOCK** betätigen, um das neue Block-Fuel zu übernehmen.
    *   **PERF Seite:** Taste **PERF** drücken.
        *   Die neuen V-Speeds (**V1**, **VR**, **V2**) für den bevorstehenden Start eintragen.
        *   Die neue **FLEX TEMP** eintragen.
        *   Die neue Start-Trimmung bei **THS/FLAPS** eintragen (z. B. `1/UP0.8`).

---

### 4. Übergang zurück in die Standard-SOP
Sobald die MCDU-Programmierung abgeschlossen ist, das Cargo Loading dem Ende zugeht und das Cockpit vorbereitet ist, erfolgt der Übergang zurück in die reguläre [Standard Operating Procedures (SOP)](sop.md):

*   **Nahtloser Anschluss:** 
    *   Main Deck Cargo Door über das EFB schließen.
    *   **Brake Fan Check:** ECAM WHEEL-Seite prüfen. Verifizieren, dass die Bremstemperaturen unter 150°C liegen und **BRK FAN** auf **OFF** steht.
    *   Da die APU bereits läuft und **APU BLEED** bereits auf **ON** steht, entfällt der APU-Startschritt und die Druckluftversorgung für den Triebwerksstart ist sofort verfügbar.
    *   Die Prozedur wechselt an dieser Stelle direkt zu [Standard SOP – Abschnitt 2: Engine Start & Pushback](sop.md#2-engine-start--pushback) für das Einholen der Pushback- / Start-Freigabe und das Einschalten des **BEACON** Lights. Nach dem erfolgreichen Anlassen beider Triebwerke werden **APU BLEED** und **APU MASTER SW** gemäß Standard-SOP auf **OFF** geschaltet.
    *   Der Flug wird ab diesem Punkt exakt nach der Haupt-SOP fortgeführt.


