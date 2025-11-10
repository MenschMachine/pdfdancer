# PDFDancer

**Precision editing for PDFs you didn’t create.** PDFDancer lets engineering teams open any PDF in a short-lived cloud
session, locate the exact text line, paragraph, image, vector path, or form field they need, and push pixel-perfect
updates from Python, TypeScript, or Java. No desktop tooling, no brittle overlays—just real structural edits.

- Fix inbound contracts, statements, and applications without rebuilding templates.
- Run identical workflows across stacks thanks to SDK parity and shared documentation.
- Start immediately; the SDKs can request anonymous access, then scale up with real API tokens when you’re ready.

<video controls autoplay loop muted playsinline width="720">
  <source src="media/pdfdancer-demo.mp4" type="video/mp4" />
  PDFDancer demo showing pixel-perfect edits
</video>

---

## Why engineering teams pick PDFDancer

- **Locate anything** – Search by text prefix, regex, content type, or coordinate windows to grab precisely the elements
  you need (paragraphs, text lines, images, form fields, paths, and full pages).
- **True structural edits** – Builders and editors modify the PDF objects themselves, so every downstream system sees
  first-party content rather than stamped annotations.
- **Smart fonts & graphics** – Built-in font catalog, custom TTF uploads, and ML-assisted glyph matching keep typography
  consistent; vector APIs expose paths, strokes, fills, and Form XObjects for advanced layouts.
- **Forms + data workflows** – Inspect, validate, fill, or reset AcroForm fields at scale, complete with snapshots so you
  can diff before/after payloads.
- **Production ready** – Session-level auth, configurable timeouts/retries, audit-friendly logs, and optional custom
  base URLs support enterprise deployments.

---

## Built for modern PDF operations

- **Contract clean rooms** – Standardize clauses, insert initials, and auto-redact sensitive text before documents leave
  your workspace.
- **Finance packet assembly** – Merge customer PDFs, restyle metrics, add charts, and keep legacy letter/A4 templates
  untouched.
- **Form automation** – Enumerate, fill, and validate inbound applications or government forms using deterministic
  selectors.
- **Compliance + QA** – Stamp regulatory warnings, move stray elements back into the grid, or export clean snapshots for
  auditing.
- **Developer tooling** – Embed PDF fix-ups in CI/CD, CLI utilities, or browser review apps with the same SDK surface in
  every language.

---

## How PDFDancer works

1. **Open a session** with `PDFDancer.open()` (existing PDF) or `PDFDancer.new()` (blank canvas). Pass file paths, byte
   arrays, or streams.
2. **Select content** using selectors like `selectParagraphsStartingWith`, `selectFormFieldsByName`,
   `selectImagesAt(x,y)`, or raw coordinate queries.
3. **Edit or add** content via fluent builders that support moves, replacements, reflow-safe styling, custom fonts,
   image uploads, vector drawing, and form updates.
4. **Export** results to disk, a byte array, or a downstream service—without losing the original layout.

Sessions are intentionally single-threaded; create one session per concurrent workflow for predictable results.

---

## Launch in minutes

```bash
# Python 3.10+
pip install pdfdancer-client-python==0.2.22

# Node.js 20+ or modern browsers
npm install pdfdancer-client-typescript@1.0.16

# Java 11+
implementation("com.pdfdancer.client:pdfdancer-client-java:0.1.2")
```

- *No token required for prototypes.* Omit credentials and the SDK will mint an anonymous session automatically.
- *Production & higher limits.* Set `PDFDANCER_TOKEN` (or pass `token=` explicitly) and optionally customize
  `PDFDANCER_BASE_URL`, timeouts, and retries.
- *Consistent API surface.* Builders such as `newParagraph`, `newImage`, `selectFormFieldsByName`, and snapshot helpers
  behave identically across languages, so examples translate 1:1.

---

## Documentation & support

- **Guides & recipes** – [docs.pdfdancer.com](https://docs.pdfdancer.com) covers concepts, positioning, fonts, forms,
  vector graphics, snapshots, and advanced automation patterns.
- **Status & changelog** – [status.pdfdancer.com](https://status.pdfdancer.com) for uptime, incidents, and release
  history.
- **Help** – Contact your existing success channel or email `support@pdfdancer.com` for enterprise onboarding, roadmap
  discussions, or self-hosted deployments.

---

## Open-source repositories

- `pdfdancer-api-docs` – Docusaurus site that renders the unified SDK/API documentation and deploys it to GitHub Pages.
  [MenschMachine/pdfdancer-api-docs](https://github.com/MenschMachine/pdfdancer-api-docs)
- `pdfdancer-client-java` – JVM SDK with fluent selectors/builders, strict validation, and export helpers for any
  server-side or desktop workload. [MenschMachine/pdfdancer-client-java](https://github.com/MenschMachine/pdfdancer-client-java)
- `pdfdancer-client-python` – Python 3.10+ client mirroring the same object model, context managers, and structured
  exceptions. [MenschMachine/pdfdancer-client-python](https://github.com/MenschMachine/pdfdancer-client-python)
- `pdfdancer-client-python-examples` – Bite-sized Python recipes that cover text, page, image, snapshot, and form
  workflows out of the box. [MenschMachine/pdfdancer-client-python-examples](https://github.com/MenschMachine/pdfdancer-client-python-examples)
- `pdfdancer-client-typescript` – TypeScript SDK for Node.js and browser apps with retry/timeout controls, streaming
  helpers, and ergonomic builders. [MenschMachine/pdfdancer-client-typescript](https://github.com/MenschMachine/pdfdancer-client-typescript)
- `pdfdancer-client-typescript-examples` – TypeScript/TSX scripts mirroring the Python cookbook for quick demos and CI
  smoke tests. [MenschMachine/pdfdancer-client-typescript-examples](https://github.com/MenschMachine/pdfdancer-client-typescript-examples)
