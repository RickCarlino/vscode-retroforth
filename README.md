# RetroForth VSCode

I lazily created a RetroForth syntax highlighter with GPT-4 in one sitting.

# Install Locally

1. Download a .vsix file from the [releases page](https://github.com/RickCarlino/vscode-retroforth/releases). You can alternatively build from source (see below).
1. `ctrl + shift +x` to open the extensions panel.
1. Select the `...` menu.
1. Select "Install from VSIX..."

# Build From Source

You will need to have a recent version of NodeJS/NPM installed.

```
git clone https://github.com/RickCarlino/vscode-retroforth
cd vscode-retroforth
npx @vscode/vsce package
```

# How It Works

 * `.retro` files are pure RetroForth. No Unu support.
 * `.unu` files are literate source files. There is one difference to a lot of
 the RetroForth files you will find on the internet: Code fences need to be labeled as `retro` (triple backtick code fences) or `retro-test` (tilde code fences) "```retro" retro or "~~~retro-test". Please look at the raw, unrendered version of this markdown file if you don't understand the examples below:

```retro
'This_is_retro_code s:put nl
```

~~~retro-test
'This_is_retro_test_code s:put nl
~~~

Again, this plugin was created in one sitting using generative AI. It is going to have small problems, but it is the only RetroForth plugin for VSCode available. Please raise an issue if it does not work for you.

`rules.md` contains the prompt used to generate this code.