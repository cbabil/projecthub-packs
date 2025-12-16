# React Pack

**Version: 0.2.1**

Modern React + TypeScript development setup with Vite, ESLint 9 (flat config), Prettier, and Husky git hooks.

## Contents

### react-gitignore
Standard ignore patterns for React/Node.js projects. Covers:
- `node_modules/`, build outputs (`dist/`, `.next/`)
- Environment files (`.env`, `.env.local`)
- Editor/OS files (`.vscode/`, `.DS_Store`)

### react-workspace
Complete React + TypeScript starter with:
- **Vite 6** - Fast dev server and build tool
- **React 18.3** - Latest React with concurrent features
- **TypeScript 5.6** - Strict type checking
- **ESLint 9** - Flat config with React hooks and refresh plugins
- **Prettier** - Consistent code formatting
- **Husky** - Git hooks for pre-commit checks

## Usage

1. Install the pack via ProjectHub
2. Create a new project and select `react-workspace`
3. Run:
   ```bash
   npm install
   npm run dev
   ```

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start dev server |
| `npm run build` | Type-check and build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint |
| `npm run lint:fix` | Fix ESLint issues |
| `npm run format` | Format with Prettier |
| `npm run typecheck` | Run TypeScript type checking |

## Git Hooks

Pre-commit hooks are automatically installed via Husky when you run `npm install`. The hooks check for:
- Sensitive data (email, username, API keys, passwords)
- Sensitive files (.env, .pem, .key, etc.)
- Linting and type errors

## Compatibility

- ProjectHub >= 1.0
- Node.js >= 18
