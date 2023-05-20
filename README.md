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

 * `.retro` and `.ilo` files are pure RetroForth. No Unu support yet.

Again, this plugin was created in one sitting using generative AI. It is going to have small problems, but it is the only RetroForth plugin for VSCode available. Please raise an issue if it does not work for you.

`rules.md` contains the prompt used to generate this code.