This is an alternative Kate syntax highlighter for JavaScript, which works well
with Closure-style code.

This highlighter recognizes a few things that the built-in highlighter doesn't:
- Function declarations and arguments, separately.
- JsDoc tags, including type annotations.
- "this", property references and method calls.
- Class references (partial).
- Named constants.
- Closure compiler directives.
- Common Closure globals/namespaces/functions.

The other differences from the built-in highlighter are:
- Properly limits what can come after a period.
- Does not recognize global variables when used after a period.
- Does not differentiate identifiers and identifier paths.
- Does not do in-regex highlighting.

Drop it into `~/.kde/share/apps/katepart/syntax` for Kate to find. For example:

    mkdir -p ~/.kde/share/apps/katepart/syntax
    wget https://raw.github.com/max99x/kate-js-closure/master/js-closure.xml \
      -O ~/.kde/share/apps/katepart/syntax/js-closure.xml

To set it as the default JS highlighter, go to Settings -> Configure Kate -> Open/Save -> Modes & Filetypes, select Scripts/JavaScript-Closure and set Priority to 1.

![Screenshot](https://github.com/max99x/kate-js-closure/raw/master/screenshot.png)
