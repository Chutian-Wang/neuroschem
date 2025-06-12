# NeuroSchem Roadmap

> *Versioned milestones from first alpha to stable 1.0*

---

## 📅 Timeline at‑a‑glance

| Milestone                              | Target window  | Status      |
| -------------------------------------- | -------------- | ----------- |
| **v0.1.x – Schema & Validator**        | Jun → Jul 2025 | ☐ *Pending* |
| **v0.2.x – Basic Drawing**             | Aug 2025       | ☐ *Pending* |
| **v0.3.x – Auto‑Layout MVP**           | Sep → Oct 2025 | ☐ *Pending* |
| **v0.4.x – LLM Handshake**             | Nov 2025       | ☐ *Pending* |
| **v0.5.x – EDA Gateways**              | Dec 2025       | ☐ *Pending* |
| **v0.6.x – UX Polish & Docs**          | Jan → Feb 2026 | ☐ *Pending* |
| **v0.7–0.8 – Public Beta**             | Mar 2026       | ☐ *Pending* |
| **v0.9 – Release Candidate**           | Apr 2026       | ☐ *Pending* |
| **v1.0.0 – Stable Human⇄AI Co‑design** | May 2026       | ☐ *Pending* |

---

## 🛠 v0.1 Series — “Schema First”

**Goal:** Lock a versioned YAML/JSON netlist contract & provide a rock‑solid validator.

* **0.1.0 Core Models**

  * `Circuit`, `Component`, `Net`, enum types (`PinSide`, `Unit`).
  * 100 % docstring coverage.
* **0.1.1 CLI Validate**

  * `neuroschem validate design.yaml` → colored errors / `--json` flag.
* **0.1.2 Schema Docs**

  * Auto‑generate JSON‑Schema & host on Read‑the‑Docs.
* **0.1.3 Round‑trip Dump**

  * `neuroschem normalize` → canonical YAML for deterministic diffs.

### Exit criteria

* Invalid pin or duplicate refdes fails fast with a single‑line error.

---

## 🎨 v0.2 Series — “First Draw”

**Goal:** Deterministic vector output for ≤ 20‑part circuits.

* **0.2.0 Linear Renderer** – chain two‑pin parts; stack multi‑pin ICs.
* **0.2.1 SVG + PNG** – output formats with DPI flag.
* **0.2.2 Anchor Hints** – support per‑pin side hints in YAML.
* **0.2.3 Visual Snap Tests** – baseline images in CI.

---

## 🗺 v0.3 Series — “Auto‑Layout MVP”

**Goal:** Graphviz‑driven hierarchical layout & Manhattan wiring.

* **0.3.0 Optional `layout` extra** – re‑introduce `networkx`, `graphviz` deps.
* **0.3.1 Graph Build ↔ Coords** – hyper‑net expansion, DOT export, grid‑snap.
* **0.3.2 Wire Router** – orthogonal segments w/ hop glyphs.
* **0.3.3 ERC pass** – crossings / stubs / unconnected nets.

---

## 🤖 v0.4 Series — “LLM Handshake”

**Goal:** Helper layer so ChatGPT & co. can generate/fix netlists autonomously.

* **0.4.0 Prompt module** – Jinja templates & reply parser.
* **0.4.1 Notebook demos** – spec → YAML → SVG round‑trip tutorial.
* **0.4.2 Streaming Errors API** – NDJSON output for reflection loops.

---

## 🔗 v0.5 Series — “EDA Gateways”

**Goal:** Export to mainstream CAD & simulation.

* **0.5.0 KiCad export** – `.kicad_sch` generator.
* **0.5.1 SPICE netlist** – passive & FET translation.
* **0.5.2 EasyEDA JSON** – optional JSON writer or extension script.

---

## 🎁 v0.6 Series — “UX Polish & Docs”

**Goal:** Freeze features; focus on usability.

* Progress bar & rich‑text output for large designs.
* Zoomable HTML viewer.
* Complete tutorial set & FAQ.

---

## 🌐 v0.7–0.8 Series — “Public Beta”

* Open GitHub Discussions/Discord.
* Triage bugs; write migration helpers if schema tweaks surface.

---

## ✅ v0.9 Series — “Release Candidate”

* Bug‑fix only; lock schema as v1.
* Reproducible wheels on all major OSes.

---

## 🚀 v1.0.0 — Stable Human⇄AI Co‑design

### Capabilities

1. Natural‑language spec → validated YAML netlist via LLM.
2. `neuroschem validate` for fast iterative error checking.
3. High‑quality SVG/PNG schematic rendering.
4. KiCad/EasyEDA & SPICE export for downstream work.
5. Error feedback easily digestible by both humans & LLMs.

### Quality promises

* Semantic‑versioning; no breaking changes until v2.
* ≥ 90 % test coverage & visual regression tests.
* Extensible plugin hooks.

---

> *Edit this roadmap as milestones evolve. Use checkboxes (☐/☑) to track completion and keep the timeline honest.*
