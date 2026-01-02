# Muhwezi Portfolio

>A modern, responsive developer portfolio built with React, TypeScript, Vite, and Tailwind CSS.

## Features

- Clean, responsive design
- Project showcase with cards
- Technology icons
- Light/dark theme toggle
- Modular React components
- Deployed to GitHub Pages

## Tech Stack

- [React](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/) for fast builds and HMR
- [Tailwind CSS](https://tailwindcss.com/) for utility-first styling
- [ESLint](https://eslint.org/) for code quality

## Getting Started

1. **Clone the repository:**
  ```bash
  git clone https://github.com/your-username/Muhwezi-portfolio.git
  cd Muhwezi-portfolio
  ```
2. **Install dependencies:**
  ```bash
  npm install
  ```
3. **Run the development server:**
  ```bash
  npm run dev
  ```
  The app will be available at [http://localhost:5173](http://localhost:5173).

## Building for Production

To build the optimized static site:

```bash
npm run build
```
The output will be in the `dist/` folder.

## Deployment

This portfolio is automatically deployed to GitHub Pages using GitHub Actions. On every push to the `main` branch, the site is built and published from the `dist/` directory.

## Folder Structure

- `src/components/` – Reusable React components (Header, Footer, ProjectCard, etc.)
- `src/data/` – Project data
- `src/hooks/` – Custom React hooks
- `public/` – Static assets

## Customization

- Update your projects in `src/data/projects.ts`.
- Edit content and styles in the components as needed.

## License

MIT
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
