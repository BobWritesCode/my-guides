# Setting up REACT with TypeScript and EsLint

## Setting up REACT with TypeScript

- run: `npx create-react-app app-name --typescript`
- run: `cd 'app-name'`
- run `npm start`
- run `tsc --init` to get .tsconfig.json file in root
- in the .tsconfig.json add/update this

```python
{
  ...
  "module": "ES6",
  ...
}
```

- run `npm init @eslint/config`
- Should have package.json file?

## Setting up EsLint

Official guide: <https://eslint.org/docs/latest/use/getting-started>

- run `npm init @eslint/config`

## Setting up EsLint-TypeScript

Official guide: <https://typescript-eslint.io/getting-started/>

- run `npm install --save-dev @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint typescript`
- create `.eslintrc.cjs` file in root
- add this:

``` js
module.exports = {
  extends: ['eslint:recommended', 'plugin:@typescript-eslint/recommended'],
  parser: '@typescript-eslint/parser',
  plugins: ['@typescript-eslint'],
  root: true,
};
```

- run `npx eslint .`

.eslintrc.js

```js
module.exports = {
  root: true,
  env: {
    browser: true,
    es2021: true
  },
  extends: [
    "eslint:recommended",
    "plugin:import/errors",
    'plugin:react/recommended',
    "plugin:react/jsx-runtime"
  ],
  plugins: [
    'react',
    "import",
    "jsx-a11y",
  ],
  overrides: [
    {
      files: ['*.ts', '*.tsx'],
      parser: '@typescript-eslint/parser',
      parserOptions: {
        project: './tsconfig.json',
        ecmaVersion: 2021,
        sourceType: "module",
        ecmaFeatures: {
          jsx: true
        }
      },
      plugins: [
        'react',
        "import",
        "jsx-a11y",
        '@typescript-eslint',
      ],
      extends: [
        'plugin:@typescript-eslint/recommended',
        'plugin:@typescript-eslint/recommended-requiring-type-checking',
      ],
      rules: {
        semi: ['error', 'always'],
        quotes: ['warn', 'single'],
        "react/jsx-uses-vars": "error",
        "react/jsx-uses-react": "error"
      }
    },
    {
      files: ['*.js'],
      extends: [
      ],
      parserOptions: {
        project: './tsconfig.json',
        ecmaVersion: 2021,
        sourceType: "module",
        ecmaFeatures: {
          jsx: true
        }
      },
      plugins: [
        "react"
      ],
      extends: [
      ],
      rules: {
        // semi: ['error', 'always'],
      }
    }
  ],
  rules: {
    "react/prop-types": "off",
    // suppress errors for missing 'import React' in files
    'react/react-in-jsx-scope': 'off',
    // allow jsx syntax in js files (for next.js project)
    'react/jsx-filename-extension': ["warn", { extensions: ['.js', '.jsx', '.ts', '.tsx'] }],
  },
};
```

tsconfig.json

```json
{
  "include": ["**/*.tsx", "**/*.js"],
  "compilerOptions": {
    "moduleResolution": "node",
    "strict": true,
    "target": "es6",
    "jsx": "react-jsx",
    "allowSyntheticDefaultImports": true,
    "noImplicitAny": true,
  }
}
```

create file called `declarations.d.tsx` and put filenames that TS does not know in here

example

```js
declare module '*.module.css' {
  const classes: { [key: string]: string };
  export default classes;
}
// This is for REACT css modules like navBar.module.css

declare module '*.json' {
  const classes: { [key: string]: string };
  export default classes;
}
// To receive Json
```
