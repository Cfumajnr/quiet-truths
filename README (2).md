# Luhya Language & Culture — Project Workspace

> Working title. Final name to be chosen by the founder/community.
> Principle: **Native speakers → validated data → evaluation → model.**

## 📁 What's in this folder

```
luhya-ai/
├── README.md            ← you are here (project map)
├── METHODOLOGY.md       Data & evaluation methodology (provenance, tiers, authority)
├── DEPLOY.md            Free deployment + phone testing guide
│
├── app/                 THE APP (what users see)
│   ├── index.html       Main app: Translate · Learn · Culture · Contribute
│   ├── validate.html    Validator workspace (native speakers review entries)
│   ├── coordinator.html Coordinator console (issue codes, resolve disputes, export)
│   ├── guide.html       Validator onboarding guide (English / Kiswahili)
│   ├── data.json        Offline dictionary + phrases + proverbs (from corpus)
│   ├── manifest.json    PWA manifest (installable on Android)
│   ├── sw.js            Service worker (offline support)
│   ├── icon-512.png     App icon (green/gold seedling in speech bubble)
│   └── brand.json       Name/tagline in one place for easy rebranding
│
├── server/
│   └── server.py        Zero-dependency backend: contributions, validation
│                        tiers, invite codes, disputes, corpus export
│
├── corpus/
│   └── corpus.v0.jsonl  8,487 canonical entries (Lubukusu 5,194 + Lulogooli 3,293)
│                        Provenance-first schema; all honestly marked "unverified"
│                        (validations.jsonl, contributions.jsonl, corpus.v1.jsonl
│                         appear here as real usage begins)
│
├── schema/
│   └── entry.schema.json  The canonical record format (provenance, consent,
│                          cultural sensitivity, validation tiers)
│
├── benchmark/
│   ├── BENCHMARK.md     MulembeBench spec: 8 frozen test sets
│   ├── RESULTS.md       Results log (MB-DID baseline: 99.8% dialect ID)
│   └── baseline_dialect_id.py  Reproducible baseline script
│
└── data/
    ├── train-*.parquet       Raw imported dataset (HF, CC-BY-4.0)
    └── validation-*.parquet  (kept for provenance / reproducibility)
```

## 🔗 Live app routes (when server is running)

| Route | Who it's for |
|---|---|
| `/index.html` | Everyone — dictionary, learning, proverbs, contribute |
| `/validate.html` | Vetted native speakers (invite code required) |
| `/coordinator.html` | Community coordinator (key required) |
| `/guide.html` | New validator onboarding (EN/SW) |

## 🔑 Demo access codes (change before real deployment)

- Validator demo code: `MULEMBE2026` · Elder demo code: `ELDER2026`
- Coordinator key: `COORD2026` (issues real one-time codes like `BXK-V-7KM3QP`)

## 📊 Current state

- Corpus: 8,487 entries in canonical schema, tier: unverified (honest)
- Benchmark: MB-DID baseline run (99.8%); MT sets await gold data
- Pipeline: contribute → validate → bronze/silver/gold → export — fully tested
- Cost so far: **$0** · Next cost: $25 Play Store fee, only after testing
