# Idle RPG Development Guide

## Working with Cline AI Assistant

This guide outlines best practices for developing the Idle RPG project with Cline as your AI development companion.

### Session Management

#### Starting a New Development Session
1. Open the project workspace in VSCode
2. Review the current checkpoint in `.cline/checkpoints.md`
3. Check for any actively running terminals
4. Start development server: `yarn dev`
5. Review recent commits: `git log --oneline -5`

#### Before Each Session
- [ ] Confirm current working directory: `/home/grim/repos/idle-rpg`
- [ ] Check git status: `git status`
- [ ] Verify development server status
- [ ] Review last checkpoint progress

#### Ending a Session
- [ ] Commit all changes with descriptive messages
- [ ] Push changes to GitHub: `git push origin master`
- [ ] Update checkpoint progress in `.cline/checkpoints.md`
- [ ] Note any incomplete tasks or issues for next session

### Development Workflow

#### Feature Development Process
1. **Plan** - Define the feature scope and acceptance criteria
2. **Implement** - Write code incrementally, testing frequently
3. **Test** - Verify functionality in browser and check for errors
4. **Refine** - Polish UI/UX and optimize performance
5. **Commit** - Save progress with clear commit messages
6. **Document** - Update checkpoints and add any notes

#### Git Workflow
```bash
# Check current status
git status

# Add changes
git add .

# Commit with descriptive message
git commit -m "Feature: Add click mechanic with resource generation

- Implement basic click handler
- Add gold counter with animations
- Store state in Zustand store
- Persist game state to localStorage"

# Push to GitHub
git push origin master
```

#### Testing Checklist
- [ ] Development server starts without errors
- [ ] No console errors in browser
- [ ] UI renders correctly on different screen sizes
- [ ] Interactive elements respond to user input
- [ ] Game state persists between page refreshes
- [ ] All new features work as expected

### Project Architecture

#### File Organization
```
src/
├── components/          # Reusable UI components
│   ├── ui/             # Generic UI components (Button, Card, etc.)
│   └── game/           # Game-specific components
├── stores/             # Zustand state management
│   └── gameStore.ts    # Main game state store
├── hooks/              # Custom React hooks
│   └── useGameState.ts # Game state management hooks
├── types/              # TypeScript type definitions
│   └── game.ts         # Game-related interfaces
├── utils/              # Utility functions
│   ├── gameLogic.ts    # Game calculations and logic
│   └── storage.ts      # Local storage helpers
└── assets/             # Static assets (images, sounds)
```

#### Component Design Principles
- **Separation of Concerns**: Keep game logic separate from UI components
- **Reusability**: Create generic components that can be reused
- **Type Safety**: Use TypeScript interfaces for all props and data
- **Performance**: Use React.memo and useMemo where appropriate
- **Accessibility**: Include proper ARIA labels and keyboard navigation

### Code Standards

#### TypeScript Guidelines
- Always define interfaces for props and data structures
- Use strict type checking
- Prefer `interface` over `type` for object definitions
- Use meaningful names for variables and functions

#### React Best Practices
- Use functional components with hooks
- Implement proper error boundaries
- Keep components small and focused
- Use custom hooks for complex state logic

#### Styling Guidelines
- Prefer CSS custom properties for dynamic values
- Use semantic class names
- Keep game-specific styles in dedicated CSS classes
- Ensure responsive design with mobile-first approach

### Debugging Tips

#### Common Issues and Solutions
1. **Tailwind classes not working**
   - Check PostCSS configuration
   - Verify Tailwind directives in index.css
   - Ensure content paths are correct in tailwind.config.js

2. **Development server errors**
   - Clear node_modules and reinstall: `rm -rf node_modules && yarn`
   - Check for syntax errors in configuration files
   - Verify all dependencies are properly installed

3. **Game state not persisting**
   - Check localStorage implementation
   - Verify JSON serialization/deserialization
   - Ensure state updates trigger properly

4. **Performance issues**
   - Use React DevTools to identify re-renders
   - Implement memoization where appropriate
   - Check for memory leaks in timers/intervals

### Next Steps

When ready for Checkpoint 2 (Core Game Mechanics):
1. Define game state interface in `src/types/game.ts`
2. Create Zustand store in `src/stores/gameStore.ts`
3. Implement click handler and resource generation
4. Add basic upgrade system
5. Create localStorage persistence
6. Test all functionality thoroughly

### Useful Commands

```bash
# Development
yarn dev                 # Start development server
yarn build              # Build for production
yarn preview            # Preview production build
yarn lint               # Run ESLint

# Git
git status              # Check working directory status
git log --oneline -10   # View recent commits
git diff                # See unstaged changes
git add .               # Stage all changes
git reset --hard HEAD   # Reset to last commit (destructive)

# Project
find src -name "*.ts*"  # List all TypeScript files
grep -r "TODO" src/     # Find TODO comments
du -sh node_modules     # Check node_modules size
