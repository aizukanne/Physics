# Plan: Adding Visual Guidance to CONTENT_DEVELOPMENT_GUIDE.md

This document outlines the plan for updating the `CONTENT_DEVELOPMENT_GUIDE.md` to include comprehensive guidance on using images and diagrams in the Physics course content.

## 1. Add Introduction
*   Briefly state the goal: Create high-quality, engaging Physics educational content.

## 2. Stress Importance of Visuals
*   Explain *why* images/diagrams are crucial:
    *   Illustrating abstract concepts (fields, wave-particle duality).
    *   Visualizing experimental setups.
    *   Breaking down complex processes.
    *   Representing data (graphs, charts).
    *   Improving engagement and retention.

## 3. Guidelines for Inclusion
*   Specify *when* to add visuals:
    *   Concepts difficult to grasp via text alone.
    *   Showing relationships (force diagrams, vector addition).
    *   Depicting apparatus or procedures.
    *   Representing circuits, ray diagrams, potential wells, etc.
    *   Guiding question: "Would a picture make this clearer?"

## 4. Generating Diagrams and Images
*   Suggest methods/tools:
    *   **Mermaid:** For simple diagrams embedded in Markdown.
    *   **External Tools:** `draw.io` (diagrams.net), Inkscape, GeoGebra.
    *   **Simulation/Graphing Software:** Output from physics/math software.
    *   **Hand-drawn:** Clear, neat, legible scans/photos.

## 5. Image Formatting and Storage
*   Define standards:
    *   **Formats:** PNG (diagrams), JPG (photos), SVG (vector).
    *   **Naming:** `[topic#]-[subtopic#]_[description].[format]` (e.g., `02-1_free_body_diagram.png`).
    *   **Storage:** `assets/` or `images/` subfolder within each topic directory (e.g., `01-Measurements-and-Units/assets/`).
    *   **Alt Text:** Mandatory descriptive alt text for accessibility.

## 6. Review and Update
*   Encourage continuous improvement by adding visuals to existing content.

## Decision Flowchart (Mermaid)

```mermaid
graph TD
    A[Identify Concept/Process] --> B{Clear with text alone?};
    B -- No --> C[Add Visual];
    B -- Yes --> D[Text Sufficient];
    C --> E{Visual Type?};
    E --> F[Diagram];
    E --> G[Graph/Chart];
    E --> H[Illustration/Setup];
    E --> I[Photo];
    F --> J{Creation Tool?};
    J --> K[Mermaid];
    J --> L[draw.io/Inkscape/GeoGebra];
    J --> M[Hand-drawn];
    G --> N[Graphing Software];
    H --> L;
    I --> O[Use Existing/Take Photo];
    K --> P[Embed Code];
    L --> Q[Create Image File];
    M --> Q;
    N --> Q;
    O --> Q;
    Q --> R[Save to Assets Folder];
    R --> S[Add to Markdown w/ Alt Text];
    P --> S;
    S --> T[End];
    D --> T;