<p align="center">
  <img src="screenshots/welcome.png" alt="PracticeHub Welcome Screen" width="700"/>
</p>

<h1 align="center">Practice<em>Hub</em></h1>

<p align="center">
  <strong>A minimalist study workstation designed for language learners.</strong><br/>
  Focus. Learn. Grow. — Built to harness the power of words.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0--beta-orange?style=flat-square" alt="Version"/>
  <img src="https://img.shields.io/badge/status-In%20Development-yellow?style=flat-square" alt="Status"/>
  <img src="https://img.shields.io/badge/platform-Windows-blue?style=flat-square" alt="Platform"/>
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/electron-33.x-9feaf9?style=flat-square&logo=electron&logoColor=white" alt="Electron"/>
  <img src="https://img.shields.io/badge/react-19.x-61dafb?style=flat-square&logo=react&logoColor=white" alt="React"/>
  <img src="https://img.shields.io/badge/typescript-5.8-3178c6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
</p>

---

> [!WARNING]
> **This is an early beta release.** PracticeHub is actively under development. Features may change, break, or be removed without prior notice. Your feedback and contributions are welcome as we continue to refine the experience.

---

## 📖 About

**PracticeHub** is a cross-platform desktop application that provides an all-in-one study environment for language learners. Import books and texts, read with built-in tools, build your personal dictionary, practice vocabulary through interactive quizzes, and stay motivated with a gamified learning experience — all without leaving the app.

Whether you're studying English, preparing for exams, or simply expanding your vocabulary through reading, PracticeHub keeps everything you need in one elegant, distraction-free workspace.

---

## ✨ Features

### 📚 Smart Library
Manage your reading materials with an intuitive library interface. Import content via text paste or AI-powered PDF upload. Organize by mode: **Normal**, **Language Learning**, or **Study Session**.

<p align="center">
  <img src="screenshots/homepage.png" alt="Library Dashboard" width="800"/>
</p>

---

### 📄 Immersive Reader
A clean, focused reading experience with page-by-page navigation, progress tracking, and text highlighting in multiple colors. Supports **Language Learning Mode** with instant dictionary lookups and note-taking.

<p align="center">
  <img src="screenshots/reader.png" alt="Reader View" width="800"/>
</p>

---

### 📝 Add New Content
Import your study materials easily. Paste text directly or upload PDF files with AI-assisted text extraction. Choose your study mode, add cover images, and configure repetition settings for memorization practice.

<p align="center">
  <img src="screenshots/add_content.png" alt="Add Content Modal" width="800"/>
</p>

---

### 📗 Personal Dictionary
Build your own vocabulary database while reading. Each word entry includes definitions, pronunciation (with TTS audio), example sentences, and links to YouGlish for real-world pronunciation examples. Words are automatically organized alphabetically and grouped by source book.

<p align="center">
  <img src="screenshots/dictionary.png" alt="Dictionary Overview" width="800"/>
</p>

<p align="center">
  <img src="screenshots/dictionary_detail.png" alt="Dictionary Word Detail" width="800"/>
</p>

---

### 🎯 Practice Mode
Test your knowledge with four interactive practice modes:

| Mode | Description |
|------|-------------|
| **Word → Meaning** | See an English word and guess its meaning |
| **Meaning → Word** | See the definition and recall the English word |
| **Fill in the Blank** | Read a sentence and find the missing word in context |
| **Sound → Word** | Listen to pronunciation and type the correct word |

<p align="center">
  <img src="screenshots/practice_mode.png" alt="Practice Mode Selection" width="800"/>
</p>

---

### 🌴 Jungle — Gamified Motivation
Stay motivated with the **Jungle** mini-game. Earn drops and seeds through study activities, then use them to build your own virtual forest. Plant trees, create ponds, and lay paths — your jungle grows as your knowledge does.

<p align="center">
  <img src="screenshots/jungle.png" alt="Jungle Game" width="800"/>
</p>

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | [Electron](https://www.electronjs.org/) 33.x |
| **Frontend** | [React](https://react.dev/) 19 + [TypeScript](https://www.typescriptlang.org/) 5.8 |
| **Build Tool** | [Vite](https://vitejs.dev/) 6 |
| **Styling** | [Tailwind CSS](https://tailwindcss.com/) (CDN) + Custom CSS Variables |
| **Database** | [sql.js](https://sql.js.org/) (SQLite in browser) |
| **PDF Processing** | [pdf.js](https://mozilla.github.io/pdf.js/) |
| **Typography** | [Lora](https://fonts.google.com/specimen/Lora) + [Inter](https://fonts.google.com/specimen/Inter) |
| **Packaging** | [electron-builder](https://www.electron.build/) (NSIS installer) |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/practicehub.git
cd practicehub

# Install dependencies
npm install

# Start in development mode
npm run dev
```

### Build for Production

```bash
# Build the app
npm run build

# Create distributable installer (Windows)
npm run dist
```

The installer will be generated in the `release/` directory.

---

## 📂 Project Structure

```
practicehub/
├── electron/              # Electron main process
│   ├── main.ts            # App entry point & window management
│   ├── preload.ts         # Secure bridge between main & renderer
│   ├── database.ts        # SQLite database operations
│   ├── ipcHandlers.ts     # IPC communication handlers
│   └── audioCache.ts      # TTS audio caching system
├── src/                   # React renderer process
│   ├── App.tsx            # Root application component
│   ├── types.ts           # TypeScript type definitions
│   ├── components/
│   │   ├── Library.tsx        # Main library dashboard
│   │   ├── Reader.tsx         # Immersive text reader
│   │   ├── Dictionary.tsx     # Personal dictionary
│   │   ├── PracticeMode.tsx   # Vocabulary practice quizzes
│   │   ├── StudyNotes.tsx     # Study notes manager
│   │   ├── Jungle.tsx         # Gamified motivation system
│   │   ├── ShadowingLibrary.tsx # Shadowing technique library
│   │   ├── WelcomeScreen.tsx  # Landing screen
│   │   └── YouGlishWidget.tsx # YouGlish pronunciation widget
│   ├── services/          # Business logic services
│   └── utils/             # Utility functions
├── public/                # Static assets
├── index.html             # HTML entry point
├── vite.config.ts         # Vite configuration
└── package.json           # Project metadata & scripts
```

---

## 🎨 Design Philosophy

PracticeHub follows a **minimalist, paper-inspired** design language:

- 🌗 **Dark & Light Mode** — Seamless theme switching with smooth view transitions
- 📐 **Clean Typography** — Lora (serif) for headings, Inter (sans-serif) for body text
- 🎨 **Warm Accent Palette** — Earthy burnt orange accent colors that feel inviting, not distracting
- ✨ **Subtle Animations** — Page transitions and micro-interactions that feel natural
- 🖥️ **Custom Title Bar** — Native-feeling frameless window with custom window controls

---

## 🗺 Roadmap

- [ ] Multi-language support (UI localization)
- [ ] Cloud sync & backup
- [ ] Spaced repetition algorithm (SM-2) for vocabulary practice
- [ ] Import/export dictionary as CSV
- [ ] macOS & Linux support
- [ ] Community content sharing
- [ ] Advanced reading analytics & statistics
- [ ] Mobile companion app

---

## 🤝 Contributing

Contributions are welcome! Since this project is in early beta, please open an issue first to discuss any changes you'd like to make.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <strong>Practice<em>Hub</em></strong> — Focus. Learn. Grow.<br/>
  <sub>Made with ❤️ by the PracticeHub Team</sub>
</p>
