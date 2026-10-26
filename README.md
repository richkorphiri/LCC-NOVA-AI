# LCC NOVA AI

Records and services web chat for Lusaka City Council. Prototype by Team Apex, University of Zambia, for the AI for Public Good Challenge. Not an official council service. Synthetic sample data only.

Static site (no build step): `index.html` + `crest.png` + `data/records.js`.

## Run locally
Open `index.html` in a browser.

## Update the data
1. Put your CSV in `sample/records.csv` and one `.txt` per record in `sample/docs/`.
2. `node scripts/build-data.mjs sample` (needs Node 18+). This rewrites `data/records.js`.
3. Commit and push. Vercel redeploys.
Never commit real council data without written approval (see `.gitignore`).

## Connect the Voiceflow agent
Open `index.html`, find `const VOICEFLOW_PROJECT_ID = "";` near the bottom, paste your Project ID between the quotes, commit and push.

## Voiceflow knowledge base files
In `kb/`: upload `LCC_KB_records_table.csv` as a Table and the PDFs in `kb/pdf/` as Docs. Agent prompt: `kb/Voiceflow_Agent_Instructions.txt`.
