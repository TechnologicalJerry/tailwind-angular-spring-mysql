# Tailwind CSS Setup for Angular

This document explains how Tailwind CSS has been configured in this Angular project.

## Installation

The following packages have been installed:

```bash
npm install -D tailwindcss postcss autoprefixer
```

## Configuration Files

### 1. tailwind.config.js
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{html,ts}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 2. postcss.config.js
```javascript
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

### 3. styles.scss
The main styles file has been updated to include Tailwind CSS directives:

```scss
@tailwind base;
@tailwind components;
@tailwind utilities;

/* You can add global styles to this file, and also import other style files */
```

## Usage

You can now use Tailwind CSS classes in your Angular templates. For example:

```html
<div class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 flex items-center justify-center p-4">
  <div class="max-w-md w-full bg-white rounded-lg shadow-lg p-6">
    <h1 class="text-2xl font-bold text-gray-900 mb-2">Hello Tailwind!</h1>
    <button class="bg-blue-500 hover:bg-blue-600 text-white font-semibold py-2 px-4 rounded-lg">
      Click me
    </button>
  </div>
</div>
```

## Development

To start the development server:

```bash
npm start
# or
ng serve
```

The application will be available at `http://localhost:4200`

## Build

To build for production:

```bash
npm run build
# or
ng build
```

## Customization

You can customize Tailwind CSS by modifying the `tailwind.config.js` file. For example, to add custom colors:

```javascript
module.exports = {
  content: [
    "./src/**/*.{html,ts}",
  ],
  theme: {
    extend: {
      colors: {
        'custom-blue': '#1e40af',
      },
    },
  },
  plugins: [],
}
```

## Resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Angular Documentation](https://angular.dev)
- [PostCSS Documentation](https://postcss.org)
