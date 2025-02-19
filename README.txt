>> Node.js
sudo curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -

>> package.json
"scripts": {
    "next-dev": "next dev --turbopack",
    "next-build": "next build",
    "next-start": "next start",
    "next-lint": "next lint",
    "prettier": "prettier"
}

>> Tailwind
pnpm add -D tailwindcss@latest @tailwindcss/postcss@latest postcss@latest

>> postcss.config.mjs
const config = {
  plugins: {
    "@tailwindcss/postcss": {}
  }
}
export default config

>> page.tsx
<h1 className="text-5xl font-bold underline text-blue-400">
  I&apos;m running Tailwind 4.
</h1>   

>> ESLint
pnpm add -D eslint@latest eslint-config-next@latest

>> .eslintrc.json
{
  "extends": [
    "next/core-web-vitals",
    "next/typescript"
  ],
  "rules":{ 
    "quotes": ["error", "double", { 
      "allowTemplateLiterals": true 
    }],
    "semi": ["error", "never"],
    "indent": ["error", 2],
    "comma-dangle": ["error", "never"],
    "no-unused-vars": "off",
    "@typescript-eslint/no-unused-vars": "off"
  }
}

>> Prettier
pnpm add -D prettier@latest  prettier-plugin-tailwindcss@latest

>> .prettierrc.json
{
  "semi": false,
  "singleQuote": false,
  "jsxSingleQuote": false,
  "tabWidth": 2,
  "trailingComma": "none",
  "printWidth": 80,
  "bracketSpacing": true,
  "arrowParens": "always",
  "endOfLine": "auto",
  "bracketSameLine": false,
  "plugins": ["prettier-plugin-tailwindcss"]
}