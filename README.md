# ASxxxx STM8 Assembly Code Syntax Highlighting Lexer for Code::Blocks IDE

This is a syntax highlighting lexer for the [Code::Blocks IDE](https://www.codeblocks.org/) supporting the particular dialect of STM8 assembly code used by the [ASxxxx](https://shop-pdp.net/ashtml/asxxxx.php) assembler. [SDCC](http://sdcc.sourceforge.net/)'s SDAS assemblers are also based on a fork of the ASxxxx assembler, so this also supports that.

Syntax features recognised are:

* Comments
* Instructions
* Identifiers (labels, symbols, etc.)
* Numbers
* Operators
* Strings
* Registers (A, X, Y, etc.)
* Directives ('dot' keywords, e.g. ".area")

Default highlighting colours are fairly arbitrary - you will probably want to customise them. Colours can be customised in *Settings > Editor > Syntax highlighting*.

By default, *.asm and *.s files are highlighted (although, several other highlighters also match *.asm, so you may need to select this one manually if C::B chooses the wrong one). Additional file extension masks can be specified in the settings window (as mentioned above).

## Installation

1. Copy both the `.xml` and `.sample` files to installation location:
   * **Windows**: Copy files to the `%APPDATA%\CodeBlocks\share\codeblocks\lexers` folder. You may need to create the `lexers` folder if it doesn't already exist.
   * **Linux  / BSD / macOS**: Sorry, no idea! I haven't used Code::Blocks on these platforms. If I had to guess, the files should be copied to wherever the user-specific `share/codeblocks/lexers` folder resides, probably somewhere in the user home directory (i.e. `~`).
2. Restart (or start) Code::Blocks.

Once successfully installed, Code::Blocks should report in the status pane upon startup that the lexer was found and loaded without error. For example:

```
Scanning for lexers in C:\Users\<your username>\AppData\Roaming\CodeBlocks\share\codeblocks/lexers/...
Found 1 lexers
Scanning for lexers in C:\Program Files\CodeBlocks\share\codeblocks/lexers/...
Found 61 lexers
...
Loading lexer_asxxxx_stm8
...
```

A new 'ASxxxx STM8 Assembly' entry should also appear in the list of supported syntax highlighting languages in the Editor settings window.

## Resources

Other information that may be of use to anyone seeking to make modifications or create their own syntax highlighting lexer:

* https://wiki.codeblocks.org/index.php?title=Creating_a_custom_lexer_for_Code::Blocks_editor
* https://sourceforge.net/p/codeblocks/code/HEAD/tree/trunk/src/sdk/wxscintilla/include/wx/wxscintilla.h
* https://shop-pdp.net/ashtml/asst8.htm

## Licence

This work is licenced under the Creative Commons Attribution 4.0 International (CC BY 4.0) licence.
For the full licence text, please see the LICENSE.txt file, or https://creativecommons.org/licenses/by/4.0/.