# Awesome-Raster-Graphics-Photo-Editing-Software

## Top RAW Photo Processing Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Scene-Referred Workflows, GPU-Accelerated Pipelines & Local AI Denoising*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **RAW Photo Processing**. These tools decode camera sensor data into editable images — applying demosaicing, highlight reconstruction, color grading, and noise reduction — with a spectrum running from subscription-based commercial suites to open-source editors that keep your files and edits entirely on your own machine.

**Examples** include darktable, RawTherapee, RapidRAW, Filmulator, and ART (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, non-destructive editing, and local AI processing — ideal for photographers who want Lightroom-class control without Adobe's subscription or cloud dependency.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Adobe Lightroom Classic** — **The reference commercial RAW workflow.** Deep catalog management, non-destructive editing, and tight Creative Cloud integration. **Subscription required** (~$9.99–$19.99/month). **Trade-offs**: cloud dependency for many features, subscription lock-in, and the desktop version feels increasingly neglected in favor of the cloud companion . **Best for photographers** whose workflow and client expectations are built around Adobe's ecosystem.

- **Capture One Pro** — **The studio-grade tethering and color standard.** Exceptional color grading, session-based workflows, and industry-leading tethering for studio shoots. **Subscription or perpetual licensing** at premium pricing. **Best for commercial and studio photographers** needing the most precise color control and reliable tethering.

- **DxO PhotoLab** — **The lens-correction and denoising specialist.** Deep Optics modules for lens-specific correction and DeepPRIME denoising that is widely regarded as best-in-class. **One-time purchase** with optional upgrades. **Best for photographers** shooting with supported lenses who want automatic optical corrections and superior high-ISO noise handling.

## Open-Source GitHub Projects

- **darktable** — **The closest thing to a free Lightroom.** GPL-3.0 licensed, **5.4.0 stable** (December 2025) . **Runs entirely on your own computer** — RAW files and edits stay under your control rather than being tied to a subscription service . **Digital asset management is fully integrated**: the Lighttable mode handles collections, tagging, filtering, and rating, while Darkroom mode handles processing . **Lightroom XMP sidecar files are detected and used** — not fully compatible, but tags, ratings, and some edits carry over, easing migration . **The modern scene-referred workflow gives it excellent highlight recovery** and more natural tonal transitions, especially in high-contrast images . **Masks are exceptionally powerful** — you can apply a mask to almost any setting, draw it, use shapes, or base it on color or brightness values . **The honest caveat**: **it comes with a pretty hefty learning curve** — tools aren't always obviously named, and your first couple of hours will be tough . **Best for photographers wanting a mature, fully featured Lightroom alternative** who are willing to invest in learning its workflow.

- **RawTherapee** — **The advanced control specialist.** GPL-3.0 licensed, written in C++ with a GTK+ front-end . **Notable for the advanced control it gives the user over the demosaicing and development process** . **Uses a patched version of dcraw for reading RAW files**, with an in-house solution adding high-quality support for certain camera models unsupported by dcraw . **Target audience ranges from enthusiast newcomers** who wish to broaden their understanding of digital imaging to semi-professional photographers . **The honest caveat**: **professionals will probably lack peripheral features** such as digital asset management, printing, and uploading — RawTherapee is not aimed at being an all-in-one program . **Best for photographers wanting deep control over demosaicing and development** who pair it with a separate DAM.

- **RapidRAW** — **The fast, GPU-accelerated Lightroom alternative in active development.** **v1.5.2** (March 2026) added **AI denoising based on nind-denoise** applied directly to RAW images, preserving detail while removing noise . **Image analytics panel** with Luma Waveform, RGB Waveform, RGB Parade, Vectorscope, and RGB Histogram . **Parametric color and luminance masks** for targeting specific color ranges or luminance zones . **SAM-2-based subject masks** with single-click selection . **JPEG XL, WebP, and CUBE LUT export** — the LUT export lets you grade a frame in RapidRAW and apply the same grade in a video editor . **LRU cache and region-of-interest rendering** make editing while zoomed in significantly faster . **The honest caveat**: **not yet code-signed** — Windows SmartScreen and macOS quarantine warnings require manual bypass, and it is in active development, changing constantly . **Best for photographers** wanting a fast, responsive Lightroom-style editor with modern AI features, accepting early-stage software maturity .

- **Filmulator** — **The film-development simulator with a simplified interface.** **A Qt Quick GUI adaptation of Filmulator** — a film emulator with all of the positives and none of the negatives . **Simulates the development of film as if exposed to the same light as the camera's sensor**, bringing inherent benefits: large bright regions become darker (compressing dynamic range), small bright regions enhance local contrast, saturation is enhanced in bright regions, and detail is retained in extremely saturated regions . **Design ideology**: have the best tool for any job, and only that one tool — a slight decrease in flexibility in exchange for a greatly simplified and streamlined user interface . **The honest caveat**: **Linux and Windows focused** — the interface is minimal and opinionated, not a full Lightroom replacement . **Best for photographers** wanting a film-like rendering with minimal slider tweaking, especially those who prefer a streamlined workflow over exhaustive control.

- **ART** — **The RawTherapee derivative with a simpler interface.** **Free, open-source, cross-platform raw image processing program** . **Trades a bit of customization and control over various processing parameters for a simpler and (hopefully) easier to use interface**, while still maintaining the power and quality of RawTherapee . **Available via Flathub** for easy Linux installation . **Best for photographers** who find RawTherapee's interface overwhelming but want its underlying processing power.

- **AlcedoStudio** — **The GPU-accelerated RAW editor with node-based grading.** **Open-source**, with a **32-bit float pipeline that stays fluid even with 150-megapixel files** — preview holds 2.5K at 60fps while dragging sliders, resolving to 4K on release . **Neural Engine demosaicing** distilled from DemosaicNet, running on the GPU for Fujifilm X-Trans and Bayer files . **Node-based grading**: each photo's edit is a node graph with Develop, Color Grade, and Display Transform nodes, each carrying its own masks . **Git-like edit history** saved inside the project file, with named versions and branching . **Library stored in DuckDB** for responsive browsing and search, plus **natural-language search with multilingual CLIP models** running locally . **The honest caveat**: **newer project** — evaluate stability and camera support before committing a production workflow . **Best for photographers** wanting a modern GPU-accelerated editor with node-based non-destructive grading and local AI search.

- **CalibRaw** — **The cross-platform RAW editor with local AI masks.** **Free, open-source, GPU-accelerated, non-destructive** editor for Linux, Android, Windows, and macOS . **Comprehensive color and tone tools**: 8-band color mixer, 3-way color grading in Oklab, tone curves, and sigmoid tone mapping . **Demosaicing** for Bayer RCD and Fujifilm X-Trans, with automatic lens correction via Lensfun . **HDR Merge and Focus Stacking** for bracketed and focus-bracketed shots . **AI masks** for subject/background (BiRefNet), sky (SkySeg U2Net), depth range, and click-to-select objects (SAM 2.1) . **AI Remove** via Big-LaMa for object removal with native grain restoration . **AI Denoise** via RawNIND for Bayer and X-Trans RAWs . **Privacy**: every model runs on your device, downloaded only after you agree, verified by SHA-256 . **Best for photographers** wanting a modern editor with local AI masking and removal, accepting the project's relative youth.

### Additional Strong Open-Source Options

- **AlcedoStudio** — Already listed above; notable for its DuckDB library and Git-like edit history.
- **Filmulator** — Already listed above; notable for its film-development simulation approach.

**Frameworks for building custom systems**: Combine **darktable** for mature DAM plus RAW processing with scene-referred workflow, **RapidRAW** for fast GPU-accelerated editing with modern AI features, **RawTherapee** or **ART** for deep demosaicing and development control, **AlcedoStudio** for node-based non-destructive grading with local AI search, and **CalibRaw** for local AI masks and object removal — to build a RAW processing stack tailored to your need for catalog management versus pure editing, and your tolerance for learning curves versus polished defaults.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- RAW processors differ significantly in learning curve, DAM integration, and AI capability. **darktable is the closest free Lightroom replacement** with integrated library management and scene-referred workflow, but **its learning curve is steep** and tools aren't always obviously named . **RawTherapee gives the most control over demosaicing** but **lacks digital asset management and printing** — it's not an all-in-one program . **RapidRAW is fast and promising** but **not yet code-signed** and in active development, changing constantly . **Filmulator is deliberately minimal** — its film-development simulation is unique but it's not a full-featured editor . **AlcedoStudio and CalibRaw are newer projects** — evaluate stability and camera support before committing a production workflow . **No open-source tool fully matches Lightroom Classic's polish**, but darktable comes closest for catalog-plus-editing workflows.
- Self-hosted open-source solutions require proper GPU drivers (OpenCL/Metal for darktable and AlcedoStudio), sufficient disk space for RAW files and caches, and awareness that local AI models may require downloads and SHA-256 verification.

---

**Made for photographers choosing RAW processing tools that match their workflow needs, control preferences, and tolerance for learning curves.**
Let's make RAW photo processing more open, local-first, and AI-capable.
