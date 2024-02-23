Setup husky in nextjs project:
1. npm install husky lint-staged --save-dev
2. In your package.json file, add the following configuration:

"husky": {
  "hooks": {
    "pre-commit": "npm run lint"
  }
}
3. npx husky init
It will create .husky folder in root directory

4. Add the following configuration in your package.json script object:
 "prepare": "husky",
 "lint": "eslint . --ext .js,.jsx,.ts,.tsx, json && prettier --write .",

Setup Eslint in nextjs project:
1. npm install eslint eslint-config-next --save-dev
2. npx eslint --init


First, run the development server:
npm run dev

Setup Prettier :
1. npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier

2. update eslint.json file content:
{
  "extends": ["next", "next/core-web-vitals", "plugin:prettier/recommended"],
  "plugins": ["prettier"]
}
3. update prettierrc.json and prettierignore file