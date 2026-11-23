<div align="center">

# ❄️ WINTER ASSET STUDIO

### An offline, AI-powered production environment for game assets

**From an engineering prompt to 3D characters, animation, audio, and game-ready workflows.**

<p>
  <img src="https://img.shields.io/badge/AI-LOCAL%20INFERENCE-2563eb?style=for-the-badge" alt="Local AI inference" />
  <img src="https://img.shields.io/badge/MODE-FULLY%20OFFLINE-0f766e?style=for-the-badge" alt="Offline" />
  <img src="https://img.shields.io/badge/STATUS-IN%20DEVELOPMENT-8b5cf6?style=for-the-badge" alt="In development" />
  <img src="https://img.shields.io/badge/SOURCE-PRIVATE-374151?style=for-the-badge" alt="Private source" />
</p>

*One workspace. Multiple AI models. A unified creative pipeline.*

[**The Pipeline**](#-production-pipeline) · [**Character Showcase**](#-bear-character-showcase) · [**Audio Preview**](#-audio--sound-design) · [**Roadmap**](#-roadmap)

</div>

---

## ✦ Overview

**Winter Asset Studio** is an experimental desktop environment for building game assets with **locally executed AI models**, coordinated through structured engineering prompts and an integrated workflow.

The goal is to connect the stages that normally require jumping between many different tools: concept generation, 3D geometry, materials, rigging, animation, sound design, and eventually game-system development.

Rather than relying on hosted inference services, the studio is built around a **local-first, offline approach**. AI workloads run on the developer's GPU; models and required dependencies must be obtained during setup.

> **Development note:** This is a work-in-progress project. The images document real interface states and experiments, while the full end-to-end workflow is still being developed. Features listed in the roadmap are goals, not completed capabilities.

<div align="center">
  <img src="assets/bear-walk-preview.png" width="900" alt="Bear character walking animation workspace preview in Winter Asset Studio" />
  <br />
  <sub>Walking-animation workspace: captured frame from the local animation preview. An actual animated GIF will replace this still when available.</sub>
</div>

## ⚡ What makes it different?

<table>
<tr>
<td width="50%"><b>🖥️ Fully local</b><br />Models execute on local GPU hardware, avoiding cloud inference for the core workflow.</td>
<td width="50%"><b>🔒 Private by design</b><br />Creative experiments, intermediate results, and working files remain under the developer's control.</td>
</tr>
<tr>
<td><b>🧠 Prompt-driven workflow</b><br />Structured engineering prompts are intended to coordinate specialized tools across production stages.</td>
<td><b>🌡️ GPU-aware execution</b><br />The prototype UI includes temperature monitoring, cooling thresholds, and execution safeguards.</td>
</tr>
<tr>
<td><b>🧩 Modular pipeline</b><br />Different models and tools can be evaluated independently and integrated as workflows mature.</td>
<td><b>🎮 Built for game production</b><br />The long-term goal is to progress from concepts to assets that can be validated and used in game engines.</td>
</tr>
</table>

## 🔁 Production pipeline

```mermaid
flowchart LR
    P[Structured engineering prompt] --> O[Workflow orchestration]
    O --> C[Concept / reference]
    C --> G[3D geometry]
    G --> T[Texturing / materials]
    T --> R[Rigging / skeleton]
    R --> A[Animation testing]
    A --> V[Asset validation]
    O -.-> S[Sound effects / music]
    O -.-> K[AI-assisted game code]
    S -.-> V
    K -.-> V
    classDef shown fill:#153a50,stroke:#47b0db,color:#fff;
    classDef planned fill:#353044,stroke:#a78bfa,color:#fff,stroke-dasharray: 4 4;
    class C,G,T,R,A shown;
    class S,K,V planned;
```

**Solid path:** stages shown in the current visual experiments. **Dashed paths:** broader integration and validation goals, not claims of finished automation.

---

## 🐻 Bear character showcase

A practical test character used to explore the studio's asset-production stages, from concept to animation and sound.

### 01 / Concept & GPU control

A character reference inside the studio workspace, with local GPU workload monitoring and thermal protection settings visible in the interface.

<div align="center"><img src="assets/bear-concept-gpu.png" width="920" alt="Bear concept and GPU workload controls" /></div>

### 02 / 3D geometry

An example 3D mesh preview. **Hunyuan3D Shape 2.1** is shown as the selected geometry-stage option in this experiment.

<div align="center"><img src="assets/bear-geometry.png" width="920" alt="3D bear geometry generation preview" /></div>

### 03 / Texturing & materials

The character after the texture stage. **Hunyuan Paint 2.0** appears in the interface for this test.

<div align="center"><img src="assets/bear-texture.png" width="920" alt="Textured bear asset preview" /></div>

### 04 / Rigging & skeleton

Skeletal structure and deformation tests. The screenshot shows **SkinTokens / TokenRig** among the rigging options and an example of a job interrupted by a GPU safeguard.

<div align="center"><img src="assets/bear-rigging.png" width="920" alt="Bear rigging and skeleton test" /></div>

### 05 / Animation

A quadruped animation workspace featuring the character, timeline controls, and movement testing.

<div align="center"><img src="assets/bear-animation-workspace.png" width="920" alt="Bear animation workspace screenshot" /></div>

**Walking preview**

![Bear walking animation workspace still](assets/bear-walk-preview.png)

*Still frame from the walking-animation preview. A full-motion capture will be added to the showcase.*

<!-- When a valid animated GIF is available, save it as assets/bear-walk.gif and replace the image above with:
![Bear walking — real animation captured from Winter Asset Studio](assets/bear-walk.gif)
-->

---

## 🔊 Audio & sound design

An experimental growl sound from the project's audio workflow:

**[▶ Listen to the bear sound effect (MP3)](audio/bear-growl-preview.mp3)** · 

> The MP4 uses a **still image** alongside the audio. It is a sound preview, not a moving-character animation. GitHub may display media links differently depending on the device/browser.

Sound effects and music form part of the broader intended production pipeline; this public showcase currently contains one sound-effect example.

---

## 🦊 Additional example / Fox asset pipeline

Another character experiment showing multiple visual stages, including the reference, 3D form, textured appearance, and skeletal rig view.

<div align="center"><img src="assets/fox-asset-pipeline.png" width="760" alt="Fox concept, geometry, texture and rigging workflow" /></div>

---

## 🛠️ Architecture & technical direction

| Area | Current direction |
|:--|:--|
| Runtime | Local desktop environment, offline after initial setup |
| AI processing | Local GPU inference using specialized models |
| Orchestration | Engineering prompts and modular workflows |
| 3D | Geometry generation, texturing, rigging, animation experiments |
| Monitoring | GPU temperature and task interruption controls shown in the UI |
| Audio | Experimental local sound-effect workflow |
| Target | More reliable, testable, reusable game-production pipelines |

**Development hardware:** NVIDIA RTX 5070 Ti (16 GB VRAM). This is an example development setup, **not** a verified minimum system requirement or compatibility guarantee.

The project is not currently distributed as an installable application. Its source code, AI model configurations, and internal implementation remain private.

## 🧭 Roadmap

- [x] Multi-stage asset workflow interface and prototype experiments
- [x] Screenshots of geometry, texturing, rigging, and animation workspaces
- [x] Experimental sound-effect preview
- [x] GPU-monitoring and protection controls shown in the UI
- [ ] Demonstrated, validated end-to-end unattended asset generation
- [ ] Consistent character rigging and reusable motion pipeline
- [ ] Broader SFX and music generation integration
- [ ] AI-assisted game-code and engine integration workflow
- [ ] Automated asset validation, export, and production-quality testing

*Checked items indicate demonstrated prototype work or UI features, not a claim that the entire pipeline is production-ready.*

## 🔐 Code & availability

This repository is a **public portfolio showcase** and contains **documentation and example media only**. It does not include the proprietary studio source code, installed AI models, configuration secrets, or a downloadable application.

This project is under active development. The screenshots and examples are intended to communicate its direction and experimental progress, not a finished commercial product.

## 👤 Creator

**Alexandre Kamimura Paulo (Wintersky)**  
Independent developer · Software & AI systems · Game development

[GitHub](https://github.com/AlexWintersky) · [Email](mailto:wintersky.dev@gmail.com)

---

<div align="center">

**Built locally. Designed to turn ideas into interactive worlds.**

<sub>Winter Asset Studio · Public project showcase</sub>

</div>
