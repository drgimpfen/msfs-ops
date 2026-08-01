# FlyByWire A320NX – Transit Standard Operating Procedures (SOP)

Diese SOP beschreibt die zeitoptimierte **Transit Procedure** (Turnaround) für Multistop-Flüge mit dem **FlyByWire A320NX** im **MSFS 2024** gemäß Airbus FCOM Standard. 

### Zweck & Prozessbeschreibung des Transit-Ablaufs
Bei kurzen Zwischenstopps am Gate (Transit) wird das Flugzeug nicht vollständig heruntergefahren. Der Ablauf ist darauf ausgelegt, die Bodenzeit zu minimieren und das Flugzeug ohne Kaltstart sicher und effizient für das nächste Flugsegment vorzubereiten:
* **Strom- & Zapfluftversorgung:** Die APU läuft durchgehend weiter und übernimmt via **APU BLEED ON** die Klimatisierung sowie die elektrische Versorgung des Flugzeugs. Es ist keine externe Ground Power Unit (GPU) erforderlich.
* **Avionik & Systeme:** Die Trägheitsnavigationssysteme (ADIRS 1, 2, 3) verbleiben im **NAV**-Modus (kein zeitintensives Re-Alignment erforderlich). Sauerstoff (**CREW SUPPLY**) und Notbeleuchtung (**EMER EXIT LT**) verbleiben in ihrer aktiven Betriebsstellung.
* **Ablaufkette:**
  1. **Arrival & Secure:** Ankunft am Gate, Feststellbremse setzen, Übernahme auf APU BLEED und Abstellen der Triebwerke (siehe [Standard SOP – Abschnitt 7: After Landing, Taxi & Shutdown](sop.md#7-after-landing-taxi--shutdown)).
  2. **Ground Handling via EFB:** Deboarding der aussteigenden Passagiere, Refueling (Betankung bei laufender APU) und anschließendes Boarding des Folgesegments.
  3. **FMGS / MCDU Transit Setup:** Bereinigung des alten Flugplans durch Initialisierung des neuen SimBrief-Uplinks und Neuprogrammierung von Flugplan, Performance- und Gewichtsdaten.
  4. **Departure Transition:** Nahtloser Übergang in den Triebwerksstart und Pushback der [Standard SOP – Abschnitt 2: Engine Start & Pushback](sop.md#2-engine-start--pushback).

---

## Inhaltsverzeichnis
- [1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup)
- [2. Deboarding, Refueling & Boarding via EFB (FlyPad)](#2-deboarding-refueling--boarding-via-efb-flypad)
- [3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)](#3-mcdu-reset--komplett-neuprogrammierung-transit-setup)
- [4. Übergang zurück in die Standard-SOP](#4-übergang-zurück-in-die-standard-sop)

---

### 1. Arrival, Parking & Transit Setup
Nachdem das Flugzeug am Gate positioniert, die Parkbremse gesetzt und die Klimatisierung auf APU BLEED übernommen wurde (siehe [Standard SOP – Abschnitt 7: After Landing, Taxi & Shutdown](sop.md#7-after-landing-taxi--shutdown)), beginnt der Transit-Prozess ohne vollständiges Herunterfahren des Flugzeugs:

*   **Triebwerks-Abstellung & Stromversorgung (APU Continuous):**
    *   Die Triebwerke nacheinander abschalten (**ENG MASTER 1** und **2** auf **OFF**).
    *   Da die APU bereits während des Einrollens gestartet wurde und **APU BLEED** am Standplatz auf **ON** geschaltet wurde, verbleiben **APU** und **APU BLEED** durchgehend auf **ON**. Es wird komplett auf eine externe GPU verzichtet.
*   **Cockpit Leftover Management & Bodensicherheit (Transit-Zustand):**
    *   **BEACON Light:** Sobald die Triebwerke auslaufen ($N_1 < 5\%$), das **BEACON** Light auf **OFF** schalten (Freigabe für die Bodencrew, dass gefahrlos am Flugzeug gearbeitet werden kann).
    *   **Anti-Glare & Ground Crew Safety:** **NOSE** Light und **RWY TURN OFF** Lights werden sofort nach dem Anhalten am Gate auf **OFF** geschaltet, um Marshaller, Jetway-Operator und Bodenpersonal nicht zu blenden.
    *   **Lichter-Management:** **NAV & LOGO** verbleibt auf **1** (oder **2**), **STROBE** auf **AUTO**, **LANDING** Lights auf **OFF**.
    *   **Avionik:** Die Avionik (ADIRS 1, 2, 3) verbleibt während des gesamten Turnarounds im **NAV**-Modus (keine Neuausrichtung erforderlich).
    *   **Passagiersignale:** **SEAT BELTS** auf **OFF** schalten, **NO SMOKING** auf **ON** oder **AUTO** und **EMER EXIT LT** auf **ARM** belassen.

---

### 2. Deboarding, Refueling & Boarding via EFB (FlyPad)
Die Steuerung der Bodenabfertigung erfolgt über das EFB (FlyPad), während im Hintergrund das FMGS vorbereitet wird.

*   **Deboarding (Passagierwechsel):**
    *   Im FlyPad das Menü *Ground Services* oder *Fuel/Payload* öffnen.
    *   Den **Deboarding**-Prozess starten und das Absinken der Passagier- und Frachtanzahl auf Null abwarten.
*   **Refueling (Betankung bei laufender APU / Hot Refueling):**
    *   Bei durchlaufender APU kann direkt mit dem Betanken fortgefahren werden.
    *   Im EFB (oder via SimBrief-Integration) den neuen Flugplan und die Gewichtsdaten für das Folgesegment laden.
    *   Das neue **Block Fuel** eintragen und den **Refueling**-Prozess starten. Der Tankvorgang wird über die Fuel-Anzeige im ECAM überwacht.
*   **Boarding für das Folgesegment:**
    *   Sobald das Refueling abgeschlossen ist und die neuen Passagier- und Frachtdaten geladen sind, den **Boarding**-Prozess starten.

---

### 3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)
Für das Folgesegment muss das FMGS bereinigt und vollständig neu programmiert werden.

*   **ATC IFR Clearance (BeyondATC):**
    *   Vor Abschluss des Boardings Delivery via BeyondATC kontaktieren: *"Request IFR Clearance"*. Die neue Freigabe, initiale Steigflughöhe und den neuen Squawk-Code an der FCU bzw. am Transponder einstellen.
*   **Bereinigung des alten Flugplans (Detaillierter Reset-Workflow):**
    *   Im FlyByWire A320NX dient der **INIT-A-Uplink** als primärer Reset-Mechanismus:
    *   Taste **INIT** drücken und über den Line Select Key (LSK) neben **INIT REQUEST** die neuen SimBrief-Daten für das Folgesegment anfordern.
    *   Das System erkennt automatisch das neue *FROM/TO*-Paar. Durch Bestätigen/Überschreiben der INIT-A-Seite löscht und ersetzt das FMGS den alten Flugplan-Verlauf automatisch.
    *   *Alternative (manueller Clean-up in der F-PLN Seite):* Falls Reste des alten Flugplans im **F-PLN** verbleiben, die Taste **F-PLN** drücken, den alten Abflughafen oder verbliebenen Wegpunkt auswählen, **CLR** drücken und auf den entsprechenden LSK klicken, bis eine saubere Ausgangsbasis entsteht.
*   **Detaillierte Neuprogrammierung der MCDU:**
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
        *   Die neue Start-Trimmung bei **THS/FLAPS** eintragen (z. B. `1/UP0.5`).
        *   *Hinweis zur APPR Phase:* Die **APPR**-Seite bleibt am Boden unberührt; sie wird laut Standard-SOP erst im Sinkflug ausgefüllt.

---

### 4. Übergang zurück in die Standard-SOP
Sobald die MCDU-Programmierung abgeschlossen ist, das Boarding dem Ende zugeht und das Cockpit vorbereitet ist, erfolgt der Übergang zurück in die reguläre [Standard Operating Procedures (SOP)](sop.md):

*   **Nahtloser Anschluss:** 
    *   Abschließende Schritte des Boardings durchführen (Schließen der Türen über das EFB).
    *   Da die APU bereits läuft und **APU BLEED** bereits auf **ON** steht, entfällt der APU-Startschritt und die Druckluftversorgung für den Triebwerksstart ist sofort verfügbar.
    *   Die Prozedur wechselt an dieser Stelle direkt zu [Standard SOP – Abschnitt 2: Engine Start & Pushback](sop.md#2-engine-start--pushback) für das Einholen der Pushback- / Start-Freigabe und das Einschalten des **BEACON** Lights. Nach dem erfolgreichen Anlassen beider Triebwerke werden **APU BLEED** und **APU MASTER SW** gemäß Standard-SOP auf **OFF** geschaltet.
    *   Der Flug wird ab diesem Punkt exakt nach der Haupt-SOP fortgeführt.
