# Headwind Airbus A330-900neo (A339X) – Transit SOP (Turnaround)

Dieses Dokument beschreibt das zeitoptimierte Transit- und Turnaround-Verfahren für den **Headwind Airbus A330-900neo (A339X)** (Passagier) im **MSFS 2024**. Es kommt zum Einsatz, wenn das Flugzeug nach einem Flugabschnitt am Gate verbleibt, nicht vollständig stromlos geschaltet wird und effizient für den nächsten Flugabschnitt (Leg) vorbereitet wird.

> **Voraussetzung:**
> Das Flugzeug wurde gemäß [SOP – Abschnitt 7: After Landing, Taxi & Shutdown](sop.md#7-after-landing-taxi--shutdown) am Gate abgestellt, die Triebwerke sind abgeschaltet, aber die APU (oder externe Stromversorgung GPU) sichert die elektrische und pneumatische Versorgung.

## Inhaltsverzeichnis
- [1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup)
- [2. FMGEC / MCDU Reset & Re-Initialization](#2-fmgec--mcdu-reset--re-initialization)
- [3. Pre-Departure Flow & Fast Cockpit Prep](#3-pre-departure-flow--fast-cockpit-prep)

---

### 1. Arrival, Parking & Transit Setup
Ziel dieses Abschnitts ist die schnelle Sicherung des Flugzeugs am Boden bei aufrechterhaltener Strom- und Zapfluftversorgung, während das Aussteigen der Passagiere (Deboarding) beginnt.

*   **APU Bleed & Power Check:** Verifizieren, dass **APU BLEED** auf **ON** steht (bzw. **EXT PWR** angeschlossen und auf **ON** ist).
*   **Lights:** **BEACON** Light auf **OFF** schalten (Freigabe für Bodenpersonal/Jetway). **NAV & LOGO** bleibt auf **1** (oder **2**).
*   **Deboarding & Ground Services (via flyPad):**
    *   Über das FlyByWire flyPad (EFB) den Jetway ankoppeln und das Passagier-Deboarding auslösen.
    *   Treibstoff- und Catering-Services via flyPad/GSX initiieren.
*   **ADIRS Continuous Alignment:** Die drei ADIRS-Schalter bleiben auf **NAV** geschaltet. Eine erneute Schnell-Ausrichtung (Fast Re-Align) erfolgt bei Bedarf über die MCDU.

---

### 2. FMGEC / MCDU Reset & Re-Initialization
Ziel dieser Phase ist das Bereinigen der alten Flugplandaten und die vollständige Programmierung des neuen Streckenabschnitts über den FlyByWire ATSU AOC Uplink.

*   **SimBrief Uplink (Neues Leg):**
    *   Im flyPad das neue SimBrief OFP laden.
    *   MCDU Taste **MCDU MENU** drücken $\rightarrow$ LSK **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ LSK **INIT DATA REQ**.
*   **INIT A Page:** Taste **INIT** drücken $\rightarrow$ LSK **INIT REQUEST** betätigen. **FROM/TO**, **FLT NBR**, **COST INDEX** und **CRZ FL** aktualisieren.
*   **F-PLN (Flight Plan):** Departure Runway/SID sowie Anflugverfahren für das neue Leg eintragen und Flugplan auf Discontinuities prüfen.
*   **INIT B Page:** Erneut **INIT** drücken $\rightarrow$ **NEXT PAGE** $\rightarrow$ LSK **ZFW/ZFWCG** und **BLOCK** betätigen, um die neuen Fracht- und Treibstoffwerte zu laden.
*   **PERF Page:** Neue $V$-Speeds (**V1**, **VR**, **V2**), **FLEX TO TEMP** und Klappen/THS-Trimming aus dem flyPad übernehmen.

---

### 3. Pre-Departure Flow & Fast Cockpit Prep
Erneute Herstellung der Abflugbereitschaft für den nachfolgenden Start.

*   **Abschluss Boarding:** Nach Abschluss des Boardings Jetway trennen, Türen schließen.
*   **Before Pushback Flow:** **SEAT BELTS** auf **ON**, **EMER EXIT LT** auf **ARM**, **BEACON** auf **ON**.
*   **Pushback & Start:** Übergang zu [SOP – Abschnitt 2: Engine Start & Pushback](sop.md#2-engine-start--pushback).
