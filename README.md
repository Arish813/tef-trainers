# TEF Trainers

Two self-contained browser tools for TEF Canada written-expression practice, built around the
**Regarder → Cacher → Écrire → Vérifier** (look–cover–write–check) method.

**Live:** https://arish813.github.io/tef-trainers/

| Tool | What it does |
|---|---|
| `orthographe.html` | Word-level spelling drill. A word is shown inside a sentence with its tricky syllable highlighted, then hidden; you retype the full sentence from memory and get a character-level diff. Anki-style grading (Encore / Difficile / Bien / Acquis) schedules how soon each word comes back within the session. |
| `paragraphe.html` | Paragraph-level reconstruction. Paste a model text, then rebuild it line by line from memory with word-level diffing. Tracks both score and peek count per text over time — fewer peeks at the same score means the memory is actually consolidating. |

## Why this exists

The writing block was diagnosed as **orthographic memory**, not grammar knowledge: most errors are
phonetic (writing what you hear — `houres` → `heures`, `querant` → `quarante`, `mainé` → `mené`).
Reading rules doesn't fix that. Retrieval practice does.

## Data & privacy

No backend, no accounts, no analytics, no network calls. Everything lives in the browser's
`localStorage` (`tef-ortho-v1` / `tef-paragraphe-v1`).

Because storage is per-device, each tool has **⬇ Sauvegarder (.json)** and **⬆ Restaurer (.json)**:
export on one device, transfer the file yourself, import on the other. Restore **replaces** local
data rather than merging, so the most recent export wins.

## Running locally

Open any of the `.html` files directly in a browser. No build step, no dependencies, no server.
