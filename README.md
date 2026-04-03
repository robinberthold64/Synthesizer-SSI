# Synthesizer-SSI
Exploring a polyphonic analog synth architecture with continuous routing and modular voice cards

# Polyphonic Analog Synth – Voice Card Architecture

## Overview

This project explores the design of a polyphonic analog synthesizer based on a modular **voice card architecture**.
Each voice is implemented as a self-contained unit, including the full analog audio path and local digital control.

The goal is not to reinvent synthesis from scratch, but to **combine and extend established analog design principles** into a flexible and coherent system.

---

## Architecture

Each voice card includes:

* 2× VCO (based on SSI2130)
* 2× Filters (multimode + ladder, e.g. SSI2140 / SSI2144)
* VCA-based routing system
* Stereo output stage with dual bus architecture
* Local digital control (MCU + DACs)

### Core Principle

Signal paths are not switched, but continuously controlled:

> Morphing, crossfading, and distribution replace fixed routing.

---

## Key Ideas

* Continuous signal flow instead of discrete switching
* Functional separation of components (e.g. carrier/modulator roles)
* Integration of analog signal path with digital control
* Dual stereo output buses for flexible external processing

---

## Current Status

* Overall architecture defined and documented
* Voice structure and signal flow established
* Core components selected (SSI2130, SSI2140/2144, SSI2164)
* Critical challenges identified

The project is now transitioning from **concept development** to **circuit-level implementation**.

---

## Open Challenges

* VCA structure and possible reduction
* Gain staging across all signal levels
* Filter input scaling and stability
* DAC allocation and modulation structure
* Practical integration into a polyphonic system

---

## Context

This project builds on established analog synthesizer principles.

Many of the underlying technical challenges have already been solved in commercial instruments.
However, these solutions are often not publicly documented.

The challenge is therefore not only integration, but also:

> understanding and translating existing know-how into a new architecture.

---

## Looking for Collaboration

I am interested in exchange and collaboration in the following areas:

* Analog circuit design (VCA, filters, gain staging)
* KiCad / PCB layout
* Digital control (MCU, DACs, timing)

The concept is largely developed –
the focus is now on **implementation and refinement through practice**.

---

## Repository Content

* `/docs` → Concept documentation
* `/images` → Block diagrams / architecture
* (future) `/kicad` → Schematics and PCB designs

---

## Motivation

The goal is to develop a synthesizer that is:

* structurally clear
* technically grounded
* and flexible in sound design

The next step is to turn this architecture into real hardware.

---
