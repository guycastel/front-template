# React + TypeScript + Vite Template

A clean, minimal template for starting new React projects with modern tooling.

## 🚀 Features

- **React 18** with TypeScript
- **Vite** for fast development and building
- **CSS Modules** for scoped styling
- **clsx** for conditional class names
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
├── App.tsx              # Main App component
├── App.module.css       # App styles (CSS Modules)
├── main.tsx             # App entry point
├── index.css            # Global styles
├── types/
│   └── css.d.ts         # CSS Modules TypeScript definitions
└── assets/              # Static assets
```

## 🎨 CSS Modules Usage

This template uses CSS Modules for component-scoped styling:

```tsx
// Component.tsx
import styles from './Component.module.css'

function Component() {
  return (
    <div className={styles.container}>
      <h1 className={styles.title}>Hello World</h1>
    </div>
  )
}
```

```css
/* Component.module.css */
.container {
  padding: 1rem;
}

.title {
  font-size: 2rem;
  color: #333;
}
```

### Benefits

- **Scoped styles** - No global CSS conflicts
- **TypeScript support** - Autocomplete for class names
- **Automatic optimization** - Vite handles minification and hashing

## 🎯 Conditional Styling with clsx

For dynamic class names, this template includes `clsx` for clean conditional styling:

```tsx
import clsx from 'clsx'
import styles from './Component.module.css'

function Component({ isActive, isDisabled }) {
  return (
    <div
      className={clsx(styles.button, {
        [styles.active]: isActive,
        [styles.disabled]: isDisabled,
      })}
    >
      Dynamic Button
    </div>
  )
}
```

### clsx Benefits
- **Clean syntax** - No more template literals for complex conditions
- **Conditional classes** - Easy true/false class toggling
- **Multiple formats** - Supports strings, objects, arrays
- **TypeScript friendly** - Full type safety with CSS Modules

## 🔧 Configuration

- ESLint configuration in `eslint.config.js`
- Prettier configuration in `.prettierrc`
- TypeScript configuration in `tsconfig.json`
- Vite configuration in `vite.config.ts`

### Code Style Rules

- **No semicolons** at end of lines
- **100 characters** soft limit (Prettier will wrap at this length)
- **120 characters** hard limit (ESLint will error beyond this)
- **Single quotes** for strings
- **2 spaces** for indentation

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
