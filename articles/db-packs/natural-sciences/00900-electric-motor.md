# Electric motor

An electric motor converts electrical energy into mechanical energy (torque) through the Lorentz force: a current-carrying conductor in a magnetic field experiences a sideways push, F = I ℓ × B. The inverse device, a generator, converts mechanical energy back into electrical energy. Motors consume roughly half of all electricity produced worldwide, powering disk drives, household appliances, industrial machinery, and electric vehicles.

## Anatomy

Every motor has two main parts. The **stator** is the stationary outer component; the **rotor** is the spinning inner part that delivers mechanical power through its shaft. Electrically, the **armature** carries the current on which the Lorentz force acts, and the **field magnets** (electromagnets or permanent magnets) supply the magnetic field. In most designs the field magnets sit on the stator and the armature on the rotor, though the arrangement can be reversed.

Between rotor and stator lies a thin **air gap** carrying the magnetic flux. The gap must be small to maximise torque, yet large enough that the rotating parts do not touch. The stator core uses thin insulated **laminations** of electrical steel to suppress eddy currents, which would otherwise waste energy as heat. **Bearings** support the shaft, carrying radial and axial loads.

## How torque is produced

Torque comes from the vector product of the magnetic field with the current-carrying conductors. For continuous rotation, at least one field must keep reversing its pull on the rotor.

**Mechanical commutation (DC and universal motors).** A **commutator** is a rotary switch on the rotor shaft. Stationary carbon **brushes** reverse the current in the rotor windings every half-turn (180°), so torque always points the same way. Speed is controlled by varying supply voltage, but the brushes wear, spark, generate radio interference, and limit speed and lifespan.

**Supply-driven commutation (AC motors).** Alternating current reverses many times per second, so no mechanical switch is needed. The AC stator winding produces a rotating magnetic field that drags the rotor along. **Induction motors**, the dominant industrial type, act like a transformer: the stator is the primary, the rotor the secondary, and current is induced in the rotor without electrical connection. The rotor must run slightly slower than the stator field; this difference, called **slip**, is what allows induction and torque. **Synchronous motors** lock the rotor to the stator field's exact frequency, so slip is zero.

**Electronic commutation (brushless DC).** Brushless DC (BLDC) motors place permanent magnets on the rotor and replace the mechanical commutator with electronic switching controlled by position sensors (typically Hall-effect). They reach 85–96.5% efficiency, avoid brush wear, and appear wherever reliability matters, from disk drives to electric-vehicle traction motors above 100 kW.

## Rise of AC

Volta's 1799 battery and Ørsted's 1820 discovery that current creates a magnetic field made electromagnetic motors possible. Faraday demonstrated electromagnetic rotation in 1821; Jedlik added a commutator in 1827–28; by the 1830s Sturgeon and Jacobi had built practical DC machines. Gramme commercialised the design in 1871, and Sprague's 1886 non-sparking DC motor with constant speed under load launched trolleys, elevators, and subways.

AC developed alongside DC. Ferraris and Tesla independently invented the induction motor in 1885–88, and Westinghouse acquired Tesla's two-phase patents. Dolivo-Dobrovolsky's 1889 three-phase system, with cage and wound-rotor machines, became the global standard, and the first long-distance three-phase transmission (175 km at 15 kV) was demonstrated at Frankfurt in 1891. Since the 1980s, variable-frequency drives (VFDs) have let AC motors match the speed control once exclusive to DC. In 2022, global motor sales reached an estimated 800 million units per year, growing about 10% annually.

## Performance

**Back EMF** is the voltage the rotating armature induces in itself, opposing supply and proportional to speed (V_back ∝ ω). It makes a DC motor self-regulating: load rises, speed falls, back EMF drops, current rises, torque rises until equilibrium returns. **Efficiency** η = P_mechanical / P_electrical. Peak efficiency sits near 75% of rated load, and larger motors are generally more efficient, ranging from about 15–20% (shaded-pole fractional-horsepower) to 98% (large permanent-magnet machines). Major losses are resistive I²R heating, hysteresis and eddy-current losses in the iron, bearing friction, and aerodynamic drag from cooling fans.

**Torque density** depends on air-gap area, back-iron depth, and magnetic saturation; liquid cooling raises continuous torque density about fourfold over air. Advanced designs have pushed power density toward 20 kW/kg, with yokeless axial-flux machines claiming peaks near 15 kW/kg.

## Variants and trade-offs

Specialised types include **stepper motors**, which advance in discrete steps via sequential coil energisation and appear in printers and quartz watches; **servo motors**, which pair a motor with an encoder or resolver for closed-loop position and speed control; **linear motors**, rotary motors unrolled into straight-line force (maglev trains, roller coasters); and **piezoelectric motors**, which use crystal shape change to produce ultrasonic vibration and slow motion.

Sources disagree on whether permanent-magnet synchronous, induction, or switched-reluctance motors achieve the highest continuous torque density; one source finds parity when each is optimally designed, others show permanent-magnet designs significantly ahead at ratings up to 1 MW. **Transverse-flux motors** decouple pole count from winding size for high torque density, but cogging, torque ripple, and manufacturing complexity have kept them in niche roles. **Doubly-fed machines**, with two independent multiphase winding sets, roughly double the constant-torque speed range of singly-fed motors, but control becomes unstable near synchronous speed. **Coreless rotors** reach mechanical time constants under one millisecond, ideal for disk-drive actuators and robotic servos, but they lack thermal mass and require aggressive cooling even at small sizes.

The recognition of the critical air gap, combined with AC polyphase systems and variable-frequency drives, replaced line shafts and belts with distributed, point-of-use mechanical power across modern industry.
