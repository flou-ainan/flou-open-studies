#Install and config Styled JSX in NextJS Project
Motivation: 
    I found it a little more difficult than it usually is to install and use a very simple tool recommended by the Next documentation itself.
    So, i've made this tutorial.


##Install and Settings

1) Install the package:

```bash
npm install --save styled-jsx
```

3) Create a file named `.babelrc` in the root of your NextJS project

NextJS have babel settings under the hood ([docs](https://nextjs.org/docs/pages/building-your-application/configuring/babel)), but if you need to extend it you will need to add this file.

```json
{
  "presets": ["next/babel"],
  "plugins": []
}
```

2) Add `styled-jsx/babel` to `plugins` in your babel configuration:

Your file will be like this

```json
{
    "presets": ["next/babel"],
    "plugins": ["styled-jsx/babel"]
}
```
3) Set Vscode syntax highlight, code auto completion and color helper

In your VSCode hit `Ctrl + P` to launch Quick Open, paste the following commands and press enter.

#### Install Syntax Highlighting [Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=Divlo.vscode-styled-jsx-syntax)

```
ext install Divlo.vscode-styled-jsx-syntax
```
#### Install Autocomplete [Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=Divlo.vscode-styled-jsx-languageserver)


```
ext install Divlo.vscode-styled-jsx-languageserver
```

#### Install Styled Colors [Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=nyxb.vscode-styled-colors)

```
ext install nyxb.vscode-styled-colors
```

4) If you use Eslint on your project

If you're using `eslint-plugin-import`, the `css` import will generate errors, being that it's a "magic" import (not listed in package.json). To avoid these, simply add the following line to your eslint configuration file `.eslint.json` in your root directory:

```json
"settings": {"import/core-modules": ["styled-jsx/css"] }
```

### That was it for me
If you use Typescript or have any other things to config that are not listed here, take a look into the original documentation [here](https://github.com/vercel/styled-jsx#styled-jsx)
