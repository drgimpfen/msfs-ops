# FlyByWire A320NX – Transit Standard Operating Procedures (SOP)

This SOP describes the time-optimized **Transit Procedure** (Turnaround) for multi-leg flights with the **FlyByWire A320NX** in **MSFS 2024** according to Airbus FCOM standards.

### Purpose & Process Description of the Transit Workflow
During short gate turnarounds (Transit), the aircraft is not completely powered down. The workflow is designed to minimize ground time and prepare the aircraft safely and efficiently for the next flight segment without a full cold-start setup:
* **Power & Pneumatic Supply:** The APU runs continuously and provides electrical power and cabin air conditioning via **APU BLEED ON**. No external Ground Power Unit (GPU) is required.
* **Avionics & Systems:** The Inertial Reference Systems (ADIRS 1, 2, 3) remain in **NAV** mode (no time-consuming IRS re-alignment required). Oxygen (**CREW SUPPLY**) and emergency lighting (**EMER EXIT LT**) remain in their active operational positions.
* **Transit Sequence:**
  * **[1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup):** Gate arrival, set parking brake, transfer air supply to APU BLEED, and engine shutdown.
  * **[2. Deboarding, Refueling & Boarding via EFB (flyPad)](#2-deboarding-refueling--boarding-via-efb-flypad):** Deboarding arriving passengers, refueling (fueling with APU running), followed by boarding the next leg.
  * **[3. MCDU Reset & Complete Re-programming (Transit Setup)](#3-mcdu-reset--complete-re-programming-transit-setup):** Clearing the previous flight plan, uplifting new SimBrief data, and reprogramming flight plan, performance, and weight figures.
  * **[4. Transition Back to Standard SOP](#4-transition-back-to-standard-sop):** Preparation for pushback and seamless transition into the engine start procedure of [Standard SOP – Section 2: Engine Start & Pushback](sop.md#2-engine-start--pushback).

---

## Table of Contents
- [1. Arrival, Parking & Transit Setup](#1-arrival-parking--transit-setup)
- [2. Deboarding, Refueling & Boarding via EFB (flyPad)](#2-deboarding-refueling--boarding-via-efb-flypad)
- [3. MCDU Reset & Complete Re-programming (Transit Setup)](#3-mcdu-reset--complete-re-programming-transit-setup)
- [4. Transition Back to Standard SOP](#4-transition-back-to-standard-sop)

---

### 1. Arrival, Parking & Transit Setup
Once the aircraft is parked at the gate, the parking brake is set, and air conditioning is transferred to APU BLEED (refer to [Standard SOP – Section 7: After Landing, Taxi & Shutdown](sop.md#7-after-landing-taxi--shutdown)), the transit process commences without a cold shut down:

*   **Engine Shutdown & Power Supply (APU Continuous):**
    *   Switch off engines sequentially (**ENG MASTER 1** and **2** to **OFF**).
    *   Since the APU was started during taxi-in and **APU BLEED** was selected **ON** at the stand, both **APU** and **APU BLEED** remain continuously **ON**. Connecting an external GPU is completely omitted.
*   **Cockpit Leftover Management & Ground Safety (Transit State):**
    *   **BEACON Light:** Switch **BEACON** light to **OFF** as soon as engines spool down ($N_1 < 5\%$).
    *   **Anti-Glare & Ground Crew Safety:** Switch **NOSE** light and **RWY TURN OFF** lights to **OFF** immediately upon stopping at the stand to avoid blinding ground personnel and jetway operators.
    *   **Lighting Management:** **NAV & LOGO** remains on **1** (or **2**), **STROBE** on **AUTO**, **LANDING L & R** switches on **RETRACT**.
    *   **Avionics:** ADIRS 1, 2, 3 remain in **NAV** mode throughout the turnaround (no re-alignment required).
    *   **Passenger Signs:** **SEAT BELTS** to **OFF**, **NO SMOKING** to **ON** or **AUTO**, and **EMER EXIT LT** on **ARM**.
    *   **BRK FAN:** Check ECAM WHEEL page. Switch **BRK FAN** to **ON** if brake temperatures exceed 150°C.

---

### 2. Deboarding, Refueling & Boarding via EFB (flyPad)
Ground handling is controlled via the EFB (flyPad) while FMGS setup takes place in parallel.

*   **Deboarding (Passenger Disembarkation):**
    *   Open the *Ground Services* or *Payload/Fuel* menu in the flyPad.
    *   Start the **Deboarding** process and wait for passenger and cargo count to reach zero.
*   **Refueling (Fueling with APU Running / Hot Refueling):**
    *   Fueling proceeds directly with the APU running.
    *   Import new flight plan and weight data for the next segment via flyPad SimBrief integration.
    *   Enter the new **Block Fuel** and initiate **Refueling**. Monitor fuel load progress on the ECAM FOB display.
*   **Boarding for Next Segment:**
    *   Once refueling is complete and new passenger/payload data is loaded, start **Boarding**.

---

### 3. MCDU Reset & Complete Re-programming (Transit Setup)
The FMGS must be cleared and completely reprogrammed for the next segment.

*   **ATC IFR Clearance (ATC):**
    *   Contact ATC Delivery prior to completion of boarding: *"Request IFR Clearance"*. Set cleared initial altitude on FCU and tune the assigned squawk code on the transponder.
*   **Flight Plan Reset Workflow:**
    *   **SimBrief ATSU Uplink:** Press **MCDU MENU** key $\rightarrow$ LSK **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ press LSK **INIT DATA REQ** to fetch new flight plan data.
    *   **INIT A Reset:** Press **INIT** key and press the Line Select Key (LSK) next to **INIT REQUEST**. The system loads the new *FROM/TO* pair and automatically overwrites the previous route.
    *   **Flight Plan Cleanup:** If residual waypoints from the previous leg remain in **F-PLN**, press **F-PLN** key, select residual waypoints or discontinuities, press **CLR**, and click the corresponding LSK until a clean flight plan is established.
*   **Detailed MCDU Reprogramming:**
    *   **INIT A Page:** Verify **FROM/TO**, **FLT NBR**, **COST INDEX**, and new cruise flight level (**CRZ FL**).
    *   **F-PLN Page:** Press **F-PLN** key.
        *   Select departure airport $\rightarrow$ LSK **DEPARTURE** $\rightarrow$ select assigned runway and SID $\rightarrow$ press LSK **INSERT**.
        *   Program en-route routing (or load via uplink).
        *   Select destination airport $\rightarrow$ LSK **ARRIVAL** $\rightarrow$ select approach, STAR, and VIA $\rightarrow$ press LSK **INSERT**.
        *   Clear any remaining **F-PLN DISCONTINUITY** with **CLR**.
    *   **INIT B Page:** Press **INIT** key again and navigate to Page 2 (**NEXT PAGE**). Verify **ZFW / ZFWCG** and press LSK next to **BLOCK** twice to accept new block fuel.
    *   **PERF Page:** Press **PERF** key.
        *   Enter new takeoff speeds (**V1**, **VR**, **V2**).
        *   Enter new **FLEX TEMP**.
        *   Enter new takeoff trim setting at **THS/FLAPS** (e.g., `1/UP0.5`).

---

### 4. Transition Back to Standard SOP
Once MCDU programming is complete, boarding is finalizing, and the cockpit is prepared, transition back into the standard procedure takes place:

*   **Cockpit Re-Arming & Safety Flow:**
    *   **FUEL PUMPS:** Switch all six **FUEL PUMPS** (L TK, C TK, R TK) to **ON**.
    *   **Passenger Signs:** Switch **SEAT BELTS** to **ON** (signals passengers to remain seated prior to pushback).
    *   **BARO Reference:** Set FCU barometric reference (**BARO**) to local departure airport QNH.
    *   **XPDR / Transponder:** Set assigned squawk code from ATC clearance, verify **ATC/XPDR MODE** is set to **AUTO** / **STBY**.
*   **Seamless Re-entry:**
    *   Finalize boarding (close aircraft doors via EFB).
    *   **Brake Fan Check:** Check ECAM WHEEL page. Verify brake temperatures are below 150°C and **BRK FAN** is **OFF**.
    *   Since the APU is already running and **APU BLEED** is **ON**, engine start bleed air is immediately available.
    *   Proceed directly to [Standard SOP – Section 2: Engine Start & Pushback](sop.md#2-engine-start--pushback) to request pushback/start clearance and switch **BEACON** light to **ON**. After both engines are started, switch **APU BLEED** and **APU MASTER SW** to **OFF** per standard SOP.
    *   Continue flight operations following the main SOP.
