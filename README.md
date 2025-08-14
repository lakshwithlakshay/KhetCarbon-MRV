# KhetCarbon-MRV
A multi-layer MRV platform designed for India’s smallholder landscape. Farmers or field agents capture plot-level data via a simple mobile app, which syncs with satellite and drone feeds. AI models analyze and merge datasets to estimate carbon credits, generate registry-compatible reports, and provide farmers with earnings projections.





KhetCarbon MRV — Scalable MRV for Agroforestry & Rice

Low-cost, offline-first MRV platform for smallholder agroforestry and rice carbon projects. Fuses mobile evidence, remote sensing, and a verifier dashboard to produce verification-ready, IPCC-aligned reports.

✨ Key Features

Offline mobile data capture (photos w/ EXIF, GPS polygon, checklists, IVR consent)

RS indicators: NDVI, NDMI; rice methane reduction vs baseline

Evidence pack: hash-linked logs, versioned records, exportable PDF

Verifier dashboard: queue, case detail, request info, sign & export

Localization (EN/HI), low-end device friendly

🧠 Tech Stack

Mobile/Web: React (PWA), Tailwind, shadcn/ui, Framer Motion

Backend (MVP): FastAPI/Node, PostgreSQL + PostGIS, object storage (S3)

RS/ML: Rasterio/xarray, LightGBM → ONNX/TFLite (edge-capable)

Security: JWT, role-based access, hash-chain audit log

Integrations: SMS/WhatsApp, registry export (JSON/PDF)

📦 Repo Structure

khetcarbon-mrv/
├─ apps/
│  ├─ web/           # React PWA (this mockup)
│  └─ verifier/      # Verifier UI (merged for demo)
├─ services/
│  ├─ api/           # FastAPI/Node (stubs)
│  └─ rs/            # RS/ML pipelines (notebooks + scripts)
├─ docs/
│  ├─ concept-note/
│  ├─ ipcc-alignment.md
│  └─ cost-model.xlsx
├─ sample_evidence/  # JSON, EXIF-stripped photos (synthetic)
└─ LICENSE


🚀 Quick Start (Mock UI)

Clone repo

cd apps/web && npm i && npm run dev

Open http://localhost:5173
(No backend required for the mock.)

🧪 Evidence Pack (sample)

form.json (farmer profile, practice checklist)

photos/*.jpg (timestamp, GPS)

gps.geojson (plot polygon)

audit.log (append-only hash chain)

indicators.json (NDVI/NDMI + uncertainty)

🧭 IPCC Alignment

IPCC 2006 Guidelines + 2019 Refinement

Versioned emission factors in /docs/ipcc-alignment.md

Uncertainty bands displayed in reports

💰 Cost & Sustainability

Target ops cost: ₹50–₹150/farmer/season via offline-first capture, automated RS pre-screening, and asynchronous verification.

🔐 Responsible AI

Consent-first flows, privacy by design, explainable indicators, bias checks across agro-climatic zones.
