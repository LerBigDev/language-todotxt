# Language Todo.TXT Plus - Syntax Highlighting Atom Plugin

This is for comfort work with Todo.TXT-formatted `*.txt` files.

If you doesn't know anything about Todo.TXT, go to [TodoTXT.com](http://todotxt.com) & read all about it! It's worth it :smile:


## Features

- Support of Ukrainian & Russian symbols
- Add **comments**, **failed tasks**, **bold** & **itlaic** emphasis, **raw**, **strikethrought**
- Projects, contexts & extensions can contant only letters & `-` (dash): `foo-bar:goo-moo @foo-bar +goo-moo`
- Support of indentations

  ```TodoTXT
  foo bar @Monaco
    goo doo +zoo
  ```


## Very Quick Usage Guide

Syntax        | Description     | Example
---           | ---             | ---
`~~...~~`     | Strikethrough   | `~~foo bar~~`
`**...**`     | Bold            | `bar **foo** goo`
`_..._`       | italic          | `bar _foo_ goo`
`- ...`       | Failed task     | `- foo bar task @prj`
`x ...`       | Complited task  | `x foo bar +task`
`+{prj-name}` | Project         | 
`@{context}`  | Context         | 
`{param}:{value}` | Extension   | 
`t:{yyyy-mm-dd}` | Date, way 1  | `foo t:2017-07-06 bar` 
`{yyyy-mm-dd}` | Date, way 2    | `foo 2017-07-06 bar`
`due:{yyyy-mm-dd}` | Due to date | `foo due:2017-07-06 bar`
`(A-Z) ...`   | Priority        | `(A) foo @bar goo` 
~             | ~               | `(B) goo @joo noo` 
`... # ...`   | Comments        | ` foo  # bar`



## Big Example

```TodoTXT
(A) buy **milk** @house-tasks +im-good-man
(Z) fix ~~the chair~~ the table @house-tasks
(B) _go for a walk_ with dog +im-good-man

do some big project +project-name due:2017-12-31
  some part of the project @important
    deeper indention @too-deep
  another **part** of the projec, with code `int main()`
  x complited part of +project-name
  - faild part
  
2017-07-06 this is another task with some-param:some-value
x 2017-06-01 2016-05-21 due:2017-08-31 some ended task with ending date
```



## Support

For more info, write me: `git.lerbigdev at gmail.com`

With best regards, your LerDev :smile:
