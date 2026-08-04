# Headwind Airbus A330-900neo (A339X) – Standard Operating Procedures (SOP)

This guide describes the Standard Operating Procedures (SOP) for the **Headwind Airbus A330-900neo (A339X)** (Passenger) in **MSFS 2024**. It leads chronologically through all flight phases from Cold & Dark gate setup to final shutdown – aligned with real Airbus FCOM standards, ATC integration (e.g., **BeyondATC**, **VATSIM**, **IVAO**), **SimBrief** flight planning, the **FlyByWire flyPad (EFB)**, the **FBW ATSU Systems Core** architecture, and **Winwing Sim URSA Minor** hardware mapping.

> **Transit / Turnaround Note:**
> For quick intermediate stops without a complete shutdown, refer directly to the time-optimized [Transit SOP](transit-sop.md).

## Table of Contents
- [1. Pre-Flight & Cockpit Preparation (Cold & Dark at Gate)](#1-pre-flight--cockpit-preparation-cold--dark-at-gate)
- [2. Engine Start & Pushback](#2-engine-start--pushback)
- [3. Taxi & Before Takeoff Preparation](#3-taxi--before-takeoff-preparation)
- [4. Takeoff & Departure](#4-takeoff--departure)
- [5. Cruise, Fuel Trim Tank & Approach Setup](#5-cruise-fuel-trim-tank--approach-setup)
- [6. Approach & Landing](#6-approach--landing)
- [7. After Landing, Taxi & Shutdown](#7-after-landing-taxi--shutdown)

---

### 1. Pre-Flight & Cockpit Preparation (Cold & Dark at Gate)
The flight originates in an unpowered state at the gate. The objective of this phase is to establish electrical power, process passenger ground handling (refueling, boarding via jetway/stairs), and complete FMGS/MCDU initialization via FlyByWire ATSU architecture.

*   **Power On:** On the Overhead Panel, switch **BAT 1** and **BAT 2** to **ON**. Check battery voltage on digital voltmeters ($> 25.5\text{ V}$). Power up the FlyByWire flyPad (EFB) on the left captain's console.
*   **Initial Ground Lighting:** Immediately after powering on, switch **NAV & LOGO** light to **1** (or **2**). Position 1 powers navigation lights via the AC Essential Bus, signaling electrical readiness to ground personnel.
*   **Ground Services & GPU (via flyPad):** Navigate to *Ground Services* in the flyPad and request the Ground Power Unit (GPU). When the green *AVAIL* light illuminates on the overhead panel, press **EXT PWR** (blue *ON* illuminates).
    *   Connect jetway (passenger boarding bridge) via flyPad.
    *   Navigate to *Payload/Fuel* in the flyPad, fetch SimBrief data, and initiate *Refueling* and passenger/baggage *Boarding*.
*   **Overhead Panel Setup:**
    *   Switch **CREW SUPPLY** (Oxygen) to **ON**.
    *   Verify all fuel pumps (**FUEL PUMPS**) are **ON** or **AUTO**.
    *   Passenger signs & emergency lighting: Set **EMER EXIT LT** to **ARM**. Set **NO SMOKING** to **ON** or **AUTO**. Set **SEAT BELTS** to **ON**.
*   **ATC IFR Clearance:** Request clearance from ATC Delivery/Ground: *"Request IFR Clearance"*. Set cleared initial altitude on FCU and tune the transponder squawk code.
*   **ADIRUs Initialization:** On the Overhead Panel, turn all three ADIRS selectors (1, 2, 3) from OFF to **NAV**.
*   **Detailed MCDU / ATSU Setup (FlyByWire Architecture):**
    *   **SimBrief Uplink (AOC):** Press **MCDU MENU** key $\rightarrow$ LSK **ATSU** $\rightarrow$ LSK **AOC MENU** $\rightarrow$ LSK **INIT/PRES** $\rightarrow$ press LSK **INIT DATA REQ**.
    *   **INIT A Page:** Press **INIT** key. Press LSK next to **INIT REQUEST**. System loads **FROM/TO**, **FLT NBR**, **COST INDEX**, and **CRZ FL**. Verify GPS/IRS alignment status.
    *   **F-PLN (Flight Plan):** Press **F-PLN** key. Select departure airport LSK $\rightarrow$ LSK **DEPARTURE** $\rightarrow$ select assigned runway and SID $\rightarrow$ press LSK **INSERT**. Enter en-route waypoints and destination STAR/Approach. Clear any **F-PLN DISCONTINUITY** using **CLR**.
    *   **INIT B Page:** Press **INIT** key again and select **NEXT PAGE**. Press LSK next to **ZFW/ZFWCG** and press LSK next to **BLOCK** twice to import fuel figures from SimBrief.
    *   **PERF Page:** Press **PERF** key. Enter calculated takeoff speeds (**V1**, **VR**, **V2**), **FLEX TO TEMP**, and flap/THS trim setting (**THS/FLAPS**, e.g., `1/UP0.8`).
*   **Finalize Boarding:** Upon boarding completion (indicated in flyPad), disconnect jetway via flyPad. Aircraft doors are closed.

---

### 2. Engine Start & Pushback
This phase covers immediate engine start preparation. The goal is starting the Auxiliary Power Unit (APU), disconnecting ground power, executing pushback (via GSX / Toolbar Pushback / MSFS), and starting both Rolls-Royce Trent 7000 engines.

*   **APU Start (approx. 10 min prior to pushback):**
    *   Switch **APU MASTER SW** to **ON**.
    *   Switch **APU START** to **ON** (ON LED illuminates).
    *   Once *APU AVAIL* illuminates on ECAM: Switch **APU BLEED** to **ON** (pneumatic air supply takeover).
*   **Disconnect Ground Power (GPU Disconnect):**
    *   Switch **EXT PWR** on Overhead Panel to **OFF** (blue ON extinguishes, green AVAIL remains).
    *   Disconnect GPU via flyPad *Ground Services*.
*   **ATC Clearance & Beacon Light:**
    *   Request pushback and engine start clearance from ATC Ground: *"Request Pushback and Engine Start"*.
    *   Upon clearance (*"Pushback and Engine Start approved"*), switch **BEACON** light to **ON**.
*   **Before Start Flow & Checklist:**
    *   **THRUST LEVERS:** Verify both thrust levers are in **IDLE** detent.
    *   **PARKING BRAKE:** Remains **ON**.
    *   Execute Before Start Checklist.
*   **Pushback Initiation (GSX / Toolbar Pushback / MSFS):**
    *   *Note:* Since the flyPad on the A339X does not feature an internal pushback menu, initiate pushback via **GSX Pro**, **Toolbar Pushback**, or MSFS menu (`Shift + P`).
    *   When tug driver reports: *"Pushback tractor connected, release parking brake"*:
        *   Switch **PARKING BRAKE** to **OFF**.
*   **Engine Start Procedure (Trent 7000 Start Flow):**
    *   Turn **ENG MODE SELECTOR** (center pedestal) from NORM to **IGN/START** (ECAM switches to ENG page, check bleed pressure ~30 psi).
    *   **Start Engine 2 (Right Engine First):**
        *   Move **ENG MASTER 2** to **ON**.
        *   *ECAM Monitoring:* Observe $N_2$ rise. At $N_2 \ge 16\%$, IGN indication appears, Fuel Flow (FF) and EGT rise, followed by $N_1$ increase. At approx. $50\% N_2$, starter disengages. At approx. $58–60\% N_2$, green *AVAIL* appears on ECAM $\rightarrow$ Engine 2 is stable.
    *   **Start Engine 1 (Left Engine):**
        *   Once Engine 2 displays *AVAIL*, move **ENG MASTER 1** to **ON**.
        *   Perform identical ECAM monitoring ($N_2 \rightarrow$ IGN $\rightarrow$ FF/EGT $\rightarrow N_1 \rightarrow$ *AVAIL*).
*   **After Start Flow (Post Pushback & Start):**
    *   Once the aircraft comes to a stop on taxiway and pushback is finished:
        *   Set **PARKING BRAKE** to **ON** (confirm to ground crew: *"Parking brake set"*).
    *   **ENG MODE SELECTOR:** Turn **ENG MODE SELECTOR** back to **NORM** once both engines display green *AVAIL*.
    *   Switch **APU BLEED** to **OFF**.
    *   Switch **APU MASTER SW** to **OFF** (APU cools down and shuts off).
    *   Confirm tug disconnect and acknowledge ground crew bypass pin signal.

---

### 3. Taxi & Before Takeoff Preparation
This phase includes taxiing to the active runway, configuring flight systems (flaps, trim, spoilers, WXR/TCAS), and performing final technical takeoff checks (T/O Config & Flight Controls Check).

*   **ATC Clearance & Taxi Lighting:** Request taxi clearance from ATC: *"Request Taxi"*. Upon clearance, switch **NOSE** light to **TAXI**. Switch **RWY TURN OFF** lights to **ON** when maneuvering on taxiways or crossing runways.
*   **After Start Flow / T/O Config:**
    *   Set **FLAPS** to calculated takeoff position (e.g., **FLAPS 1** or **FLAPS 2**).
    *   Arm **GND SPOILERS** (pull speedbrake lever UP).
    *   Set **PITCH TRIM** wheel according to MCDU THS calculation (e.g., 0.8 UP).
    *   **RUD TRIM:** Verify rudder trim reads `0.0°` (press **RESET** if required).
    *   Set **AUTOBRAKE** to **MAX**.
*   **Weather Radar & Anti-Ice Setup:**
    *   **WXR RADAR PANEL:** Set **SYS** to **1** (or **2**), **PWS** to **AUTO**, **MODE** to **WX** or **WX+T**.
    *   **ENG / WING ANTI ICE:** Switch ON as required if OAT $\le 10^\circ\text{C}$ in visible moisture.
*   **Transponder & TCAS Setup:**
    *   Set **ATC / XPDR MODE** to **AUTO** (or **ON**).
    *   Set **ALT RPTG** to **ON**.
    *   Set **TCAS MODE** to **TA/RA**.
*   **Flight Controls Check:** Monitor ECAM F/CTL page: Stick Full Up, Down, Left, Right; Rudder Pedals Left, Right.
*   **Flight Instruments & T/O CONFIG Test:** Press blue **T/O CONFIG** button on center pedestal **once**. Verify green *NORMAL* on ECAM.
*   **Brake Fan Check:** Check ECAM WHEEL page. Verify brake temperatures are below 150°C and **BRK FAN** is **OFF**.

---

### 4. Takeoff & Departure
Arrival at holding point and takeoff roll execution. The goal is obtaining takeoff clearance, setting takeoff power, executing a smooth rotation, initial climb, and transition into climb profile (Thrust Reduction & Clean-Up).

*   **ATC Clearance:** Report to ATC: *"Ready for Departure"*. Await *"Line up and wait"* or *"Cleared for Takeoff"*.
*   **Line-up System & Lighting Check:** When entering the runway:
    *   Switch **STROBE** from AUTO to **ON**.
    *   Switch single **LANDING** light switch to **ON**.
    *   Switch **NOSE** light from TAXI to **T.O.** (Takeoff).
    *   **CALLS PANEL (Overhead):** Press **ALL** button (or trigger **SEAT BELTS** signs) to signal takeoff to cabin crew (*"Cabin Crew, take your seats for takeoff"*).
    *   **TCAS & PWS Check:** Verify **TCAS** is **TA/RA** and **PWS** is **AUTO**.
    *   **ECAM T/O MEMO Visual Check:** Once cabin is ready, `CABIN READY` switches to green on ECAM. Visually verify all ECAM T/O MEMO lines are green.
*   **Takeoff Roll & Power Set:**
    *   Release brakes, advance **THRUST LEVERS** symmetrically to approx. 50% N1 and await stabilization.
    *   Advance thrust levers into **FLEX/MCT** (or **TOGA**) detent.
    *   **FMA Check:** Verify **"MAN FLEX"** (or MAN TOGA), **"SRS"**, **"RWY"**, **"A/THR BLUE"**.
    *   At VR: Rotate smoothly (approx. 3°/sec pitch rate toward 15° pitch attitude).
*   **Post Takeoff & Departure Handoff:**
    *   At positive rate of climb: *"Positive Climb"* $\rightarrow$ **LANDING GEAR** lever **UP**.
    *   **ATC Handoff:** Perform frequency change to Departure/Radar upon instruction.
    *   **Autopilot Activation & Climb Logic:** Above 100 ft AGL, **AP1** can be engaged by pressing **AP1** button on FCU.
        *   **Managed Climb (Push / CLB):** Press **ALT** knob on FCU ("Push"). Dot appears in FCU display, FMA displays **CLB**.
        *   **Open Climb (Pull / OP CLB):** Pull **ALT** knob ("Pull"). Dot extinguishes, FMA displays **OP CLB**.
    *   At Thrust Reduction Altitude (**LVR CLB** flashes on FMA): Retract **THRUST LEVERS** manually into **CL** detent.
    *   **Acceleration Altitude & Clean Up:** Retract flaps incrementally according to F/S speeds (**FLAPS 0**). Disarm **GND SPOILERS**.
*   **Transition Altitude (Baro Reference Switch):**
    *   When passing Transition Altitude, pull **BARO** knob (**BARO KNOB PULL**) to switch to **STD** (Standard 1013.25 hPa / 29.92 inHg).
*   **10,000 ft AAL (Climb):**
    *   Switch single **LANDING** light switch to **OFF**. Switch **NOSE** light to **OFF**. Switch **RWY TURN OFF** lights to **OFF**.
    *   Switch **SEAT BELTS** to **OFF** (weather permitting).

---

### 5. Cruise, Fuel Trim Tank & Approach Setup
This phase covers cruise monitoring and descent/landing preparation. The goal is continuous system/fuel monitoring (including automatic A330 Trim Tank transfer for CG optimization), acquiring destination weather, and completing MCDU/FCU programming for descent and approach.

> **Airmanship & Workload Management:**
> Cruise phase serves early approach preparation and briefing (*Aviate, Navigate, Communicate*). Energy management is top priority. Perform descent plausibility check (3 NM distance per 1,000 ft altitude loss).

*   **Cruise & Trim Tank Monitoring:**
    *   Regularly monitor flight path, fuel burn, and FMA status (`SPEED`, `ALT CRZ`, `NAV`).
    *   *Trim Tank System (A330neo Specifics):* During climb, the automatic A330 fuel system transfers fuel from wing tanks to the tail trim tank to shift Center of Gravity (CG) aft for minimum cruise drag. Automatic forward transfer occurs prior to descent/landing.
*   **Descent Planning & Approach Setup (approx. 80 NM prior to TOD):**
    *   Obtain destination weather (ATIS).
    *   **MCDU PERF APPR Page:** Enter QNH, Temperature, MAG WIND, Decision Altitude (**BARO** / **RADIO** minimums), and flap configuration (**CONF FULL** or **CONF 3**).
    *   **F-PLN:** Verify and activate destination STAR and Approach.
*   **Descent Initiation & FCU Operation (DES vs. OP DES):**
    *   Dial cleared lower ATC altitude on **FCU** approx. 5–10 NM prior to TOD.
    *   **Managed Descent (Push / DES):** At TOD, press **ALT** knob ("Push"). Dot appears in FCU display, FMA displays **DES**.
    *   **Open Descent (Pull / OP DES):** Pull **ALT** knob ("Pull"). Dot extinguishes, FMA displays **OP DES**.
*   **Passing FL100 / 10,000 ft AAL (Descent):**
    *   Switch single **LANDING** light switch to **ON**.
    *   Switch **SEAT BELTS** to **ON**.
    *   **CALLS PANEL (Overhead):** Press **ALL** button (or trigger **SEAT BELTS** switch) to notify cabin crew (*"Cabin Crew, prepare for landing"*).
    *   **EFIS Panel:** Prepare **LS** button, pre-select barometric reference (**BARO**) to destination QNH (set at Transition Level).
    *   **MCDU RAD NAV:** Verify tuned ILS frequency and inbound course.

---

### 6. Approach & Landing
This phase covers initial approach through touchdown. The goal is establishing landing configuration, capturing guidance signals (ILS Localizer & Glideslope), timely manual takeover, touchdown, and deceleration.

*   **Initial Approach & LS Activation:**
    *   **LS Button (EFIS Panel):** When entering approach sector, press **LS** button to display ILS scales on PFD.
    *   At Green Dot Speed: Select **FLAPS 1**.
*   **Approach Clearance & APPR Activation (FCU):**
    *   Upon receiving approach clearance (*"Cleared ILS Approach Runway..."*) and on intercept heading:
        *   **APPR Button:** Press **APPR** button on FCU (FMA displays `LOC` blue and `G/S` blue).
        *   **AP2 Button:** Press **AP2** button on FCU for Dual-Channel Autoland / CAT III preparation (FMA displays `AP 1+2`).
*   **Established Report (ATC Communication):**
    *   Once Localizer is captured (FMA displays `LOC` green): Report to ATC: *"Established ILS Runway [Runway Identifier]"*.
*   **Final Approach Sequence & Flaps Timeline:**
    *   At S-Speed: Select **FLAPS 2**.
    *   At approx. 2,000 ft AAL (or 1/2 dot below Glideslope): Select **GEAR DOWN**, arm **GND SPOILERS**, switch **NOSE** light to **T.O.**, switch **RWY TURN OFF** lights to **ON**.
    *   Below VFE for Flaps 3: Select **FLAPS 3**, followed by **FLAPS FULL** at F-speed.
    *   **AUTOBRAKE:** Select **MED** or **LOW**. Execute Landing Checklist.
*   **Autopilot Disconnect (Manual Landing):**
    *   Once runway is in sight and aircraft is stabilized (between 1,000 ft and 500 ft AGL), take manual control.
    *   **Autopilot Disconnect:** Disconnect via joystick **AUTOPILOT OFF** button using a **double click** (first click disconnects AP, second click silences audio warning).
*   **Touchdown & Reversers:** At *"Retard"* callout, retard **THRUST LEVERS** to **IDLE**. Upon touchdown, apply **REVERSERS** to **REV MAX** or **REV IDLE**. At 70 knots, reduce to **REV IDLE** and close before vacating runway.

---

### 7. After Landing, Taxi & Shutdown
Safe runway exit, taxiing to gate, engine shutdown, and securing the aircraft.

*   **Runway Vacated:**
    *   Once yellow holding line is crossed: Switch **STROBE** to **AUTO** (or **OFF**), switch single **LANDING** light switch to **OFF**, switch **NOSE** light to **TAXI**. Switch **RWY TURN OFF** lights to **OFF**.
    *   **WXR RADAR PANEL:** Switch **SYS** and **PWS** to **OFF**.
    *   **TCAS & XPDR:** Set **TCAS MODE** to **STBY** (or `TA ONLY`), set **ATC/XPDR MODE** to **AUTO** / **STBY**.
    *   **FLAPS:** Retract flaps to **0**. **GND SPOILERS:** Disarm spoilers.
    *   **ENG ANTI ICE:** Switch off if previously active.
*   **Taxi to Gate & APU Management:**
    *   Request taxi to gate from ATC Ground (*"Request taxi to gate"*).
    *   Approx. 3 minutes prior to reaching gate: Switch **APU MASTER SW** to **ON** and **APU START** to **ON**.
*   **Parking Position & Shutdown:**
    *   **Ground Crew Safety:** When turning into stand (visual contact with marshaller / VDGS), switch **NOSE** light (Taxi) to **OFF** to avoid blinding ground personnel.
    *   Stop aircraft precisely on stop mark, set **PARKING BRAKE** to **ON**.
    *   Once ECAM displays *APU AVAIL*: Switch **APU BLEED** to **ON**.
    *   Connect jetway via flyPad (if using GPU: switch **EXT PWR** to **ON**).
    *   **BRK FAN:** Check ECAM WHEEL page. Switch **BRK FAN** to **ON** if brake temperatures exceed 150°C.
*   **Engine Shutdown Flow:**
    *   **ENG MASTER 1 & 2:** Move to **OFF** after verifying 3-minute idle cool-down.
    *   Once engines come to a complete stop ($N_1 < 5\%$): Switch **BEACON** light to **OFF**, switch all **FUEL PUMPS** to **OFF**.
    *   Switch **SEAT BELTS** to **OFF** (signals passengers to unbuckle/disembark) and initiate passenger deboarding via flyPad.

> **Transit / Turnaround Procedure:**
> For an immediate follow-on flight leg, skip *Securing the Aircraft* below and proceed directly to [Transit SOP – Section 1: Arrival, Parking & Transit Setup](transit-sop.md#1-arrival-parking--transit-setup).

*   **Securing Aircraft (Cold & Dark):**
    *   Switch **NO SMOKING** to **OFF**, **EMER EXIT LT** to **OFF**.
    *   Switch **APU BLEED** to **OFF**, **CREW SUPPLY** (Oxygen) to **OFF**.
    *   Turn ADIRS 1, 2, 3 sequentially to **OFF**, switch **NAV & LOGO** light to **OFF**.
    *   Switch **BRK FAN** to **OFF** (after cooling), **APU MASTER SW** to **OFF**, switch **BAT 1 & 2** to **OFF**.

The aircraft is now in a completely unpowered Cold & Dark state.
