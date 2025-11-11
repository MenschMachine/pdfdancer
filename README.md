# PDFDancer

**The editing API for PDFs you didn’t create.** Open any PDF you receive, target the exact paragraph, line, glyph, vector, or form field you need, and commit real edits from Python, TypeScript, or Java—no template rebuilds, no overlay tricks, no designer involved. ML-backed font recommendations/substitutions keep typography intact even when the original font files are missing.

This repo is the developer landing page for the PDFDancer ecosystem.

- Product tour: [pdfdancer.com](https://www.pdfdancer.com)
- Docs + SDK surface: [`pdfdancer-api-docs`](https://github.com/MenschMachine/pdfdancer-api-docs) / [docs.pdfdancer.com](https://docs.pdfdancer.com)

![PDFDancer demo showing pixel-perfect edits](media/pdfdancer-demo.gif)

🎥 Full walkthrough: watch the high-resolution demo at [pdfdancer.com/demo](https://www.pdfdancer.com/demo).

---

## Why backend developers stay

- **Edits the PDFs you already have** – PDFDancer treats PDFs like a document format, not a printer target. No begging for the source file—even if the text is split into glyphs or vectorized runs.
- **Selectors written for humans** – Target text via prefixes, regex, fonts, bounding boxes, or semantic IDs; the DSL is identical in every SDK.
- **Reflow-safe text + fonts** – Work at paragraph/line level instead of glyph soup. Built-in ML font recommendations/substitutions keep embedded fonts editable while kerning and ligatures stay intact.
- **ML font intelligence** – Automatic font matching, substitution, and upload helpers keep obscure or missing fonts editable without breaking layout.
- **Vector + asset control** – View and tweak paths, strokes, fills, Form XObjects, and embedded images directly in code.
- **Forms are first-class** – Enumerate, validate, fill, and reset AcroForm/XFA fields with before/after snapshots for audits.
- **Deploy on your terms** – Anonymous eval mode, hosted API, or self-hosted installs with auth scopes, retry knobs, and structured logs.

---

## How it compares to legacy libraries

| You expect… | PDFDancer delivers | Traditional tools do… |
| --- | --- | --- |
| Edit PDFs you didn’t author | Treats PDFs like a document format: exposes paragraphs, lines, glyphs, vectors, forms for direct edits | Force layout rebuilds, page shuffles, or annotation overlays |
| Semantic selectors | Text/regex/font/bounding-box selectors shared across SDKs | Expose low-level operator streams; you track glyph runs manually |
| Layout-safe text & font edits | Paragraph-level reflow plus ML font recommendations keep spacing, kerning, ligatures, and custom fonts intact | Store text as disconnected glyphs, substitute fonts blindly, and break layout when you edit |
| Font intelligence | ML-powered matching/substitution plus managed uploads | Leave you to hunt down missing fonts manually |
| Vector & asset control | Inspect/change paths, strokes, fills, Form XObjects, and embedded images | Flatten vectors to bitmaps or punt to desktop design tools |
| Form automation | Enumerate/fill/reset AcroForm & XFA with snapshots | Stop at basic checkbox filling; advanced logic still needs Acrobat |

---

## What developers ship with PDFDancer

- **Localization without layout drift** – Swap copy in multilingual brochures, contracts, or product sheets while paragraph shapes stay intact.
- **Compliance-safe edits** – Insert clauses, update rates, or delete sensitive text directly inside existing agreements and disclosures.
- **Financial & regulatory packets** – Normalize inbound statements, restyle disclaimers, and guarantee mandatory sections remain untouched.
- **Designer/agency handoffs** – Lock creative layouts, expose approved regions, and let scripts change prices, SKUs, or timelines safely.
- **Form-heavy workflows** – Enumerate, validate, fill, and reset AcroForm/XFA fields across applications, onboarding packs, or inspections.

---

## Getting started

Skip straight to the [PDFDancer Getting Started guide](https://docs.pdfdancer.com) for SDK installation, auth, and first-edit walkthroughs.

---

## Access & pricing

- **Free evaluation** – Spin up sessions without credentials; exported PDFs carry a subtle watermark so you can verify workflows safely.
- **Pro plans** – Upgrade for watermark-free exports, higher throughput, and extended retention. Pricing lives on [pdfdancer.com/pricing](https://www.pdfdancer.com/#pricing) along with contact options for enterprise deployments.

---

## Where to go next

- **Complete API docs** – [`pdfdancer-api-docs`](https://docs.pdfdancer.com) houses the SDK references, guides, and the Getting Started walkthrough.
- **Blog** – [pdfdancer.com/blog](https://www.pdfdancer.com/blog/) covers deep dives, release notes, and customer workflows.
- **Changelog** – [pdfdancer.com/changelog](https://www.pdfdancer.com/changelog/) tracks what’s new.
- **Roadmap** – Follow along at [docs.pdfdancer.com/roadmap](https://docs.pdfdancer.com/roadmap/) for upcoming milestones.
- **Talk with us** – Ping your success channel or email `support@pdfdancer.com` for onboarding, roadmap input, or self-hosted deployments.

---

## Open-source ecosystem

- `pdfdancer-api-docs` – Unified SDK/API docs rendered with Docusaurus and deployed to GitHub Pages. [MenschMachine/pdfdancer-api-docs](https://github.com/MenschMachine/pdfdancer-api-docs)
- `pdfdancer-client-java` – JVM SDK exposing fluent selectors, validation, and exports for servers or desktops. [MenschMachine/pdfdancer-client-java](https://github.com/MenschMachine/pdfdancer-client-java)
- `pdfdancer-client-python` – Python 3.10+ SDK mirroring the object model, context managers, and structured exceptions. [MenschMachine/pdfdancer-client-python](https://github.com/MenschMachine/pdfdancer-client-python)
- `pdfdancer-client-python-examples` – Bite-sized Python recipes covering text, page, image, snapshot, and form flows. [MenschMachine/pdfdancer-client-python-examples](https://github.com/MenschMachine/pdfdancer-client-python-examples)
- `pdfdancer-client-typescript` – TypeScript SDK for Node.js and browsers with retry/timeout controls, streaming helpers, and ergonomic builders. [MenschMachine/pdfdancer-client-typescript](https://github.com/MenschMachine/pdfdancer-client-typescript)
- `pdfdancer-client-typescript-examples` – TypeScript/TSX scripts mirroring the Python cookbook for demos and CI smoke tests. [MenschMachine/pdfdancer-client-typescript-examples](https://github.com/MenschMachine/pdfdancer-client-typescript-examples)
