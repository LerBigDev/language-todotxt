# language-todotxt package

Adds syntax highlighting to todo.txt files in atom.

Originally [converted](http://atom.io/docs/latest/converting-a-text-mate-bundle) from the [tmTodoTXT TextMate bundle](https://github.com/sideshowcoder/tmTodoTXT).

## New Features

I (LerDev) add some new features for better look & feel, also get some of them from GFM version of Markdown

## Usage

For more comprehensive info about Todo.txt markup see [this](https://github.com/ginatrapani/todo.txt-cli)

Here we consider only examples of additional features

### Undone, canceled

If you need to mark task as undone or canceled (failed :), use `-` (dash) instead of `x`. Example:

```
- (A) 2010-01-01 due:2011-01-01 Lorem ipsum lorem ipsum 
```

Must render something like this:

~~(A) 2010-01-01 due:2011-01-01 Lorem ipsum lorem ipsum~~


### Raw in-line code

If you need to insert some in-line raw code, & want that it was properly emphasized. Example:
	
```
(A) 2010-01-01 Lorem ipsum `lorem_i = ipsum * 2 - ipsm($lorem)`
```

Result:

(A) 2010-01-01 Lorem ipsum `lorem_i = ipsum * 2 - ipsm($lorem)`

### Comments

Use `#` to comment all that follows the `#` (hash). Example:

```
# That was very useful comment
(A) 2010-01-01 Lorem ipsum lorem +ipsum
```

Must be render as common comment line in any programming language

### Better Cyrillic support

So now you can use russian (ukrainian) `x` for mark task as done

### Improve regex parser for context '@', project '+' & extension ':'

All of the above tags can content only those charactes & symbols: `[a-zA-Z0-9]`, `-` (dash), `&`, `_`. Also any other symbol will stop highlighting of tag, thus, you can write senteces like this:

```
(A) 2010-01-01 Lorem ipsum lorem +ipsum-lorem: ipsum @lorem!!!
```

, where `:` & `!!!` doesn't highlighted as project & context respectively!



## Themes With Full Support Of New Features

I currently tested this version only with Atom's [Pubster Syntax](https://github.com/plttn/pubster-syntax), which also has full support of Atom's [Language Markdown](https://atom.io/packages/language-markdown), so I recommend it for usage with Todo.txt & Language Markdown