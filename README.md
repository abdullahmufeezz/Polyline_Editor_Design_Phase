# README: Polyline Editor Design Phase

## Project Overview
[cite_start]The **Polyline Editor Lab** is a specialized application designed for **2D and 3D vertex editing**[cite: 74]. [cite_start]This project focuses on transitioning from user needs to a functional application rooted in core **Human-Computer Interaction (HCI)** principles to ensure a deterministic, user-friendly experience[cite: 2, 3].

---

## Technical Specifications
* [cite_start]**Student:** Muhammad Abdullah Mufeez (B23110006080) [cite: 17, 18]
* [cite_start]**Course:** HCI-CG (III-year Sec-A) [cite: 19]
* [cite_start]**Instructor:** Dr. Humera Tariq [cite: 20]
* [cite_start]**Design Paradigm:** Keyboard-first modal editing [cite: 74]

---

## Key Features & HCI Principles

### 1. Structural Design (State Transition Network)
[cite_start]The system utilizes a **State Transition Network (STN)** to manage application flow[cite: 3].
* [cite_start]**Defined States:** IDLE, DRAWING, MOVING, DELETING, and HOVERING[cite: 4, 64].
* [cite_start]**Deterministic Transitions:** Key presses (e.g., 'b', 'm', 'd') and mouse clicks facilitate movement between states to prevent the system from becoming stuck[cite: 5].

### 2. Visibility & Feedback
* [cite_start]**Visual Indicators:** Selected vertices are highlighted with a circle or glow to improve precision[cite: 8].
* [cite_start]**Status Bar:** A persistent bar displays the current mode, polyline count (up to 100), zoom level, and undo/redo history[cite: 9, 95, 97, 98].
* [cite_start]**Current Mode Display:** Explicitly states the active tool (e.g., HAND mode) to reduce user confusion[cite: 90, 91].

### 3. Controls & Affordances
* **Logical Mapping:** Controls are mapped to intuitive keys:
    * [cite_start]**B:** Begin (Drawing) [cite: 75, 76]
    * [cite_start]**D:** Delete [cite: 77]
    * [cite_start]**M:** Move [cite: 81]
    * [cite_start]**H:** Hand/Hover [cite: 82]
    * [cite_start]**R:** Refresh [cite: 80, 83]
    * [cite_start]**Q:** Quit [cite: 84]
* [cite_start]**Fitts’s Law Optimization:** Mouse interaction uses a **10-pixel threshold** to balance speed and accuracy during vertex selection[cite: 12].

### 4. Constraints & Safety Nets
* [cite_start]**Error Recovery:** Includes **Undo/Redo** functionality (Ctrl+Z) to allow users to recover from mistakes[cite: 13, 97].
* [cite_start]**Data Integrity:** Deleting a vertex automatically reconnects adjacent points to maintain the polyline structure[cite: 14].
* [cite_start]**3D Depth Control:** Specific constraints allow vertex depth adjustment via `Alt + Arrow` keys or a dedicated slider[cite: 100].

---

## Design Evolution
1.  [cite_start]**Low-Fidelity Design:** Initial wireframing of the canvas, mode selection area, and status panels[cite: 21, 24, 33].
2.  [cite_start]**STN Logic:** Mapping every possible user action to ensure a robust functional flow[cite: 35, 36].
3.  [cite_start]**Final High-Fidelity UI:** A polished interface featuring a grid-based canvas, thematic styling, and integrated 3D depth tools[cite: 72, 89, 99].
