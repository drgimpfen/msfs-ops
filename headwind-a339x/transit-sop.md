# Headwind Airbus A330-900neo (A339X) – Transit SOP (Turnaround)

This document describes the time-optimized transit and turnaround procedure for the **Headwind Airbus A330-900neo (A339X)** (Passenger) in **MSFS 2024**. It applies when the aircraft remains parked at the gate between legs without powering down, preparing efficiently for the subsequent segment.

> **Prerequisite:**
> The aircraft has been parked at the gate per [SOP – Section 7: After Landing, Taxi & Shutdown](sop.md#7-after-landing-taxi--shutdown), engines are shut down, and electrical/pneumatic power is maintained via APU (or external GPU).

## Table of Contents
- [1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup)
- [2. FMGEC / MCDU Reset & Re-Initialization](#2-fmgec--mcdu-reset--re-initialization)
- [3. Pre-Departure Flow & Fast Cockpit Prep](#3-pre-departure-flow--fast-cockpit-prep)

---

### 1. Arrival, Parking & Transit Setup
The goal of this section is to rapidly secure the aircraft on the ground with electrical power and air supply maintained while passenger deboarding begins.

*   **APU Bleed & Power Check:** Verify **APU BLEED** is **ON** (or **EXT PWR** connected and **ON**).
*   **Lights:** Switch **BEACON** light to **OFF** (signals clearance for ground crew/jetway operator). **NAV & LOGO** remains on **1** (or **2**).
*   **Deboarding & Ground Services (via flyPad):**
    *   Connect jetway and initiate passenger deboarding via the FlyByWire flyPad (EFB).
    *   Initiate refueling and catering services via flyPad / GSX.
*   **ADIRS Continuous Alignment:** All three ADIRS selectors remain in **NAV**. Fast IRS re-alignment can be triggered via MCDU if required.

---

### 2. FMGEC / MCDU Reset & Re-Initialization
The objective of this phase is to clear previous flight plan data and fully program the new route segment via the FlyByWire ATSU AOC uplink.

*   **SimBrief Uplink (New Leg):**
    *   Load the new SimBrief OFP into the flyPad.
    *   Press **MCDU MENU** key $\rightarrow$ LSK **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ press LSK **INIT DATA REQ**.
*   **INIT A Page:** Press **INIT** key $\rightarrow$ press LSK **INIT REQUEST**. Update **FROM/TO**, **FLT NBR**, **COST INDEX**, and **CRZ FL**.
*   **F-PLN (Flight Plan):** Enter departure runway/SID and arrival procedure for the new leg, and check the flight plan for discontinuities.
*   **INIT B Page:** Press **INIT** key $\rightarrow$ **NEXT PAGE** $\rightarrow$ press LSK **ZFW/ZFWCG** and **BLOCK** to accept new weight and fuel figures.
*   **PERF Page:** Enter new takeoff speeds (**V1**, **VR**, **V2**), **FLEX TO TEMP**, and flap/THS trim setting from the flyPad.

---

### 3. Pre-Departure Flow & Fast Cockpit Prep
Re-establishing departure readiness for the subsequent flight.

*   **Finalize Boarding:** Once boarding is complete, disconnect jetway and close aircraft doors.
*   **Before Pushback Flow:** **SEAT BELTS** to **ON**, **EMER EXIT LT** to **ARM**, **BEACON** to **ON**.
*   **Pushback & Start:** Transition directly to [SOP – Section 2: Engine Start & Pushback](sop.md#2-engine-start--pushback).
