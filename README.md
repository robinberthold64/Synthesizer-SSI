Polyphonic Analog Synthesizer – Continuous Signal Architecture

Overview
This project explores a different approach to analog synthesizer design.

Instead of building a system around fixed signal paths and discrete states, the instrument is conceived as a continuously controllable signal network.

Oscillators, filters, and amplifiers are not connected through switches, but through voltage-controlled relationships.
Signal flow is not selected — it is shaped.

Concept Focus
This project does not aim to replicate existing polyphonic synthesizers.
It explores three central ideas:

continuous signal routing instead of switching
structural control of sound generation
decentralized voice architecture

The goal is not to add more features, but to rethink how signal flow itself is controlled.

Core Principle


The instrument is not based on fixed signal paths, but on a continuously controllable signal network.

Every connection between functional blocks exists simultaneously and can be shaped in real time.
This means:
no hard switching between signal paths
no discrete routing states
no reliance on predefined configurations

Instead, the system behaves as a dynamic structure whose topology can be continuously transformed.

Structural Approach
Each voice is implemented as an independent unit (“Voice Card”) containing:

a complete analog signal structure
local digital control (MCU + DACs)
all control voltages generated locally
Rather than forming a linear signal chain, each voice behaves as a network of controllable gain stages and signal distributions.

What Makes It Different

Continuous Signal Routing
All signal paths are controlled through VCAs.
Transitions between sources, filters, and outputs are continuous rather than switched.

Structure as a Parameter

The topology of the signal path itself becomes part of the sound design.
Routing, blending, and interaction between components are not fixed — they are controllable variables.
Voice Coupling as a System
Voices can be paired and treated as structured dual units.
Offsets can be defined across:

pitch
filter parameters
timing
modulation

This goes beyond simple detuning and enables controlled divergence between coupled voices.

Dynamic Filter Topology
Two fundamentally different filters are integrated into a shared structure.
Their relationship can be continuously transformed:

parallel ↔ serial
source distribution per filter
internal filter morphing
The result is not a fixed filter configuration, but a continuously evolving topology.

Per-Voice Output Distribution
Each voice can be distributed across two independent stereo buses.
This enables:
selective external processing
separation of coupled voices
flexible routing beyond internal effects

The system deliberately avoids an internal effects section and instead supports external processing as part of the architecture.

Decentralized Control Architecture
Each voice generates its control voltages locally.
This reduces interference, shortens sensitive signal paths, and allows the system to scale without central bottlenecks.

Modulation as Structural Control
Modulation does not only affect parameters such as pitch or cutoff.

It also affects:

routing relationships
signal distribution
filter interaction

This turns modulation into a tool for shaping the structure of the sound itself.

Current Status

overall architecture defined and internally consistent
voice structure and signal flow established
core components selected (SSI2130, SSI2140/2144, SSI2164)
critical challenges identified (VCA structure, gain staging, digital integration)


The project is transitioning from conceptual design toward circuit-level implementation, where further refinement will occur through practical constraints.

Open Challenges

VCA count and structural optimization
gain staging across heterogeneous signal levels
precise filter integration and scaling
DAC structure and modulation distribution
practical implementation of the full routing architecture

These challenges arise directly from the chosen design principles and define the next development phase.

Context

This project builds on established analog synthesizer principles.

Many of the underlying technical challenges have already been solved in commercial instruments, but are only partially documented.

The task is therefore not only integration, but also:

understanding, reconstructing, and translating existing know-how into a new architectural context.


Looking for Collaboration

This project is entering the phase where practical implementation becomes critical.

I am interested in exchange and collaboration in:

analog circuit design (VCA structures, gain staging, filter integration)
KiCad schematic and PCB design
digital control systems (MCU, DACs, timing, modulation)

The goal is not to start from scratch, but to bring an existing architecture into a realizable form.

Repository Content

/docs → full concept documentation
/images → structural diagrams
(future) /kicad → schematics and PCB layouts

Motivation

The aim is to develop an instrument where:

signal flow is not fixed but continuously shaped
structure becomes part of sound design
complexity is not avoided, but organized

Rather than offering more features, the system explores a different relationship between control and sound.
