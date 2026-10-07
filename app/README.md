# ScreenIQ – Resume Screening Prototype

A static, no-build web app for first-level resume screening. Everything runs in the browser: resumes are never uploaded to a server.

## Features
- Select a folder (or files): TXT, PDF (text-based) and DOCX are read and screened
- Extraction: name, email, phone, sections, merged (non-overlapping) experience, skill evidence, education level
- Hard (mandatory) vs soft (preferred) requirements; hard-fail cap, UNVERIFIED skills go to REVIEW
- Ranked results, per-requirement evidence, recruiter override with required reason
- Protected attributes are never used in scoring

## Not included (needs a backend)
OCR for scanned PDFs, legacy .doc, database, embeddings/semantic matching, folder watching, login/roles, audit log.

## Deploy
### GitHub
```bash
git init && git add . && git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<you>/resume-screening-app.git
git push -u origin main
```
### Vercel
1. vercel.com → Add New → Project → import the GitHub repo
2. Framework Preset: **Other**. No build command. Output directory: `public` (already set in vercel.json)
3. Deploy

Or with the CLI: `npm i -g vercel && vercel --prod`

## Run locally
Open `public/index.html` in a browser (or `npx serve public`).
