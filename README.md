# Idle RPG

An idle/clicker/incremental RPG game built with modern web technologies.

## 🎮 About

This is an incremental/idle game featuring:
- Click-based resource generation
- Automatic progression systems
- Character progression and upgrades
- Modern, attractive UI/UX
- Future plans for RPG elements (classes, loot, combat)

## 🛠️ Tech Stack

- **React 19** - UI framework
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Utility-first styling
- **Zustand** - State management
- **Framer Motion** - Animations
- **React Hook Form** - Form handling

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- Yarn package manager

### Installation

1. Clone the repository
```bash
git clone https://github.com/Mundisoft/idle-rpg.git
cd idle-rpg
```

2. Install dependencies
```bash
yarn
```

3. Start the development server
```bash
yarn dev
```

4. Open your browser and navigate to `http://localhost:5173`

## 📁 Project Structure

```
src/
├── components/     # Reusable UI components
├── stores/         # Zustand state management
├── hooks/          # Custom React hooks
├── types/          # TypeScript type definitions
├── utils/          # Utility functions
└── assets/         # Static assets
```

## 🎯 Development Roadmap

### Phase 1: Foundation ✅
- [x] Project setup with React + TypeScript
- [x] Tailwind CSS configuration
- [x] Build tooling (Vite)
- [x] Git repository setup

### Phase 2: Core Game (In Progress)
- [ ] Basic click mechanics
- [ ] Resource management
- [ ] Simple upgrade system
- [ ] Progress persistence

### Phase 3: Game Enhancement
- [ ] Multiple resource types
- [ ] Achievement system
- [ ] Visual polish and animations
- [ ] Prestige mechanics

### Phase 4: RPG Features (Future)
- [ ] Character classes
- [ ] Equipment and loot
- [ ] Combat system
- [ ] Quest system

## 🤝 Contributing

This is a personal learning project, but suggestions and feedback are welcome!

## 📝 License

MIT License - see LICENSE file for details.

## 🔧 Development Commands

- `yarn dev` - Start development server
- `yarn build` - Build for production
- `yarn preview` - Preview production build
- `yarn lint` - Run ESLint

## 🎨 Design System

The game uses a custom Tailwind CSS configuration with:
- **Primary colors**: Blue theme for UI elements
- **Gold accents**: For currency and valuable items
- **Emerald accents**: For positive feedback and success states
- **Custom animations**: Hover effects, click feedback, and floating elements
