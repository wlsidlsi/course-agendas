**I. Fundamental Circuit Concepts**

*   Understanding Basic Electrical Quantities
    *   Voltage (V): Electrical potential difference, measured in volts.
    *   Current (I): Flow of electric charge, measured in amperes.
    *   Resistance (R): Opposition to current flow, measured in ohms.
*   Ohm's Law and Power Dissipation
    *   Applying Ohm's Law: `V = IR` (Voltage equals Current times Resistance).
    *   Calculating Power: `P = VI` (Power equals Voltage times Current) or `P = I^2R` or `P = V^2/R`.
    *   Understanding power dissipation in resistors as heat.
*   Series and Parallel Resistors
    *   Calculating equivalent resistance in series: `R_eq = R1 + R2 + ... + Rn`.
    *   Calculating equivalent resistance in parallel: `1/R_eq = 1/R1 + 1/R2 + ... + 1/Rn`.
    *   Analyzing voltage and current division in series and parallel circuits.
*   Kirchhoff's Laws
    *   Kirchhoff's Current Law (KCL): Sum of currents entering a node equals the sum of currents leaving the node.
    *   Kirchhoff's Voltage Law (KVL): Sum of voltage drops around a closed loop equals zero.
    *   Applying KCL and KVL to solve circuit problems.
    *   Example: Analyze a simple circuit with multiple resistors and voltage sources using KCL and KVL.

**II. Circuit Analysis Techniques**

*   Nodal Analysis
    *   Identifying nodes and reference node in a circuit.
    *   Writing KCL equations at each node.
    *   Solving the system of equations to find node voltages.
    *   Example: Solve a circuit with multiple independent current sources using nodal analysis.
*   Mesh Analysis
    *   Identifying meshes (loops) in a circuit.
    *   Assigning mesh currents to each loop.
    *   Writing KVL equations for each mesh.
    *   Solving the system of equations to find mesh currents.
    *   Example: Solve a circuit with multiple independent voltage sources using mesh analysis.
*   Source Transformations
    *   Converting between voltage sources with series resistance and current sources with parallel resistance.
    *   Applying source transformations to simplify circuit analysis.
    *   Example: Simplify a complex circuit using source transformations before applying nodal or mesh analysis.
*   Superposition Theorem
    *   Understanding the principle of superposition for linear circuits.
    *   Finding the response due to each independent source acting alone.
    *   Summing the individual responses to find the total response.
    *   Example: Determine the current through a resistor in a circuit with both voltage and current sources using superposition.
*   Thevenin's and Norton's Theorems
    *   Finding the Thevenin equivalent circuit (Vth and Rth) at a pair of terminals.
    *   Finding the Norton equivalent circuit (In and Rn) at a pair of terminals.
    *   Using Thevenin's or Norton's theorem to simplify circuit analysis or design.
    *   Example: Find the Thevenin equivalent of a complex circuit connected to a load resistor.

**III. Operational Amplifiers (Op-Amps)**

*   Ideal Op-Amp Characteristics
    *   Infinite input impedance, zero output impedance, infinite open-loop gain.
    *   Understanding the concept of virtual short.
*   Op-Amp Configurations
    *   Inverting Amplifier: Understanding gain calculation `Vout = -Rf/Rin * Vin`.
    *   Non-Inverting Amplifier: Understanding gain calculation `Vout = (1 + Rf/Rin) * Vin`.
    *   Voltage Follower (Buffer): Understanding unity gain.
    *   Summing Amplifier: Understanding how to sum multiple input voltages.
    *   Difference Amplifier: Understanding how to amplify the difference between two input voltages.
*   Op-Amp Applications
    *   Active Filters (Low-Pass, High-Pass, Band-Pass) – design and analysis.
    *   Integrators and Differentiators – understanding circuit behavior.
    *   Comparators – understanding threshold detection.
*   Real Op-Amp Limitations
    *   Input bias current, input offset voltage, finite open-loop gain, slew rate.
    *   Understanding how these limitations affect circuit performance.

**IV. Time-Domain Circuit Analysis**

*   Capacitors and Inductors
    *   Understanding capacitor voltage-current relationship: `I = C dV/dt`.
    *   Understanding inductor voltage-current relationship: `V = L dI/dt`.
    *   Energy stored in capacitors: `E = 1/2 CV^2`.
    *   Energy stored in inductors: `E = 1/2 LI^2`.
*   RC and RL Circuits
    *   Analyzing transient response of RC and RL circuits to step inputs.
    *   Calculating time constants (`τ = RC` for RC circuits, `τ = L/R` for RL circuits).
    *   Understanding the charging and discharging behavior of capacitors and inductors.
    *   Example: Calculate the voltage across a capacitor in an RC circuit as a function of time after a switch is closed.
*   RLC Circuits
    *   Understanding series and parallel RLC circuits.
    *   Analyzing the transient response of RLC circuits: overdamped, critically damped, and underdamped responses.
    *   Calculating damping ratio and natural frequency.
    *   Example: Determine the type of damping and sketch the voltage response in a series RLC circuit to a step input.

**V. AC Circuit Analysis**

*   Sinusoidal Sources and Phasors
    *   Representing sinusoidal voltages and currents using phasors.
    *   Understanding impedance of resistors, capacitors, and inductors in AC circuits (`Z_R = R`, `Z_C = 1/(jωC)`, `Z_L = jωL`).
    *   Applying phasor analysis to solve AC circuit problems.
*   AC Circuit Power Analysis
    *   Calculating instantaneous power, average power, reactive power, and apparent power.
    *   Understanding power factor and power factor correction.
    *   Example: Calculate the average power delivered to a load in an AC circuit.
*   Frequency Response
    *   Understanding the concept of frequency response and Bode plots.
    *   Analyzing the frequency response of simple filters (low-pass, high-pass, band-pass).
    *   Example: Sketch the Bode plot for a given transfer function of a filter.
*   Transformers
    *   Understanding the operation of ideal and real transformers.
    *   Calculating voltage, current, and impedance transformations.
    *   Analyzing circuits with transformers.

**VI. Digital Logic Circuits**

*   Number Systems and Boolean Algebra
    *   Binary, decimal, octal, and hexadecimal number systems.
    *   Boolean algebra operations: AND, OR, NOT, XOR.
    *   DeMorgan's theorem.
*   Logic Gates
    *   AND, OR, NOT, NAND, NOR, XOR, XNOR gates.
    *   Truth tables and logic gate symbols.
*   Combinational Logic Circuits
    *   Designing combinational logic circuits using logic gates.
    *   Simplifying Boolean expressions using Karnaugh maps (K-maps).
    *   Examples: Adders, subtractors, multiplexers, decoders.
*   Sequential Logic Circuits
    *   Latches and flip-flops (SR, D, JK, T).
    *   Registers and counters.
    *   Finite State Machines (FSMs).

**VII. Semiconductor Devices (Basic Understanding)**

*   Diodes
    *   Understanding the characteristics of a PN junction diode.
    *   Diode models (ideal, constant voltage drop, piecewise linear).
    *   Diode applications: rectifiers, clippers, clampers.
*   Bipolar Junction Transistors (BJTs)
    *   Understanding the operation of NPN and PNP transistors.
    *   BJT characteristics and operating regions (cutoff, active, saturation).
    *   BJT biasing techniques.
*   Field-Effect Transistors (FETs)
    *   Understanding the operation of JFETs and MOSFETs (NMOS and PMOS).
    *   FET characteristics and operating regions.
    *   FET biasing techniques.
