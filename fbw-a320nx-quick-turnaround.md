# FlyByWire A320NX – Quick-Turnaround Standard Operating Procedures (SOP)
Willkommen zurück im Flight Deck, Captain! Diese SOP setzt nahtlos dort an, wo die reguläre Ankunft endet (nach dem Einparken am Gate). Sie beschreibt den professionellen, zeitoptimierten Ablauf für einen "Quick-Turnaround" bei einem Multistop-Leg, um das Flugzeug schnell, sicher und systemeffizient für den nächsten Flug vorzubereiten.

## Inhaltsverzeichnis
- [1. Arrival, Parking & Transit Setup](#1.-arrival,-parking-&-transit-setup)
- [2. Deboarding, Refueling & Boarding via EFB (FlyPad)](#2.-deboarding,-refueling-&-boarding-via-efb-(flypad))
- [3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)](#3.-mcdu-reset-&-komplett-neuprogrammierung-(transit-setup))
- [4. Übergang zurück in die Standard-SOP](#4.-übergang-zurück-in-die-standard-sop)

---

### 1. Arrival, Parking & Transit Setup
Nachdem das Flugzeug am Gate positioniert wurde, wird der Übergang in den Boden- und Transit-Zustand eingeleitet, ohne das Cockpit komplett stromlos zu schalten (kein kompletter Kaltstart nötig).

*   **Parken & Sichern:** 
    *   **PARKING BRAKE** auf **ON**.
    *   Über das FlyPad (EFB) das Anfordern der Chocks und des Jetways (Fluggastbrücke) auslösen.
*   **Stromversorgung & Klimatisierung sicherstellen (APU Continuous):**
    *   Da die APU bereits während des Einrollens bzw. kurz nach der Landung gestartet wurde, läuft sie stabil weiter.
    *   Sicherstellen, dass **APU BLEED** auf **ON** steht (Versorgung von Elektrik und Klimaanlage).
    *   Die Triebwerke werden nacheinander abgeschaltet (**ENG MASTER 1** und **2** auf **OFF**). Es wird im gesamten Turnaround komplett auf eine externe GPU verzichtet.
*   **Cockpit Leftover Management (Transit-Zustand):**
    *   Die Avionik (ADIRS 1, 2, 3) bleibt während des gesamten Turnarounds im **NAV**-Modus eingeschaltet, um eine Neuausrichtung (Alignment) zu sparen.
    *   Lichter-Management für den Boden: **BEACON** Light bleibt auf **ON** (sofern Passagiere an Bord sind oder Bodenarbeiten laufen, alternativ nach Stillstand auf OFF), **NAV & LOGO** bleibt auf **1** (oder **2**), **STROBE** auf **AUTO/OFF**, **LANDING** Lights auf **OFF**.
    *   Passagiersignale: **SEAT BELTS** auf **OFF**, **NO SMOKING** auf **ON** oder **AUTO**, **EMER EXIT LT** auf **ARM** belassen.

---

### 2. Deboarding, Refueling & Boarding via EFB (FlyPad)
Die Bodenabfertigung wird komplett über das EFB (FlyPad) gesteuert, während im Hintergrund das FMGS vorbereitet wird.

*   **Deboarding (Passagierwechsel):**
    *   Öffne das FlyPad und navigiere in das Menü *Ground / Services* oder *Fuel/Payload*.
    *   Starte den **Deboarding**-Prozess. Warte, bis die Passagier- und Frachtanzahl auf Null gesunken ist.
*   **Refueling (Betankung bei laufender APU / Hot Refueling):**
    *   Da die APU durchläuft, können wir direkt mit dem Betanken fortfahren.
    *   Lade im EFB (oder via SimBrief-Integration) den neuen Flugplan / die neuen Gewichtsdaten für das Folgesegment.
    *   Trage das neue **Block Fuel** ein und starte den **Refueling**-Prozess. Überwache den Tankvorgang über die Fuel-Anzeige im ECAM.
*   **Boarding für das Folgesegment:**
    *   Sobald das Refueling abgeschlossen ist und die neuen Passagier- und Frachtdaten im EFB geladen sind, starte den **Boarding**-Prozess.

---

### 3. MCDU Reset & Komplett-Neuprogrammierung (Transit Setup)
Da ein neuer Flug ansteht, muss das FMGS für das neue Leg bereinigt und vollständig neu programmiert werden.

*   **Bereinigung des alten Flugplans (Detaillierter Reset-Workflow):**
    *   Im FlyByWire A320NX ist der alte Flugplan (sowie der durchflogene Teil) noch im System aktiv. Um einen sauberen Neustart zu garantieren, nutzt man den **INIT-A-Uplink** als primären Reset-Mechanismus:
    *   Drücke die physische Taste **INIT** und lade über den Line Select Key (LSK) neben **INIT REQUEST** die neuen SimBrief-Daten für das neue Leg ein. 
    *   Das System erkennt automatisch das neue *FROM/TO*-Paar (z.B. der aktuelle Flughafen als neuer Abflughafen und das neue Ziel). Durch das Bestätigen/Überschreiben der INIT-A-Seite löscht und ersetzt das FMGS im Hintergrund den alten Flugplan-Verlauf automatisch.
    *   *Alternative (manueller Clean-up in der F-PLN Seite):* Falls Reste des alten Flugplans im **F-PLN** verbleiben, drücke die **F-PLN** Taste, wähle den alten Abflughafen oder den ersten verbliebenen Wegpunkt des alten Legs aus, drücke **CLR** und klicke auf den entsprechenden LSK, um den alten Routenstrang abschnittweise zu löschen, bis eine saubere "Departure/Arrival"-Basis entsteht.
*   **Detaillierte Neuprogrammierung der MCDU:**
    *   **INIT A Seite:** Nach dem erfolgreichen Uplink (wie oben beschrieben) prüfen, ob **FROM/TO**, **FLT NBR**, **COST INDEX** und die neue Reiseflughöhe (**CRZ FL**) korrekt übernommen wurden.
    *   **F-PLN Seite:** Drücke die Taste **F-PLN**.
        *   Wähle den Abflughafen $\rightarrow$ wähle LSK **DEPARTURE** $\rightarrow$ wähle die neue Runway und SID gemäß der neuen ATC-Freigabe $\rightarrow$ drücke LSK **INSERT**.
        *   Programmiere das neue Enroute-Routing (oder lade es über den SimBrief-Uplink).
        *   Wähle den Zielflughafen $\rightarrow$ wähle LSK **ARRIVAL** $\rightarrow$ wähle den neuen Approach, die STAR und ggf. das VIA $\rightarrow$ drücke LSK **INSERT**.
        *   Überprüfe den Flugplan auf verbleibende **F-PLN DISCONTINUITY** und entferne diese mit **CLR** und dem jeweiligen LSK.
    *   **INIT B Seite:** Drücke erneut **INIT** und wechsle zur Seite 2 (bzw. **NEXT PAGE**). Überprüfe das neue **ZFW / ZFWCG** und drücke zweimal den rechten LSK neben **BLOCK**, um das neue SimBrief-Block-Fuel zu übernehmen.
    *   **PERF Seite & APPR Phase:** Drücke die Taste **PERF**. 
        *   Trage die neuen V-Speeds (**V1**, **VR**, **V2**) für den neuen Start ein (berechnet über das EFB).
        *   Trage die neue **FLEX TEMP** ein.
        *   Trage die neue Start-Trimmung bei **THS/FLAPS** ein (z.B. `1/UP0.5`).
        *   Wechsle in die **APPR** Phase (via *NEXT PAGE* in PERF) und trage das aktuelle **QNH**, die **TEMP**, den **MAG WIND** sowie die **BARO / RADIO** Minimums für den neuen Zielflughafen ein.

---

### 4. Übergang zurück in die Standard-SOP
Sobald die MCDU-Programmierung abgeschlossen ist, das Boarding dem Ende zugeht und das Cockpit für den Abflug gerüstet ist, wird nahtlos in die reguläre Standard-SOP zurückgewechselt:

*   **Nahtloser Anschluss:** 
    *   Führe die abschließenden Schritte des Boardings durch (Schließen der Türen über das EFB).
    *   Da die APU bereits läuft, musst du sie nicht erneut starten. Du überspringst den APU-Startschritt und gehst im Leitfaden direkt zu dem Punkt weiter, an dem die Pushback-Freigabe eingeholt wird und das **BEACON** Light auf **ON** geschaltet wird (kurz vor dem Ausrollen / Anlassen der Triebwerke).
    *   Setze den Flug ab diesem Punkt exakt nach der Standard-SOP fort.

Guten Flug auf dem nächsten Leg, Captain!
