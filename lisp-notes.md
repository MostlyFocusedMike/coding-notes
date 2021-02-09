# Lisp Notes
These notes are coming from the free Lisp book http://www.gigamonkeys.com/book/

# Chapter 2
This book is hella out of date and the software for lisp-in-a-box no longer seems to work, use https://portacle.github.io/ instead (it's a pain to open with macs the first time, but once you finally get it onto your dock and open it from there, it will work. (copy the file from the .dmg into your applications folder as well)

## Choosing a Lisp Implementation
- Unlike other langs (Python, Java) which have a benevolent dictator controlling the standard, lisp instead has an ANSI standard to block this
- There are many implementations of Lisp that cover the standard Common Lisp standard, but have extra extensions
- Everything in this book works with the Common Lisp implementation
- See CH. 32 for more info on Lisp types
--------------------------------------------------------------------------------------------------------------------------------
## Getting Up and Running with Lisp in a Box
In order to get the SLIME (Superior Lisp Interaction Mode for Emacs) working you will need to use Emacs. Here are some handy key bindings

```plaintext
The little line at the bottom where the meta commands go is called the
"mini-buffer"
C-g C-g   abandon meta commands

NAVIGATION
C-v       Page down
M-v       Page up
C-l       that's the L key, and it makes it scrolls up/down so centered of screen

			  Previous line, C-p
				  :
				  :
   Backward, C-b .... Current cursor position .... Forward, C-f
				  :
				  :
			    Next line, C-n

M-f       Move forward by word
M-b       Move backward by word
C-a       Move to start of line
C-e       Move to end of line

C-w       Cut  (Kill-region)
M-w       Copy (Kill-ring-save)
C-y       Paste (yank)
M-y       Paster older things
C-/       Undo


C-x C-c   Quit emacs
C-x C-s   Save file

WINDOW CONTROLS

C-x b     Switch Current window's buffer (look up ido-mode)
C-x o     Move to other window
C-x 2     Split window -----
C-x 3     Split Window |
C-x 0     Get rid of current window
C-x 1     Get rid of other windows
```
-----------------------------------------------------------------------------------------------------------------------------------

## Free Your Mind: Interactive Programming
- The REPL for Lisp works like other REPLS where it remembers values entered previously and hitting enter at the end will run the line

## Experimenting in the REPL
- numbers in lisp evaluate to themselves, they are `self-evaluating objects`
- Something more interesting is:

```lisp
(+ 1 1 )
; returns 2
```
### Lists in Lisp
- Anything in lisp is is a list, and the first element in a list is evaluated as a function
- In this case `+` is a function which adds everything in the list together
- There are other ways to evaluated a list expression, more on that later

## "Hello, World" Lisp Style
- Super easy to do

```lisp
>> "Hello, World"
"Hello, World"
```

- Strings, like numbers, are self-evaluating objects
- To do this as a program and not just a `value`, you can run a function `FORMAT` which returns `NIL` but outputs value to the screen as a side effect

```lisp
>> (format t "Hello, World")
"Hello, World"
```

### FORMAT
- `FORMAT` is covered more in depth in CH. 18
- Every expression in Lisp evaluated to some result, even if it's just `NIL` which is lisp's `null` value

### Defining a function with DEFUN
- You define functions in Lisp with the `DEFUN` expression:

```lisp
>> (defun hello-world () (format t "hello, world"))
```