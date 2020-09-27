# npm-init

Frequently used node package manager configuration.

## NPM

**Installation**   
```
$ npm init -y
```

---

## Sass

**Installation**   
```
$ npm install node-sass
```

**Usage**   

output: [nested | expanded | compact | compressed]
```
$ node-sass src/assets/scss --output dist/assets/scss
$ node-sass --output-style compressed src/assets/scss --output dist/assets/scss
```

watch
```
$ node-sass --watch src/assets/scss --output dist/assets/scss
```

**Documents**   
<https://www.npmjs.com/package/node-sass>   

---

## Autoprefixer

**Installation**   
```
$ npm install postcss postcss-cli autoprefixer
```

**Configuration**   
Make the configuration file .browserslistrc.
```
# Browsers that we support

last 2 version
> 1%
IE > 8
```

**VSCode**   
Edit the configuration file settings.json.
```
{
  "autoprefixer.options": {
    "overrideBrowserslist": [
      "last 2 version",
      "> 0.1%",
      "IE > 8"
    ]
  },
}
```

**Usage**   
```
$ npx postcss src/assets/css --use autoprefixer -d dist/assets/css
```

**Documents**   
<https://www.npmjs.com/package/autoprefixer#cli>   
<https://github.com/browserslist/browserslist>   

---

## ESLint

**Installation**   
```
$ npm install eslint
```

**Configuration**   
Make the configuration file .eslintrc.json.
```
{
  "env": {
    "commonjs": true,
    "es6": true,
    "node": true
  },
  "extends": ["prettier", "eslint"],
  "plugins": ["prettier"],
  "parserOptions": {
    "ecmaVersion": 2018
  },
  "rules": {
    "prettier/prettier": "error"
  },
}
```

**VSCode**   
Edit the configuration file settings.json.
```
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
  "source.fixAll.eslint": true
  },
}
```

**Documents**   
<https://eslint.org/docs/user-guide/configuring>   
<https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint>   

---

## TSLint

**Installation**   
```
$ npm install -g typescript tslint
```

**Configuration**   

Make the configuration file tslint.json.
```
tslint --init
```

Edit the configuration file tslint.json.
```
{
  "defaultSeverity": "error",
  "extends": ["tslint:latest", "tslint-eslint-rules", "tslint-config-prettier"],
  "jsRules": {},
  "rules": {},
  "rulesDirectory": []
}
```

**VSCode**   

Edit the configuration file settings.json.
```
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
  "source.fixAll.tslint": true
  },
}
```

**Documents**   

---

## Prettier

**Installation**   
```
$ npm install --save-dev --save-exact prettier eslint-plugin-prettier eslint-config-prettier tslint-config-prettier 
```

**Configuration**   
Make the configuration file .prettierrc.
```
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true
}
```

**VSCode**   
Edit the configuration file settings.json.
```
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true
  },
  "[javascript]": {
    "editor.formatOnSave": true
  },
  "[javascriptreact]": {
    "editor.formatOnSave": true
  },
  "[typescript]": {
    "editor.formatOnSave": true
  },
  "[typescriptreact]": {
    "editor.formatOnSave": true
  },
  "[json]": {
    "editor.formatOnSave": true
  },
  "[graphql]": {
    "editor.formatOnSave": true
  },
  "files.autoSave": "afterDelay",
  "prettier.trailingComma": "all",
  "prettier.tabWidth": 2,
  "prettier.semi": true,
  "prettier.singleQuote": true
}
```

**Documents**   
<https://prettier.io/docs/en/configuration.html>   
<https://github.com/prettier/eslint-config-prettier>   
<https://github.com/prettier/tslint-config-prettier>   
<https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode>   

---

## Babel

**Installation**   
```
$ npm install --save-dev @babel/core @babel/cli
$ npm install --save-dev @babel/preset-env
```

**Configuration**   
Make the configuration file .babelrc.
```
{
  "presets": ["@babel/preset-env"]
}
```

Edit the configuration file package.json.
```
{
  "scripts": {
    "build": "babel src/assets/js -w -d dist/assets/js"
  }
}
```

**Usage**   
```
$ npm run build
```

**Documents**   
<https://babeljs.io/docs/en/configuration>   
