# Autonomous aircraft

An autonomous aircraft flies under the control of on-board computers and sensors, with no pilot in the cockpit and no remote operator steering it moment to moment. Most contemporary autonomous aircraft are unmanned aerial vehicles (UAVs, commonly drones) running pre-programmed algorithms. Air taxis are an emerging class where artificial intelligence replaces the pilot so the vehicles can operate at scale.

## History

The earliest recorded unmanned aerial activity was military: in July 1849, Austria used unmanned balloons as aerial bomb carriers, a forerunner of the aircraft carrier. Radio-controlled drones appeared in the early 1900s as gunnery targets, and A. M. Low's powered "Aerial Target" of 1916 was an early attempt at a powered UAV. Through the twentieth century, automated navigation was developed mainly for cruise missiles, using terrain contour matching (TERCOM): comparing ground elevation below the aircraft to a stored map to correct position.

On 17 December 2025, two Bayraktar Kızılelma unmanned fighters flew in close formation using only onboard AI, the first autonomous close-formation flight by two unmanned jets. The aircraft is the first unmanned fighter with full autonomous capability.

## Passengers

Autopilots relieve pilots of routine tasks, but a human pilot remains legally required. Personal air vehicles carrying one to four passengers who cannot fly the aircraft are widely seen as depending on autonomy for adoption, and several air taxis are under development.

## Control system architecture

On-board computing evolved from analog controls to microcontrollers, then to system-on-a-chip (SOC) and single-board computers (SBC) such as Raspberry Pi.

Sensors come in two classes. Proprioceptive sensors measure the aircraft's own state (rotation rate, acceleration). Exteroceptive sensors measure the outside world, such as distance to obstacles. A unit's sensor count is described by degrees of freedom (DOF): 6 DOF means a 3-axis gyroscope plus a 3-axis accelerometer, a typical inertial measurement unit (IMU); 9 DOF adds a compass; 10 DOF adds a barometer; 11 DOF usually adds a GPS receiver.

Actuators are the moving parts the computer commands. Digital electronic speed controllers vary motor RPM and drive propellers; servomotors move control surfaces on fixed-wing aircraft and helicopters; other actuators release payloads, weapons, lights, or speakers.

## The flight stack

UAV software is called the flight stack or autopilot. Its job is to read sensors, command motors to keep the aircraft stable, and link to ground control for mission planning. Because aircraft must react in real time, they run on small computers with a real-time operating system such as NuttX, preemptive-RT Linux, Xenomai, or ROS 2.

The stack splits into three layers. Firmware executes machine code directly on the processor. Middleware handles flight control, navigation, and radio management (PX4, Cleanflight, ArduPilot). The operating system layer runs heavier tasks such as optical flow, obstacle avoidance, SLAM, and decision-making (ROS, Linux). Most stacks are open source and fork freely: CleanFlight descended from BaseFlight, and BetaFlight, iNav, and RaceFlight forked from CleanFlight.

## Control loops

UAVs use open-loop, closed-loop, or hybrid control. Open-loop sends commands without sensor feedback. Closed-loop uses feedback, typically a PID controller that adjusts output to minimise the error between measured and desired state; feedforward can apply a known correction before the error develops.

## Communications

Most UAVs use radio to exchange control commands, telemetry, and video. Early drones had only narrowband uplink; bidirectional command-and-control and downlink telemetry came later, with a separate analog video link for imagery. Long-range military flights use satellite links.

Modern autonomous applications need broadband links carrying all data on one channel, using quality-of-service techniques to keep command and control low-latency, and often carrying TCP/IP traffic routable over the internet. MAVLink is the standard protocol between ground control and the vehicle. Trials use cellular mesh and LTE for drone uplinks, and 5G mandates a user-plane latency of 1 ms for ultra-reliable low-latency communications, a target aimed partly at autonomous aircraft.

## Autonomy, from reflexes to cognition

Basic autonomy, such as holding level flight or maintaining altitude, comes from proprioceptive sensors. Advanced autonomy requires situational awareness, a model of the surrounding environment built from exteroceptive sensors, achieved by sensor fusion that combines data from multiple sensors into a single consistent picture.

A common software structure is the hierarchical control system, which breaks behaviour into layers. As of 2016, the lowest loops could run as fast as 32,000 times per second, while higher loops ran about once per second. Mid-layer algorithms include path planning, trajectory generation, and trajectory regulation, each constraining the aircraft to stay close to a planned path. The most common control mechanism is the PID controller, which can hold a quadcopter hovering by using IMU data to calculate precise inputs for the motors.

Common built-in features include altitude hold, position hold, return-to-home on signal loss, follow-me (tracking a moving person or object via GPS, image recognition, or beacon), and GPS waypoint navigation.

## Levels of autonomy

The US Air Force Research Laboratory proposed a ten-level scale (0 to 10) in 2002, framed around the OODA loop (Observe, Orient, Decide, Act): perceiving the situation, understanding it, choosing an action, and executing it. Level 0 is Remotely Piloted, with no onboard decision-making. The scale rises through preplanned missions and reactive fault handling, to mid-range levels that add multi-vehicle coordination and collision avoidance, up to higher levels that infer enemy tactics and coordinate tactical groups. Level 10 is Fully Autonomous: the aircraft is cognizant of all within the battlespace and capable of total independence.

The 2012 US Congressional Research Service report listed air-to-air combat as a possible future UAV task, and the Department of Defense's Unmanned Systems Integrated Roadmap FY2013–2038 anticipates a larger combat role, contingent on progress in autonomy, human-UAV interaction, and UAV-specific munitions.

## Reactive autonomy, SLAM, and swarming

Reactive autonomy handles immediate responses such as collision avoidance, wall following, and corridor centring. It relies on range sensors (optic flow from cameras, lidar, radar, sonar) that analyse reflected electromagnetic or sound waves. Some forms are already in consumer products and are expected to become widespread within a decade.

Simultaneous localization and mapping (SLAM) combines odometry (movement measured by sensors like IMUs) with external observations to build a 3D map of the world and the aircraft's place in it. High-altitude outdoor navigation usually relies on GPS and is simple mapping rather than true SLAM. SLAM matters most at low altitude and indoors, where photogrammetry (reconstructing 3D shape from photographs) and lidar are active research areas.

Swarming draws on swarm robotics: networks of agents that reconfigure as members enter or leave, often using bio-inspired steering and flocking behaviours.

Source: adapted from "Autonomous aircraft" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Autonomous_aircraft
