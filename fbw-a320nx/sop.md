# FlyByWire A320NX – Standard Operating Procedures (SOP)

This guide describes the Standard Operating Procedures (SOP) for the **FlyByWire A320NX** in **MSFS 2024**. It leads chronologically through all flight phases from Cold & Dark setup to final shutdown – aligned with real-world Airbus FCOM specifications, ATC integration (e.g., **BeyondATC**, **VATSIM**, **IVAO**), **SimBrief** flight planning, the **flyPad (EFB)**, and **Winwing Sim URSA Minor** hardware mappings.

> **Transit / Turnaround Note:**
> For quick intermediate stops without a complete shutdown, refer directly to the time-optimized [Transit SOP](transit-sop.md).

## Table of Contents
- [1. Pre-Flight & Cockpit Preparation (Cold & Dark at Gate)](#1-pre-flight--cockpit-preparation-cold--dark-at-gate)
- [2. Engine Start & Pushback](#2-engine-start--pushback)
- [3. Taxi & Before Takeoff Preparation](#3-taxi--before-takeoff-preparation)
- [4. Takeoff & Departure](#4-takeoff--departure)
- [5. Cruise, Descent Planning & Approach Setup](#5-cruise-descent-planning--approach-setup)
- [6. Approach & Landing](#6-approach--landing)
- [7. After Landing, Taxi & Shutdown](#7-after-landing-taxi--shutdown)

---

### 1. Pre-Flight & Cockpit Preparation (Cold & Dark at Gate)
The flight originates in an unpowered state at the gate or stand. The objective of this phase is to establish electrical power, process ground handling (refueling, payload loading, passenger boarding), and complete FMGS/MCDU initialization.

*   **Power On:** On the Overhead Panel, switch **BAT 1** and **BAT 2** to **ON**. Check battery voltage on the digital voltmeters ($> 25.5\text{ V}$). Power up the flyPad (EFB) on the left captain's console.
*   **Initial Ground Lighting:** Immediately after powering on, switch **NAV & LOGO** light to **1** (or **2**). Position 1 powers navigation lights via the AC Essential Bus, signaling electrical readiness to ground personnel.
*   **Ground Services (via flyPad):** Navigate to *Ground Services* in the EFB and request the Ground Power Unit (GPU). When the green *AVAIL* light illuminates on the overhead panel, press **EXT PWR** (blue *ON* illuminates).
    *   Connect jetway (passenger boarding bridge) via the EFB.
    *   Navigate to *Payload/Fuel* in the flyPad, fetch SimBrief data, and initiate *Refueling* and passenger/cargo *Boarding*.
*   **Overhead Panel Setup:** 
    *   Switch **CREW SUPPLY** (Oxygen) to **ON**.
    *   Switch all six **FUEL PUMPS** (L TK, C TK, R TK) to **ON**.
    *   Passenger signs & emergency lighting: Set **EMER EXIT LT** to **ARM**. Set **NO SMOKING** (or **NO PORTABLE ELEC DEVICE**) to **ON** or **AUTO**. Set **SEAT BELTS** to **ON**.
*   **ATC IFR Clearance:** Request clearance from ATC Delivery: *"Request IFR Clearance"*. Upon receiving route, initial altitude, and assigned squawk, set the cleared altitude on the FCU (Flight Control Unit) and tune the transponder code.
*   **ADIRUs Initialization:** On the Overhead Panel, turn all three ADIRS selectors (1, 2, 3) from OFF to **NAV**.
*   **Detailed MCDU / FMGS Setup (DIFRIP Flow):** 
    *   **SimBrief Uplink (AOC):** Press **MCDU MENU** key $\rightarrow$ LSK **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ press LSK **INIT DATA REQ**.
    *   **INIT A Page:** Press **INIT** key. Press LSK next to **INIT REQUEST**. Verify **FROM/TO**, **FLT NBR**, **COST INDEX**, and **CRZ FL**. Verify GPS/IRS alignment status.
    *   **F-PLN (Flight Plan):** Press **F-PLN** key. Select departure airport LSK $\rightarrow$ LSK **DEPARTURE** $\rightarrow$ select assigned runway and SID $\rightarrow$ press LSK **INSERT**. Select destination airport LSK $\rightarrow$ LSK **ARRIVAL** $\rightarrow$ select STAR, Approach, and VIA $\rightarrow$ press LSK **INSERT**. Clear any **F-PLN DISCONTINUITY** using **CLR**.
    *   **RAD NAV:** Verify tuned VOR and ILS frequencies/courses.
    *   **INIT B Page (Next Page):** Press **INIT** key and select **NEXT PAGE**. Press LSK next to **ZFW/ZFWCG** and press LSK next to **BLOCK** twice to import fuel figures from SimBrief. Verify TOW and LW.
    *   **PERF Page:** Press **PERF** key. Enter calculated takeoff speeds (**V1**, **VR**, **V2**). Enter **FLEX TO TEMP**. Enter takeoff flap/trim setting at **THS/FLAPS** (e.g., `1/UP0.5`).
*   **Finalize Boarding:** Upon boarding completion (indicated in EFB), disconnect jetway via EFB. Aircraft doors are closed and slides armed.

---

### 2. Engine Start & Pushback
This phase covers immediate engine start preparation. The goal is starting the Auxiliary Power Unit (APU), disconnecting external power/ground services, executing pushback, and starting both CFM56 / LEAP-1A engines.

*   **APU Start (approx. 10 min prior to pushback):**
    *   Switch **APU MASTER SW** to **ON**.
    *   Switch **APU START** to **ON** (ON LED illuminates).
    *   Once *APU AVAIL* illuminates on the ECAM: Switch **APU BLEED** to **ON** (pneumatic air supply takeover).
*   **Disconnect Ground Power (GPU Disconnect):**
    *   Switch **EXT PWR** on the Overhead Panel to **OFF** (blue ON extinguishes, green AVAIL remains).
    *   Disconnect GPU via flyPad *Ground Services*.
*   **ATC Clearance & Beacon Light:**
    *   Request pushback and start clearance from ATC Ground: *"Request Pushback and Engine Start"*.
    *   Upon clearance (*"Pushback and Engine Start approved"*), switch **BEACON** light to **ON**.
*   **Before Start Flow & Checklist:**
    *   **FUEL PUMPS:** Verify all six **FUEL PUMPS** are **ON**.
    *   **SEAT BELTS:** Verify **SEAT BELTS** switch is **ON**.
    *   **THRUST LEVERS:** Verify both thrust levers are in **IDLE** detent.
    *   **PARKING BRAKE:** Remains **ON**.
    *   Complete Before Start Checklist down to line / below line.
*   **Pushback Initiation & Tug Connection:**
    *   Initiate pushback via EFB, MSFS Ground Services, BeyondATC, or Toolbar Pushback.
    *   Wait for tug connection notification.
    *   When ground crew/tug driver reports: *"Pushback tractor connected, release parking brake"*:
        *   Switch **PARKING BRAKE** to **OFF**.
*   **Engine Start Procedure (Engine Start Flow):**
    *   Turn **ENG MODE SELECTOR** (center pedestal) from NORM to **IGN/START** (ECAM switches automatically to ENG page, verify bleed pressure ~30 psi).
    *   **Start Engine 2 (Right Engine First):**
        *   Move **ENG MASTER 2** to **ON**.
        *   *ECAM Monitoring:* Observe $N_2$ rise. At $N_2 \ge 16\%$, IGN indication appears, Fuel Flow (FF) and EGT rise, followed by $N_1$ increase. At approx. $50\% N_2$, starter disengages. At approx. $58–60\% N_2$, green *AVAIL* appears on ECAM $\rightarrow$ Engine 2 is stable.
    *   **Start Engine 1 (Left Engine):**
        *   Once Engine 2 displays *AVAIL*, move **ENG MASTER 1** to **ON**.
        *   Perform identical ECAM monitoring ($N_2 \rightarrow$ IGN $\rightarrow$ FF/EGT $\rightarrow N_1 \rightarrow$ *AVAIL*).
*   **After Start Flow (Post Pushback & Start):**
    *   Once the aircraft comes to a stop on the taxiway and pushback is completed:
        *   Set **PARKING BRAKE** to **ON** (confirm to ground crew: *"Parking brake set"*).
    *   **ENG MODE SELECTOR:** Turn **ENG MODE SELECTOR** back to **NORM** once both engines display green *AVAIL*.
    *   Switch **APU BLEED** to **OFF**.
    *   Switch **APU MASTER SW** to **OFF** (APU cools down and shuts off).
    *   Confirm tug disconnect and acknowledge ground crew bypass pin signal.

---

### 3. Taxi & Before Takeoff Preparation
This phase includes taxiing to the active runway, configuring flight systems (flaps, trim, spoilers, radar/TCAS), and performing final technical takeoff checks (T/O Config & Flight Controls Check).

*   **ATC Clearance & Taxi Lighting:** Request taxi clearance from ATC: *"Request Taxi"*. Upon clearance, switch **NOSE** light to **TAXI**. Switch **RWY TURN OFF** lights to **ON** when maneuvering on taxiways or crossing runways.
*   **After Start Flow / T/O Config:**
    *   Set **FLAPS** to calculated takeoff position (e.g., **FLAPS 1**).
    *   Arm **GND SPOILERS** (pull speedbrake lever UP).
    *   Set **PITCH TRIM** wheel according to MCDU THS calculation (e.g., 0.5 UP).
    *   **RUD TRIM:** Verify rudder trim reads `0.0°` (press **RESET** if required).
    *   Set **AUTOBRAKE** to **MAX**.
*   **Weather Radar & Anti-Ice Setup:**
    *   **WXR RADAR PANEL:** Set **SYS** to **1** (or **2**), **PWS** to **AUTO**, **MODE** to **WX** or **WX+T**.
    *   **ENG ANTI ICE:** Switch **ENG ANTI ICE 1 & 2** to **ON** if OAT $\le 10^\circ\text{C}$ in visible moisture (fog, rain, snow, wet taxiways).
*   **Transponder & TCAS Setup:**
    *   Set **ATC / XPDR MODE** to **AUTO** (or **ON**).
    *   Set **ALT RPTG** to **ON**.
    *   Set **TCAS MODE** to **TA/RA**.
*   **Flight Controls Check:** Monitor ECAM F/CTL page: Stick Full Up, Down, Neutral; Stick Full Left, Right, Neutral; Rudder Pedals Full Left, Right, Neutral.
*   **Flight Instruments & T/O CONFIG Test:** Press the blue **T/O CONFIG** button on the center pedestal **once**. This verifies takeoff configuration (flaps, pitch trim, spoilers). ECAM **CABIN READY** remains blue **CHECK** until cabin ready signal is triggered.
*   **Brake Fan Check:** Check ECAM WHEEL page. Verify brake temperatures are below 150°C and **BRK FAN** is **OFF**.

---

### 4. Takeoff & Departure
Arrival at holding point and takeoff roll execution. The goal is obtaining takeoff clearance, setting takeoff power, executing a smooth rotation, initial climb, and transition into the climb profile (Thrust Reduction & Clean-Up).

*   **ATC Clearance:** Report to ATC: *"Ready for Departure"*. Await *"Line up and wait"* or *"Cleared for Takeoff"*.
*   **Line-up System & Lighting Check:** When entering the runway:
    *   Switch **STROBE** from AUTO to **ON**.
    *   Switch **LANDING L & R** switches (both retractable landing light switches) from RETRACT to **ON**.
    *   Switch **NOSE** light from TAXI to **T.O.** (Takeoff).
    *   **CALLS PANEL (Overhead):** Press **ALL** button (or trigger **SEAT BELTS** signs) to signal takeoff to cabin crew (*"Cabin Crew, take your seats for takeoff"*).
    *   **TCAS & PWS Check:** Verify **TCAS** is **TA/RA** and **PWS** is **AUTO**.
    *   **ECAM T/O MEMO Visual Check:** Once cabin is ready, `CABIN READY` switches to green on ECAM. Visually verify all ECAM T/O MEMO lines are green.
*   **Takeoff Roll:**
    *   Advance **THRUST LEVERS** symmetrically to approx. 50% N1 and await engine stabilization.
    *   Advance thrust levers smoothly to **FLEX/MCT** (or **TOGA**) detent.
    *   **FMA Check:** Verify **"MAN FLEX"** (or MAN TOGA), **"SRS"**, **"RWY"**, **"A/THR BLUE"**.
    *   At VR: Rotate smoothly (approx. 3°/sec pitch rate toward 15° pitch attitude).
*   **Post Takeoff & Departure Handoff:**
    *   At positive rate of climb: *"Positive Climb"* $\rightarrow$ **LANDING GEAR** lever **UP**.
    *   **ATC Handoff:** Acknowledge and perform frequency change to Departure/Radar upon Tower instruction.
    *   **Autopilot Activation & Climb Logic:** Above 100 ft AGL, **AP1** can be engaged by pressing **AP1** button on FCU.
        *   **Managed Climb (Push / CLB):** Press **ALT** knob on FCU ("Push"). A dot appears next to altitude, FMA displays **CLB**. System follows MCDU vertical profile complying with SID altitude/speed restrictions.
        *   **Open Climb (Pull / OP CLB):** Pull **ALT** knob ("Pull") if ATC cancels restrictions (*"cancel level restrictions"*). Dot extinguishes, FMA displays **OP CLB**. Aircraft climbs directly to dialed altitude.
    *   At Thrust Reduction Altitude (approx. 1,500 ft AAL, **LVR CLB** flashes on FMA): Retract **THRUST LEVERS** manually into **CLB** detent.
    *   **Acceleration Altitude & Clean Up:** At Acceleration Altitude, pitch lowers for speed increase. Monitor PFD Speed Tape:
        *   As speed exceeds S-speed: Retract flaps to **FLAPS 0**.
        *   Disarm **GND SPOILERS** by pushing speedbrake lever down.
*   **Transition Altitude (Baro Reference Switch):**
    *   When passing Transition Altitude (BARO display flashes on PFD): Pull **BARO** knob (**BARO KNOB PULL**) to switch from QNH to **STD** (Standard 1013.25 hPa / 29.92 inHg).
*   **10,000 ft AAL (Climb):**
    *   Move **LANDING L & R** switches from ON to **RETRACT**. Switch **NOSE** light to **OFF**. Switch **RWY TURN OFF** lights to **OFF**.

---

### 5. Cruise, Descent Planning & Approach Setup
This phase covers cruise monitoring and descent/landing preparation. The goal is continuous system/fuel monitoring, acquiring destination weather, and completing MCDU/FCU programming for descent and approach.

*   **Cruise Monitoring & Top of Climb (TOC):** Switch **SEAT BELTS** to **OFF** upon reaching cruising altitude (weather permitting). Regularly monitor fuel progress via MCDU PROG page and ECAM FUEL page.
*   **Weather & Arrival Clearance (ATC Handoff):** Approx. 80–100 NM prior to Top of Descent (TOD), obtain destination ATIS, contact ATC, and confirm arrival routing.
*   **MCDU Arrival Setup:**
    *   Press **F-PLN** key, scroll to destination, select **ARRIVAL**.
    *   Select approach procedure (e.g., ILS 08R), STAR, and VIA, then press **INSERT**.
    *   Check flight plan for **F-PLN DISCONTINUITY** and clear with **CLR**.
*   **MCDU Performance Setup for Approach:**
    *   Press **PERF** key and navigate to **APPR** page.
    *   Enter **QNH**, **TEMP**, **MAG WIND**, and Decision Altitude (**BARO** / **RADIO** minimums).
*   **Descent Initiation & FCU Operation (DES vs. OP DES):**
    *   Switch **SEAT BELTS** to **ON** prior to or at TOD.
    *   **FCU Altitude Pre-Select:** Dial cleared lower ATC altitude on **FCU** approx. 5–10 NM prior to TOD.
    *   **Managed Descent (Push / DES):** At TOD, press **ALT** knob ("Push"). Dot appears in FCU display, FMA displays **DES**. Aircraft follows computed profile complying with MCDU constraints.
    *   **Open Descent (Pull / OP DES):** Pull **ALT** knob ("Pull"). Dot extinguishes, FMA displays **OP DES**. Aircraft descends at idle thrust directly to selected altitude.
*   **Passing FL100 / 10,000 ft AAL (Descent):**
    *   Move **LANDING L & R** switches from RETRACT to **ON**.
    *   **CALLS PANEL (Overhead):** Press **ALL** button (or trigger **SEAT BELTS** switch) to notify cabin crew (*"Cabin Crew, prepare for landing"*).
    *   **EFIS Panel:** Prepare **LS** button, pre-select barometric reference (**BARO**) to destination QNH (set at Transition Level).
    *   **MCDU RAD NAV:** Verify tuned ILS frequency and inbound course.

---

### 6. Approach & Landing
This phase covers initial approach through touchdown. The goal is establishing landing configuration, capturing guidance signals (ILS Localizer & Glideslope), timely manual takeover, touchdown, and deceleration.

> **Airmanship & Deceleration Tips:**
> To prevent "High and Fast" scenarios during ATC shortcuts, use **SPEED BRAKES** (up to half) in combination with **OP DES** or extend landing gear (**GEAR DOWN**) early for additional drag.

*   **Initial Approach & Deceleration (DECEL Pseudo-Waypoint):**
    *   **LS Button (EFIS Panel):** When entering approach sector (prior to LOC capture), press **LS** button on EFIS panel to display ILS scales on PFD.
    *   Passing **(DECEL)** pseudo-waypoint (or activating APPR phase on MCDU PERF page) automatically manages target speeds on PFD:
        *   At Green Dot Speed: Select **FLAPS 1**.
        *   At S-Speed: Select **FLAPS 2**.
*   **Approach Clearance & APPR Activation (FCU):**
    *   Upon receiving approach clearance (*"Cleared ILS Approach Runway..."*) and on intercept heading:
        *   **APPR Button:** Press **APPR** button on FCU (FMA displays `LOC` blue and `G/S` blue).
        *   **AP2 Button:** Press **AP2** button on FCU for Dual-Channel Autoland / CAT III preparation (FMA displays `AP 1+2`).
*   **Established Report (ATC Communication):**
    *   Once Localizer is captured and centered (FMA displays `LOC` green): Report to ATC: *"Established ILS Runway [Runway Identifier]"*.
*   **Final Approach Sequence & Gear Extension:**
    *   At 1 Dot below Glideslope (approx. 2,000 ft AAL / 6 NM out): Select **GEAR DOWN**, arm **GND SPOILERS**, switch **NOSE** light to **T.O.**, and switch **RWY TURN OFF** lights to **ON**.
    *   As speed decelerates: Select **FLAPS 3**, followed by **FLAPS FULL** at F-speed. Ensure full landing configuration is established prior to 1,000 ft AAL.
    *   **AUTOBRAKE:** Select **MED** or **LOW**. Execute Landing Checklist.
*   **Autopilot Disconnect (Manual Landing):**
    *   Once runway is in sight and aircraft is stabilized (typically between 1,000 ft and 500 ft AGL), take manual control.
    *   **Autopilot Disconnect:** Press **AUTOPILOT OFF** button on joystick using a **double click** (first click disconnects AP, second click silences audio warning).
*   **Touchdown & Reversers:** At *"Retard"* callout, retard **THRUST LEVERS** to **IDLE**. Upon main gear touchdown, apply **REVERSERS** to **REV MAX** or **REV IDLE**. At 70 knots, reduce reversers to **REV IDLE** and close before vacating runway.

---

### 7. After Landing, Taxi & Shutdown
Safe runway exit, taxiing to gate, engine shutdown, and securing the aircraft.

> **Airmanship & Taxi-In Management:**
> * **Runway Vacated:** Do not stop upon crossing the yellow holding line. Keep rolling smoothly while reconfiguring systems and contacting Ground.
> * **Engine Cool-Down Period:** A 3-minute engine idle period protects turbine shafts from thermal shock. Taxi time from runway exit to stand counts toward this 3-minute requirement.

*   **Runway Vacated:**
    *   Once yellow holding line is fully crossed: Switch **STROBE** from ON to **AUTO** (or **OFF**), move **LANDING L & R** switches to **RETRACT**, switch **NOSE** light to **TAXI**.
    *   Switch **RWY TURN OFF** lights to **OFF** upon exiting active runway area.
    *   **WXR RADAR PANEL:** Switch **SYS** and **PWS** to **OFF**.
    *   **TCAS & XPDR:** Set **TCAS MODE** to **STBY** (or `TA ONLY`), set **ATC/XPDR MODE** to **AUTO** / **STBY**.
    *   **FLAPS:** Retract flaps to **0** (leave extended if slush, snow, or icing exists on taxiways).
    *   **GND SPOILERS:** Disarm spoilers (push lever down).
    *   **ENG ANTI ICE:** Switch off if previously active (provided no ground icing conditions exist).
*   **Taxi to Gate & APU Management:**
    *   Request taxi to gate from ATC Ground (*"Request taxi to gate"*).
    *   Approx. 3 minutes prior to reaching gate: Switch **APU MASTER SW** to **ON** and **APU START** to **ON**.
*   **Parking / Gate Arrival:**
    *   **Ground Crew Safety:** When turning into stand (visual contact with marshaller / VDGS), switch **NOSE** light (Taxi) to **OFF** to avoid blinding ground personnel.
    *   Stop aircraft precisely on stop mark, set **PARKING BRAKE** to **ON**.
    *   Once ECAM displays *APU AVAIL*: Switch **APU BLEED** to **ON**.
    *   Connect jetway / passenger stairs via flyPad (if using GPU: switch **EXT PWR** to **ON**).
    *   **BRK FAN:** Check ECAM WHEEL page. Switch **BRK FAN** to **ON** if brake temperatures exceed 150°C.
*   **Engine Shutdown Flow:**
    *   **ENG MASTER 1 & 2:** Move to **OFF** after verifying 3-minute idle cool-down.
    *   Once engines come to a complete stop ($N_1 < 5\%$): Switch **BEACON** light to **OFF**, switch all 6 **FUEL PUMPS** to **OFF**.
    *   Switch **SEAT BELTS** to **OFF** (signals passengers to unbuckle/disembark).

> **Transit / Turnaround Procedure:**
> For an immediate follow-on flight leg, skip *Securing the Aircraft* below and proceed directly to [Transit SOP – Section 1: Arrival, Parking & Transit Setup](transit-sop.md#1-arrival-parking--transit-setup).

*   **Securing the Aircraft (Cold & Dark):**
    *   Switch **NO SMOKING** to **OFF**, **EMER EXIT LT** to **OFF**.
    *   Switch **APU BLEED** to **OFF**, **CREW SUPPLY** (Oxygen) to **OFF**.
    *   Turn ADIRS 1, 2, 3 sequentially to **OFF**, switch **NAV & LOGO** light to **OFF**.
    *   Switch **BRK FAN** to **OFF** (after cooling), **APU MASTER SW** to **OFF**.
    *   Finally, switch **BAT 1** and **BAT 2** to **OFF**.

The aircraft is now in a completely unpowered Cold & Dark state.
