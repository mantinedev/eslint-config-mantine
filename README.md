# eslint-config-mantine

## Install

```sh
yarn add --dev @eslint/js eslint eslint-plugin-jsx-a11y eslint-plugin-react typescript-eslint eslint-config-mantine
```

## Usage

In your `eslint.config.js`:

```tsx
const mantine = require("eslint-config-mantine");
const tseslint = require("typescript-eslint");

module.exports = tseslint.config(
  ...mantine,
  {
    languageOptions: {
      parserOptions: {
        project: "./tsconfig.eslint.json",
      },
    },
  },
  { ignores: ["**/*.{mjs,cjs,js,d.ts,d.mts}"] }
);
```

## License

MIT
