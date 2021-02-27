# Recolor

Uses the [colorize](https://github.com/kingcons/colorize) syntax highlighting library to create a colorized  WordprocessingML version of your code for inclusion in a Microsoft Word `docx` file.

*function* **RECOLOR-STRING** `string` `&OPTIONAL` `(coloring-type :lisp)`

Returns a string representation of `string` as colorized according to `coloring-type` (which is passed thorugh to colorize) as WordprocessingML. colorize currently supports the following types:

* :common-lisp

* :elisp

* :scheme

* :clojure (*alpha*)

* :c

* :c++

* :java

* :python

* :erlang

* :haskell

* :objective-c

* :diff

* :webkit

The resulting WordprocessingML refers to (Microsoft Word) styles with the same names as the colorize CSS styles with "md" prepended (so that, for example, "symbol" becomes "mdsymbol"). You should arrange for these styles to be present in your `docx` file:

* mdsymbol

* mdspecial

* mdkeyword

* mdcomment

* mdstring

* mdatom

* mdmacro

* mdvariable

* mdfunction

* mdattribute

* mdcharacter

* mdsyntaxerror

* mddiff-deleted

* mddiff-added
