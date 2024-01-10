Pawink is a nextjs boilerplate for helping developer build product faster.

This readme shows how to build this boilerplate, which can let you feel free to change details in this boilerplate.

This project use pnpm pakcage manager, you can install by following command:

```bash
npm install -g pnpm
```

for more details you can check following [Installation
pnpm](https://pnpm.io/installation)

## Get started

### nextjs

```bash
pnpm create next-app@latest pawink --typescript --tailwind --eslint
```

choose questions as following:

> ✔ Would you like to use `src/` directory? … <u>No</u> / Yes

> ✔ Would you like to use App Router? (recommended) … No / <u>Yes</u>

> ✔ Would you like to customize the default import alias (@/\*)? … <u>No</u> / Yes

This command creates nextjs app with typescript and tailwindcss.

### move global.css

I'd like to move globals.css to a individual folder, use this command

```bash
mkdir styles && mv app/globals.css styles/globals.css
```

### shadcn/ui

now let's add ui component library, change directory into your project and exec following command:

```bash
pnpm dlx shadcn-ui@latest init
```

anwser a few questions:

> Would you like to use TypeScript (recommended)? no / <u>yes</u>

> Which style would you like to use? › Default

> Which color would you like to use as base color? › Slate

> Where is your global CSS file? › › styles/globals.css

> Do you want to use CSS variables for colors? › no / <u>yes</u>

> Are you using a custom tailwind prefix eg. tw-? (Leave blank if not)

> Where is your tailwind.config.js located? › tailwind.config.ts

> Configure the import alias for components: › @/components

> Configure the import alias for utils: › @/lib/utils

> Are you using React Server Components? › no / <u>yes</u>

for more details you can check [shadcn ui installation by nextjs](https://ui.shadcn.com/docs/installation/next)

### prettier

```bash
pnpm add --save-dev --save-exact prettier prettier-plugin-organize-imports prettier-plugin-tailwindcss

touch .prettierrc

touch .prettierignore

```

add following code to your .prettierrc file

```json
{
  "arrowParens": "always",
  "bracketSameLine": false,
  "bracketSpacing": true,
  "semi": true,
  "experimentalTernaries": false,
  "singleQuote": true,
  "jsxSingleQuote": true,
  "quoteProps": "as-needed",
  "trailingComma": "all",
  "singleAttributePerLine": false,
  "htmlWhitespaceSensitivity": "css",
  "vueIndentScriptAndStyle": false,
  "proseWrap": "preserve",
  "insertPragma": false,
  "printWidth": 80,
  "requirePragma": false,
  "tabWidth": 2,
  "useTabs": false,
  "embeddedLanguageFormatting": "auto",
  "plugins": ["prettier-plugin-organize-imports", "prettier-plugin-tailwindcss"]
}
```

add following code to your .prettierignore file

```
# Ignore artifacts:
build
coverage
pnpm-lock.yaml
```

now exec format

```bash
pnpm exec prettier . --write

```

now every file show be formatted

for more messages, you can check following urls:

[install prettier](https://prettier.io/docs/en/install)

[prettier-plugin-tailwindcss
](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)

[Prettier Plugin: Organize Imports](https://github.com/simonhaenisch/prettier-plugin-organize-imports)

## STILL in progressing
