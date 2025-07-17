# 💼 AI-Powered CV Tailoring Desktop App

An offline-first, lightweight desktop application that helps users tailor their CV to any job posting using AI or rule-based logic. Built with Electron + SvelteKit and designed for developers who want full control over their data, with optional AI integration via API or local LLM.

---

## 🚀 Project Vision

Instead of pasting an entire CV, users fill out structured sections: **Experience**, **Projects**, **Education**, **Skills**, etc. Then, by pasting a job description, the app intelligently rewrites or selects the most relevant parts of the CV to match the job.

---

## 🛠 Tech Stack

| Layer           | Technology                     |
|----------------|----------------------------------|
| Desktop App     | Electron                        |
| Frontend        | SvelteKit + Tailwind CSS        |
| Backend Logic   | TypeScript (rule-based + prompt templates) |
| Optional AI     | Claude/OpenAI APIs or local Ollama (LLM) |
| Packaging       | electron-builder                |
| State Management| Svelte stores (or localStorage) |

---

## ⚙️ Core Features

- 📋 Section-based CV input (Projects, Experience, Skills, etc.)
- 📄 Job description input
- 🧠 CV tailoring (rule-based or AI-powered)
- 🪄 Optional integration with Claude/OpenAI APIs or local LLM (Ollama)
- 📤 Export tailored CV to PDF or Markdown
- 🌐 100% offline support (no API key required by default)

---

## 🧩 Functional Modules

1. **CV Builder**
   - Fill in structured CV data: Experience, Projects, Education, Skills
   - Save/load drafts locally
2. **Job Description Parser**
   - Paste job description
   - Extract keywords and requirements
3. **Tailoring Engine**
   - Match CV content to job keywords
   - Rewrite or highlight relevant content
   - AI prompt (if online mode)
4. **Preview + Export**
   - Live preview of tailored CV
   - Export as Markdown, PDF, or plain text
5. **Settings**
   - Toggle AI mode (Offline / Claude / OpenAI / Local LLM)
   - Add API key if needed

---

## 🧭 Development Process Flow

### ✅ Phase 1: Boilerplate Setup

- [ ] Scaffold Electron + SvelteKit using `vite-plugin-electron`
- [ ] Add Tailwind CSS for UI
- [ ] Setup project structure (frontend + main process folders)
- [ ] Configure `electron-builder` for packaging

### 🧱 Phase 2: CV Builder

- [ ] Create forms for CV sections (Projects, Experience, Skills, Education)
- [ ] Use Svelte stores or localStorage to persist CV data
- [ ] Add live preview of raw CV data

### 📄 Phase 3: Job Post Parser

- [ ] Add form to paste job description
- [ ] Parse and extract required skills and responsibilities
- [ ] Highlight keywords for tailoring

### 🧠 Phase 4: Tailoring Engine

- [ ] Implement rule-based matcher (e.g. check overlap between job and CV)
- [ ] Design AI prompt template (e.g. “Rewrite this experience to match…”)
- [ ] Add option to use Claude/OpenAI via API or Ollama (localhost:11434)

### 👀 Phase 5: Preview + Export

- [ ] Preview tailored CV in rich text or markdown
- [ ] Export tailored version as PDF / Markdown / .txt

### 🛠️ Phase 6: Settings + API Integration

- [ ] Add toggle for “AI Mode: None / Claude / OpenAI / Local LLM”
- [ ] Store API key locally (optional)
- [ ] Add error handling for offline/invalid requests

### 📦 Phase 7: Packaging & Testing

- [ ] Use `electron-builder` to generate `.exe` / `.dmg` installers
- [ ] Test on Windows/Linux/macOS (if possible)
- [ ] Write basic user guide

---

## 🧪 Optional Enhancements

- 🔍 Smart scoring system: Rank how well CV matches job
- ✨ AI-generated summary/profile
- 🌐 Translate CV to other languages
- 🗂️ Resume templates with themes (Markdown-based)

---

## 🧠 Prompt Example (AI Mode)
Given the following experience:
"Developed a logistics dashboard with Angular and Spring Boot..."

And the job description:
"Looking for engineers with experience in supply chain analytics using Angular and REST APIs..."

Rewrite the experience to better match the job posting.
---

## 📁 Project Structure
IkigaiResume/
├── electron/ # Electron main process
│ └── main.ts
├── src/
│ ├── routes/ # Pages (CV, Job Post, Tailor, Settings)
│ ├── components/ # Form inputs, Preview, Match Results
│ ├── lib/ # Tailoring logic, AI prompt builder
│ ├── stores/ # Svelte stores for app state
├── static/ # Assets
├── package.json
├── vite.config.js
├── electron-builder.config.js

---

## 💬 Contributing

This is a solo project for now, but contributions are welcome if open-sourced.  
Planned license: **MIT**

---

## 📌 Final Notes

- No internet connection required for rule-based tailoring
- AI mode works with local models or Claude/OpenAI if enabled
- Everything runs locally — your data never leaves your machine by default

