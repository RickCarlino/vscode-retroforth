RetroForth Syntax Rules:

  Tokens: Every element in RetroForth is a "token", constituted by a group of ASCII characters divided by whitespace (tabs, spaces, carriage returns).

  Reverse Polish Notation (RPN): RetroForth employs RPN. For example, to add 2 and 2, we write #2 #2 +.

  Special Tokens: Some tokens are unique due to their initiating sigil. For instance, an integer token starts with "#". The syntax highlighter should recognize these sigils.

  Scope: All identifiers are global unless they are defined in a closure, which is explained later.

  Multiline comments: They don't exist in Retro.

  Sigils:
    * : Indicates the beginning of a new word definition (akin to a function definition). All subsequent tokens are part of the new word's definition until a ; token is found. They should be foldable.
    * ( Marks a stack effect comment. Spaces are not permitted as they create a new token. e.g., (aa-b).
    * # Represents an integer literal, e.g., #456.
    * . Indicates a floating point number literal. e.g., .1.23.
    * ' Specifies a string literal. Strings use the underscore character instead of a space. If a literal underscore is required, it needs escaping with "". e.g., 'this_is_an_underscore:_\_.
    * ! Denotes a storage operation into a pre-defined variable.
    * & Pushes the address of a pre-defined variable onto the stack.
    * @ Pushes the stored value of a pre-defined variable onto the stack.
    * The sigils $, \, ^, `, and | are valid but less frequently used.

  Words: Any token not starting with a sigil is a "word", essentially a function call. While there aren't any keywords in RetroForth, some function calls are so critical that they might be considered as such.

  Key Words:
    * {{, ---reveal---, and }} - Double curly braces represent a closure, a section where you can define private words. It should be foldable.
    * [ and ] - Start and end of an anonymous function "quotation". Quotations are nestable. e.g., [ #1 #2 + ] call.
    * { and } - Start and end of an array (struct). e.g., { #1 #2 }.
    * ; - End of a definition, which begins with a token starting with ":". e.g., :foo 'bar ;. It should be foldable.
    * The words ",", "const", "double:const", "double:var", "FALSE", "I", "J", "K", "s,", "s:const", "TRUE", "var", "var-n", "var-s" should be highlighted differently due to their importance.
    * "repeat" and "again" - Start/end of an unconditional loop. They should be foldable.
