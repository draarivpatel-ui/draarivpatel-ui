# Aariv Patel

Open-source tools for scientific computing, hardware design, emulation and audio. Each project is plain JavaScript, HTML and CSS (or Verilog), has no runtime dependencies, and ships with a test suite that runs under Node's built-in test runner.

Most of this code was written with AI coding agents under my direction. I write the specifications, review each change, and check every feature in a real browser before it ships.

Portfolio: [aariv.me](https://aariv.me)

Each project below links to its repository and to its live page, which is served from GitHub Pages.

## Hardware, EDA and emulation

**[LogicGate](https://github.com/draarivpatel-ui/logicgate)** · [live](https://aariv.me/logicgate/) · 52 tests
Boolean equations to minimal two-level SOP and POS forms, using Quine-McCluskey prime generation and Petrick's exact cover. Includes Karnaugh maps, gate and D flip-flop netlist simulation, and IEEE 1364-2001 Verilog export with self-checking testbenches. The minimizer is checked against brute-force oracles.

**[Chipper-8](https://github.com/draarivpatel-ui/chipper-8)** · [live](https://aariv.me/chipper-8/) · 63 tests
A CHIP-8 virtual machine modeled on the 1977 RCA COSMAC VIP. It implements all 35 classic opcodes, with a two-pass assembler that resolves forward and backward labels. A cycle-by-cycle trace shows each opcode with its disassembly, alongside a RAM window around the program counter. Switchable interpreter quirks cover the COSMAC VIP and CHIP-48 behavior. Four games are written in its assembly language.

**[PadCraft](https://github.com/draarivpatel-ui/padcraft)** · [live](https://aariv.me/padcraft/) · 45 tests
Generates a complete build for RP2040 diode-matrix macropads from one configuration. The output is a KiCad 8 board file, a front copper Gerber, an ASCII STL switch plate, an OpenSCAD plate and enclosure, and KMK and QMK firmware. The generator parses its own KiCad output back and checks it.

**[RetroSave](https://github.com/draarivpatel-ui/retrosave)** · [live](https://aariv.me/retrosave/) · 49 tests
A deterministic dungeon crawler built around a technical datasheet interface. Floors are generated from a seed, and connectivity is checked by breadth-first search. Replays are signed with FNV-1a, so a single edited character is rejected. Includes an 8x8 sprite bitmask editor.

**[ttgf-cordic-alu](https://github.com/draarivpatel-ui/ttgf-cordic-alu)** · [live](https://aariv.me/ttgf-cordic-alu/) · 118 tests
An AI-assisted reference design for a multiplier-free, 8-stage CORDIC tile in Verilog. It has four operations. Rotation gives cosine and sine, vectoring gives magnitude and angle, a saturating accumulator handles running sums, and an LFSR and CRC-8 unit produces pseudo-random bytes and checksums. A co-simulation test compares the Verilog against a JavaScript model of the same design on every clock edge. Its layout was built in the Tiny Tapeout GF180MCU flow on GitHub Actions, and the precheck and gate-level test jobs passed. It has not been taped out and has not been run on hardware.

## Scientific computing, physics and CAD

**[SpectralFlow](https://github.com/draarivpatel-ui/spectralflow)** · [live](https://aariv.me/spectralflow/) · 67 tests
A D2Q9 lattice Boltzmann wind tunnel for NACA 4-digit airfoils. It uses BGK collision, a Zou-He inlet, halfway bounce-back walls, and a viscosity clamp for stability. The bench plots surface pressure Cp(x/c), wake profiles, and lift and drag history, with CSV and JSON export.

**[OrbitLab](https://github.com/draarivpatel-ui/orbitlab)** · [live](https://aariv.me/orbitlab/) · 125 tests
An astrodynamics kernel and flight dynamics console. It has an elliptic and hyperbolic Kepler solver, a universal-variable Lambert solver, an RK4 propagator with J2 oblateness, and Hohmann and bi-elliptic transfers. The porkchop plot draws contours of total delta-v and characteristic energy. Exports include GMAT scripts and CCSDS OEM ephemerides.

**[VoxelSynth](https://github.com/draarivpatel-ui/voxelsynth)** · [live](https://aariv.me/voxelsynth/) · 64 tests
Integer-lattice constructive solid geometry and signed-distance CAD for printable enclosures and mounts. Greedy quad meshing avoids T-junctions, and a half-edge check confirms that the mesh is watertight. Exporters write ASCII and binary STL, OBJ, and OpenSCAD.

## Audio DSP, civic and culinary systems

**[BeatGrid](https://github.com/draarivpatel-ui/beatgrid)** · [live](https://aariv.me/beatgrid/) · 97 tests
A Euclidean rhythm generator using Bjorklund's algorithm, with phase analysis of polymetric patterns. The analysis covers the cycle length by LCM, a coincidence matrix, and a syncopation index. It writes Standard MIDI File Format 0 and LilyPond files. It never opens an audio context.

**[TaalTrainer](https://github.com/draarivpatel-ui/taaltrainer)** · [live](https://aariv.me/taaltrainer/) · 162 tests
A Hindustani tabla practice room. Thirteen bol strokes are synthesized in real time with AudioWorklet modal resonators. It has four cyclic taals with a live avartan wheel, twelve graded call-and-response lessons scored against millisecond tolerance windows, and a recorder that transcribes phrases into Devanagari notation.

**[RailPulse](https://github.com/draarivpatel-ui/railpulse)** · [live](https://aariv.me/railpulse/) · 45 tests
A GTFS static feed parser that reads CSV or ZIP files in the browser, plus a rail reliability analyzer. It computes Marey time-distance diagrams, headway coefficient of variation, bunching rate, and excess passenger wait. A seeded cascade simulator shows delay propagating through a corridor. Seven corridors are preloaded.

**[FlavorForge](https://github.com/draarivpatel-ui/flavorforge)** · [live](https://aariv.me/flavorforge/) · 33 tests
A kitchen kinetics notebook. It models Maillard browning with Arrhenius rate laws, starch gelatinization with a hydration-shifted sigmoid, yeast growth, and espresso extraction with a Hill equation solved by bisection. It also scales recipes by baker's percentage and prints formula sheets.

## Other projects

- **[wasitme](https://github.com/draarivpatel-ui/wasitme)** is a timeline of what changed in your Claude Code and Codex sessions.
- **[Regatta](https://github.com/draarivpatel-ui/regatta)** runs several AI coding agents at once on macOS, with safety rails for operations that change a repository.
- **[AarivOS](https://github.com/draarivpatel-ui/webos)** is a small operating system that runs in a browser tab.
- **[Devlog Timer](https://github.com/draarivpatel-ui/devlog-timer)** is a timer for Hack Club Stardance builders, so no hours are lost to the 10-hour cap.
- **[Pulse](https://github.com/draarivpatel-ui/pulse-new-tab)** is a custom new-tab page with a clock, search, editable quick links, and a starfield.
- **[Garlic Panic](https://github.com/draarivpatel-ui/garlic-panic)** is a microgame collection in Godot 4, with three microgames, five lives, and one speed multiplier.
- **[studio](https://github.com/draarivpatel-ui/studio)** holds case studies of charity websites built with AI agents under my direction.

## Running a project's tests

Each README gives the exact test command. For BeatGrid, the steps are these.

```sh
git clone https://github.com/draarivpatel-ui/beatgrid
cd beatgrid
node --test test.js
```

## Licenses

Eleven projects are MIT licensed. ttgf-cordic-alu is Apache-2.0.
