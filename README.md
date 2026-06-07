# 🏢 Workroom

> A modern virtual workspace platform that transforms online collaboration into an immersive, natural experience.

![Version](https://img.shields.io/badge/version-1.0.0--beta-a78bfa?style=flat-square)
![Status](https://img.shields.io/badge/status-public%20beta-34d399?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-38bdf8?style=flat-square)

---

## Overview

Workroom reimagines remote collaboration by placing users inside beautifully designed 2D virtual offices. Inspired by the design language of macOS Tahoe, it combines glassmorphism, smooth animations, and clean interfaces to create a premium digital environment for teams, schools, communities, and events.

Unlike traditional video conferencing platforms, Workroom is spatial — users control avatars, move freely through the workspace, and communication activates naturally based on proximity.

---

## Features

### 🗺️ 2D Office Explorer
Move your avatar with WASD or arrow keys through a top-down rendered office. Walk into meeting rooms, drop into the lounge, or retreat to a focus zone.

### 🎙️ Proximity-Based Voice & Video
Audio and video fade with distance — just like a real room. Conversations happen spontaneously as avatars move near each other, with no "start meeting" button required. Includes spatial audio, background blur, and noise suppression.

### 🏗️ Office Templates
Launch in seconds from professionally designed layouts:

| Template | Best For |
|---|---|
| **Startup HQ** | Engineering teams, sprint rooms, investor lounges |
| **Creative Studio** | Design teams, critique rooms, art direction |
| **School Campus** | Online classrooms, libraries, tutoring sessions |
| **Community Hub** | Events, town halls, large-scale communities |

All templates are fully customisable.

### 🔒 Private Rooms & Permissions
Lock rooms to specific members, set guest access levels, create admin-only spaces, or designate whiteboard-only zones.

### 💬 Persistent Chat & Reactions
Every room has its own chat thread with file sharing, polls, and emoji reactions — no app switching needed.

### 🎨 Avatar Customisation
Hundreds of skins, accessories, and cosmetics — many unlockable through gameplay.

### 🏆 Gamification System
- **Experience Points (XP)** earned through collaboration and daily participation
- **Achievements** for streaks, introductions, voice conversations, and more
- **Badges** displayed on your profile (Pioneer, Collab, Fast, Ideas, Streak, and more)
- **Cosmetic rewards** tied to in-office activity

---

## Getting Started

### Prerequisites

- A modern browser (Chrome 100+, Firefox 100+, Safari 16+, Edge 100+)
- No downloads required for end users

### Running Locally (Frontend)

```bash
git clone https://github.com/your-org/workroom.git
cd workroom
open workroom.html
```

Or serve with any static server:

```bash
npx serve .
# → http://localhost:3000
```

### Environment Setup (Full Stack)

```bash
cp .env.example .env
npm install
npm run dev
```

Key environment variables:

```env
VITE_API_URL=https://api.workroom.app
VITE_WS_URL=wss://ws.workroom.app
VITE_GOOGLE_CLIENT_ID=your_google_client_id
VITE_GITHUB_CLIENT_ID=your_github_client_id
```

---

## Project Structure

```
workroom/
├── workroom.html          # Main single-file frontend (landing page)
├── src/
│   ├── office/            # 2D canvas engine & avatar logic
│   ├── voice/             # Proximity audio/video system
│   ├── gamification/      # XP, badges, achievements
│   ├── templates/         # Office template definitions
│   └── auth/              # Sign-in & account creation flows
├── public/
│   ├── avatars/           # Default avatar assets
│   └── icons/             # UI icons and badges
├── docs/                  # Extended documentation
└── README.md
```

---

## Design System

Workroom's UI is built on a macOS Tahoe–inspired design language:

- **Glassmorphism** — `backdrop-filter: blur()` layered surfaces with translucent borders
- **Typography** — Mona Sans (UI) + Instrument Serif (display italics)
- **Color palette** — Deep navy base (`#09090f`) with purple (`#a78bfa`), sky blue (`#38bdf8`), and emerald (`#34d399`) accents
- **Motion** — CSS keyframe animations for avatar floats, proximity rings, voice waves, and scroll reveals
- **Dark-first** — Designed exclusively for dark mode environments

---

## Roadmap

- [ ] Mobile app (iOS & Android)
- [ ] Screen sharing inside the 2D office
- [ ] Whiteboard rooms with collaborative drawing
- [ ] Webhook integrations (Slack, Notion, Linear)
- [ ] Custom avatar builder
- [ ] Public API for office bots and automations
- [ ] Multi-floor office support
- [ ] Guest mode (no account required)

---

## Contributing

Contributions are welcome. Please open an issue before submitting a pull request so we can discuss the change.

```bash
git checkout -b feature/your-feature-name
git commit -m "feat: describe your change"
git push origin feature/your-feature-name
```
---

<p align="center">Made with 🤍 for distributed teams everywhere.</p>
