# Awesome-Raster-Graphics-Photo-Editing-Software

# Awesome-Raster-Graphics-Photo-Editing-Software

# Top Raster Graphics & Photo Editing Software Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Layer-Based Compositing, Non-Destructive Editing & GPU-Accelerated Workflows*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Raster Graphics & Photo Editing Software**. These tools manipulate pixel-based imagery — retouching, compositing, color grading, and illustration — with a spectrum running from the industry-standard commercial suites to open-source editors that have matured into genuine daily drivers.

**Examples** include GIMP, Krita, PhotoCraft, and the commercial platforms (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, GPU-native rendering, and transparent file format support — especially relevant as **GIMP 3.2.6** ships with non-destructive link layers and vector layers [citation:1][citation:2], and **PhotoCraft** emerges as a Rust-native Photoshop alternative with genuine PSD round-trip fidelity [citation:6][citation:7].

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Adobe Photoshop** — **The industry-standard raster editor.** Layer-based compositing, masks, smart objects, and a massive plugin ecosystem. **Subscription required** (~$22.99/month standalone). **Trade-offs**: subscription lock-in, cloud dependency for many features, and an increasingly bloated interface. **Best for professionals** whose client workflows and file deliverables demand .psd compatibility and Adobe ecosystem integration.

- **Affinity Photo** — **The one-time-purchase professional alternative.** **Free after Canva's acquisition**, with a fast native engine, full PSD import/export, and focus stacking, HDR merging, and 360-degree editing. **Trade-offs**: **no Linux build** and no plugin ecosystem comparable to Photoshop. **Best for designers on Windows or Mac** wanting professional raster editing without subscriptions.

- **Corel PaintShop Pro** — **The accessible Windows-only alternative.** **One-time purchase** with a perpetual license option. **Best for hobbyists and small businesses** on Windows wanting a Photoshop-like toolset without Adobe's subscription, accepting Windows-only availability.

- **Photopea** — **The browser-based Photoshop clone.** **Free with ads; paid tier (~$5/month) removes ads.** **Opens native .psd files directly** with full layer, mask, and smart object support. **Trade-offs**: **requires an internet connection** and shows ads on the free tier. **Best for users needing Photoshop compatibility in a browser** without installing anything.

## Open-Source GitHub Projects

- **GIMP (GNU Image Manipulation Program)** — **The reference open-source raster editor.** GPL-licensed, **3.2.6** (September 2026) [citation:2] . **Cross-platform** on GNU/Linux, macOS, and Windows [citation:2] . **GIMP 3.2 introduced significant non-destructive workflows**: **Link Layers** let you incorporate external images into compositions and update automatically when source files change, and the **Path tool can now create Vector Layers** for scalable shapes with adjustable fill and stroke [citation:1] . **High-quality photo manipulation, original artwork creation, and scripted image manipulation** with multi-language support (C, C++, Python, Scheme) . **The honest caveat**: **the interface and workflow differ significantly from Photoshop** — muscle memory doesn't transfer, and some professional workflows (advanced typography) require workarounds. **Best for Linux users, students, and budget-conscious designers** needing a full-featured free editor with active development and a proven track record.

- **Krita** — **The painting-first raster editor.** GPL-licensed, **5.3.0** (March 2026) stable, with **6.0.0** as an experimental Qt6 build [citation:10] . **Exceptional brush engine** with pressure sensitivity, stabilizers, and wrap-around mode for seamless textures. **The 5.3 release completely rewrote the text tool** with on-canvas editing, full OpenType support, and text flowing in shapes — making comic panels easier than ever [citation:3][citation:10] . **New filters** include color propagation and reset transparency, with faster Liquify mode and real-time recorder dock [citation:10] . **Improved PSD support** including text objects in PSD files [citation:10] . **The honest caveat**: **it is not a general-purpose photo editor** — it lacks the advanced selection and compositing tools of GIMP or Photoshop, and is optimized for painting and illustration rather than photo retouching. **Best for digital painters, illustrators, and concept artists** wanting the best free painting experience available.

- **PhotoCraft (ArtCraft)** — **The Rust-native Photoshop alternative in early alpha.** Part of **ArtCraft's Crafting Apps** suite aiming to rebuild Adobe's toolset as open-source Rust applications [citation:6] . **Layers, masks, adjustment layers, layer styles, text, vectors, brushes, and smart objects** [citation:6][citation:7] . **PSD/PSB round-trip fidelity**: achieved a round trip of **134 out of 135 test files** where content remained unchanged after load and save [citation:6] . **Supports RGB, CMYK, Lab, grayscale, and 8/16/32-bit documents** with ICC color management and soft proofing [citation:6] . **GPU rendering via Metal, Vulkan, DirectX 12, and WebGPU** [citation:6] . **The honest caveat**: **early alpha** — much of Photoshop's feature surface exists in some form, but **it is not yet a Photoshop replacement for daily professional work**, with gaps in AI/generative features, depth in typography, and plug-in compatibility [citation:7] . **Best for early adopters** wanting a native Linux Photoshop alternative with genuine PSD compatibility, accepting alpha-stage maturity.

### Additional Strong Open-Source Options

- **RapidRAW** — **The GPU-accelerated RAW editor built with performance in mind.** **Active development** with AI NIND denoising, subject mask models, image analytics (vectorscopes, waveforms, parades, histograms), and JPEG XL/WebP/AVIF export [citation:11] . **Not yet code-signed** — macOS and Windows show warnings requiring manual bypass [citation:12] . **Best for photographers** wanting a fast, modern Lightroom-style editor, accepting early-stage software maturity.
- **Pixelmator Pro** — **Not open-source**, but notable as a Mac-only one-time-purchase alternative with ML-powered upscaling and a polished native interface. Best for Mac users wanting a non-subscription Photoshop alternative.

**Frameworks for building custom systems**: Combine **GIMP** for general-purpose raster editing with non-destructive link and vector layers, **Krita** for painting and illustration with an exceptional brush engine, **PhotoCraft** for a Rust-native Photoshop-familiar experience with PSD round-trip fidelity, and **RapidRAW** for RAW photo processing — to build a raster editing stack tailored to your platform (Linux vs Windows/Mac), primary use case (photo retouching vs painting vs compositing), and tolerance for alpha-stage software.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Raster editors differ significantly in primary use case (photo retouching vs painting vs compositing), platform support, and file format fidelity. **GIMP is the most complete general-purpose open-source editor** with active development and new non-destructive workflows, but its workflow differs from Photoshop and advanced typography workflows require workarounds [citation:1] . **Krita is a painting tool, not a photo editor** — it excels at illustration but lacks advanced compositing and selection tools . **PhotoCraft is early alpha** — its PSD round-trip fidelity is impressive but it is not yet a production Photoshop replacement [citation:7] . **Affinity Photo has no Linux build**, and **Corel PaintShop Pro is Windows-only**. **Photopea requires an internet connection** and shows ads on the free tier.
- Self-hosted open-source solutions require proper GPU drivers (OpenGL for GIMP, GPU rendering for PhotoCraft), sufficient RAM for large layered documents, and awareness that PSD compatibility varies by tool and feature set.

---

**Made for designers, photographers, and illustrators choosing raster editing tools that match their platform, workflow, and budget.**
Let's make raster graphics and photo editing more open, GPU-native, and workflow-appropriate.
