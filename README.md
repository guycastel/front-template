# React + TypeScript + Vite Template

A clean, minimal template for starting new React projects with modern tooling.

## 🚀 Features

- **React 18** with TypeScript
- **Vite** for fast development and building
- **ESLint** for code quality
- **Prettier** for code formatting
- **npm** as package manager

## 📦 Getting Started

1. Clone this repository or use it as a template
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start development server:
   ```bash
   npm run dev
   ```

## 📜 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run lint:fix` - Run ESLint with auto-fix
- `npm run format` - Format code with Prettier
- `npm run format:check` - Check code formatting

## 🛠️ Project Structure

```
src/
├── App.tsx          # Main App component
├── App.css          # App styles
├── main.tsx         # App entry point
├── index.css        # Global styles
└── assets/          # Static assets
```

## 🔧 Configuration

- ESLint configuration in `eslint.config.js`
- Prettier configuration in `.prettierrc`
- TypeScript configuration in `tsconfig.json`
- Vite configuration in `vite.config.ts`

## 📝 License

This template is free to use for any project.

````

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config({
  plugins: {
    // Add the react-x and react-dom plugins
    'react-x': reactX,
    'react-dom': reactDom,
  },
  rules: {
    // other rules...
    // Enable its recommended typescript rules
    ...reactX.configs['recommended-typescript'].rules,
    ...reactDom.configs.recommended.rules,
  },
})
````
