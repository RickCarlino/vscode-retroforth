# RetroForth VSCode

I lazily created a RetroForth syntax highlighter with GPT-4 in one sitting.

How it works:

 * Install this extension.
 * `.retro` files are pure RetroForth. No Unu support.
 * `.unu` files are literate source files. There is one difference to a lot of
 the retroforth files you will find on the internet: Code fences need to be labeled as `retro` (triple backtick code fences) or `retro-test` (tilde code fences)`\`\`\`retro` or `~~~retro-test`. Please look at the raw, unrendered version of this markdown file if you don't understand the examples below:

```retro
'This_is_retro_code s:put nl
```

~~~retro-test
'This_is_retro_test_code s:put nl
~~~

Again, this plugin was created in one sitting using generative AI. It is going to have small problems, but it is the only RetroForth plugin for VSCode available. Please raise an issue if it does not work for you.