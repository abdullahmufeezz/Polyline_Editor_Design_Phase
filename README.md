# README: Polyline Editor Design Phase

## Project Overview
The **Polyline Editor Lab** is a specialized application designed for **2D and 3D vertex editing**. This project focuses on transitioning from user needs to a functional application rooted in core **Human-Computer Interaction (HCI)** principles to ensure a deterministic, user-friendly experience.

---

## Details
* **Student:** Muhammad Abdullah Mufeez (B23110006080) 
* **Course:** HCI-CG (III-year Sec-A) 
* **Instructor:** Dr. Humera Tariq 
* **Design Paradigm:** Keyboard-first modal editing 

---

## Key Features & HCI Principles

### 1. Structural Design (State Transition Network)
The system utilizes a **State Transition Network (STN)** to manage application flow.
* **Defined States:** IDLE, DRAWING, MOVING, DELETING, and HOVERING.
* **Deterministic Transitions:** Key presses (e.g., 'b', 'm', 'd') and mouse clicks facilitate movement between states to prevent the system from becoming stuck.

### 2. Visibility & Feedback
* **Visual Indicators:** Selected vertices are highlighted with a circle or glow to improve precision.
* **Status Bar:** A persistent bar displays the current mode, polyline count (up to 100), zoom level, and undo/redo history.
* **Current Mode Display:** Explicitly states the active tool (e.g., HAND mode) to reduce user confusion.

### 3. Controls & Affordances
* **Logical Mapping:** Controls are mapped to intuitive keys:
    * **B:** Begin (Drawing) 
    * **D:** Delete 
    * **M:** Move 
    * **H:** Hand/Hover 
    * **R:** Refresh 
    * **Q:** Quit 
* **Fitts’s Law Optimization:** Mouse interaction uses a **10-pixel threshold** to balance speed and accuracy during vertex selection.

### 4. Constraints & Safety Nets
* **Error Recovery:** Includes **Undo/Redo** functionality (Ctrl+Z) to allow users to recover from mistakes.
* **Data Integrity:** Deleting a vertex automatically reconnects adjacent points to maintain the polyline structure.
* **3D Depth Control:** Specific constraints allow vertex depth adjustment via `Alt + Arrow` keys or a dedicated slider.

---

## Design Evolution
1.  **Low-Fidelity Design:** Initial wireframing of the canvas, mode selection area, and status panels.
2.  **STN Logic:** Mapping every possible user action to ensure a robust functional flow.
3.  **Final High-Fidelity UI:** A polished interface featuring a grid-based canvas, thematic styling, and integrated 3D depth tools.
