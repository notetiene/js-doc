# sass-doc
Insert SassDoc style comment easily in Emacs

## Installation
1. Put `sass-doc.el` somewhere in your emacs load path.
2. Add a line below to your .emacs file:

```scheme
(require 'sass-doc)
```

## Example
Paste the codes below into your configuration file and you:

1. insert function document by pressing `Ctrl + c, i`
2. insert `@tag` easily by pressing `@` in the SassDoc style comment

 If you want to see the tag description, just input the next command
   M-x sass-doc-describe-tag

## Configuration
```scheme
(setq sass-doc-mail-address "your email address"
       sass-doc-author (format "your name <%s>" sass-doc-mail-address)
       sass-doc-url "url of your website"
       sass-doc-license "license name")

 (add-hook 'sass-mode-hook
           #'(lambda ()
               (define-key sass-mode-map "\C-ci" 'sass-doc-insert-function-doc)
               (define-key sass-mode-map "@" 'sass-doc-insert-tag)))
```
